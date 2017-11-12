# Design Decision Tool for IaaS on IBM Cloud

The Design Decision Tool contains the potential advantages and disadvantages of the available components used for designing and building your infrastructure as a Service (IaaS) on IBM Cloud.  Use this information during your solution design to help select the best options to meet your workload requirements.  More information is provided in the [IaaS Solutions Design training class](http://www.softlayer.com/training-courses) which takes you through hands-on workshops to assist you with making architecture choices for your IaaS.

## How to use the Design Decision Tool 

The Design Decision Tool supports the infrastructure process (Figure 1) by stepping you through each component of your infrastructure to help you determine which options to use based on your requirements.  You are encouraged to use the design process and decision tool when designing your IaaS.

![Figure 1: IaaS design process](/images/rainbow_tool_fig1.png)

Figure 1: IaaS design process

A high-level example of an e-commerce workload has been provided to assist you with the Design Decision Tool. After reviewing the example you can then apply the concepts to your workload. 

## Indie Tix, Online Ticket Retailer (e-Commerce Example)

Indie Tix is an online ticket retailer that promotes indie music to mainstream listeners by putting on concerts in intimate venues (500 to 3,500 seats). In their current environment, they are facing increases in demand as indie artists are gaining popularity due to Internet exposure and mainstream air play.

They will be designing an architecture based on three tiers – web, application, and database - based on their current and future needs. The tiers are divided into three layers – presentation (web), business (application), and data (database) – with a server residing in each. Figure 2 illustrates Indie Tix’s architecture.

![Figure 2: Indie Tix's 3-tier architecture design](/images/rainbow_tool_fig2.png)

Figure 2: Indie Tix's 3-tier architecture design

The first component to be determined is the global load balancer, which has the following requirements:

* Available storefront – up to 24x7 – for top-tier customers
* Anticipate traffic spikes that “follow the sun”
* Handle seasonal spikes in service usage
* Support 7,500 unique shoppers daily and 100 connections per second
* Support highly variable and unpredictable compute requirements

After selecting the load balancer link and reviewing the Considerations and Caveats for each option, your choices should be narrowed down to:



Table 1: Global load balancer options for Indie Tix

Based on the pros and cons presented in Table 1, Indie selected the Citrix NetScaler VPX for their global load balancer. The next component is the firewall, then the local load balancer, and so on. You use the Design Decision Tool to match the best component option based on the IaaS design requirement. 

## IaaS Components

The following links will take you to the Considerations and Caveats for each option within a design component category:

* ![Compute Options](#compute)
* ![Storage Options](#storage)
* ![Backup Options](#backup)
* ![Disaster Recovery Options](#disaster_recovery)
* ![Firewall Options](#firewall)
* ![VPN Options](#vpn)
* ![Load Balancer Options](#load_balancer)
* ![Reverse Proxy Options](#reverse_proxy)
* ![Direct Link Options](#direct_link)

### <a name="compute"></a> Compute Options

![Compute](/images/rainbow_tool_compute.png)

### <a name="storage"></a> Storage Options

![Storage](/images/rainbow_tool_storage.png)

### <a name="backup"></a> Backup Options

![Backup Options](/images/rainbow_tool_backup.png)

### <a name="diaster_recover"></a> Disaster Recovery Options

![Disastery Recovery Options](/images/rainbow_tool_disaster_recovery.png)

### <a name="firewall"></a> Firewall Options

![Firewall Options](/images/rainbow_tool_firewall.png)
 
### <a name="vpn"></a> VPN Options

![VPN Options](/images/rainbow_tool_vpn.png)

### <a name="load_balancer"></a> Load Balancer Options

![Load Balancer Options](/images/rainbow_tool_load_balancer.png)

### <a name="reverse_proxy"></a> Reverse Proxy Options

![Reverse Proxy Options](/images/rainbow_tool_reverse_proxy.png)

### <a name="direct_link"></a> Direct Link Options

![Direct Link Options](/images/rainbow_tool_direct_link.png)


