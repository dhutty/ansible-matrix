Role Name
=========

This installs the matrix chat app

Requirements
------------

Synapse/turn listen on the following ports:
TCP 8008 : Matrix via HTTP
TCP 8448 : Matrix via HTTPS
UDP/TCP 3478/3479 TURN Server



Role Variables
--------------

- username `synapse`:  under wich user the server should be installed and run
- git_repo `https://github.com/matrix-org/synapse/tarball/master`:  URL to Git Repo you want to install
- hostname `10.99.99.230`:  FQDN to be used
- enable_registration `true`:  this will open registration by default, take care if you run a public server!
- enable_registration_captcha `false`: Use captcha for registration
- recaptcha_private_key `YOURPRIVATEKEYHERE`
- recaptcha_public_key `YOURPUBLICKEYHERE`
- turn_shared_secret `YOURSHAREDSECRETHERE`

Dependencies
------------

None

Example Playbook
----------------


    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

GPLv3+

Author Information
------------------

github/bitbucket: awesomefireduck
