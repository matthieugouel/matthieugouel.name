+++
title = "Towards a Publicly Available Framework to Process Traceroutes with MetaTrace"
date = "2023-10-24"
tags = ["research", "poster", "imc2023"] 
abstract  = "The objective of this research is to contribute towards the development of an open-source framework for processing large-scale traceroute datasets. By providing such a framework, we aim to benefit the community by saving time in everyday traceroute analysis and enabling the design of new scalable reactive measurements, where prior traceroute measurements are leveraged to make informed decisions for future ones. It is important to clarify that our goal is not to surpass proprietary solutions like BigQuery, which are utilized by CDNs for processing billions of traceroutes. These proprietary solutions are not freely accessible to the public, whereas our focus is on creating an open and freely available framework for the wider community. Our contributions include (1) sharing the ideas and thinking process behind building MetaTrace, which efficiently utilizes ClickHouse features for traceroute processing; and (2) providing an open-source implementation of MetaTrace."
+++

**Matthieu Gouel**, Omar Darwich, Maxime Mouchet, Kevin Vermeulen

The objective of this research is to contribute towards the development of an open-source framework for processing large-scale traceroute datasets. By providing such a framework, we aim to benefit the community by saving time in everyday traceroute analysis and enabling the design of new scalable reactive measurements, where prior traceroute measurements are leveraged to make informed decisions for future ones.
It is important to clarify that our goal is not to surpass proprietary solutions like BigQuery, which are utilized by CDNs for processing billions of traceroutes. These proprietary solutions are not freely accessible to the public, whereas our focus is on creating an open and freely available framework for the wider community.
Our contributions include (1) sharing the ideas and thinking process behind building MetaTrace, which efficiently utilizes ClickHouse features for traceroute processing; and (2) providing an open-source implementation of MetaTrace.

We evaluated MetaTrace using two types of queries: predicate queries for filtering traceroutes based on conditions, and aggregate queries for computing metrics on traceroutes. Our results show that MetaTrace is significantly faster compared to alternative solutions.
For predicate queries, it outperforms a multiprocessed Rust solution by a factor of 552 and is 3.4 times faster than ClickHouse without MetaTrace optimizations. For aggregate queries, MetaTrace processes 202 million traceroutes in 11 seconds, with its performance scaling linearly with traceroute volume. Notably, on a single server, MetaTrace can perform a predicate query on a 6-year dataset of 6 billion traceroutes in just 240 seconds.
Furthermore, MetaTrace is resource-efficient, making it accessible for research groups with limited resources to conduct Internetscale traceroute studies.

---

Paper on ACM library: https://dl.acm.org/doi/abs/10.1145/3618257.3625001  
Paper in Open Access: https://hal.science/hal-04218315v1/document  


---

Source code of MetaTrace: https://github.com/dioptra-io/metatrace  

```
@inproceedings{gouel2023poster,
  title={Poster: Towards a Publicly Available Framework to Process Traceroutes with MetaTrace},
  author={Gouel, Matthieu and Darwich, Omar and Mouchet, Maxime and Vermeulen, Kevin},
  booktitle={ACM Internet Measurement Conference (IMC 2023)},
  year={2023}
}
```
