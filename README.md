# Ansible Role: CouchDB

[![Build Status](https://travis-ci.org/singleplatform-eng/ansible-role-couchdb.svg?branch=master)](https://travis-ci.org/singleplatform-eng/ansible-role-couchdb)

Installs CouchDB on Debian/Ubuntu servers.

## Requirements

None

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    couchdb_port: "5984"
    couchdb_bind_address: "127.0.0.1"
    couchdb_database_dir: "/var/lib/couchdb"
    couchdb_view_index_dir: "/var/lib/couchdb"
    couchdb_max_dbs_open: 100
    couchdb_delayed_commits: true
    couchdb_log_level: "info"

## Dependencies

None

## Example Playbook

    - hosts: webservers
      vars:
        couchdb_max_dbs_open: 150
      roles:
        - { role: personnage.couchdb }

## License

MIT / BSD

## Author Information

This role was created in 2016 by [The Personnage](https://github.com/personnage).

It has been modified to support generic configuration options in the settings template.
