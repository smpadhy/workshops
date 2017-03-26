name: inverse
layout: true
class: center, middle, inverse
---
# Reproducible Research using ReproNIm
### smruti@mit.edu
---
Many thanks to the ReproNIm team

[source](https://github.com/smpadhy/repronim-ppt/tree/gh-pages) | CC-BY

(You can update this presentation - just send a pull-request)

Acknowledgement - NIH funding
---
layout: false
### Reproducible Research
- Reproducible Research
  - Definition/Discussion Replication/Reproducibility
  - Challenges in NeuroImaging Research Reproducibility
  - State of Art
  - Approaches so far
      VMs/Conatiners
      Workflows
      Provenace tracking
      ...
- ReproNIM
  - Project Goal
  - Project Information
  - Data discovery
  - Data Modeling and Integration -- with focus on Brainverse and NIDM model
  - Execution Environments - NICEMAN
- Example with some data - How reproducibility would be ensured with Brainverse and NICEMAN

.footnote[.red.bold[*] Important footnote]
---
### Reproducible Research

- **Re-executability (Publication-level Replication)**. The exact same data, operated on by the
exact same analysis should yield the exact same result.
    - Take any given publication and cast it in a reproducible fashion
    - Problem since current publications do not actually provide complete specification.
- **Generalizable Reproducibility** across publications. Huge problem since we dis-incentivize publication of replication studies as 'not novel’.
-
---
### Specturum of Reproducibility
- Original Exp: Data  +  Analysis  =  Result
- Re-executibility: Exact Same Data + Exact Same Analysis should yield the Exact Same Result
- (GR 1) Exact Same Data + Nominally ‘Similar’ Analyses should yield a ‘Similar’ Result (i.e. FreeSurfer subcortical volumes compared to FSL FIRST)
- (GR 2) Nominally ‘Similar’ Data + Exact Same Analysis should yield a ‘Similar’ Result (i.e. my kids with autism compared to your kids with autism)
- (GR) Nominally ‘Similar’ Data + Nominally ‘Similar’ Analyses should yield a ‘Similar’ Result

With lack of precise characterization of data, analysis and results, ‘Similar’ has lots of wiggle room for interpretation (both to enhance similarity and discount differences)!
---
### Issues that affect Reproducibility
- Low power
- Mistakes
- Ineffective Data Sharing
- Methodological Variance
- Sampling
- P – hacking (P-phishing)
- Publication Bias
- Only reporting potentially significant results, and not the rest

---
### ReproNIm - Overview
- Center for Reproducible Neuroimagimg Computation
- “(Discover, Replicate, Innovate)^Repeat"
- Develops End- to End system

---
### Resource Discovery
Key aspects of repeatable science - ability to **share** and **locate** data and software

**Requirement**

Assists end-user with specific analytic goal to find appropriate data and software which are subsequently submitted to the specified workflow and local/cloud-based execution envrionments.

--

**Current state**

- Existing Infastructures do not offer the automation necessary for rapid repeatable study
    - Community resource index and search envrionments (e.g. NIF)
    - Community data storage and computing resources (e.g., NITRC)

--
With ever increasing growth of data, software and analysis in neuroimaging, more sophisticated search and discovery algorithms and environment are required !

---

### Resource Discovery - Approach
- Create an comphrensive environment that integrates NIF data resources and services with NITRC tools registry and computational environment

- Implement search, discovery and publich interfaces through enhancement of neuroimaging semantic framework

- Develop a recommendation system for the appropriate selection of data and tools for subsequent analysis

- **NeuroBLAST**, a search engine that

    - allows users to find matching/similar studies based on a combination of task, analysis, and activation patterns

- Data discovered will be available for download through DataLad


???
Notes
- Neuroscience Information framework (NIF) and Neuroimaging Informatics Tools and Resources Clearinghouse (NITRC)

---
### Data Model, Provenance and Integration
**Requires**
- provide a consistent and
extensible data model for communicating information in brain imaging, associated software tools, and to
provide a set of commonly used reproducible workflows with integrated provenance tracking
- Data stored in organized fashion
- Accompanied by metadata
  - captures contextual information about how those data were
      - acquired
      - processed
      - analyzed
  - unique URIs for representation of entities, classes and relationships
- Semantic Web Technologies
    - Ontology
    - Provenance
--

[**Neuroimaging Data Model (NIDM)**](http://nidm.nidash.org)
<img src="assets/nidm-model.png" width="85%"/>

???
Notes:
To re-use shared data and reproduce results, the data must not only be stored in an organized fashion, but
accompanied by metadata that captures contextual information about how those data were acquired,
processed, and analyzed. In addition, the metadata must use unique URIs for entities, classes and
relationships.
---
### **BrainVerse**
- Electronic Laboratory Notebook - As Desktop App for neuroimaging research
- Allows neuroimaging research to be carried out collaboratively
- Will support reuse/share of data, software and results
- Uses NIDM model
    - Curation of data and results happens at the source
    - Data saved locally or to a remote store as NIDM file
- Being developed using Electron framework, primarily written in Javascript
- Architected as web application as well so later on can be deployed as web service
---
### **Execution Environments**
**Requires**:
Full automation and tracking of computing environments

- Reproducible analysis requires accessibility. Accessibility requires that software and tools be deployed in
computing environments available to end users without technical system and software installation knowledge.
This deployment needs to be well specified (e.g., exactly which tools are installed), automated (so it can be
reconstructed later on), and controlled (e.g., the environment is tested).

--

NeuroImaging Computational Environments MANager (**“NICEMAN”**)

--

It **supports**:
- easy and reproducible execution of
neuroimaging analysis workflows
- various computational platforms
- efficient reuse and integration of existing free and open-source software products
- provides data sharing initiatives

--

**Executes** the workflow by:
- automatically creating computation environments where necessary
- making sure software and datasets are available
- executing the workflow(s)
- providing results and detailed provenance information
about the environment back

--

*Simplifies creation and management of computing environments in Neuroimaging!*

???
Notes:
---
class: center
### ReproNIm - Overview
<img src="assets/repronim-arch.png" width="85%"/>
???
Notes
- Given a specific analysis task, this subproject will provide services for suggesting available data and software resources that are relevant, create a linked open data representation of these data, provide any available assessment metrics for these resources, and provide the available deployment/execution options available for these resources.
---
### Example

---
class: center, middle
## Thank you
---
class: center, middle
## Questions?
