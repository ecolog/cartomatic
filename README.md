![alt text](https://raw.githubusercontent.com/gongled/cartomatic/master/cartomatic.png "Cartomatic Logo")

## About

Cartomatic helps you setup server for CS-Cart or Multi-Vendor 4.0+.

[![Cartomatic: how to use](https://img.youtube.com/vi/qywoXad8ZIM/0.jpg)](http://www.youtube.com/watch?v=qywoXad8ZIM)

## Quick install

Log in to your server as superuser (root) via SSH and execute this command:

    wget -qO - http://cartoma.tk/installer | bash -s -- yourdomain.tld

Done. It works.

## Manual install

Log in to your server as superuser (root) via SSH and execute this command:

    wget -qO - http://cartoma.tk/preconf | bash

Put custom settings in the JSON file:

    cd /srv/cartomatic/<version>
    vim config/simple.json

You can also specify extra variables in files in 'group_vars' folder.

Run:

    ansible-playbook lamp.yml -c local -e @config/simple.json

Passwords will be saved in the 'credentials' folder.

## Supported platforms

* Ubuntu 14.04 x86_64
* Ubuntu 14.10 x86_64
* Ubuntu 15.04 x86_64
* Debian 6 Squeeze x86_64
* Debian 7 Wheezy x86_64
* Debian 8 Jessie x86_64
* CentOS 6 x86_64
* CentOS 7 x86_64

## Restrictions

* Works well only for clean installations.
* Not compatible with ISPManager, cPanel, Plesk etc.

## Credits

* [@jsjant](https://github.com/jsjant) for project's name.
* [@UlyanovskUI](https://twitter.com/UlyanovskUI) for logo design.
* Tatiana Durnova for the help with translation.

## License

GNU Public Licence 3 (GPL v3)
