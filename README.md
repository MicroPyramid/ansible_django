Role Name
========

Django

Description
-------------------------

Installs django and creates a project.  
Optionally arguments include uwsgi setup, nginx(web server), database(mysql or postgresql) and nginx setup.


Role Variables
-------------------------



Example Playbook
-------------------------

Required parameters: project_name, server_name  
Optional parameters: database  

- hosts: servers
  remote_user: root
  roles:
     - { role: micropyramid.django, project_name: 'your_project_name', server_name: 'domain_name or ip_addr', database: 'mysql or postgresql' }
     - { role: uwsgi_django_setup, project_name: 'your_project_name' }
     - { role: nginx_django_setup, project_name: 'your_project_name' }


License
-------

MIT

Author Information
------------------

Jagadeesh(jagadeesh@micropyramid.com), Dinesh(dinesh@micropyramid.com)
