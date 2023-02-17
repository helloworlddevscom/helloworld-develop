
# Purpose

Static HTML site for Hello World (http://www.helloworlddevs.com).

# Environments/sites

* Dev: ~http://hw.hwdevs.site/~ @TODO: We don't have a dev site yet now that we moved the site to DreamHost.
* Production: http://www.helloworlddevs.com

# Project branch strategy
    develop    :: Code currently or soon to be deployed to dev environment/site. Commit to develop or merge a feature branch into develop, and then merge develop into master when ready to deploy to production.
    master     :: Code currently deployed or about to be deployed to production.
    
# Hosting

This site is hosted on DreamHost (https://www.dreamhost.com/). You probably don't need to login to DreamHost, but if you do, the password is shared in LastPass. Search for DreamHost.

# Deploy processes

~## Dev~
@TODO: We don't have a Dev site at the moment. Update this when we create a Dev site on DreamHost.
To deploy to dev environment/site:

* Commit and push to `develop` branch.
* `ssh danlinn@198.58.114.22` to SSH into WebFaction
* In SSH session: `cd webapps/helloworlddevs_html_dev/webroot`
* In SSH session: `git pull`
  * You'll be asked for a password. Ask Jeff or Ben if you don't know it.
* You should now see your changes reflected on the dev site (http://hw.hwdevs.site/).


## Production
To deploy to production:

* Commit and push to `develop` branch.
* `git checkout master; git pull; git merge develop; git push;`
* `ssh helloworld_admin@windstone.dreamhost.com` to SSH into DreamHost. The password is in LastPass. Search for "DreamHost SSH".
* In SSH session: `cd helloworld`
* In SSH session: `git pull`
  * You'll be asked for a password. Ask Jeff, Stephen or Ben if you don't know it.
* You should now see your changes reflected on production (http://www.helloworlddevs.com).

