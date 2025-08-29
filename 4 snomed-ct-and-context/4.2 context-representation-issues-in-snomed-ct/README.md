# Procedure with Explicit Context

### Definition and Purpose <a href="#id-4.2procedurewithexplicitcontext-definitionandpurpose" id="id-4.2procedurewithexplicitcontext-definitionandpurpose"></a>

Procedures with explicit context describe situations where a medical procedure’s status, timing, or relationship to the patient is specified. These concepts clarify whether a procedure is planned, completed, or not done, among other statuses.

### Attributes Used <a href="#id-4.2procedurewithexplicitcontext-attributesused" id="id-4.2procedurewithexplicitcontext-attributesused"></a>

* **Associated Procedure**: Links the situation to the specific procedure being considered.
  * For example, |Lung transplant planned (situation)| uses this attribute to connect to |Lung transplant (procedure)|.
* **Procedure Context**: Describes the status of the procedure, such as whether it is planned, completed, or not done.
  * For example, |Lung transplant planned (situation)|, the procedure context is |Planned|.
* **Temporal Context**: Indicates when the procedure is or was to take place (past, present, future).
  * For example, |Lung transplant planned (situation)| uses |In the future| as the temporal context.
* **Subject Relationship Context**: Specifies who the procedure pertains to, usually the patient but can be a different person.
  * For example, |Mother’s surgery planned (situation)| would indicate the procedure pertains to the patient’s mother.

The default values for the context attributes for procedures assume that the procedure has occurred, is current or at a specified time, and pertains to the subject of the record.

### Associated Procedure <a href="#id-4.2procedurewithexplicitcontext-associatedprocedure" id="id-4.2procedurewithexplicitcontext-associatedprocedure"></a>

#### Awaiting transplantation of kidney  <a href="#id-4.2procedurewithexplicitcontext-awaitingtransplantationofkidney" id="id-4.2procedurewithexplicitcontext-awaitingtransplantationofkidney"></a>

The SNOMED CT concept [698306007 |Awaiting transplantation of kidney (situation)|](http://snomed.info/id/698306007) describes a patient’s status as they await a kidney transplant. A key attribute here is [363589002 |Associated procedure (attribute)|](http://snomed.info/id/363589002) Associated procedure, which is [70536003 |Transplant of kidney (procedure)|](http://snomed.info/id/70536003) . This indicates that the focus of the situation is the upcoming kidney transplantation procedure. Additionally, the concept includes the [|Procedure context (attribute)|](http://snomed.info/id/408730004) as [|To be done (qualifier value)|](http://snomed.info/id/385643006) To be done, specifying that the transplant is planned but not yet performed, and it applies to the patient at the [|Current or specified time (qualifier value)|](http://snomed.info/id/410512000) .

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

### Examples - Procedure Context <a href="#id-4.2procedurewithexplicitcontext-examples-procedurecontext" id="id-4.2procedurewithexplicitcontext-examples-procedurecontext"></a>

#### Lung transplant planned (situation) <a href="#id-4.2procedurewithexplicitcontext-lungtransplantplanned-situation" id="id-4.2procedurewithexplicitcontext-lungtransplantplanned-situation"></a>

The SNOMED CT concept [704202004 |Lung transplant planned (situation)|](http://snomed.info/id/704202004) represents a planned lung transplant for a patient. A key attribute here is [|Procedure context (attribute)|](http://snomed.info/id/408730004)\
[397943006 |Planned (qualifier value)|](http://snomed.info/id/397943006) . This attribute indicates that the lung transplant is scheduled for the future and has not yet been performed. Additionally, the concept includes [|Associated procedure (attribute)|](http://snomed.info/id/363589002)   as [|Transplant of lung (procedure)|](http://snomed.info/id/88039007)

, specifying the type of procedure planned. The [|Subject relationship context (attribute)|](http://snomed.info/id/408732007)

is [|Subject of record (person)|](http://snomed.info/id/410604004) , indicating that the procedure pertains to the patient themselves. The [|Temporal context (attribute)|](http://snomed.info/id/408731000)  is [|Current or specified time (qualifier value)|](http://snomed.info/id/410512000) , showing that the procedure is relevant at the present time or based on a specific schedule.

<figure><img src="../../.gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>

### Examples - Subject Relationship Context <a href="#id-4.2procedurewithexplicitcontext-examples-subjectrelationshipcontext" id="id-4.2procedurewithexplicitcontext-examples-subjectrelationshipcontext"></a>

#### Family history of mastectomy (situation) <a href="#id-4.2procedurewithexplicitcontext-familyhistoryofmastectomy-situation" id="id-4.2procedurewithexplicitcontext-familyhistoryofmastectomy-situation"></a>

The SNOMED CT concept [433977002 |Family history of mastectomy (situation)|](http://snomed.info/id/433977002)  represents the occurrence of mastectomy within a patient’s family history. A key attribute here is Subject relationship context, which is [303071001 |Person in the family (person)|](http://snomed.info/id/303071001) . This attribute specifies that the mastectomy is related to a family member rather than the patient themselves. The concept also includes the associated procedure as [|Excision of breast (procedure)|](http://snomed.info/id/1231734007) , indicating that the mastectomy was the specific procedure performed, and the procedure context as Done, reflecting that the procedure has been completed. The temporal context is [|Current or past (actual) (qualifier value)|](http://snomed.info/id/410511007) , signifying that the procedure occurred in the past or is relevant at present.

<figure><img src="../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

### Examples - Temporal Context <a href="#id-4.2procedurewithexplicitcontext-examples-temporalcontext" id="id-4.2procedurewithexplicitcontext-examples-temporalcontext"></a>

The SNOMED CT concept [134651000119108 |History of estrogen therapy (situation)|](http://snomed.info/id/134651000119108)  details a patient’s past use of estrogen hormone therapy. A key attribute here is [|Temporal context (attribute)|](http://snomed.info/id/408731000) , which is [410513005 |In the past (qualifier value)|](http://snomed.info/id/410513005) . This attribute specifies that the estrogen therapy occurred in the past. Additionally, the concept includes [|Associated procedure (attribute)|](http://snomed.info/id/363589002) as [|Estrogen hormone therapy (procedure)|](http://snomed.info/id/243125009) , indicating the specific therapy administered, and [|Procedure context (attribute)|](http://snomed.info/id/408730004) as [|Done (qualifier value)|](http://snomed.info/id/385658003) , showing that the therapy was completed. The subject relationship context is [|Subject relationship context (attribute)|](http://snomed.info/id/408732007)  as [|Subject of record (person)|](http://snomed.info/id/410604004) , signifying that the therapy pertains to the patient themselves.

<figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>






<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&entry.1767247133=NCPT+IG&entry.670899847=Procedure%20with%20Explicit%20Context" class="button primary">Provide Feedback</a>
