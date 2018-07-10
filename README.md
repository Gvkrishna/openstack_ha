 
## high availblity

  - **failover** -migration of a service from a primary resource to a secondary resource is referred to as . 
  - **failback** -migration of the service back to the primary resource is referred .
  - **switchover** - is when the migration is initiated manually.

Redundant infrastructure can be in **Active-Active** mode, which means that the failure of a single resource will usually result in the degradation of a service. In an **Active-Passive** mode infrastructure, the services are continually monitored and a backup or secondary resource will assume the role of the primary resource in the event that it fails. 

Services can be stateless or stateful. 
There is no dependency between requests in a **stateless**service.
there is a dependency between requests in a **stateful** service.

Data needs to be replicated between the nodes. There are different forms of replication including **master-master, master-slave and multi-master**.

## HA for Rackspace Private Cloud

The Health Check module is implemented via** Keepalived**, which is based on **Linux Virtual Servers (IPVS)** kernel module and provides layer 4 load balancing.

**Virtual Router Redundancy Protocol (VRRP)** eliminates **SPOF** by using a **Virtual IP (VIP)** for the service and binding to the service that is running on the functioning controller.  **Keepalived uses VRRP to move the VIPs around**. **MySQL and RabbitMQ service is managed via Keepalived**. HAProxy manages load balancing for HTTP- and TCP-based applications – it load balances the API services. The following diagram illustrates how this works.


https://blog.rackspace.com/implementing-high-availability-ha-for-rackspace-private-cloud




