Ansible Role for PostgreSQL
===========================

[![Build Status](https://travis-ci.org/pantarei/ansible-role-postgresql.svg?branch=master)](https://travis-ci.org/pantarei/ansible-role-postgresql)
[![GitHub tag](https://img.shields.io/github/tag/pantarei/ansible-role-postgresql.svg)](https://github.com/pantarei/ansible-role-postgresql)
[![GitHub license](https://img.shields.io/github/license/pantarei/ansible-role-postgresql.svg)](https://github.com/pantarei/ansible-role-postgresql/blob/master/LICENSE)
[![Ansible Role](https://img.shields.io/ansible/role/5980.svg)](https://galaxy.ansible.com/detail#/role/5980)

Ansible Role for PostgreSQL Installation.

Requirements
------------

This role require Ansible 2.0 or higher.

This role was designed for Ubuntu Server 14.04 LTS.

Role Variables
--------------

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">parameter</th>
<th align="left">required</th>
<th align="left">default</th>
<th align="left">choices</th>
<th align="left">comments</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left">postgresql_data_directory</td>
<td align="left">yes</td>
<td align="left">/var/lib/postgresql/9.3/main</td>
<td align="left"></td>
<td align="left">Specifies the directory to use for data storage.</td>
</tr>
<tr class="even">
<td align="left">postgresql_datestyle</td>
<td align="left">yes</td>
<td align="left">iso, mdy</td>
<td align="left"></td>
<td align="left">Sets the display format for date and time values, as well as the rules for interpreting ambiguous date input values.</td>
</tr>
<tr class="odd">
<td align="left">postgresql_default_text_search_config</td>
<td align="left">yes</td>
<td align="left">pg_catalog.english</td>
<td align="left"></td>
<td align="left">Selects the text search configuration that is used by those variants of the text search functions that do not have an explicit argument specifying the configuration.</td>
</tr>
<tr class="even">
<td align="left">postgresql_external_pid_file</td>
<td align="left">yes</td>
<td align="left">/var/run/postgresql/9.3-main.pid</td>
<td align="left"></td>
<td align="left">Specifies the name of an additional process-ID (PID) file that the server should create for use by server administration programs.</td>
</tr>
<tr class="odd">
<td align="left">postgresql_hba_file</td>
<td align="left">yes</td>
<td align="left">/etc/postgresql/9.3/main/pg_hba.conf</td>
<td align="left"></td>
<td align="left">Specifies the configuration file for host-based authentication (customarily called pg_hba.conf).</td>
</tr>
<tr class="even">
<td align="left">postgresql_ident_file</td>
<td align="left">yes</td>
<td align="left">/etc/postgresql/9.3/main/pg_ident.conf</td>
<td align="left"></td>
<td align="left">Specifies the configuration file for Section 19.2 user name mapping (customarily called pg_ident.conf).</td>
</tr>
<tr class="odd">
<td align="left">postgresql_lc_messages</td>
<td align="left">yes</td>
<td align="left">en_US.UTF-8</td>
<td align="left"></td>
<td align="left">Sets the language in which messages are displayed.</td>
</tr>
<tr class="even">
<td align="left">postgresql_lc_monetary</td>
<td align="left">yes</td>
<td align="left">en_US.UTF-8</td>
<td align="left"></td>
<td align="left">Sets the locale to use for formatting monetary amounts, for example with the to_char family of functions.</td>
</tr>
<tr class="odd">
<td align="left">postgresql_lc_numeric</td>
<td align="left">yes</td>
<td align="left">en_US.UTF-8</td>
<td align="left"></td>
<td align="left">Sets the locale to use for formatting numbers, for example with the to_char family of functions.</td>
</tr>
<tr class="even">
<td align="left">postgresql_lc_time</td>
<td align="left">yes</td>
<td align="left">en_US.UTF-8</td>
<td align="left"></td>
<td align="left">Sets the locale to use for formatting dates and times, for example with the to_char family of functions.</td>
</tr>
<tr class="odd">
<td align="left">postgresql_listen_addresses</td>
<td align="left">yes</td>
<td align="left">localhost</td>
<td align="left"></td>
<td align="left">Specifies the TCP/IP address(es) on which the server is to listen for connections from client applications.</td>
</tr>
<tr class="even">
<td align="left">postgresql_log_line_prefix</td>
<td align="left">yes</td>
<td align="left">%t</td>
<td align="left"></td>
<td align="left">This is a printf-style string that is output at the beginning of each log line.</td>
</tr>
<tr class="odd">
<td align="left">postgresql_log_timezone</td>
<td align="left">yes</td>
<td align="left">UTC</td>
<td align="left"></td>
<td align="left">Sets the time zone used for timestamps written in the server log.</td>
</tr>
<tr class="even">
<td align="left">postgresql_max_connections</td>
<td align="left">yes</td>
<td align="left">100</td>
<td align="left"></td>
<td align="left">Determines the maximum number of concurrent connections to the database server.</td>
</tr>
<tr class="odd">
<td align="left">postgresql_port</td>
<td align="left">yes</td>
<td align="left">5432</td>
<td align="left"></td>
<td align="left">The TCP port the server listens on; 5432 by default.</td>
</tr>
<tr class="even">
<td align="left">postgresql_shared_buffers</td>
<td align="left">yes</td>
<td align="left">128MB</td>
<td align="left"></td>
<td align="left">Sets the amount of memory the database server uses for shared memory buffers.</td>
</tr>
<tr class="odd">
<td align="left">postgresql_ssl</td>
<td align="left">yes</td>
<td align="left">true</td>
<td align="left"><ul>
<li>true</li>
<li>false</li>
</ul></td>
<td align="left">Enables SSL connections.</td>
</tr>
<tr class="even">
<td align="left">postgresql_ssl_cert_file</td>
<td align="left">yes</td>
<td align="left">/etc/ssl/certs/ssl-cert-snakeoil.pem</td>
<td align="left"></td>
<td align="left">Specifies the name of the file containing the SSL server certificate.</td>
</tr>
<tr class="odd">
<td align="left">postgresql_ssl_key_file</td>
<td align="left">yes</td>
<td align="left">/etc/ssl/private/ssl-cert-snakeoil.key</td>
<td align="left"></td>
<td align="left">Specifies the name of the file containing the SSL server private key.</td>
</tr>
<tr class="even">
<td align="left">postgresql_timezone</td>
<td align="left">yes</td>
<td align="left">UTC</td>
<td align="left"></td>
<td align="left">Sets the time zone for displaying and interpreting time stamps.</td>
</tr>
<tr class="odd">
<td align="left">postgresql_unix_socket_directories</td>
<td align="left">yes</td>
<td align="left">/var/run/postgresql</td>
<td align="left"></td>
<td align="left">Specifies the directory of the Unix-domain socket(s) on which the server is to listen for connections from client applications.</td>
</tr>
<tr class="even">
<td align="left">postgresql_hba</td>
<td align="left">yes</td>
<td align="left"><a href="https://github.com/pantarei/ansible-role-postgresql/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td align="left"></td>
<td align="left">Host-based authentication setting.</td>
</tr>
</tbody>
</table>

Dependencies
------------

No additional role dependencies.

Example Playbook
----------------

    - hosts: servers
      roles:
        - { role: hswong3i.postgresql }

License
-------

-   Code released under [MIT](https://github.com/pantarei/ansible-role-postgresql/blob/master/LICENSE)
-   Docs released under [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/)

Author Information
------------------

-   Wong Hoi Sing Edison
    -   <https://twitter.com/hswong3i>
    -   <https://github.com/hswong3i>

