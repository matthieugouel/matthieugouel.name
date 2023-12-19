+++
title = "Replication: Towards a Publicly Available Internet scale IP Geolocation Dataset"
date = "2023-10-24"
tags = ["research", "poster", "imc2023"] 
abstract  = "IP geolocation is one of the most widely used forms of metadata for IP addresses, and despite almost twenty years of effort from the research community, the reality is that there is no accurate, complete, up-to-date, and explainable publicly available dataset for IP geolocation. We argue that a central reason for this state of affairs is the impressive results from prior publications, both in terms of accuracy and coverage: up to street level accuracy and locating millions of IP addresses with a few hundred vantage points in months. We believe the community would substantially benefit from a public baseline dataset and code. To encourage future research in IP geolocation, we replicate two geolocation techniques and evaluate their accuracy and coverage. We show that we can neither use the first technique to obtain the previously claimed street level accuracy, nor the second to geolocate millions of IP addresses on today’s Internet and with publicly available measurement infrastructure. In addition to this reappraisal, we re-evaluate the fundamental insights that led to these prior results, as well as provide new insights and recommendations to help the design of future geolocation techniques. All of our code and data are publicly available to support reproducibility."
+++

IP geolocation is one of the most widely used forms of metadata for IP addresses, and despite almost twenty years of effort from the research community, the reality is that there is no accurate, complete, up-to-date, and explainable publicly available dataset for IP geolocation. We argue that a central reason for this state of affairs is the impressive results from prior publications, both in terms of accuracy and coverage: up to street level accuracy and locating millions of IP addresses with a few hundred vantage points in months. We believe the community would substantially benefit from a public baseline dataset and code. To encourage future research in IP geolocation, we replicate two geolocation techniques and evaluate their accuracy and coverage. We show that we can neither use the first technique to obtain the previously claimed street level accuracy, nor the second to geolocate millions of IP addresses on today’s Internet and with publicly available measurement infrastructure. In addition to this reappraisal, we re-evaluate the fundamental insights that led to these prior results, as well as provide new insights and recommendations to help the design of future geolocation techniques. All of our code and data are publicly available to support reproducibility.

---

Paper on ACM library: https://dl.acm.org/doi/10.1145/3618257.3624801  
Paper in Open Access: https://hal.science/hal-04215113/document  


---

Source code of the evaluation section: https://github.com/dioptra-io/geoloc-imc-2023    

```
@inproceedings{darwich2023replication,
  title={Replication: Towards a Publicly Available Internet scale IP Geolocation Dataset},
  author={Darwich, Omar and Rimlinger, Hugo and Dreyfus, Milo and Gouel, Matthieu and Vermeulen, Kevin},
  booktitle={ACM Internet Measurement Conference (IMC 2023)},
  year={2023},
  organization={ACM}
}
```
