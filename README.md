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

Customize and run test.yml file 
eg: ansible-playbook -i host_file test.yml --role-path=/your_directory

Note: Roles uwsgi_django_setup, nginx_django_setup are optional

License
-------

MIT
