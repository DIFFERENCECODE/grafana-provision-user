# grafana-provision-user
- Script to provision Grafana Users and Organisations

## Reference: https://grafana.com/docs/grafana/latest/http_api/org/
Released on the assumption that this might be useful for others
* PR's and suggestions welcome or fork it and fix it as you wish
* Dedicated to Törkel and his tireless heroes (now a massive army) - Thanks for giving us Grafana
* Copyleft Stichting DIFFERENCE The Netherlands
* MIT License

## Docs
* No docs (yet). What it does (at least for the original author) as follows.
* CLI script accepts at minimum two arguments like this example:
` graft --user user@gmail.com --org "SOME LARGE ORGANIZATION" `
* Creates the Org. Creates the user as a member of that Org and with Role as defined or by set by default
* You may either --create a new Org or you may --add the new User to an already exiting Org.
* Downloads the current dashboard of Org 3 (the canonical template in the case of the original author)
* Updates the dashboard for the newly created Org with this dashboard.
* Provisions standard datasources for the new Org (you can serialize your current datasources for this purpose with the Grafana API).
* Dependencies besides Grafana are: zsh jq curl

 
## TODO list
*  Include option to generate a series of users under an Organization
* Check outcome of API calls before proceeding with routine
* Decide on strategy to create template variables for organizations and users in dashboards. Perhaps implement in influxdb and maintain the dataase record via this script
* Option to first delete Org and User before creating with this script.

