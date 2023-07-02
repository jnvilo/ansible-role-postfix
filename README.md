# ansible-role-postix 

A basic SMTP setup 

# Usage:

The most basic usage is just adding it as:

    roles:
     - role: postfix

And the server will be configured with defaults. The defaults are shown below and you can override them. 
 

    roles:
      - role: postfix
        vars:
          server_hostname: "{{ ansible_hostname}}"
          mynetworks: 
           - "127.0.0.0/8"
           - "[::ffff:127.0.0.0]/104"
           - "[::1]/128"
          smtpd_banner: "$myhostname ESMTP $mail_name"   
          relayhost: ""
