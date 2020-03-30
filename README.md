Role Name
=========

A brief description of the role goes here.

Requirements
------------

Add the following to your requirements file:
```
- src: https://github.com/elixir-no-nels/ansible-role-ehos.git
  name: ehos
```


Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: ehos
      become: true
    
    
      vars:
        - openstack_auth_url: https://iaas:5000/v3
        - openstack_username: USERNAME
        - openstack_password: PASSWORD
        - openstack_domain_name: DOMAIN
        - openstack_project_name: PROJECT_NAME
        - openstack_region_name: REGION
        - openstack_user_domain_name: DOMAIN
          
        - condor_password: ChangeMe
        - condor_uid_domain: usegalaxy.no
          
          
        - openstack_flavor: m1.medium
        - openstack_image: GOLD CentOS 7
          
        - openstack_network: dualStack
 
    
      pre_tasks:
        - name: Install Dependencies
          package:
            #        use_backend: dnf
            name: ['python3', 'git', 'bzip2']
    
      tasks:
    
      roles:
        - ehos

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
