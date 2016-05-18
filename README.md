# Overview

This charm provides a mod-gearman worker.
For more informations: https://labs.consol.de/nagios/mod-gearman/index.html 

Mod-Gearman is a Naemon (formerly Nagios) addon which
extends Naemon to run scalable and distributed setups.
Worker nodes can be placed all over your network while
keeping the simplicity of a central configuration.
Mod-Gearman can even help to reduce the load on a
single Naemon host, because of its smaller and more
efficient way of executing host- and servicechecks.

This charm is tested with Ubuntu 14.04 (trusty).

# Usage

This is a subordinate salt minion charm.

Deploy the service:

    juju deploy mod-gearman-worker
    juju set mod-gearman-worker gearman-server="<IP of the gearman server>"
    juju set mod-gearman-worker hostgroups="group1,group2"
