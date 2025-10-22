---
title: "Announcing nxthdr: A Non-Profit Platform for Internet Research and Education"
date: "2025-09-30"
tags: ["project", "NXTDR"]
---


For the past year and a half, I have been working on a project called [nxthdr](https://nxthdr.dev) in my spare time. Today, this side project has become an official French *association loi 1901* (non-profit organization).

nxthdr operates a global network infrastructure designed specifically for Internet research and education. The platform offers flexible, worldwide active measurements from our own autonomous system and provides peering capabilities through multiple Internet exchanges.

<!--more-->

## Problem Statement

When doing research on how the Internet works in practice, researchers often need either (1) to perform active or passive measurements, or (2) to conduct routing experiments.

### Internet Measurements

Internet measurement research can broadly be split into two categories: **passive** and **active** measurements.

A key passive measurement is monitoring BGP announcements. There are already several well-established passive BGP monitoring platforms such as [RIPE RIS](https://www.ripe.net/analyse/internet-measurements/routing-information-service-ris/) and [RouteViews](https://www.routeviews.org/). In parallel, active measurement platforms like [RIPE Atlas](https://atlas.ripe.net/) and [CAIDA Ark](https://www.caida.org/projects/ark/) exist. Other initiatives, such as [MLab](https://measurementlab.net/), do not allow performing measurements but instead provide open datasets to the community. So one could wonder, why another platform?

First, these active platforms are not always easily accessible. For example, Ark provides data, but it is intended for long-term analysis since it is not real-time. You can perform measurements, but only after a manual onboarding process and approval. Atlas, on the other hand, provides both fresh and historical data and even a self-service measurement interface. However, it requires credits to perform measurements, which are obtained by hosting an Atlas probe.

For newcomers to the community, such as PhD or university students, there is, in my opinion, a barrier to entry for performing measurements. And even with credits or access, several limitations remain:

- The measurement tools available are often limited to standard ones like ping and traceroute. It’s difficult to test new measurement tools at scale without special access or partnerships.
- They don’t collect BGP data at the probe level. This makes it hard (or impossible) to properly correlate measurements with BGP announcements from RIS or RouteViews.
- Anycast measurements are basically impossible on these platforms, since probes are hosted in multiple ASes and the platform doesn’t control the source prefixes. It’s a niche use case, but still.

### Routing Experiments

Announcing a prefix to the Internet is not particularly hard, but it requires both resources and time. You need an IP prefix, an Autonomous System (AS) that owns it, and routers connected to the Internet through which the prefix can be announced.

That’s why many research papers on routing experiments rely on testbeds or simulations, and why students often learn BGP using GNS3, Mininet, or Packet Tracer on their laptops.

There is at least one peering platform, [PEERING](https://peering.ee.columbia.edu/), which allows researchers to announce prefixes to the Internet. However, it is not a self-service platform. And since PEERING is not a measurement platform, you cannot easily perform synchronized active measurements alongside your peering experiments without carefully coordinating external tools like Atlas or Ark.

## Proposed Solution

Building an active measurement platform with hundreds of thousands of probes around the world, like Atlas or Ark, is a huge challenge. It’s equally difficult to gain access to dozens of IXPs and IPv4 prefixes for large-scale peering experiments.

nxthdr is **not** designed to compete with these platforms in the areas they already do well. Instead, it aims to close specific gaps for researchers and provide an easy entry point for students.

We operate our own AS and several IPv6 prefixes, and we have access to multiple IXPs (NL-IX, LocIX, FranceIX) in Europe. We also maintain probing servers in multiple countries where we control the source prefixes and collect BGP announcements.

On top of this growing infrastructure, we are developing self-service tools to perform customizable active and passive measurements and routing experiments. We provide:

- Tools to easily build your own probing tools and experiments,
- Dashboards to analyze measurement, BGP, and traffic datasets,
- Notebooks, tutorials, and documentation to help you learn and explore the fascinating world of Internet research.

### Core Principles

**Open Data**
All datasets are released into the public domain under the [PDDL license](https://opendatacommons.org/licenses/pddl/) — no restrictions, delays, or authentication required.

**Open Source**
Every application and piece of infrastructure is open source. You can use them, contribute to them, or even run your own instance.

**Radically Transparent**
Our monitoring, roadmap, and finances are completely public.

## Why a Non-Profit?

The future of this project depends on our ability to raise funds to maintain and grow our infrastructure. So far, our goal has been to provide a proof-of-concept and support at least one research project and one university course.

Looking ahead, we plan to expand to more IXPs and increase the number of probing servers, enabling more research projects, students, and enthusiasts to participate.

If you are interested in supporting this initiative, please reach out at [admin@nxthdr.dev](mailto:admin@nxthdr.dev).

