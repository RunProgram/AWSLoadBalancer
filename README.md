<h1 align="center">An Application Load Balancer Built in AWS</h1>

<br>


</br>


<br>


<h2>What is a Load Balancer?</h2>

A load balancer is a service that automatically distributes incoming application traffic across multiple targets, such as EC2 instances, containers, and IP addresses, in multiple availability zones. By doing so, it increases the fault tolerance of your applications by ensuring that the failure of a single instance does not impact the availability of the service.

If, for example, you have a lot of web traffic on one target, a load balancer splits up the workload among several targets (EC2 instances in this case). This workload division provides a great way to ensure that one target isn't overloaded with traffic and also provides protection if one target goes down or offline.
</br>
</br>
</br>

<p align="center">
<img src="/diagram.png" width="80%" height="80%">
</p>

</br>


<h2>Overview</h2>

- **3 EC2 Compute Machines**: The ELB works with 3 EC2 instances, each running a simple "Hello World" HTML page.
- **Elastic Load Balancer (ELB)**: The elastic load balancer is configured across two Availability Zones (AZ) for redundancy. It automatically sends traffic to the correct EC2 instance based on how much traffic it is receiving and processing.
- **Route53 DNS Routing**: Using a custom domain name, the web adress is routed via Route53's provided DNS server. Configured with NS.

