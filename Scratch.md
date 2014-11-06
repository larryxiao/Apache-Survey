# Resource Management

* http://mesos.apache.org
  * Apache Helix is a generic cluster management framework used for the automatic management of partitioned, replicated and distributed resources hosted on a cluster of nodes. Helix automates reassignment of resources in the face of node failure and recovery, cluster expansion, and reconfiguration.
  * https://amplab.cs.berkeley.edu/wp-content/uploads/2011/11/mesos.png
  * http://mesos.apache.org/assets/img/documentation/architecture3.jpg
  * http://mesos.berkeley.edu/mesos_tech_report.pdf

> While the thin interface provided by Mesos allows it to scale and allows the frameworks to evolve independently, one question remains: how can the constraints of a framework be satisfied without Mesos knowing about these constraints? For example, how can a framework achieve data locality without Mesos knowing which nodes store the data required by the framework? **Mesos answers these questions by simply giving frameworks the ability to reject offers. A framework will reject the offers that do not satisfy its constraints and accept the ones that do.** In particular, we have found that a simple policy called delay scheduling, in which frameworks wait for a limited time to acquire nodes storing the input data, yields nearly optimal data locality.

* http://helix.apache.org
  * Once configured for your system, Helix acts as the global brain for the system. It is designed to make decisions that cannot be made in isolation. Examples of such decisions that require global knowledge and coordination:
    * scheduling of maintainence tasks, such as backups, garbage collection, file consolidation, index rebuilds
    * **repartitioning of data or resources across the cluster**
    * informing dependent systems of changes so they can react appropriately to cluster changes
    * throttling system tasks and changes

* http://hadoop.apache.org/docs/current/hadoop-yarn/hadoop-yarn-site/YARN.html

* http://engineering.linkedin.com/cluster-management/auto-scaling-apache-helix-and-apache-yarn
  * ![](http://engineering.linkedin.com/sites/default/files/process-edit.png)

# Computation

* http://spark.apache.org
* http://hama.apache.org

# Discussion
repartitioning, reduce overhead (locality, communication)
