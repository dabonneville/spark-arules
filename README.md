## Top-K (Non Redundant) Association Rules with Spark

Association rule mining is a wide-spread technique to determine hidden interesting relations between items in large-scale 
transaction databases. This technique is often applied to data recorded by point-of-sale systems in supermarkets and is able 
to determine associations of the following kind:

> A customer who is willing to buy one or more products together is likely to also buy other items as well.

Association rules are used as a basis for decision making in promotional pricing, product placement and more. The application of 
such rules, however, is not restricted to market basket analysis and will be used in intrusion detection, web usage mining and other 
areas.

### Apache Spark


From the [Apache Spark](https://spark.apache.org/) website:

> Apache Spark is a fast and general engine for large-scale data processing and is up to 100x faster than Hadoop MR in memory.

The increasing number of associated projects, such as [Spark SQL](https://spark.apache.org/sql/) and [Spark Streaming](https://spark.apache.org/streaming/), enables Spark to become the future  Unified Data Insight Platform. With this perspective in mind, in this project we have integrated recently published Association Rule algorithms with Spark. This allows for a seamless usage of association rule mining either with batch or streaming data sources.

### Top-K (Non Redundant) Association Rules

Finding interesting associations between items in transaction databases is a fundamental data mining task. Finding association rules is 
usually accompanied by the following control parameters:

* **Support**: The percentage of transactions of the database where the rules occurs.

* **Confidence**: The support of the rule divided by the support of its *antecedent*.

The goal of association rule mining then is to discover all rules that have a support and confidence that is higher to user-defined thresholds 
*minimum support* and *minimum confidence*. The challenge is choose the right thresholds with respect to the considered transaction database.

This is a major problem, as one usually has limited resources for analyzing the mining results, and fine tuning of the thresholds is time-consuming job:

**Thresholds are set too high**: 
This generates too few results and valuable information may be omitted.

**Thresholds are set too low**: 
This can generate a huge amount of results, and the mining task may become very slow.



