[![Build Status](https://travis-ci.org/LibreIT/ansible-msmtp.png?branch=master)](https://travis-ci.org/LibreIT/ansible-msmtp)

msmtp
========

This role enables msmtp to deliver local email to a mail hub.  
A simple way to centralize system emails (alarms, notifications, etc).

Role Variables
--------------

Remember that you must change these variables otherwise msmtp will not be able to send mails!

      msmtp_from: my-server@my-company.com   # address of the sender for all system emails.
        # If this variable is not defined the value is ansible_hostname@ansible_domain (default).
      msmtp_to: youraddress@example.org      # address that receives all system emails.
      msmtp_hub_server: smtp.example.org     # mail hub hostname or ip.
      msmtp_hub_port: 25                     # mail hub port - e.g. 25 or 587.
      msmtp_hub_user: servers@example.org    # mail hub account user.
      msmtp_hub_pass: password               # mail hub account password.
      msmtp_send_testmail: yes               # send email in role to test.

Examples
========

    - hosts: example
      roles:
         - { role: kalos.msmtp, tags: msmtp}


Notes
------------

Password are in cleartext.

Dependencies
------------

None

License
-------

GPLv3

Author Information
------------------

Calogero Lo Leggio (kalos) - http://LibreIT.org
