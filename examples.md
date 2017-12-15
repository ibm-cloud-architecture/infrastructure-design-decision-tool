# IBM Cloud Design Decision Tool - Examples

## Using the IBM Cloud Design Decision Tool

The IBM Cloud Design Decision Tool contains the potential advantages and disadvantages of the available components that you can use for designing and building your IBM Cloud solution.  

Use this information during your solution design to help select the best options to meet your workload requirements.  More information is provided in the [Solutions Design training class](http://www.softlayer.com/training-courses) which takes you through hands-on workshops to assist you with making architecture choices for your IBM Cloud solution.

### How to use the Design Decision Tool

The Design Decision Tool supports the solution design process (Figure 1) by stepping you through each component of your solution to help you determine which options to use based on your requirements.  You are encouraged to use the design process and decision tool when designing your IBM Cloud solution.

![Figure 1: Solution design process](/images/figure1.png)

Figure 1: Solution design process

A high-level example workload has been provided to assist you with learning how to use the Design Decision Tool. After reviewing the example you can then apply the concepts to your workload.

## Online Ticket Retailer

An online ticket retailer promotes music to mainstream listeners by putting on concerts in intimate venues (500 to 3,500 seats). Their current environment is facing increases in demand as artists are gaining popularity due to Internet exposure and mainstream air play.

They will be designing a 3-tier architecture - web, application, and database - based on their current and future needs. The tiers are divided into three layers – presentation (web), business (application), and data (database) – with servers residing in each. Figure 2 illustrates their architecture.

![Figure 2: 3-tier architecture design](/images/figure3.png)

Figure 2: 3-tier architecture design

The first component to be determined is the global load balancer, which has the following requirements:

* Available storefront – up to 24x7 – for top-tier customers
* Anticipate traffic spikes that “follow the sun”
* Handle seasonal spikes in service usage
* Support 7,500 unique shoppers daily and 100 connections per second
* Support highly variable and unpredictable compute requirements

Select [![Load Balancers](/images/load_balancer_icon.png)](load_balancer.md) and review the Considerations and Caveats for each option.  Your choices should be narrowed down to:

| Options | Pros | Cons |
| --- | --- | --- |
| Dyn.com | Geolocation and ratio/weight balancing | No provisioning on private network |
| NginX | Geolocation and ratio/weight balancing | Higher maintenance requiring OS management<br>No management console |
| Citrix NetScaler VPX | Protects against failures of servers/sites<br>Geolocation and ratio/weight balancing<br>Virtual appliance reduces costs/maintenance | Requires appliance(s)for each site |

Table 1: Global load balancer options for online ticket retailer

Based on the pros and cons presented in Table 1, they selected the Citrix NetScaler VPX for their global load balancer. The next component is the firewall, then the local load balancer, and so on. Use the Design Decision Tool to match the best component option based on your solution design requirements. 

Return to [Components](README.md)
