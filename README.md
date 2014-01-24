msmtp
========

This role enables msmtp to deliver local email to a mail hub.
A simple way to centralize system email (alarms, notifications, etc).

Requirements
------------

Msmtp must be the only MTA installed on the system.

Role Variables
--------------

  **msmtp_from** - address of the sender for all system emails.  
  If this variable is not defined the value is *ansible_hostname* @ *ansible_domain* 

  **msmtp_to** - address that receives all system emails.

  **msmtp_hub_server** - mail hub hostname or ip.

  **msmtp_hub_port** - mail hub port.

  **msmtp_hub_user** - mail hub user.

  **msmtp_hub_pass** - mail hub password.


Dependencies
------------

None

License
-------

GPLv3

Author Information
------------------

Calogero Lo Leggio (kalos) - http://LibreIT.org
