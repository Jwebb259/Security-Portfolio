# Security Portfolio: Jacob W

Documented cloud security investigations, built in a live Azure tenant
(Mad Hat Labs, a multi-user training environment).

Target role: SOC Analyst / Security Analyst
Currently: TTI FMSR | Elko / Remote
Contact: https://www.linkedin.com/in/jacob-webb-128450207/

## Investigations
| # | Title | Focus | Write-up |
|---|-------|-------|----------|
| 1 | Operation Dead Deploy | Governance forensics, deployment audit trail | coming, week 1 |

# [Flagged Resource Group Investigation]
## Scenario
Recently brought on Intern had permission that allowed deployment for a "Test Environment", and did not follow company Playbook policies during set-up for Azure Resource groups. Investigating concerns regarding automated fail-safes allowing Naming violations to be created. Found that Shared key access is enabled and could be a weak point for cloud access security. 

## Environment
live multi-user Azure training tenant, Reader access.

## Investigation

1. analyzed Azure Environment, and located visible 
naming violation after sifting through resource groups.

2. went through tags associated within Interns deployment to verify ownership within the organization.

3. accessed policy information attached to deployment, found parameters for naming conventions is set to "audit".

4. found that there are no assigned Parent Initiatives for naming violation compliance.

5. Shared key access was enabled for azure tenant.



## What broke / what surprised me

1. Azure policy parameters where set to audit, should be configured to prevent violations for Resource Group naming conventions.

2. Cloud environment is accessible via public network.

3. Proper account authorizations could be configured to inherit policies.

4. The process for this investigation took a lot longer than expected having to familiarize myself within Azure.


## Findings and recommendations

1. Set-up Microsoft Entra Private Access for secure tunneling so Unauthenticated devices on public networks cannot see or reach endpoints. 

2. Add users to Management Groups for automated initiatives to prevent policy violations.

3. Rename Resource Group to "rg-jenkins-test-eastus".

## What I learned

1. there is a way to connect more private and secured than public access.

2. Azure was hard to navigate initially until redoing assignment multiple times.

3. The importance of setting up proper properties and inheritance.
   

| 2 | The Stolen Identity | App registration attack kill chain (Entra ID) | coming, week 2 |
| 3 | Privilege Audit | RBAC and least privilege | coming, week 3 |
| 4 | Spin Up and Lock Down | Compute attack surface | coming, week 4 |
| 5 | Network the Operative | Network segmentation | coming, week 5 |
| 6 | Bucket Looting | Storage exposure hunting | coming, week 6 |
| 7 | Find the Anomaly | Log analysis and KQL | coming, week 7 |
| 8 | Hunt the Threat | SIEM operations (Sentinel) | coming, week 8 |
| 9 | Score the Tenant | Cloud security posture | coming, week 9 |
| 10 | The Breach (capstone) | Full incident investigation | coming, week 10 |


