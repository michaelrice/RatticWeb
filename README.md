RatticWeb
=========

I found the original RatticWeb when I was looking for an enterprise solution for password management and it was close but 
missing a piece or two. So I did what any self-respecting Linux guy would do, I said "fork it". Initially, the only difference
is that it now it has encryption of the password field in the database. If you find this, please do not bug the RatticDB 
folks with support for this. You will use it at your own risk.

RatticWeb is the website part of the Rattic password management solution, which allows you to easily manage your users and passwords.

To quickly get a RatticDB demo running do the following:
* Install VirtualBox from https://www.virtualbox.org/
* Install Vagrant from http://www.vagrantup.com/
* Install Ansible from http://ansible.com/ or from pip, apt or yum (we need 1.4+)
* Check out this repo
* Run ```vagrant up``` in the root of this repo
* Wait for vagrant to deploy the machine
* Browse to https://localhost:8443/
* Login with Username: admin Password: rattic
* ...
* Profit!

If you decide to use RatticWeb you should take the following into account:
* The webpage should be served over HTTPS only, apart from a redirect from normal HTTP.
* The filesystem in which the database is stored should be protected with encryption.
* The access logs should be protected.
* The machine which serves RatticWeb should be protected from access.
* Tools like <a href=="http://www.ossec.net/">OSSEC</a> are your friend.

Support and Known Issues:
* Through <a href="http://twitter.com/RatticDB">twitter</a> or <a href="https://github.com/tildaslash/RatticWeb/issues?state=open">Github Issues</a>
* Apache config needs to have "WSGIPassAuthorization On" for the API keys to work  

Dev Setup: <https://github.com/tildaslash/RatticWeb/wiki/Development>

