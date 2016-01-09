Role Name
========

Django


Description
-------------------------

Installs django and creates a project.  
Optionally arguments include uwsgi setup, nginx(web server), database(mysql or postgresql) and nginx setup.


Dependencies
-------------------------

- { role: micropyramid.update_ubuntu } 
- { role: micropyramid.mysql, mysql_server_password : 'password', when: database == 'mysql' } 
- { role: micropyramid.postgresql, when: database == 'postgresql' } 


Example Playbook
-------------------------

- hosts: servers
  remote_user: root
  roles:
    - { role: micropyramid.django, project_name: 'your_project_name', database: 'mysql or postgresql or empty' }
    - { role: micropyramid.uwsgi_django_setup, project_name: 'your_project_name' }
    - { role: micropyramid.nginx_django_setup, project_name: "your_project_name", server_name: "domain_name_or_ip_addr", server_port: "port_number" }


Note: Roles uwsgi_django_setup, nginx_django_setup are optional

License
-------

MIT
