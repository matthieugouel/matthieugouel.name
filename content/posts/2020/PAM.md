+++
title = "Alias Resolution Based on ICMP Rate Limiting"
date = "2020-02-01"
tags = ["research", "paper", "pam2020"]
abstract = "Alias resolution techniques (e.g., Midar) associate, mostly through active measurement, a set of IP addresses as belonging to a common router. These techniques rely on distinct router features that can serve as a signature. Their applicability is affected by router support of the features and the robustness of the signature. This paper presents a new alias resolution tool called Limited Ltd. that exploits ICMP rate limiting, a feature that is increasingly supported by modern routers that has not previously been used for alias resolution. It sends ICMP probes toward target interfaces in order to trigger rate limiting, extracting features from the probe reply loss traces. It uses a machine learning classifier to designate pairs of interfaces as aliases. We describe the details of the algorithm used by Limited Ltd. and illustrate its feasibility and accuracy. Limited Ltd. not only is the first tool that can perform alias resolution on IPv6 routers that do not generate monotonically increasing fragmentation IDs (e.g., Juniper routers) but it also complements the state-of-the-art techniques for IPv4 alias resolution. All of our code and the collected dataset are publicly available."
+++

Kevin Vermeulen, Burim Ljuma, Vamsi Addanki, **Matthieu Gouel**, Olivier Fourmaux, Timur Friedman, Reza Rejaie

Alias resolution techniques (e.g., Midar) associate, mostly through active measurement, a set of IP addresses as belonging to a common router. These techniques rely on distinct router features that can serve as a signature. Their applicability is affected by router support of the features and the robustness of the signature. This paper presents a new alias resolution tool called Limited Ltd. that exploits ICMP rate limiting, a feature that is increasingly supported by modern routers that has not previously been used for alias resolution. It sends ICMP probes toward target interfaces in order to trigger rate limiting, extracting features from the probe reply loss traces. It uses a machine learning classifier to designate pairs of interfaces as aliases. We describe the details of the algorithm used by Limited Ltd. and illustrate its feasibility and accuracy. Limited Ltd. not only is the first tool that can perform alias resolution on IPv6 routers that do not generate monotonically increasing fragmentation IDs (e.g., Juniper routers) but it also complements the state-of-the-art techniques for IPv4 alias resolution. All of our code and the collected dataset are publicly available.

---

Paper in Open Access: https://arxiv.org/pdf/2002.00252.pdf

```
@article{vermeulen2020alias,
  title={Alias Resolution Based on ICMP Rate Limiting},
  author={Vermeulen, Kevin and Ljuma, Burim and Addanki, Vamsi and Gouel, Matthieu and Fourmaux, Olivier and Friedman, Timur and Rejaie, Reza},
  journal={arXiv preprint arXiv:2002.00252},
  year={2020}
}
```
