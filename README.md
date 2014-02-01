[![Build Status](https://travis-ci.org/LibreIT/ansible-msmtp.png?branch=master)](https://travis-ci.org/LibreIT/ansible-msmtp)
msmtp
========

This role enables msmtp to deliver local email to a mail hub.  
A simple way to centralize system emails (alarms, notifications, etc).

Role Variables
--------------

Remember that you must change these variables otherwise msmtp will not be able to send mails!

      msmtp:
        from: my-server@my-company.com   # address of the sender for all system emails.
          # If this variable is not defined the value is ansible_hostname@ansible_domain.
        to: youraddress@example.org      # address that receives all system emails.
        hub_server: smtp.example.org     # mail hub hostname or ip.
        hub_port: 25                     # mail hub port - e.g. 25 or 587.
        hub_user: servers@example.org    # mail hub account user.
        hub_pass: password               # mail hub account password.
        send_testmail: yes               # send email in role to test.

Use these variables in this way: **msmtp.hub_server** (dot between "msmtp" and "hub_server")

Examples
========

    - hosts: example
      roles:
         - { role: kalos.msmtp, tags: msmtp}


Dependencies
------------

None

License
-------

GPLv3

Author Information
------------------

Calogero Lo Leggio (kalos) - http://LibreIT.org
