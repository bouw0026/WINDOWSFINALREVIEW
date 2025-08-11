# Exam Preparation – Potential Written Questions & Answers
This document outlines **9 likely written exam questions**, their model answers, and a mapping to **broad enterprise categories** for study focus.

## Questions & Answers
### 1. Explain how Azure Traffic Manager reduces latency for users across multiple geographic regions. Include in your answer the routing methods it supports and when each is most effective.
Azure Traffic Manager is a DNS-based global traffic distribution service. It reduces latency by directing client requests to the closest or best-performing endpoint. It supports multiple routing methods:  
- **Performance routing** → lowest-latency endpoint.  
- **Priority routing** → failover to secondary if primary fails.  
- **Geographic routing** → serve region-specific content.  
- **Weighted routing** → distribute proportionally across endpoints.

**Enterprise advantage:** Improves user experience, supports failover, optimizes network path efficiency without code changes.

### 2. Azure Advisor provides optimization guidance in several categories. List these categories and provide one practical example for each in the context of enterprise cloud deployments.
Azure Advisor analyzes resource configurations and usage telemetry to provide recommendations in five categories:  
1. **Cost** → resize underutilized VMs.  
2. **Performance** → add premium storage for high IOPS workloads.  
3. **Reliability** → enable availability sets/zones.  
4. **Security** → enable encryption, secure network access.  
5. **Operational Excellence** → apply tags/automation.

**Enterprise advantage:** Consolidates best practices into actionable steps, reducing time to identify inefficiencies.

### 3. Describe the key prerequisites and components of Windows Deployment Services (WDS) in an enterprise environment. Include infrastructure dependencies, image types, and deployment methods.
**Infrastructure prerequisites:**  
- **Active Directory** (integrated mode)  
- **DHCP** for PXE boot IPs  
- **DNS** for server resolution  
- **WDS role** installed  

**Key components:** Install images, boot images, capture images, discover images.  
**Deployment methods:** Unicast or multicast.  
**Enterprise advantage:** Enables standardized, automated OS rollouts at scale.

### 4. Compare and contrast Azure Policy, Blueprints, and Role-Based Access Control (RBAC). How would these be combined to enforce compliance in a multinational corporation?
- **Azure Policy** → enforces compliance (audit/deny).  
- **Azure Blueprints** → package policies, RBAC, templates for repeatable deployments.  
- **RBAC** → role-based access control with least privilege.

**Enterprise integration:**  
1. Use Blueprints for baseline deployment.  
2. Apply Policies for standards (naming, region).  
3. Assign RBAC to limit actions.

**Result:** Scalable, compliant governance for large orgs.

### 5. An enterprise is planning hybrid identity integration between on-premises Active Directory and Azure Active Directory. Outline the available authentication methods, their advantages, and their potential security risks.
**Options:**  
- **Password Hash Sync** → hashes synced to Azure AD; simple, low maintenance.  
- **Pass-through Auth** → validates against on-prem AD.  
- **Federation (AD FS)** → token-based auth with advanced scenarios.

**Security add-ons:** MFA, Conditional Access.

**Enterprise advantage:** Balances UX and security, supports hybrid workloads.

### 6. How does Azure Pricing Calculator help enterprises plan for cost efficiency? Demonstrate by explaining at least three cost-optimization strategies available before deployment.
Azure Pricing Calculator models usage for monthly cost estimates. Strategies:  
1. Right-size VMs.  
2. Reserved Instances for 1–3 years.  
3. Choose cost-effective regions.  
4. Azure Hybrid Benefit for licenses.  
5. Shut down non-critical resources off-hours.

**Enterprise advantage:** Prevents budget overrun via pre-deployment planning.

### 7. You are tasked with designing a secure deployment of a customer-facing web application in Azure. Explain which Azure services, security features, and monitoring tools you would implement, and why.
**Services:** Azure App Service, Application Gateway with WAF, Azure Front Door.  
**Security:** NSGs, Key Vault, Azure AD.  
**Monitoring:** Azure Monitor, Defender for Cloud.

**Enterprise advantage:** Protects app availability, integrity, confidentiality while meeting compliance.

### 8. Explain the steps and considerations involved in using a capture image in WDS to create a standardized OS deployment for a large organization. Discuss advantages and limitations of this approach.
1. Prepare reference PC with OS, updates, apps.  
2. Run Sysprep to generalize.  
3. Boot into capture image.  
4. Save as WIM.  
5. Upload to WDS.

**Advantages:** Consistent builds, faster deployment.  
**Limitations:** Needs updating, large image sizes.

### 9. If setting up a public-facing web server, which DNS records should you configure, and what is their purpose?
**Required:**  
- **A record** → maps domain/subdomain to IPv4 address of the server.

**Optional / Best Practice:**  
- **CNAME record** → alias for a domain/subdomain pointing to another domain.  
- **PTR record** → reverse lookup mapping IP to domain (important for verification/logging).

**Extra credit:**  
- **AAAA record** → maps domain/subdomain to IPv6 address.  
- **TXT record** → for verification or SPF/DKIM email security policies.


## Category Mapping Matrix

| # | Broad Category | Why It's Enterprise-Relevant / Multi-Variable |
|---|----------------|----------------------------------------------|
| 1 | Azure Networking & Performance Optimization | Multi-region routing is key to uptime; tests latency, routing, failover. |
| 2 | Azure Cost Management & Optimization | Links cost, performance, security, reliability; maps recommendations to scenarios. |
| 3 | Windows Deployment Services (Infrastructure & Imaging) | Integrates AD/DHCP/DNS; tests deep infra understanding. |
| 4 | Azure Governance & Compliance | Vital for multi-tenant compliance; enforces policy at scale. |
| 5 | Identity & Access Management (Hybrid) | Hybrid identity is critical; covers auth methods and risk. |
| 6 | Azure Pricing & Licensing Tools | Links cost forecasting and deployment strategy. |
| 7 | Azure Security Architecture & Monitoring | Tests integrated architecture and security planning. |
| 8 | WDS Advanced Imaging & Standardization | Covers imaging from build to deployment, pros/cons. |
| 9 | DNS Fundamentals & Web Hosting | Foundational to web hosting; tests DNS record knowledge. |
