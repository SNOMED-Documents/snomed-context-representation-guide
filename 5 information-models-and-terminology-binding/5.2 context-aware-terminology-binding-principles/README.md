# 5.2 Context aware terminology binding principles

# Information model-driven vs Terminology-driven Context Representation

## Overarching Principle

  * Ensure that the consolidated meaning represented by the chosen SNOMED CT concept and the applied information model represent the intended semantics, and unambiguously declare the context. I.e. the verification, temporal, and subject relationship context.

Below find a set of terminology binding principles, to help guide the binding of specific types of data elements.

# Terminology Binding Principles and Examples

Adhering to these principles provides a robust framework for designing terminology bindings compatible with the SNOMED Concept Model and the structural expressivity of FHIR resources. By ensuring compatibility, we can create a cohesive system where clinical content is accurately and consistently represented across different platforms and applications. This alignment is crucial for maintaining the integrity of clinical data, allowing for seamless integration and reducing the risk of misinterpretation or data loss during exchanges.

Furthermore, this approach facilitates efficient transformations and adaptations in the context of analytics and interoperability. Standardized terminology bindings enable healthcare systems to effectively share and analyze data, supporting advanced analytics, research, and population health management.

  

Use case| Model meaning binding| Value set binding| Examples| Advice  
---|---|---|---|---  
Measurable Entities|  < [ 363787002 |Observable entity (observable entity)|](http://snomed.info/id/363787002 "363787002 | Observable entity \(observable entity\) |") | concrete values (numbers) < [ 404684003 |Clinical finding (finding)|](http://snomed.info/id/404684003 "404684003 | Clinical finding \(finding\) |") | 

  * **Question:** Systolic Blood Pressure?
  * **Meaning binding:** 75367002 |Systolic blood pressure (observable entity)|
  * Answer: 120 mmHg (using a concrete value)

|   
  
  
  * **Question:** Eye color?
  * **Meaning binding:** 247030006 |Color of iris (observable entity)|
  * **Answer:** < 366031009 |Finding of color of iris (finding)|

|   
  
Absence or Presence/Verification Status of Specific Signs, Symptoms, Diseases, etc.|  < [ 404684003 |Clinical finding (finding)|](http://snomed.info/id/404684003 "404684003 | Clinical finding \(finding\) |") |  < [ 410514004 |Finding context value (qualifier value)|](http://snomed.info/id/410514004 "410514004 | Finding context value \(qualifier value\) |") | 

  * Question: Menopause?
  * **Meaning binding:** 276477006 |Menopause finding (finding)|
  * **Answer:**
    * yes: 410515003 |Known present (qualifier value)|
    * no: 410516002 |Known absent (qualifier value)|

|   
  
< [ 243796009 |Situation with explicit context (situation)|](http://snomed.info/id/243796009 "243796009 | Situation with explicit context \(situation\) |") | 

  * Question: History of myocardial infarction?
  * **Meaning binding:** 399211009 |History of myocardial infarction (situation)|
  * **Answer** :
    * yes: 410515003 |Known present (qualifier value)|
    * no: 410516002 |Known absent (qualifier value)|

| In this case, the value will match or replace the value of the context attribute in the situation concept.  
Booleans (Yes/No Answers)|  < [ 404684003 |Clinical finding (finding)|](http://snomed.info/id/404684003 "404684003 | Clinical finding \(finding\) |") |  < [ 410514004 |Finding context value (qualifier value)|](http://snomed.info/id/410514004 "410514004 | Finding context value \(qualifier value\) |") | 

  * **Question: Allergy to Penicillin?**
  * **Meaning binding:** 91936005 |Allergy to penicillin (finding)|
  * **Answer** :  

    * yes: 410515003 |Known present (qualifier value)|
    * no: 410516002 |Known absent (qualifier value)|

| Note: While coding both "yes" and "no" values is acceptable, it's essential to consider whether it's necessary to explicitly represent the absence of a condition. It may be valid to only code the "yes" values if the absence of the condition is implicit within the context of use.If there's no preexisting expression for the "no" value, consider using qualifier values.Ensure consistency and clarity in your bindings by establishing clear rules for handling Boolean variables.  
  
  * **Question: Pregnant?**
  * **Meaning binding:** 77386006 |Pregnancy (finding)|
  * **Answer** :
    * yes: 410515003 |Known present (qualifier value)|
    * no: 410516002 |Known absent (qualifier value)|

  
  
  * **Question: Diabetes Mellitus?**
  * **Meaning binding:** 73211009 |Diabetes mellitus (disorder)|
  * **Answer** :
    * yes: 410515003 |Known present (qualifier value)|
    * no: 410516002 |Known absent (qualifier value)|

  
  
  

## Deriving SNOMED CT Expressions from the decomposed approach

When applying qualifier values to represent the absence of a condition like diabetes mellitus using SNOMED CT an expression can be derived to convey the meaning with explicit context.

_Example:_

  1. **Identify the Concept for Diabetes Mellitus:**   
Firstly, we need to identify the SNOMED CT concept representing diabetes mellitus. 

     * 73211009 |Diabetes mellitus (disorder)|
  2. **Representing the Absence/Presence of Diabetes Mellitus:**   
To represent the absence/ of diabetes mellitus, we need to create an expression that explicitly states the absence of the disorder.
     * Utilize a qualifier value to indicate the absence/presence of the disorder. 
       * 410516002 |Known absent (qualifier value)|
       * 410515003 |Known present (qualifier value)|
  3. **Creating the Expression:** By combining the concept for diabetes mellitus with the qualifier value for absence, we can create an expression that explicitly represents the absence of diabetes mellitus:

     * Using the concept model for Situation with Explicit context (clinical findings with explicit context)
     * 73211009 |Diabetes mellitus| : 408729009 |Finding context| = 410516002 |Known absent|

This expression clearly indicates that the disorder of diabetes mellitus is absent in this patient at the current point in time or the time specified in the model. It provides a single expression that encapsulates the meaning of the absence of diabetes mellitus with explicit context.

In summary, expressions representing the absence of any specific disorders or conditions in SNOMED CT can be formulated as a SNOMED expression by combining the concept representing the disorder with a qualifier value indicating absence, linked together using the appropriate context model attribute (in this case, 408729009 |Finding context| ). This approach allows for the creation of concise and unambiguously meaningful expressions that convey the absence of any particular condition, all entirely within the SNOMED CT terminology framework.

These expressions must adhere to the SNOMED CT concept model and other constraints to ensure that they extend SNOMED CT in a cohesive and meaningful way, see the [SNOMED CT Postcoordination Guide](https://confluence.ihtsdotools.org/display/DOCEXPPG/Practical+Guide+to+Postcoordination).

  

