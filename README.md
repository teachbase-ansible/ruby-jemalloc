Ruby with jemalloc
========

Installs Ruby with jemalloc and bundler.
Add permissions for deploy user (if present).

Installation
--------------

`ansible-galaxy install teachbase-ansible.ruby-jemalloc`

Role Variables
--------------

`defaults/main.yml`

| Name                        | Default Value |  Description    |
|-----------------------------|---------------|-----------------|
| ruby_version              | 2.5        | Ruby version to install |
| ruby_url                  | "http://cache.ruby-lang.org/pub/ruby/{{ ruby_version }}/{{ ruby_name }}.tar.gz" | Ruby source url |
| ruby_name                 | ruby-2.5.3 | Ruby source name |
| ruby_tmp_path             | "/usr/local/src/{{ ruby_name }}" | Where to download source | 
| jemalloc_version          | 5.2.0      | Jemalloc version to install |
| jemalloc_url              | "https://github.com/jemalloc/jemalloc/releases/download/{{ jemalloc_version }}/jemalloc-{{ jemalloc_version }}.tar.bz2"      | Jemalloc source url |


Example Playbook
-------------------------
```yml
  - hosts: servers
    roles:
       - teachbase-ansible.ruby-jemalloc
```
