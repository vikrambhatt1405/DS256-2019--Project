# DS256-2019--Project
Articles, checkpoints, stats, numbers and everything else........
## Articles

* [Streaming Distributed DNA Sequence Alignment Using Apache Spark](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8251287), 2017 IEEE 17th International Conference on Bioinformatics and Bioengineering.

The large amount of data generated by NextGeneration Sequencing (NGS) technology, usually in the order
of hundreds of gigabytes per experiment, has to be analyzed
quickly to generate meaningful variant results. The first step
in analyzing such data is to map those sequenced reads to
their corresponding positions in the human genome. One of
the most popular tools to do such sequence alignment is the
Burrows-Wheeler Aligner (BWA mem). One limitation of the
BWA program though is that it cannot be run on a cluster.
In this paper, we propose StreamBWA, a new framework
that allows the BWA mem program to run on a cluster in
a distributed fashion, at the same time while the input data
is being streamed into the cluster. It can process the input
data directly from a compressed file, which either lies on the
local file system or on a URL. Moreover, StreamBWA can start
combining the output files of the distributed BWA mem tasks
at the same time while these tasks are still being executed
on the cluster. Empirical evaluation shows that this streaming
distributed approach is approximately 2x faster than the nonstreaming approach. Furthermore, our streaming distributed
approach is 5x faster than other state-of-the-art solutions such
as SparkBWA. The source code of StreamBWA is publicly
available at https://github.com/HamidMushtaq/StreamBWA

* [SparkBWA: Speeding Up the Alignment of High-Throughput DNA Sequencing Data](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0155461),Published: May 16, 2016.

Next-generation sequencing (NGS) technologies have led to a huge amount of genomic data that need to be analyzed and interpreted. This fact has a huge impact on the DNA sequence alignment process, which nowadays requires the mapping of billions of small DNA sequences onto a reference genome. In this way, sequence alignment remains the most time-consuming stage in the sequence analysis workflow. To deal with this issue, state of the art aligners take advantage of parallelization strategies. However, the existent solutions show limited scalability and have a complex implementation. In this work we introduce SparkBWA, a new tool that exploits the capabilities of a big data technology as Spark to boost the performance of one of the most widely adopted aligner, the Burrows-Wheeler Aligner (BWA). The design of SparkBWA uses two independent software layers in such a way that no modifications to the original BWA source code are required, which assures its compatibility with any BWA version (future or legacy). SparkBWA is evaluated in different scenarios showing noticeable results in terms of performance and scalability. A comparison to other parallel BWA-based aligners validates the benefits of our approach. Finally, an intuitive and flexible API is provided to NGS professionals in order to facilitate the acceptance and adoption of the new tool. The source code of the software described in this paper is publicly available at https://github.com/citiususc/SparkBWA, with a GPL3 license

* [SparkGA: A Spark Framework for Cost Effective, Fast and Accurate DNA Analysis at Scale](https://ce-publications.et.tudelft.nl/publications/1619_sparkga_a_spark_framework_for_cost_effective_fast_and_acc.pdf),ACM-BCB’17, August 20–23, 2017, Boston, MA, USA

In recent years, the cost of NGS (Next Generation Sequencing)
technology has dramatically reduced, making it a viable method for
diagnosing genetic diseases. The large amount of data generated by
NGS technology, usually in the order of hundreds of gigabytes per
experiment, have to be analyzed quickly to generate meaningful
variant results. The GATK best practices pipeline from the Broad
Institute is one of the most popular computational pipelines for
DNA analysis. Many components of the GATK pipeline are not very
parallelizable though. In this paper, we present SparkGA, a parallel
implementation of a DNA analysis pipeline based on the big data
Apache Spark framework. This implementation is highly scalable
and capable of parallelizing computation by utilizing data-level
parallelism as well as load balancing techniques. In order to reduce
the analysis cost, SparkGA can run on nodes with as little memory
as 16GB. For whole genome sequencing experiments, we show that
the runtime can be reduced to about 1.5 hours on a 20-node cluster
with an accuracy of up to 99.9981%. Moreover, SparkGA is about
71% faster than other state-of-the-art solutions while also being
more accurate. The source code of SparkGA is publicly available at
https://github.com/HamidMushtaq/SparkGA1.git.

* [Cluster-Based Apache Spark Implementation of the GATK DNA Analysis Pipeline](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=7359893),17 December 2015.

—Fast progress in next generation sequencing has
dramatically increased the throughout of DNA sequencing, resulting in the availability of large DNA data sets ready for
analysis. However, post-sequencing DNA analysis has become the
bottleneck in using these data sets, as it requires powerful and
scalable tools to perform the needed analysis. A typical analysis
pipeline consists of a number of steps, not all of which can readily
scale on a distributed computing infrastructure. Recently, tools
like Halvade, a Hadoop MapReduce solution, and Churchill, an
HPC cluster-based solution, addressed this issue of scalability in
the GATK DNA analysis pipeline. In this paper, we present a
framework that implements an in-memory distributed version of
the GATK pipeline using Apache Spark. Our framework reduced
execution time by keeping data active in the memory between
the map and reduce steps. In addition, it has a dynamic load
balancing algorithm that better utilizes system performance using
runtime statistics of the active workload. Experiments on a 4 node
cluster with 64 virtual cores show that this approach is 63% faster
than a Hadoop MapReduce based solution.

* [Fast and accurate short read alignment with Burrows–Wheeler transform](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2705234/)

The enormous amount of short reads generated by the new DNA sequencing technologies call for the development of fast and accurate read alignment programs. A first generation of hash table-based methods has been developed, including MAQ, which is accurate, feature rich and fast enough to align short reads from a single individual. However, MAQ does not support gapped alignment for single-end reads, which makes it unsuitable for alignment of longer reads where indels may occur frequently. The speed of MAQ is also a concern when the alignment is scaled up to the resequencing of hundreds of individuals.

* [Heterogeneous Hardware/Software Acceleration of the BWA-MEM DNA Alignment Algorithm ](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=7372576)

The fast decrease in cost of DNA sequencing has
resulted in an enormous growth in available genome data,
and hence led to an increasing demand for fast DNA analysis
algorithms used for diagnostics of genetic disorders, such as
cancer. One of the most computationally intensive steps in the
analysis is represented by the DNA read alignment. In this
paper, we present an accelerated version of BWA-MEM, one of
the most popular read alignment algorithms, by implementing
a heterogeneous hardware/software optimized version on the
Convey HC2ex platform. A challenging factor of the BWAMEM algorithm is the fact that it consists of not one, but
three computationally intensive kernels: SMEM generation, suffix
array lookup and local Smith-Waterman. Obtaining substantial
speedup is hence contingent on accelerating all of these three
kernels at once. The paper shows an architecture containing
two hardware-accelerated kernels and one kernel optimized in
software. The two hardware kernels of suffix array lookup
and local Smith-Waterman are able to reach speedups of 2.8x
and 5.7x, respectively. The software optimization of the SMEM
generation kernel is able to achieve a speedup of 1.7x. This
enables a total application acceleration of 2.6x compared to the
original software version.

* [Spark Scheduler-DeepDive Talk:Data Bricks](https://databricks.com/session/apache-spark-scheduler)

As a core component of data processing platform, scheduler is responsible for schedule tasks on compute units. Built on a Directed Acyclic Graph (DAG) compute model, Spark Scheduler works together with Block Manager and Cluster Backend to efficiently utilize cluster resources for high performance of various workloads. This talk dives into the technical details of the full lifecycle of a typical Spark workload to be scheduled and executed, and also discusses how to tune Spark scheduler for better performance.



* [An intermediate data placement algorithm for load balancing in Spark computing environment](https://www.sciencedirect.com/science/article/pii/S0167739X16302126)

Since MapReduce became an effective and popular programming framework for parallel data processing, key skew in intermediate data has become one of the important system performance bottlenecks. For solving the load imbalance of bucket containers in the shuffle process of the Spark computing framework, this paper proposes a splitting and combination algorithm for skew intermediate data blocks (SCID), which can improve the load balancing for various reduce tasks. Because the number of keys cannot be counted out until the input data are processed by map tasks, this paper provides a sampling algorithm based on reservoir sampling to detect the distribution of the keys in intermediate data. Contrasting with the original mechanism for bucket data loading, SCID sorts the data clusters of key/value tuples from each map task according to their sizes, and fills them into the relevant buckets orderly. A data cluster will be split once it exceeds the residual volume of the current bucket. After filling this bucket, the remainder cluster will be entered into the next iteration. Through this processing, the total size of data in each bucket is roughly scheduled equally. For each map task, each reduce task should fetch the intermediate results from a specific bucket, the quantity in all buckets for a map task will balance the load of the reduce tasks. We implement SCID in Spark 1.1.0 and evaluate its performance through three widely used benchmarks: Sort, Text Search, and Word Count. Experimental results show that our algorithms can not only achieve higher overall average balancing performance, but also reduce the execution time of a job with varying degrees of data skew.

* [Sparrow: Scalable Scheduling for Sub-Second Parallel Jobs](https://www2.eecs.berkeley.edu/Pubs/TechRpts/2013/EECS-2013-29.pdf)

Large-scale data analytics frameworks are shifting towards shorter task durations and larger degrees of parallelism to provide low latency. However, scheduling
highly parallel jobs that complete in hundreds of milliseconds poses a major challenge for cluster schedulers,
which will need to place millions of tasks per second
on appropriate nodes while offering millisecond-level latency and high availability. We demonstrate that a decentralized, randomized sampling approach provides nearoptimal performance while avoiding the throughput and
availability limitations of a centralized design. We implement and deploy our scheduler, Sparrow, on a real cluster
and demonstrate that Sparrow performs within 14% of an
ideal scheduler.

* [An enforcement of real time scheduling in Spark Streaming](https://ieeexplore.ieee.org/abstract/document/7393730)

With the exponential growth in continuous data streams, real time streaming processing has been gaining a lot of popularity. Spark Streaming is one of the open source frameworks for reliable, high-throughput and low latency stream processing. Though it is a near real time stream processing framework running on commodity hardware, real time event processing is not guaranteed in its scheduling system. Profiling results indicate that the total delay time of events with unstable inputs is more volatile and presents big fluctuations. In this paper, we propose a simple, yet effective scheduling strategy to reduce the worst case event processing time by dynamic adjusting the time window of batch intervals. It is a real time enhancement to Spark Streaming based on Spark's framework. The proposed strategy is evaluated using two streaming benchmarks and our preliminary results demonstrate the feasibility of our approach with unstable event streams.

* [Official code repository for GATK versions 4 and up](https://github.com/broadinstitute/gatk)


* [Design and Implementation of Scheduling Pool Scheduling Algorithm Based on Reuse of Jobs in Spark](https://ieeexplore.ieee.org/document/7866139)

As a distributed computing framework based on memory, Spark is being used by more and more enterprises. Generally, Spark runs in multi-user and multi-job mode, where may exist a large number of reuse of jobs. This reuse, here, refers to the calculation reuse inside the jobs, and it can greatly shorten the executing time of jobs in Spark. Therefore, this paper proposes a scheduling pool scheduling algorithm based on reuse of jobs. This algorithm is based on the original scheduling pool scheduling algorithm in Spark and can take great advantage of the reusable parts. Experiments show that the new scheduling algorithm realizes reuse of jobs, and improves the execution efficiency of the cluster.

* [A Hard Real-time Scheduler for Spark on YARN](https://ieeexplore.ieee.org/document/8411083)

Apache Spark is a fast and general engine for large-scale data processing using distributed memory. It provides different deploy modes to meet the needs of different users and Spark on YARN is the most popular deploy mode. Different deploy modes have different scheduling mechanisms. Spark on YARN has three different schedulers, including FIFO Scheduler, Fair Scheduler, and Capacity Scheduler. However, these three schedulers cannot fit hard real-time application scenarios. With the application of Apache Spark more widely, the needs of hard real-time scheduling will increase quickly. In this paper, we proposed a novel hard real-time scheduling algorithm called DVDA (Deadline and Value Density-Aware) in order to meet the requirements of hard real-time scheduling. Compared with traditional EDF (Earliest Deadline First) algorithm which only considers the deadline, the DVDA algorithm considers both the deadline and value density of the application. Furthermore, we implement a DVDA Scheduler for Spark on YARN based on the DVDA algorithm. Finally, the experiments are conducted to verify the effectiveness of the algorithm. Experimental results show that the proposed algorithm can increase the application completed rate by 18% and 6%, Value Income by 78% and 32% compared with default Capacity scheduler and EDF-Capacity scheduler respectively.

* [A Survey of Scheduling Frameworks in Big Data Systems](https://hal-lirmm.ccsd.cnrs.fr/lirmm-01692229/document)

Scheduling frameworks have been designed for different big data systems. They are
targeted at different objectives and scales of clusters with diverse optimization methods.
In this paper, we survey sixteen popular scheduling frameworks, developed by companies
or communities, which we classify in four types: resource managers, Spark schedulers,
Microsoft Cosmos [CJL+08] scheduler and YARN-Based scheduler.

*[Practical Genomics with Apache Spark- Tom White](https://databricks.com/session/practical-genomics-with-apache-spark)

Tom White is a data scientist at Cloudera, specializing in big data and bioinformatics. Previously, Tom was a distributed systems engineer on Hadoop technologies at Cloudera, where he has worked since its foundation in 2008. Tom is a Apache Hadoop committer and author of "Hadoop: the Definitive Guide" the bestselling book published by O'Reilly Media.
