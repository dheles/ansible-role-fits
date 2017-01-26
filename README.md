Ansible-Role: FITS
=========

Installs the File Information Tool Set (FITS)

Requirements
------------

Java 1.7 or higher

Role Variables
--------------

    fits_minimum_java_version:  1.7
    fits_version:               "0.8.5"
    fits_install_dir:           "/opt"
    fits_download_dir:          "{{ ansible_env.HOME}}"
    fits_dir:                   "fits-{{ fits_version }}"
    fits_path:                  "{{ fits_install_dir }}/{{ fits_dir }}"
    fits_download_file:         "{{ fits_dir }}.zip"
    fits_url:                   "http://projects.iq.harvard.edu/files/fits/files/{{ fits_download_file }}"
    fits_checksum_algo:         "sha1"
    fits_checksum:              "1d3bc18f6dd37b10d6689ceb321fa88593463992"

Dependencies
------------

my java role (https://github.com/dheles/ansible-role-java), or any other role providing java >= 1.7 (and answering to the name "java")

Example Playbook
----------------

    - hosts: app_servers
      roles:
         - { role: fits }

License
-------

CC0

Author Information
------------------

Drew Heles
