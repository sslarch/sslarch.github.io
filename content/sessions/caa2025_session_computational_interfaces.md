---
title: "Computational interfaces: Exploring the Potential of Application Programming Interfaces (APIs) and Domain-Specific Languages (DSLs) in Archaeology"
sessionType: session
date: 2025-05-06
conference: CAA 2025, Athens
conferenceUrl: https://2025.caaconference.org/
sessionCode: S52
organisers:
- Martin Hinz
- Clemens Schmid
---

**When**: 2025-05-06,18:40-20:10 EEST  
**Where**: Room 3A, University of Western Attica, Athens, Greece

## Abstract
The CAA Special Interest Group “Scientific Scripting Languages in Archaeology” (SSLA) invites submissions for a session on the emerging potential of computational interfaces for archaeological research data and tools. This session aims to explore how Application Programming Interfaces (APIs), Command Line Interfaces (CLIs) or Domain-Specific Languages (DSLs)— collectively referred to as computational interfaces—can reduce the complexity of computational processes and can empower archaeologists to conduct more reproducible, transparent, and efficient research.

### Background and Rationale
As archaeology continues to embrace digital technologies, the need for reproducible research has become more pressing. Scripting languages are essential for this, providing archaeologists with the ability to automate workflows, reproduce analytical processes, and share methods transparently across the discipline. However, many archaeologists may refrain from adopting scripting languages due to the steep learning curve, lack of institutional and pedagogical support, and — perhaps most importantly — an inability to relate abstract computational processes to actual archaeological use-cases. APIs, CLIs, DSLs and other programming interfaces built for (and by) archaeologists offer a unique potential to address this difficulty by providing structured, machine-readable workflows and commands that match archaeological concepts and nomenclature, while simultaneously ensuring that even complex analytical tasks can be performed transparently and consistently. These interfaces therefore serve as bridges between archaeologists and the powerful world of scripting-based computational tools. However, while APIs have already begun to play a significant role in archaeology, enabling the integration of diverse digital resources, the development and application of Command line interfaces is lagging behind, and Domain-Specific Languages remain largely unexplored. **DSLs** are specialized programming languages tailored to the requirements of a particular field or task. They are often not computationally universal, i.e. able to implement any algorithm, but instead only model a narrow target domain. Many are embedded as libraries in a host language (eDSLs) to reuse syntax and compiler of the latter. While tools like **OxCal** have already incorporated DSL-like features for radiocarbon dating and chronological modeling (Bronk Ramsey, 2009), there is a significant opportunity to expand the use of DSLs across other areas of archaeological research: They could streamline processes such as spatial analysis, excavation data management, and artifact classification, allowing archaeologists to focus more on their research questions and less on the technical complexities of the tools they use. By creating languages that align closely with the terminology and workflows of archaeology, DSLs could simultaneously make sophisticated methods like Bayesian analysis, predictive modeling, and data science more accessible to archaeologists who may not have a background in computer science. **CLIs** are a more basic programmable interface. They allow access to the functionality of a software tool by calling it with a set of parameters on the command line. They thus share some of the potential described for DSLs and generally come at a lower cost both for developers and users, because they are easier to implement, run and learn. While they guarantee reusability and interoperability between tools, they also lack some of the advanced abilities of DSLs to empower users to express complex models and workflows. **APIs**, finally, have already demonstrated their value in archaeology by facilitating the integration of various tools and datasets. APIs provide standardized interfaces that allow different software systems to communicate with each other, for example over the internet, enabling archaeologists to combine data from multiple sources, such as GIS platforms and archaeological databases, in a seamless and efficient manner. The use of APIs has proven effective in enhancing data interoperability and enabling collaborative research across different institutions and disciplines. However, while APIs have made significant strides in improving data access and integration, they still require users to understand the underlying systems and data structures they interact with. This is where CLIs and DSLs could complement APIs, providing a higher level of abstraction that allows users to perform complex tasks without needing to engage with technical details. The development of computational interfaces in archaeology is a desideratum, offering the potential to revolutionize how archaeological data is processed, analyzed, and interpreted. By focusing on APIs, CLIs and DSLs, this session seeks to explore the possibilities for creating or adapting languages, both free-standing or embedded, to meet the unique needs of archaeological research.

We encourage submissions that explore various aspects of computational interfaces in archaeology, including their development, potential applications, and integration with existing tools. Suggested topics include:

**The Case for Programming Interfaces in Archaeology**: Discussions on the need for and potential benefits of developing APIs, CLIs and especially DSLs tailored to archaeological research, including how they could simplify complex analyses and make advanced tools more accessible to non-specialists.

**Development of Interfaces**: Insights into the design and development of interfaces for archaeology, focusing on how their inherent languages can be created to align with the specific needs and workflows of the field. Key technical challenges of DSLs include for example parsing (transforming code into expressions), evaluation (handling domain logic), tooling (supporting program development), and error messages, with interest in user and developer perspectives on these issues.

**Current Examples and Future Directions**: Exploration of existing tools that provide APIs or CLIs – or incorporate DSL-like features, such as OxCal. Including discussion of how these tools could be expanded or new systems developed to address other areas of archaeological research.

**The Interplay of Computational Interfaces**: Papers that examine how interfaces can complement each other by facilitating data integration and interoperability, enabling them to function more effectively within the broader ecosystem of archaeological software.

**Interdisciplinary Collaboration**: Examples of how collaborative efforts between archaeologists, computer scientists, and other specialists can enhance or can be enhanced by developing interfaces that meet the unique needs of archaeological research.

This session offers a platform for both experienced researchers and emerging scholars to share their insights and ideas. We encourage submissions that focus on the potential and challenges of developing DSLs for archaeology, as well as those that explore the role of APIs, CLIs or other computational interfaces. We welcome live-coding in the presentations.



## Presentations

1. Building a tree-walk interpreter - a didactic deep dive into the age of modelling language of the currycarbon software tool  
Clemens Schmid

2. Untapped Potential or Unusable Complexity? Challenges of Providing APIs for Archaeologists  
Lisa Steinmann and Simon Hohl

3. Open-Source Bayesian Chronological Modeling: The Role of Domain-Specific Language
Martin Hinz and Joe Roe

4. Etruscan Chamber Tombs Portal: a case study in the use of interconnected web software through dedicated APIs
Matteo Tomasini, Tristan Bridge, Aram Karimi, and Jonathan Westin

5. A command-line interface for chronological network modelling in R  
Gilles Geeraerts, Joe Roe, and Eythan Levy

### Reference

- Bronk Ramsey, C. (2009). “Bayesian Analysis of Radiocarbon Dates.” Radiocarbon, 51(1), 337-360.