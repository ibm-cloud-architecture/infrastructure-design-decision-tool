# IBM Cloud Design Decision Tool - Example

## Indie Tix, Online Ticket Retailer (e-Commerce Example)

Indie Tix is an online ticket retailer that promotes indie music to mainstream listeners by putting on concerts in intimate venues (500 to 3,500 seats). In their current environment, they are facing increases in demand as indie artists are gaining popularity due to Internet exposure and mainstream air play.

They will be designing an architecture based on three tiers – web, application, and database - based on their current and future needs. The tiers are divided into three layers – presentation (web), business (application), and data (database) – with a server residing in each. Figure 2 illustrates Indie Tix’s architecture.

![Figure 2: Indie Tix's 3-tier architecture design](/images/figure2.png)

Figure 2: Indie Tix's 3-tier architecture design

The first component to be determined is the global load balancer, which has the following requirements:

* Available storefront – up to 24x7 – for top-tier customers
* Anticipate traffic spikes that “follow the sun”
* Handle seasonal spikes in service usage
* Support 7,500 unique shoppers daily and 100 connections per second
* Support highly variable and unpredictable compute requirements

Select ![Load Balancer Options](#load_balancer) link and review the Considerations and Caveats for each option.  Your choices should be narrowed down to:

| Options | Pros(+)/Cons(-) |
| ------- | ------------------- |
| Dyn.com | (+)Geolocation and ratio/weight balancing capable, (-)No provisioning on the private network |
| NginX | (+)Geolocation and ratio/weight balancing capable, (-)Higher maintenance (must manage operating system as well), (-)No management console (CLI and configuration files only) |
| Citrix NetScaler VPX | (+)GSLB protects against failures of servers and sites, (+)Geolocation and ratio/weight balancing capable, (+)Virutal appliance = low maintenance, (-)Requires an appliance, or appliances, for each site |

Table 1: Global load balancer options for Indie Tix

Based on the pros and cons presented in Table 1, Indie selected the Citrix NetScaler VPX for their global load balancer. The next component is the firewall, then the local load balancer, and so on. You use the Design Decision Tool to match the best component option based on the IaaS design requirement. 

Return to [Components](README.md)
