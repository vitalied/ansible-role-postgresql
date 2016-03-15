Ansible Role for PostgreSQL
===========================

[![Build Status](https://travis-ci.org/vitalied/ansible-role-postgresql.svg?branch=master)](https://travis-ci.org/vitalied/ansible-role-postgresql)
[![GitHub tag](https://img.shields.io/github/tag/vitalied/ansible-role-postgresql.svg)](https://github.com/vitalied/ansible-role-postgresql)
[![GitHub license](https://img.shields.io/github/license/vitalied/ansible-role-postgresql.svg)](https://github.com/vitalied/ansible-role-postgresql/blob/master/LICENSE)
[![Ansible Role](https://img.shields.io/ansible/role/8527.svg)](https://galaxy.ansible.com/detail#/role/8527)

Ansible Role for PostgreSQL Installation.

Requirements
------------

This role require Ansible 2.0 or higher.

This role was designed for Ubuntu Server 14.04+.

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
<th>parameter</th>
<th>required</th>
<th>default</th>
<th>choices</th>
<th>comments</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>postgresql_version</td>
<td>yes</td>
<td>9.5</td>
<td></td>
<td>Specifies the postgresql version.</td>
</tr>
<tr class="even">
<td>postgresql_base_dir</td>
<td>yes</td>
<td>/srv/postgresql</td>
<td></td>
<td>
  Specifies the directory that host data storage directory.
  <br/>
  Data storage directory will be: <code>postgresql_basedir + '/' + postgresql_version + '/main'</code>
</td>
</tr>
<tr class="odd">
<td>postgresql_external_pid_file</td>
<td>yes</td>
<td>/var/run/postgresql/9.5-main.pid</td>
<td></td>
<td>Specifies the name of an additional process-ID (PID) file that the server should create for use by server administration programs.</td>
</tr>
<tr class="even">
<td>postgresql_unix_socket_directories</td>
<td>yes</td>
<td>/var/run/postgresql</td>
<td></td>
<td>Specifies the directory of the Unix-domain socket(s) on which the server is to listen for connections from client applications.</td>
</tr>
<tr class="odd">
<td>postgresql_listen_addresses</td>
<td>yes</td>
<td>localhost</td>
<td></td>
<td>Specifies the TCP/IP address(es) on which the server is to listen for connections from client applications.</td>
</tr>
<tr class="even">
<td>postgresql_port</td>
<td>yes</td>
<td>5432</td>
<td></td>
<td>The TCP port the server listens on; 5432 by default.</td>
</tr>
<tr class="odd">
<td>postgresql_ssl</td>
<td>yes</td>
<td>true</td>
<td><ul>
<li>true</li>
<li>false</li>
</ul></td>
<td>Enables SSL connections.</td>
</tr>
<tr class="even">
<td>postgresql_max_connections</td>
<td>yes</td>
<td>100</td>
<td></td>
<td>Determines the maximum number of concurrent connections to the database server.</td>
</tr>
<tr class="odd">
<td>postgresql_shared_buffers</td>
<td>yes</td>
<td>128MB</td>
<td></td>
<td>Sets the amount of memory the database server uses for shared memory buffers.</td>
</tr>
<tr class="even">
<td>postgresql_effective_cache_size</td>
<td>yes</td>
<td>384MB</td>
<td></td>
<td>configuration calculator for postgresql <a href="http://pgtune.leopard.in.ua">http://pgtune.leopard.in.ua</a></td>
</tr>
<tr class="odd">
<td>postgresql_work_mem</td>
<td>yes</td>
<td>1310kB</td>
<td></td>
<td>configuration calculator for postgresql <a href="http://pgtune.leopard.in.ua">http://pgtune.leopard.in.ua</a></td>
</tr>
<tr class="even">
<td>postgresql_maintenance_work_mem</td>
<td>yes</td>
<td>32MB</td>
<td></td>
<td>configuration calculator for postgresql <a href="http://pgtune.leopard.in.ua">http://pgtune.leopard.in.ua</a></td>
</tr>
<tr class="odd">
<td>postgresql_max_wal_size</td>
<td>yes</td>
<td>1GB</td>
<td></td>
<td>configuration calculator for postgresql <a href="http://pgtune.leopard.in.ua">http://pgtune.leopard.in.ua</a></td>
</tr>
<tr class="even">
<td>postgresql_wal_buffers</td>
<td>yes</td>
<td>3932kB</td>
<td></td>
<td>configuration calculator for postgresql <a href="http://pgtune.leopard.in.ua">http://pgtune.leopard.in.ua</a></td>
</tr>
<tr class="odd">
<td>postgresql_checkpoint_completion_target</td>
<td>yes</td>
<td>0.7</td>
<td></td>
<td>configuration calculator for postgresql <a href="http://pgtune.leopard.in.ua">http://pgtune.leopard.in.ua</a></td>
</tr>
<tr class="even">
<td>postgresql_default_statistics_target</td>
<td>yes</td>
<td>100</td>
<td></td>
<td>configuration calculator for postgresql <a href="http://pgtune.leopard.in.ua">http://pgtune.leopard.in.ua</a></td>
</tr>
<tr class="odd">
<td>postgresql_log_timezone</td>
<td>yes</td>
<td>localtime</td>
<td></td>
<td>Sets the time zone used for timestamps written in the server log.</td>
</tr>
<tr class="even">
<td>postgresql_timezone</td>
<td>yes</td>
<td>localtime</td>
<td></td>
<td>Sets the time zone for displaying and interpreting time stamps.</td>
</tr>
<tr class="odd">
<td>postgresql_hba</td>
<td>yes</td>
<td><a href="https://github.com/vitalied/ansible-role-postgresql/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td></td>
<td>Host-based authentication setting.</td>
</tr>
</tbody>
</table>

Dependencies
------------

No additional role dependencies.

Example Playbook
----------------

    - hosts: all
      roles:
        - role: vitalied.postgresql

License
-------

-   Code released under [MIT](https://github.com/vitalied/ansible-role-postgresql/blob/master/LICENSE)
-   Docs released under [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/)
