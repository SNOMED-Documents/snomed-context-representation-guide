# 1. Introduction

# Background

An important challenge for achieving semantic interoperability across borders, even when using the same terminology, lies in the potential mismatch between the terminology and the applied information models. While using consistent terminology helps in communication, the way this terminology is bound to specific information models can lead to incompatible data representations.

In SNOMED CT, **context** refers to additional semantic details that modify the meaning of a clinical concept, typically by specifying aspects such as who the subject is, the temporal status of the event, or the certainty of a finding. These details are essential in distinguishing between different interpretations of the same base concept.

The problem arises from the divergence in approaches to representing context within different implementations of systems or databases. Some implementations rely on the terminology itself to represent contextual information, while others use the information model to encapsulate and represent context. Consequently, this leads to a disparity in how context is managed and represented, creating challenges in achieving semantic interoperability. These two overall approaches are summarized below, but even within these categories, variations may occur.

  1. **Terminology-based Context Representation:**

     * In some systems, the context is embedded within the terminology itself, e.g. when SNOMED CT concepts such as |family history of asthma| or |suspected neoplasm| are captured. This approach utilizes concepts and relationships within the terminology to convey contextual information. In these cases, the defining properties of the concepts represent the contextual factor, e.g. the temporal, subject relationship, or certainty of the disorder or procedure.
  2. **Information Model-based Context Representation:**

     * Conversely, other systems embed contextual details within their information models. Instead of being explicitly represented by the terminology, the context relies on how the information model structures and organizes data elements. This can involve attributes, relationships, or additional metadata fields specifically designated to convey context.

The problems stemming from this diversity in data representation include:

  1. **Interoperability Challenges:**

     * Misalignment between systems arises due to the differing approaches in representing context. Systems relying on the terminology for context may not easily communicate with those that embed context in their information models, leading to interoperability issues.
  2. **Data Consistency and Interpretation:**

     * Varied representation methods can lead to inconsistencies and discrepancies in interpreting and exchanging data. The interpretation of contextual information becomes subjective and prone to misinterpretation when systems have contrasting approaches to representing context.
  3. **Complex Transformation and Mapping:**

     * Transforming data between systems becomes complex and cumbersome due to the disparity in context representation methodologies. Mapping terminological context to information model-based context, and vice versa, requires meticulous translation and might result in loss of nuanced contextual information.
  4. **Standardization and Harmonization Challenges:**

     * Achieving standardization and harmonization across diverse systems becomes challenging when there's no agreed-upon method for representing context. This complicates efforts to establish unified guidelines or standards for semantic interoperability.

Addressing these issues involves developing frameworks or guidelines that reconcile these differing approaches. Creating a standardized approach to represent context, bridging the gap between terminology-driven and information model-based systems, is crucial to enhancing semantic interoperability and facilitating seamless data exchange across diverse healthcare information systems.

# Objective

The objective of this SNOMED CT Implementation Guide for Context Representation is to:

  * Help implementers understand how SNOMED CT represents context.
  * Offer practical guidance for designing data models, performing terminology bindings, and interpreting SNOMED-encoded information.
  * Facilitate the transformation between systems that use the ‘Situation with Explicit Context’ hierarchy and systems that represent context in information models, in either direction.  

# Scope

This guide focuses on:

  * Describing approaches for representing context in SNOMED CT, both through terminology and information models.
  * Offering guidance on transforming data between terminology-based and information model-based context representations.
  * Providing best practices for achieving semantic interoperability.

**Out of Scope:**

  * Detailed technical implementation for specific software systems.
  * Broader aspects of clinical terminology outside context representation.
  * General SNOMED CT use cases unrelated to context representation.

# Audience

This guide is intended for the following stakeholders:

  * **SNOMED International Members:** Seeking best practices for consistent context representation and interoperability.
  * **Clinicians:** Understanding how SNOMED CT supports clinical data collection involving contextual information.
  * **Information Managers:** Integrating SNOMED CT into health information models to improve data interoperability.
  * **Software Developers:** Implementing SNOMED CT within applications that handle contextual data.

# Guide overview

This **SNOMED CT Implementation Guide for Context Representation** provides guidance on managing and implementing context within healthcare systems using SNOMED CT. The guide addresses challenges related to differing context representation approaches and supports achieving semantic interoperability despite those differences. It is organized into the following chapters:

  * **Chapter 1: Introduction**

    * Introduces the background, objectives, scope, and target audience of the guide, emphasizing the importance of addressing context representation challenges to improve interoperability.

  * **Chapter 2: Terminology and Information Models in Healthcare**

    * Examines the role of healthcare terminologies and information models, highlighting how inconsistent data representation can impact semantic interoperability.

  * **Chapter 3: Use Case**

    * Presents real-world scenarios that illustrate the importance of effective context representation for accurate data exchange and clinical decision-making.

  * **Chapter 4: Health Records and Context**

    * Discusses how context is captured and managed within electronic health records (EHRs) and the impact of record structures on context representation.

  * **Chapter 5: SNOMED CT and Context**

    * Explains how SNOMED CT represents context using the “Situation with Explicit Context” hierarchy, ensuring consistent and precise representation of clinical findings and procedures.

  * **Chapter 6: Information Models and Terminology Binding**

    * Provides guidance on integrating SNOMED CT with healthcare information models, including best practices for terminology binding and a comparison of context representation approaches like FHIR and SNOMED CT’s SWEC.

  * **Chapter 7: Technical Application**

    * Covers technical strategies for implementing context representation, including approaches for context-aware data capture, storage, and transformations between different representation methods.

# Document Maintenance

This **SNOMED CT Implementation Guide for Context Representation** is maintained by **SNOMED International**. Updates to the guide will be made when significant changes to SNOMED CT content affect the principles outlined in the guide, or when user feedback identifies areas requiring attention.

# Contact and Feedback

For general inquiries or comments unrelated to specific page content, please contact:

**Email:** [info@snomed.org](mailto:info@snomed.org)

Your input is invaluable in helping us maintain a resource that supports effective implementation and promotes interoperability across healthcare systems.
