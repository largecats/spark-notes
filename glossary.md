# Glossary

## Spark

**Worker node.** A member of the cluster. It can be a virtual machine (JVM) or a physical computer.

**Executor.** A process launched for a Spark application on a worker node.

**RDD.** Immutable distributed collection of objects with lineage dependency (i.e., how the RDD is constructed), partitioned across nodes in the cluster that can be operated in parallel. 

* The RDD API is not structured.
* Computation expressed in high-level structured APIs (Dataframe and Dataset) => low-level optimized RDD operations => Scala bytecode for executors' JVMs.

**Row.** A generic untyped JVM object type in Spark, holding a collection of different types of fields that can be accessed using an index.

**Dataframe.** A structured collection of generic objects Dataset[Row] (untyped).

* A DataFrame is an untyped view of Dataset.
* Python and R support the untyped DataFrame API.
* Can let Spark infer schema.

**Dataset.** A structured collection of strongly-typed JVM objects, dictated by a case class you define in Scala or a class in Java.

* Scala and Java support the strongly typed Dataset API.

* Schema must be supplied.
* Dataset and Dataframe are unified in Spark 2.



## Hadoop Eco-system

TBD