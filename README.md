A collection of SNMP utilities for sysadmins working with L3 networking devices like Cisco routers.

I'm using PySNMP...not totally thrilled with it, but Python should make it rather maintainable.

Common SNMP queries I run are to do with:
* OSPF and BGP (Cisco, Quagga and Vyatta/VyOS routers)
* Interface status (Net-SNMP OSes, Cisco routers, Dell and HP switches, and Vyatta/VyOS)
* IP SLA objects on Cisco routers (Cisco RTTMON MIB)
* APC UPSes (IP-enabled management cards and PowerChute on Windows) - PowerNet-MIB

Scripts I'd like to write and assemble here:
* CLI utilities:
** show-ip-sla: shows the current configuration of IP SLA objects on a Cisco router
** show-interface-status: print table of each interface and state
** show-apc-ups-status: print a table of basic status of each UPS
* Nagios checks:
** check_ospf_neighborship_interface: verify that the specified interface has a neighborship
   this probably already exists...
** check_apc_ups_power: check for power outage (longer than 30 seconds) - to be pager-worthy
** check_ip_sla: check that a configured IP SLA is not failing (to detect ISP outages)
