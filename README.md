Role Name
=========

Install Slacktee

Requirements
------------

None

Role Variables
--------------

- slacktee_webhook_url: Incoming Webhooks integration URL. See https://my.slack.com/services/new/incoming-webhook. Example: 'https://hooks.slack.com/services/T70xxxxx'
slacktee_upload_token: The user's API authentication token, only used for file uploads. See https://api.slack.com/#auth
slacktee_channel: Default channel to post messages. '#' is prepended, if it doesn't start with '#' or '@'. Example: 'mychannel'
slacktee_tmp_dir: Temporary file is created in this directory. Example: '/tmp'
slacktee_username: emporary file is created in this directory. Example: 'slacktee'
slacktee_icon: Default emoji or a direct url to an image to post messages. You don't have to wrap emoji with ':'. See http://www.emoji-cheat-sheet.com. Example: 'ghost'
slacktee_attachment: Default color of the attachments. If an empty string is specified, the attachments are not used. Example: ''
slacktee_test_message_enabled: Enable sending a test message to slack after slacktee installation. Example: yes
slacktee_test_message: Test message text. Example: 'Ansible Slacktee installed!'

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      vars:
        slacktee_webhook_url: 'https://hooks.slack.com/services/T7058xxxx'    
        slacktee_channel: 'mychannel'    
      roles:
         - slacktee

License
-------

BSD

Author Information
------------------

Antonio Barbaro <antonio.barbaro@gmail.com>
