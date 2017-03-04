Center of Internet Security - CentOS 7 benchmark
================================================

**This role is still under active development.**

Configure a CentOS 7 system to be compliant with the v2.1.1 of the CIS CentOS Linux 7 benchmark.

[CIS_CentOS_Linux_7_Benchmark_v2.1.1](https://benchmarks.cisecurity.org/tools2/linux/CIS_CentOS_Linux_7_Benchmark_v2.1.1.pdf)

This role was developed and tested against CentOS Linux release 7.3.1611 (Core).

Requirements
------------

- CentOS 7 distribution
- Have basic familiarity with the CIS Benchmark (or other similar benchmarks) and an appreciation for the impact that it may have on a system
- root access to the target machine


Why Would I Use This Role?
--------------------------

If you are attempting to obtain compliance against an industry-accepted security standard, like PCI DSS, APRA or ISO 27001, then you need to demonstrate that you have applied documented hardening standards against all systems within scope of assessment.

If you are running Amazon Linux, then this role attempts to provide one piece of the solution to the compliance puzzle.

Here Be Dragons!
----------------

If you are considering applying this role to any servers, you should have a basic familiarity with the CIS Benchmark (or other similar benchmarks) and an appreciation for the impact that it may have on a system.

Please take the time to familarise yourself with the standard and with the configurable default values, and exclude any items before applying to a system.

An examples of items that should be immediately considered for exclusion (or at least, for modification of the related default values) include:

* ```3.4.2``` and ```3.4.3```, which by default effectively limit access to the host (including via ssh) to localhost only.

Role Variables
--------------

| Name              | Default Value       | Description          |
|-------------------|---------------------|----------------------|
| `cis_centos7_*` | `yes` | BLABLABLA |

Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: meddam.cis-centos, when: "ansible_distribution" == 'CentOS' and ansible_os_major_verision == 7"}

License
-------

BSD

Author
------

Mauro Medda aka deftunix < medda.mauro at gmail dot com >
