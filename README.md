uWSGI
=====

Installs or updates [uWSGI](http://uwsgi-docs.readthedocs.org/). It'll also set the uWSGI emperor to run from a `@reboot` crontab entry.

The emperor will run a vassal for any `.ini` put in `/etc/uwsgi/vassals/`.


Requirements
------------

The role is created for Debian, Ubuntu and CentOS/RHEL 6.5/7.x. The role will also install `build-essential` and some `-dev`
packages that it needs to compile uWSGI. Ruby/Rack support is not available on CentOS/RHEL-6.x, but is on 7.x releases.


Role Variables
--------------

The role uses 5 variables, that you can also override:

* `uwsgi_install_method` - choose the way you want to install uWSGI: from `source` or using `pip`.
* `uwsgi_version` - specifies the latest stable version of uWSGI. If you’re using the `pip` install method, you can specify `lts` to get the “Long Time Support” version.
* `uwsgi_tyrant_mode` - if True, uWSGI will run in Tyrant mode (False by default)
* `uwsgi_lib_dir` - normally shouldn't be changed. The directory where plugins are installed. It's `/usr/local/lib/uwsgi` by default. (source install method)
* `uwsgi_download_url` - normally shouldn't be changed. It's `https://github.com/unbit/uwsgi/archive` by default. (source install method)


Usage
-----

    ansible-galaxy install gdamjan.uwsgi

Also check the [Ansible Galaxy](https://galaxy.ansible.com/intro) about page.


License
-------

BSD

Author and other Information
----------------------------

Damjan Georgievski

[GitHub project page](https://github.com/gdamjan/ansible-uwsgi)

