# Chapter 5 — Conclusion and Recommendations

*Text in this document is taken from the capstone manuscript.*

---

## Capabilities

> The proposed network infrastructure for X Company will enhance reliability, security, and availability due to having redundant connections to different ISPs (ISP failover), the use of High Availability mechanisms, and secure communication between all branches. In case one of the FortiGates fails, the other takes its place. With ISP failover, the system automatically switches from the primary ISP to the secondary when the primary goes down.

> Secure communication between the head office and the two branches is provided using an IPsec VPN so as to prevent unauthorized third parties from accessing confidential and sensitive information being sent via this link.

> The proposed design also includes support for a LAN-WAN architecture that incorporates VLANs and HSRP to provide internal network organization, traffic control, and gateway redundancy. Furthermore, the FortiGate firewall will allow control over the websites and applications that users can access. The Wazuh system will provide monitoring and logging functions within the simulated network.

**Summary of capabilities**

> - Increases reliability using multi-homed ISP connections and ISP failover capabilities
> - Allows for continued service delivery through FortiGate HA functionality
> - Ensures secure communications between each branch using an IPsec VPN
> - Offers VLAN segmentation and HSRP gateway redundancy
> - Applies web filtering and application control
> - Permits for ongoing auditing, logging, and monitoring through Wazuh
> - Produces a secure, resilient, and well-organized network environment

---

## Limitations

> The Proposed Design Implementation will require Technical Personnel with experience/knowledge in Network Configuration, Security Management, High Availability, ISP Failover, Web Filtering/Control, Wazuh Monitoring, and IPsec Deployment.

> While IPsec provides a level of security for Inter-Branch Communications, there are some limitations to consider. For example, IPsec can add overhead that contributes to Latency and/or a slight reduction in Network Speed, particularly under low-bandwidth conditions.

> The multiple ISP setup includes ISP Failover but does not include Load Balancing. As this Study was conducted within a Simulated Prototype Environment, results may not completely replicate actual deployment environments, including Real ISP Behavior, Hardware Variations, Physical Cabling Issues, and Actual User Traffic Volumes.

**Summary of limitations**

> - Requires technicians with technical skills to set up and maintain
> - May have a small amount of performance loss due to IPsec encryption
> - Only uses ISP failover and does not include Load Balancing
> - Results from the simulation may be different than results in an actual world deployment
> - Real-world results can be influenced by hardware, bandwidth, ISP behavior, and user volume

---

## Summary of findings

### 1. Network reliability

> X Company's proposed network structure effectively implemented a structured LAN-WAN topology using a main branch and two sub-branch structures. Findings such as these satisfy Objective 1 since they show that the proposed structure has provided a well-organized network structure to connect the main location with its remote locations.

> Implementing redundant Internet Service Provider (ISP) connections improved the reliability of the X Company network by providing a way to reduce dependency on any single internet connection. By implementing ISP failover capabilities, the network would automatically route traffic through a designated backup ISP should the primary ISP become unavailable.

> By deploying two FortiGate firewalls configured in High Availability (HA) mode, the network maintains continuous availability. When one firewall becomes non-operational, the HA configuration enables the second firewall to assume control while the first is being repaired.

> Utilizing Hot Standby Router Protocol (HSRP) at the core switch layer maintains gateway redundancy; therefore, it allows continued internal communication should the core switch fail.

### 2. Security enhancement

> The site-to-site VPN implemented via IPsec VPN provided for secure communications between the parent branch office and all child branch offices. All data exchanged between these locations is encrypted in transit.

> VLAN segmentation provides logical partitioning of intra-departmental network traffic within the LAN environment. Therefore, Objective 3 has been satisfied, since the overall organization of the internal networks has increased, and the exposure to other departments has decreased where it was deemed unnecessary.

> FortiGate's Web Filtering and Application Control has added another layer of protection to the network by controlling user access to sites and applications based on previously established security rules.

> Cloudflare protects the hosted web application from attacks by utilizing a web application firewall, traffic filters, and rate limits, and mitigates selected web application attacks.

### 3. Performance optimization

> The use of VLAN segmentation, VLSM subnetting, DHCP, and VLAN routing for a local network environment enables organized internal communication and efficient use of IP addresses, thus network organization, addressing, and manageability are improved.

> The LAN-WAN architecture used in the main branch and sub-branches of the company enabled better communication by using a more structured design.

> The integration of the cloud-hosted website, application, and MySQL database to the internal network infrastructure for business services to be accessed by customers over the Internet.

### 4. Monitoring and manageability

> The inclusion of Wazuh enables monitoring, logging, and auditing of selected security-related events within the simulated environment. This finding fulfills Objective 5 by providing improved visibility into network and system activities. Wazuh also offers built-in functionality for monitoring security events, file integrity, vulnerability issues, and log reviews.

> Based on evaluations conducted in accordance with ISO/IEC standards, the proposed infrastructure received favorable assessments in system evaluation, reliability, security, monitoring capability, and overall acceptability. The mean score of 3.73 corresponds to a "Very Good" rating, confirming that the infrastructure meets the study's requirements for system performance, security, reliability, and monitoring.

---

## Conclusion

> The design and simulation of the proposed X Company network infrastructure demonstrate how the integration of specific components enables the organization to better manage its network, strengthen security, and enhance the user experience. The use of multiple ISPs, ISP failover, High Availability, HSRP, VLANs, and Site-to-Site IPsec VPNs collectively provides the connectivity, security, and reliability required by the organization.

> Through testing and evaluation, the designed infrastructure has shown the capability to meet the organization's requirements for local and wide-area communications, internal organization, and security. Additionally, the implemented security solutions — Wazuh, Cloudflare, FortiGate, and cloud services — ensure effective management of both internal and external network resources.

> The results of testing confirm that the proposed infrastructure is functional, practical, and suitable for deployment within the organization. It has proven to be more resilient, secure, and manageable than a basic network infrastructure lacking these features, thereby serving as an effective solution to the organization's communication, security, and availability needs.

> However, it must be noted that the testing was conducted within a simulated and prototype-based environment, which may not fully reflect performance under real-world conditions with the organization's existing hardware and operational environment.

---

## Recommendations

> Based on the findings of the study, the following recommendations can be implemented to enhance the security of the proposed network infrastructure:

**1. Implement the proposed infrastructure within an actual organization's office**
> The proposed infrastructure should be implemented within an actual organization's office to evaluate the effectiveness of the network. The performance of the network within the office will help to determine whether it is successful at delivering the benefits proposed within the study.

**2. Strengthen endpoint and network security controls**
> The network infrastructure can be further enhanced by implementing additional security features. These may include deploying endpoint detection and response (EDR) software, enforcing multi-factor authentication (MFA) for all network users, and integrating additional intrusion detection and prevention (IDS/IPS) solutions to strengthen overall network protection.

**3. Enhance Wazuh monitoring and incident visibility**
> The Wazuh software can be enhanced by implementing additional rules and features to provide better visibility into the security of the network.

**4. Apply regular maintenance and security reviews**
> The organization should perform regular maintenance and security review tasks on the network, including performing regular firmware updates on the devices, conducting firewall policy and VPN configuration reviews, and conducting vulnerability and security audits of the network.

**5. Expand the architecture for future growth**
> The infrastructure can be expanded to accommodate additional branch locations of the company in the future, should the organization grow. Future expansions would include VLANs, endpoints to monitor, firewall policies, VPN tunnels, and more to accommodate the growing number of branches.

**6. Explore cloud-native SASE architecture**
> Future researchers in this area may investigate the use of cloud-native Secure Access Service Edge (SASE) as a means of securing the organization's users, branches, and cloud services. The benefits of utilizing this technology would include scalability and control of the services provided to those users.

**7. Explore AI-based anomaly detection and failover optimization**
> In addition to the current infrastructure and security measures in place, some future improvements include incorporating AI into the network to detect network anomalies, as well as optimizing the failover process of the ISP's internet links to provide better coverage and fewer downtimes.

**8. Improve documentation and training for administrators**
> Proper technical documentation and training of the administrators regarding the management of the Fortinet devices and their features, such as HA, failover to ISPs, HSRP, VLANs, IPsec, Web Filtering, Application Control, Wazuh, and Cloudflare and cloud services, will ensure that the administrators can maintain the network properly.

---

**Previous:** [← Testing and Results](05-testing-and-results.md) · [Back to README](../README.md)
