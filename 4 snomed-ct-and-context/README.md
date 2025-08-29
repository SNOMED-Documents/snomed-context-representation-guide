# SNOMED CT and Context

This chapter delves into how context is represented within SNOMED CT, highlighting how context-free hierarchies interact with explicit contextual details present in the Situation with Explicit Context subset. Understanding these nuances holds significance for healthcare practitioners and informaticians, impacting the accuracy and utility of clinical terminologies.

## Content without Explicit Context

The top-level hierarchies of SNOMED CT, excluding the Situations with Explicit Contexts hierarchy, are typically meant to be interpreted within the framework of an information model. These hierarchies, including Clinical Finding, Procedure, Body Structure, and Substance, among others, do not inherently carry explicit contextual information within the concepts themselves. Instead, their interpretation relies heavily on the applied information model within a specific healthcare system or setting. The information model defines how these SNOMED CT concepts are structured, related, and utilized within a particular context. It offers a structured framework for their meaningful interpretation and application in clinical scenarios. This reliance on the information model ensures that these concepts are accurately understood and used within the context of healthcare delivery, aiding in precise data representation, clinical decision-making, and interoperability across different healthcare systems.

### Defining Properties and the Concept Model

The SNOMED CT concept model serves as the framework for SNOMED CT's quality, defining relationship types (attributes) that encapsulate the defining properties of concepts. For each top-level hierarchy or sub-hierarchies, it specifies the set of attributes applicable to concepts within that domain, and it outlines the range of concepts suitable as the value for each attribute. This set of rules supports uniformity and coherence across concept definitions.

The concept model is integral to ensuring SNOMED CT's quality standards. It fosters consistency in concept definitions, vital for the accurate functioning of the Description Logic reasoner. Adhering to this model enables the reasoner to accurately derive inferences, ensuring dependable and precise outcomes when searching, querying, or utilizing SNOMED CT data.

The attributes outlined in the SNOMED CT concept model represent inherent properties that must be true for every instance of that concept. These attributes do not change the fundamental nature or primary type of the concept within its hierarchy. Rather, they establish consistent and unchanging characteristics unique to each instance in the hierarchy, maintaining the core identity of the concept. For this reason, concepts such as 'family history of asthma' or 'diarrhea not present' are not included in the Clinical finging top-level hierarchy. These concepts don't depict actual disorders; instead, they describe particular contextualized situations associated with conditions like asthma and diarrhea. Similarly, within the Procedure hierarchy, concepts such as 'no history of mammogram' or 'Hypersensitivity skin test not done' wouldn't be present. These concepts don't signify specific clinical procedures; rather, they indicate situations or contexts surrounding procedures like mammograms or hypersensitivity skin tests.

Maintaining the integrity and scope of each hierarchy within SNOMED CT is crucial. Altering the meanings of concepts or introducing concepts with explicit context can compromise the terminology's usability for precise data retrieval, analysis, and decision support. When concepts deviate from their intended definitions within their hierarchies, it hampers the accuracy and reliability of information retrieval and analysis processes. This situation becomes particularly critical in healthcare settings, where inaccuracies or ambiguous interpretations due to altered concepts can lead to safety-critical outcomes. Therefore, upholding the intended scope and definitions within hierarchies in SNOMED CT is vital for ensuring the reliability and safety of clinical data interpretation, decision-making, and patient care.

For more information about the SNOMED CT concept model, please refer to the _**Editorial Guide**_ and the [Machine Readable Concept Model](https://app.gitbook.com/o/h8Z6qGxuQrzM9vbx5bPT/s/wLJPOzgAQsSAYr6nhvCl/).

## Content with Explicit Context

SNOMED CT was purposefully designed with a specific hierarchy, known as the Situation with Explicit Context (SWEC), to maintain a clear separation of contextualized findings and procedures. This hierarchy intends to define clinical situations as precoordinated concepts, i.e. clinical findings or procedures associated with contextual factors. The concept model guiding SWEC precisely defines acceptable contextual factors for each concept, enabling the documentation of contextualized clinical information while maintaining a standardized structure crucial for accurate data utilization and interoperability. Importantly, unlike other clinical hierarchies in SNOMED CT that are generally context-free, SWEC concepts are distinguished by their inclusion of context-specific details within the concepts themselves. This self-contained representation of SWEC concepts reduces reliance on external models for context interpretation.

### Situations with Explicit Context

The Situation with Explicit Context (SwEC) hierarchy is designed to capture and represent clinical findings and procedures within specific contexts, ensuring that their meaning is fully understood in the appropriate circumstances.

#### Concept Model

The concept model for SwECs includes two core attributes that apply universally to any concept within the hierarchy. Additionally, two specific attributes apply to Procedures with Explicit Context, and another two attributes are specific to Clinical Findings with Explicit Context. The table below outlines the purpose and semantic interpretation of each of these attributes.

<table><thead><tr><th>Attribute</th><th>Domain</th><th>Description</th></tr></thead><tbody><tr><td><a href="http://snomed.info/id/408732007">408732007 |Subject relationship context (attribute)|</a></td><td><p></p><pre data-overflow="wrap"><code>&#x3C;&#x3C;  243796009 |Situation with explicit context (situation)|
</code></pre></td><td><p>Specifies the relationship of the subject to the patient.</p><p>For example, <a href="http://snomed.info/id/161077003">161077003 |Father smokes (situation)|</a> is defined with the subject relationship context “Father of subject.”</p></td></tr><tr><td><a href="http://snomed.info/id/408731000">408731000 |Temporal context (attribute)|</a></td><td><pre data-overflow="wrap"><code>&#x3C;&#x3C;  243796009 |Situation with explicit context (situation)|
</code></pre></td><td><p>Indicates the timing of the procedure or finding, whether it occurred in the past, present, or is planned for the future.</p><p>For example, <a href="http://snomed.info/id/161550001">161550001 |History of hematuria (situation)|</a> is defined with the temporal context “In the past.”</p></td></tr><tr><td><a href="http://snomed.info/id/246090004">246090004 |Associated finding (attribute)|</a></td><td><pre data-overflow="wrap"><code>&#x3C;&#x3C; 413350009 | Finding with explicit context (situation)|
</code></pre></td><td><p>Links the situation to a related clinical finding or event.<br>It specifies the clinical concept whose context is being modified.</p><p>For example, <a href="http://snomed.info/id/86699002">86699002 |Apyrexial (situation)|</a> is defined with the associated finding “Fever”</p></td></tr><tr><td><a href="http://snomed.info/id/408729009">408729009 |Finding context (attribute)|</a></td><td><pre data-overflow="wrap"><code>&#x3C;&#x3C; 413350009 | Finding with explicit context (situation)|
</code></pre></td><td><p>Describes whether the finding is known, absent, or uncertain, as well as anticipated future findings.</p><p>For example, <a href="http://snomed.info/id/86699002">86699002 |Apyrexial (situation)|</a> is defined with the finding context “Known absent.”</p></td></tr><tr><td><a href="http://snomed.info/id/363589002">363589002 |Associated procedure (attribute)|</a></td><td><pre data-overflow="wrap"><code>&#x3C;&#x3C; 129125009 | Procedure with explicit context (situation)|
</code></pre></td><td><p>Links the situation to a procedure.</p><p>For example, <a href="http://snomed.info/id/183976008">183976008 |Operative procedure planned (situation)|</a> is defined with the associated procedure “Surgical procedure.”</p></td></tr><tr><td><a href="http://snomed.info/id/408730004">408730004 |Procedure context (attribute)|</a></td><td><pre data-overflow="wrap"><code>&#x3C;&#x3C; 129125009 | Procedure with explicit context (situation)|
</code></pre></td><td><p>Indicates the status or completion of a procedure, such as planned, ongoing, or completed.</p><p>For example, <a href="http://snomed.info/id/183976008">183976008 |Operative procedure planned (situation)|</a>  is defined with the procedure context “Planned.</p></td></tr></tbody></table>

The following pages will present examples of the different types of situations with explicit context, illustrating how each attribute is applied.






<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&entry.1767247133=NCPT+IG&entry.670899847=SNOMED%20CT%20and%20Context" class="button primary">Provide Feedback</a>
