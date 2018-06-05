sbog/mediawiki
==============

Role to install Mediawiki.

#### Requirements

Ansible 2.4

#### Role Variables

```yaml
mediawiki_hostname: wiki.example.ru
mediawiki_ssl_enabled: true
mysql_port: 3306
mysql_bind_address: "127.0.0.1"
mysql_root_db_pass: mysqlroot
mysql_users:
  - name: wikiadmin
    pass: wikiadminpass
    priv: "wikidb.*:ALL"
mysql_db:
  - name: wikidb
    replicate: no
```

#### Dependencies

bennojoy.mysql

#### Example Playbook

```yaml
- name: Install Mediawiki
  hosts: localhost
  remote_user: root
  roles:
    - mediawiki
```

#### License

Apache 2.0

#### Author Information

Stanislaw Bogatkin (https://sbog.ru)
