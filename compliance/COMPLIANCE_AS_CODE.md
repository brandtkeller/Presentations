---
title: Compliance as Code presentatioin
description: An example slide deck created using Marpit
paginate: true
marp: true
theme: gaia
class: invert
footer: 'https://github.com/brandtkeller/Presentations'
---

# Compliance as Code

---

# Introduction

- Brandt Keller - Software Engineer - Defense Unicorns
- GitHub: https://github.com/brandtkeller
- LinkedIn: https://www.linkedin.com/in/brandtkeller/
- Prior Employment:
    - Boeing DevSecOps - Nostromo Software Factory
<!--
- Name
- Employment history
- Current work in this space
-->

---

# Why?

Why introduce "as code" into the element of compliance?

- Standard format options
    - Stronger automation posture
- Stronger posture towards version control
- Maintenance optimization & Cognitive Burden decrease
    - It can be monitored for staleness and further integrates Security with Development

<!--
- We have many disparate ways to catalog and document compliance
- Very little is done in a standard format
- very little is actively maintained as software or systems change
- passive vs active compliance
- Ability to split systems into components that can be maintained separately
-->

---

# Format
Open Security Controls Assessment Language - OSCAL
- NIST maintained 
- Gaining adoption from Governance, Risk Management, Compliance Tooling and platforms
- Postures data for automation (Emphasizing 'Machine-Readable')
- Open Source tooling is becoming more [widely available](https://github.com/oscal-club/awesome-oscal)

<!--
- Open Security Controls Assessment Language (OSCAL)
- You can standardize on another format if you so choose - but we are seeing any industry adoption for OSCAL for compliance related acitivities in GRC tooling
- what we hear as pushback for using OSCAL is something like "but isn't oscal just as static as my spreadsheet?
- The answer is yes and no - OSCAL doesn't execute any automation itself - but the act of starting this is casting a vote towards your ability to utilize or build automation.
-->

---

# How does someone get started?

Review your compliance landscape
- What are you responsible for?
    - Application
    - Platform
    - System etc
- Break the system into components
- Build out component compliance information regarding controls

<!--
- Review the Models and the intent
- Applications rolling up into platforms
- Platform development
-->
---

# How does someone get started? - cont

- Understand how components can reduce administrative and cognitive burden by de-coupling from a full-system view.
- Writing control response information in detail to guide proper manual validation and/or future automation.
- Understand where aggregation may benefit you - System vs Component

---

# Automation

We have and will continue to build more options towards automation that can process OSCAL.
- Establishing OSCAL artifacts allows for current/future utilization
- Defining what problem you want to solve
    - Selection of a supported language that can process OSCAL
    - Automation of OSCAL management vs OSCAL control validation


<!--
- Re-iterate the importance of the "machine readable format"
- Why automate? easy - it gets us into reproducible validation towards controls
- OSCAL management being the processes that keep these artifacts up-to-date aswell as the transition between models and/or GRC tooling
- Control validation being some automated check to report the control implementation is satisfied. 
-->

---

# Examples

[Awesome OSCAL](https://github.com/oscal-club/awesome-oscal) Primary locations for monitoring for new updates.

Where I have personally contributed
- [Lula](https://github.com/defenseunicorns/lula)
- [go-oscal](https://github.com/defenseunicorns/go-oscal)
- [Platform One Big Bang OSCAL Artifacts](https://repo1.dso.mil/big-bang/product/packages/istio-controlplane/-/blob/main/oscal-component.yaml)
- [Big Bang OSCAL Generator](https://github.com/defenseunicorns/bigbang-oscal-component-generator)
- [Component Aggregator](https://github.com/brandtkeller/component-generator)

---

# Lula Demo

<!--
- Open Source
- Component Focus
- Ability to aggregate
- audit vs enforcement
- domain awareness
- Continuous runtime & CICD
-->

---

# Questions?