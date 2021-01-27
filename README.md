# Zerotwo // @MissZerotwo_bot 

[![Codacy Badge](https://api.codacy.com/project/badge/Grade/e96f7c790e574fa0ab2f774ceff6b8ef)](https://app.codacy.com/manual/anilchauhanxda/stella?utm_source=github.com&utm_medium=referral&utm_content=anilchauhanxda/allukabot&utm_campaign=Badge_Grade_Dashboard)
[![Open Source Love](https://badges.frapsoft.com/os/v1/open-source.png?v=103)](https://github.com/ellerbrock/open-source-badges/)  
[![GPLv3 license](https://img.shields.io/badge/License-GPLv3-blue.svg)](http://perso.crans.org/besson/LICENSE.html)

[![GitHub forks](https://img.shields.io/github/forks/anilchauhanxda/stella.svg?style=social&label=Fork&maxAge=2592000)](https://GitHub.com/anilchauhanxda/stella/network/) [![GitHub stars](https://img.shields.io/github/stars/anilchauhanxda/stella.svg?style=social&label=Star&maxAge=2592000)](https://GitHub.com/anilchauhanxda/stella/stargazers/)

[![Zerotwo](https://telegra.ph/zertwo-01-27](https://heroku.com/deploy) 

### Python dependencies

Install the necessary python dependencies by moving to the project directory and running:

`pip3 install -r requirements.txt`.

This will install all necessary python packages.

### Database

If you wish to use a database-dependent module (eg: locks, notes, userinfo, users, filters, welcomes),
you'll need to have a database installed on your system. I use postgres, so I recommend using it for optimal compatibility.

In the case of postgres, this is how you would set up a the database on a debian/ubuntu system. Other distributions may vary.

- install postgresql:

`sudo apt-get update && sudo apt-get install postgresql`

- change to the postgres user:

`sudo su - postgres`

- create a new database user (change YOUR_USER appropriately):

`createuser -P -s -e YOUR_USER`

This will be followed by you needing to input your password.

- create a new database table:

`createdb -O YOUR_USER YOUR_DB_NAME`

Change YOUR_USER and YOUR_DB_NAME appropriately.

- finally:

`psql YOUR_DB_NAME -h YOUR_HOST YOUR_USER`

This will allow you to connect to your database via your terminal.
By default, YOUR_HOST should be 0.0.0.0:5432.

You should now be able to build your database URI. This will be:

`sqldbtype://username:pw@hostname:port/db_name`

Replace sqldbtype with whichever db youre using (eg postgres, mysql, sqllite, etc)
repeat for your username, password, hostname (localhost?), port (5432?), and db name.
