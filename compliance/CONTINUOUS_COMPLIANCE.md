---
title: Compliance as Code presentatioin
description: An example slide deck created using Marpit
paginate: true
marp: true
theme: gaia
class: invert
---

# Continuous Compliance with Lula

![w:400 h:400](./images/logo.png)

---

# Introduction
- Compliance Vs Security
- ATO <-> cATO
- Improving on the cATO
- Continuous Compliance
- Lula
- Demo

<!--
- Demo prepared - wanted to "set the stage" 
-->

---
<!-- _footer: https://ventureinsecurity.net/p/the-importance-of-adopting-a-security -->
# Compliance Vs Security

![w:1120 h:400](./images/data-breach.png)

<!--
- The intent of implementing compliance requirements is to promote security.
- You can look at compliance as a checkbox activity to create some body of evidence that "do compliance stuff" - OR - you can meet the intent of compliance and promote security through continuous validation.
-->

---

# ATO <-> cATO
- What do we need to be approved initially?
- How do we plan to deliver updates to be approved continuously?
- What do we plan to deliver and how will it impact security?

- Considerations need to be made:
    - Approve a process that is continuously auditable vs point in time product
    - Re-usable compliance artifacts that are validated continuously
    - CI/CD and GitOps to perform validation on change

<!-- 
- The goal here isn't to bike shed about which to use
- More important to focus on how to deliver - securely - and how to drive for optimal outcomes with regards to approval.
- Holistically - we want to look at
    - How we get there initially - keying in on future sustainability
    - How do we plan to retain approval as we deliver updates
    - What are we delivering - how does it impact security? some apps more than others
- Given what we want to do - we start to make considerations for optimal processes
- Note: You can do all of this without OSCAL and Lula 
-->

---
<!--_footer: 1. Governance, Risk, Compliance-->
# Improving on the cATO
- Re-usable Components
    - OSCAL models
- Pre-runtime Validation
    - CI/CD quality gates for GitOps workflow -> Compliance Mapping
- Event-driven runtime Validation
    - Integration with GRC[1] tooling
    - Live Visualization
<!--
- The mission ultimately demands transparency and insights in real-time 
- OSCAL is - in my opinion - how we cast a vote towards tomorrow that we want process to be better. 
- It's an artifact that does nothing on it's own - but positions itself for standard automated use. 
- if you had an OSCAL component definition today - I can already consume it wth a variety of tools 
- Re-use cannot be understated here - upstream artifacts can be consumed for use downstream with greater specificity where required
-->

---

# Continuous Compliance

- We want the ability to visualize compliance and security in real-time
    - Automation becomes very apparent here
    - The accuracy of our control responses must be continually iterated
    - Verification needs to include both presence of the capability and proper configuration

<!--
- Expanding on that last slide with runtime validation
- Continuous Compliance means we can get real-time insights into automated validation checks 
- those can be fed into GRC tooling to visualize against a system security plan 
- I've seen - to my horror - control responses for something like the AC - Access Control family state "Service mesh provides mTLS between services" - but what about when it doesn't - Do you have policy and other checks in place to ensure that can't be circumvented?
-->

---

# Lula
- Free and Open Source Project
    - https://github.com/defenseunicorns/lula
    - No licensing
- Static manifest and Runtime validation of control satisfaction
- Allows the provided OSCAL to establish provenance for the validation activity    
- Collaboration with NIST to drive enhancements to OSCAL
    - Build and Maintain OSCAL developer libraries and tools 
        - See go-oscal

<!--
- First and foremost a free and open source project - no strings attached
- The goal with lula is to build a tool that places the trust for the activity it performs in the compliance data it ingests. 
- The provenance of control validation with Lula lies in the OSCAL it ingests
-->

--- 

# Demo
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;![w:400 h:400](./images/nist-logo-png-transparent.png)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ![w:400 h:400](./images/logo.png)
<!--

-->

--- 

# Summary
- Re-usable components saves time and results in more accurate compliance state
    - Artifacts are long-lived and continually evaluated for update
-  Transparency
    - Understanding the implications of software updates
    - Continuous Compliance = Insight into Real Time Risk

<!--
- Current initiatives include: 
    - looking at multiple engines for validation
    - Support for Infrastructure validation as well as generic API validation
    - Provenance in establishing i
-->