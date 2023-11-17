---
title: "Chainguard Glossary"
lead: "Software supply chain security vocabulary"
description: "Software supply chain security vocabulary"
type: "article"
date: 2022-08-01T15:21:01+02:00
lastmod: 2023-08-10T19:14:34+00:00
draft: false
tags: ["Conceptual"]
images: []
menu:
  docs:
    parent: "software-security"
weight: 10
toc: true
---

## General terms

### Software supply chain

Like in material good supply chains, a software supply chain is composed of activities that an organization undertakes to deliver an end product or service to a consumer. Software supply chain activities involve the transformation of dependencies, packages, components, binaries, build and packaging scripts, code and other software artifacts, and infrastructure into a finished software deliverable that is deployed into production. Participants in the supply chain include actors like developers, reviewers, testers, and maintainers who are working on the product at hand, but also includes those who maintain and contribute to packages and package managers, and other software that may be incorporated into a given product. Software supply chains also include information relevant to the software, such as versioning, signatures, and hashes.

---

### Software supply chain attacks

An intentional act of inserting malicious functionality into — or taking advantage of a known vulnerability within — the build, source, components or deployment software or infrastructure with the goal of propagating that harmful functionality through current distribution methods.

---

### Software development life cycle

The methodology and process for planning, designing, creating, testing, deploying, and maintaining software.

---

### Software artifact

An artifact is an immutable blob of data. Examples of artifacts include a file, a git commit, a container image, a firmware image.

---

### Software vulnerability

A software vulnerability is a weakness in a program which, if left unaddressed, may be used by attackers to access, manipulate, or compromise a computer system. A vulnerability can impact various parts of a system depending on where or how it is introduced, and can be targeted through different vectors based on the type of weakness it introduces. Developers refer to vulnerabilities by their corresponding CVE ID when patching or remediating any known security flaws.

---

### Attestation

An attestation allows consumers of a software artifact to verify the quality of that artifact independently from the producer of the software. It also requires software producers to provide verifiable proof of the quality of their software. You can think of an attestation as a **proclamation** that _software artifact X was produced by Y person at Z time._

---

### CI/CD

A pipeline approach to code development and release. CI stands for **c**ontinuous **i**ntegration, referring to the automation of testing code modifications frequently to avoid conflict between developer changes. CD stands for **c**ontinuous **d**elivery and/or **d**eployment, referring to the next stage of the pipeline where code is automatically merged to a repository or production environment after passing tests to fast-track the release of new changes to customers. CI/CD aims to reduce slowdowns experienced by manual code checking and approval, shortening the development cycle and allowing for more updates to reach consumers.

---

### CISA

The [**C**ybersecurity and **I**nfrastructure **S**ecurity **A**gency (CISA)](https://www.cisa.gov/) is a U.S. federal government agency under the Department of Homeland Security. Since its inception in 2018, CISA has championed the adoption of secure software development practices, such as the use of SBOMs and VEX documentation. CISA operates the Known Exploited Vulnerabilities (KEV) Catalog, a helpful tool to software developers who are working on vulnerability remediation. Additionally, they sponsor the National Vulnerability Database (NVD).

---

### CVE

Standing for **C**ommon **V**ulnerabilities and **E**xposures, CVEs are records assigned to publicly disclosed software vulnerabilities, stored in a searchable catalog. Each CVE consists of a unique CVE ID, a description of the vulnerability, and any relevant references or advisories. The CVE Program is operated by The MITRE Corporation and supported by a variety of U.S. government agencies.

---

### KEV Catalog

The [**K**nown **E**xploited **V**ulnerabilities (KEV) Catalog](https://www.cisa.gov/known-exploited-vulnerabilities-catalog) is populated with CVEs that have existing exploits “in the wild”. Operated by the Cybersecurity and Infrastructure Security Agency (CISA), the KEV Catalog serves as a tool for developers as it identifies CVEs that need to be prioritized for remediation because of their exploitability status.

---

### NVD

The [National Vulnerability Database (NVD)](https://nvd.nist.gov/) is operated by the [National Institute of Standards and Technology (NIST)](https://www.nist.gov/), an agency of the U.S. Department of Commerce. The NVD analyzes CVE records and their related public advisories to provide additional information on how a vulnerability impacts a software product. The NVD is often used by vulnerability scanners as a primary reference.

---

### Provenance

Provenance is the verifiable information about software artifacts describing _where_, _when_ and _how_ something was produced.

---

### Zero-day

The origin and exact meaning of this term varies among sources, but a zero-day is a recently discovered vulnerability. One explanation for the term is that a zero-day vulnerability is a very new vulnerability for which there isn't a fix, and developers have "zero days" to find a solution. Others define it as an unknown vulnerability or exploit already affecting your system. "Zero-day" refers to the age of the vulnerability, as derived from when you or your security org first becomes aware of it; because the vulnerability is "zero days" old, no one is yet aware of it and there isn't a known fix for it. The derivative terms **zero-day attack** or **zero-day exploit** refer to an attack taking advantage of such a previously unknown vulnerability.

---


## Security tools and frameworks

### Certificate authority

Often abbreviated as **CA**, a certificate or certification authority is a governing body that stores, signs, and issues digital certificates that can verify claims about the ownership of a given public key. Software consumers can use a CA to verify the assertions made about the private key that corresponds with the certified public key. A trusted third party, CAs use the X.509 or EMV standard to format certificates.

---

### Code signing

The process of digitally signing software artifacts to verify the author of the software as well as guarantee that the code has not been altered in any way since it was signed. Cryptographic hashes are used to sign software in order to validate authenticity and integrity. Code signing results in a signature.

---

### OCI

OCI stands for the **O**pen **C**ontainer **I**nitiative, which is an open governance structure that was set up to create and foster open industry standards around software container formats and runtimes.

---

### OIDC

OIDC is short for **O**pen**ID** **C**onnect, an identity layer that is built on top of the OAuth 2.0 protocol, and is governed by the OpenID Foundation. The tool allows for identity authentication and identity verification based on the authentication performed by a provider such as Apple, Google, GitLab, Microsoft, and others.

---

### PKI

Standing for **p**ublic **k**ey **i**nfrastructure, PKI arranges the necessary elements of infrastructure to manage public-key encryption, binding public keys with respective identities of entities (including individuals and organizations).

---

### Red teaming

Conducting a red team assessment consists of a goal-based adversarial activity to demonstrate how attackers can combine exploits to compromise the integrity of software or other technology.

---

### SBOM

An acronym, SBOM stands for a **s**oftware **b**ill **o**f **m**aterials (plural: SBOMs or software bill*s* of materials). An SBOM is like an electronic packaging slip or receipt, it is a formal record that contains the details and supply chain relationships (such as dependencies) of the components used in building given software.

---

### Sigstore

A suite of tools to sign, verify, and monitor software artifacts. Within the umbrella of Sigstore are Cosign for artifact signing and verification, the certificate authority Fulcio, and the transparency log Rekor. All of this tooling can be used independently of each other.

---

### SLSA

Standing for **S**upply chain **L**evels for **S**oftware **A**rtifacts, SLSA (pronounced “salsa”) is a security framework that offers a check-list of standards and controls in order to prevent tampering, improve integrity, and secure packages and infrastructure. SLSA has a build track with three levels of increasing security.

---

### SSDF

A project of the United States Department of Commerce's National Institute of Standards and Technology (NIST), the **S**ecure **S**oftware **D**evelopment **F**ramework (SSDF) is a set of guidelines and recommendations to establish a secure software development practice.

---

### Tekton

Tekton provides a cloud-native solution for building CI/CD systems with a focus on software supply chain security through offering artifact signatures and attestations through Tekton Chains.

---

### TUF

**T**he **U**pdate **F**ramework, known as TUF, offers a framework for securing software update systems.

---

## Attacks and vulnerabilities

### Codecov Hack

An example of a software supply chain attack that took place in early 2021. The code coverage tool Codecov experienced a sophisticated attack in which their Bash uploader script was modified by a malicious actor. The affected script allowed the attacker to extract customer credentials passing through Codecov’s continuous integration (CI) platform, exposing services accessible with these credentials to further exploitation.

---

### Log4Shell

An internet vulnerability involving a nearly ubiquitous piece of software, Log4j. The vulnerability received attention in December 2021 and much work was done to mitigate the vulnerability, which can be exploited by a remote code execution attack.

---

### SolarWinds Hack

The commonly used term to refer to the software supply chain breach that involved the SolarWinds Orion system, which occurred in 2020. Hackers gained access to networks, systems, and data of thousands of SolarWinds customers, and compromised the systems of over 30,000 organizations who relied on Orion software. This was one of the largest software supply chain attacks of its kind recorded to date.

---

### Typosquatting

Typosquatting is a cyber attack that is done by adversaries who try to pass a string (such as a URL) that they own as something that is official. For example, instead of the official chainguard.dev an adversary may register chain-guard.dev, cha1nguard.dev, or chainguar.dev in order to pretend to be the official site.
