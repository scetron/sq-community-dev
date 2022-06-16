---
title: Developing a new Service in Suzie Q
author: Stephen Corry
keywords: suzieq, development, testing, service
marp: true
theme: gaia
---

# Developing a new Suzie Q Service
<br>
<br>
<br>
<br>
<br>
<br>

Suzie Q Community Meeting
June 16, 2022
Stephen Corry

---
# Goal

Add basic multicast collection data to Suzie Q. Want the time based state of multicast in a searchable format, similar to the other services that are already available.

### Use Case

Distributed, site specific pollers and collectors for other Services in Suzie Q. 
Also collecting routing and interface information.

---

# TLDR;

- Relatively easy to add services once the requirements were determined.

--- 
# Developer Experience
Relatively easy to get started using Poetry

Easier with Container lab

Excellent Tool, but needs more developer documentation

Other items:
- Tough: Normalization
- Hard: Testing
- Nice to have: Development Container

---
# Documentation

*What documentation can't be improved?*

Helpful hints, but partially out of date, which might lead you down the wrong path.

Much, prompt, help on Slack. 

Look forward to some updates as a result of this exercise.

---
# Normalization

The service definition and data normalization was difficult.

- Jmespath like syntax
- Difficult data structures from different manufacturers
- Easier to use TextFSM and `_clean_<nos>` python

---
# Testing

Lots of Existing Tests
- Integration: tests all services for new namespace
- new namespace may not have all services activated
- Commands to generate parquet data
- No commands to generate output fixtures