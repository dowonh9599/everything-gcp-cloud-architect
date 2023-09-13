# Pricing and Billing

per-second billing for its:

* Compute Engine (IaaS compute offering)
  * sustained-use discounts: discount for every incremental minute from exceeding 25% of the month.
  * can customize to fit the optimal amounts of vCPU and memory for their applications so that you can tailor your pricing for your workloads.
  * Price Calculator: https://cloud.google.com/products/calculator
* Google Kubernetes Engine (Container IaaS)
* Dataproc (big data system like Hadoop, operating as a service)
* App Engine flexible environment VMs (PaaS)

> How can I make sure I don’t accidentally run up a big Google Cloud bill

* define budgets at the billing account level or at the project level.
  * can be a fixed limit
  * another metri like a percentage of the previous month’s spend
* can create an alert that notifies when your expenses reach 50%, 90% and 100% (customizable) of the maximum capacity.
* Reports, a visual tool in the Google Cloud Console to monitor expenditure based on a project or services
* Quotas, which are designed to prevent the over-consumption of resources because of an error or a malicious attack
  * Rate quotas: reset after a specific time.
    * e.g. GKE service implements a quota of 1,000 calls to its API from each Google Cloud project every 100 seconds.&#x20;
  * Allocation quotas: govern the number of resources you can have in your projects.
    * each Google Cloud project has a quota allowing it no more than five Virtual Private Cloud networks.&#x20;
