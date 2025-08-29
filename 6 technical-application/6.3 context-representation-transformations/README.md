# Context Representation Transformations

In today's interconnected digital ecosystem, the seamless exchange of information between diverse systems is more critical than ever. A fundamental obstacle to achieving true interoperability lies in how different systems represent context information about concepts. Some systems embed this context directly within the terminology, using codes with rich, nuanced meanings. Others represent context through their information models, structuring data to convey context via relationships and attributes. This disparity creates a landscape where data exchanged between systems may lose its intended meaning unless carefully transformed and interpreted.

This chapter focuses on the strategies and methodologies for implementing transformations between these heterogeneous models. We will delve into the technical challenges of mapping context from terminologies to information models and explore practical solutions to bridge these differences. By examining real-world scenarios and leveraging interoperability standards, we aim to equip you with the knowledge and tools necessary to ensure that context is preserved and accurately conveyed during data exchange. Understanding these transformation processes is essential for developers, architects, and stakeholders striving to enhance interoperability and achieve consistent, reliable communication across varied systems.

**Example of a transformation from a "Situation with explicit context" concept to a FHIR FamilyMemberHistory Resource information model**

{% tabs %}
{% tab title="Pre-transformation: SNOMED CT Concept / Expression" %}
<figure><img src="../../images/278301534.png" alt=""><figcaption></figcaption></figure>


{% endtab %}

{% tab title="Post-transformation: FHIR Resource" %}
<figure><img src="../../images/278301533.png" alt=""><figcaption><p>Figure 6.3-1: </p></figcaption></figure>


{% endtab %}
{% endtabs %}

* [6.3.1 FHIR and SWEC Comparison](../../6%20technical-application/6.3%20context-representation-transformations/6.3.1-FHIR-and-SWEC-Comparison_278301535.html)



* [6.3.2 Transformations between SWEC and FHIR](../../6%20technical-application/6.3%20context-representation-transformations/6.3.2-Transformations-between-SWEC-and-FHIR_278301536.html)






<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&entry.1767247133=NCPT+IG&entry.670899847=Context%20Representation%20Transformations" class="button primary">Provide Feedback</a>
