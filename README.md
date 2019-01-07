
<![endif]-->

<![if !vml]>![06_sap_corporate_RGB](file:///C:/Users/I077430/AppData/Local/Temp/msohtmlclip1/01/clip_image002.gif)<![endif]>

Project Architect:

n.n.

Authors:

n.n.

**Software Design Description**

<Component / Sub-Component / Function>

cProject Title

Version

Status

Date

Reviewed/Approved at / by

Template Version: SDD 4..0b

**INTERNAL / CONFIDENTIAL**

Storage location for temporary versions of this architecture concept document:  
<![if !supportLineBreakNewLine]>  
<![endif]>

Final version:

**Read before using this template!**

**How to use this template**

**The purpose of a design doc is**

<![if !supportLists]>(a) <![endif]>develop design concepts for the target component,

<![if !supportLists]>(b) <![endif]>enable review of the key concepts,

<![if !supportLists]>(c) <![endif]>support alignment between stakeholders,

<![if !supportLists]>(d) <![endif]>record trade-offs and reasons for major design decisions as needed.

<![if !supportLists]>(e) <![endif]>In addition we use this document as a ‘Guide to the code’ when the implementation is done.

**Consider these guidelines when using this template:**

-   Document only what is needed by reviewers and required for development of high quality software
-   Less is better! Write short / concise and so that it is easy to understand. Focus on key design challenges, not completeness (large documents are a waste and no one will read them!)
-   Write for ease of understanding but don’t waste time on unnecessary polishing.
-   ‘Pair Design’ recommended (= develop key concepts together with a colleague)
-   Document design details & 'guide to the code' after the implementation. Only write what is not contained in the code/system already
-   A template is a template and not a form. Only fill what is needed and relevant.
-   This template is a base template. We expect large development units to derive their own versions that are specific to their environment / technology.

**Some guidelines on reviews**

-   An Expert Review is mandatory only for chapter 2
-   Differentiate between **expert review** (with _few_ experts, deep review, issues & changes likely) and **light review / information rollout** (many people, no/few issues expected).
-   Expert Review Participants: only experts & _directly affected people_ (provider and consumers)

-   Design for team topic: review with dev team + stakeholders
-   (Public) Interfaces / Cross-alignment: Providers and consumers
-   Do a real meeting (not just mail / doc) to discuss the key design topics
-   Try for no more than 7 people!

-   Light Review Participants: There can be many participants. Can be mail / doc based, meetings to discuss remaining issues are optional

**Hidden Text contains important useful hints on how to fill in the template. Activate / deactivate these texts by pressing the following button in MS Word toolbar:** <![if !vml]>![](file:///C:/Users/I077430/AppData/Local/Temp/msohtmlclip1/01/clip_image004.jpg)<![endif]>

Additional guidelines:

<![if !supportLists]>§<![endif]>All graphical descriptions of architecture aspects must follow SAP standards for modeling:

<![if !supportLists]>o<![endif]>**Technical Architecture Modeling (**[**TAM**](http://ency.wdf.sap.corp:1080/wiki/Technical_Architecture_Modeling)**)**

<![if !supportLists]>o<![endif]>**SOA modeling using ARIS**.

<![if !supportLists]>§<![endif]>Do not delete non-applicable/optional items or sections of this template, but mark them with "Not relevant" and give a short reasoning why this is the case. This makes reading easier for readers which were not involved in the design discussions.

<![if !supportLists]>§<![endif]>The design document has to be available in **English** language.

<![if !supportLists]>§<![endif]>Always store your documents in document management systems such as **cProjects/cFolders** and avoid entering links to documents on shares or servers.

<![if !supportLists]>§<![endif]>Describe the **changes and revisions** of this document in the table on the title page.

<![if !supportLists]>o<![endif]>Document versions follow the scheme x.y.z.

<![if !supportLists]>o<![endif]>When you change a document, create a new version and keep the old document version. Make sure that “Track Changes” is turned on in the new version and accept all existing changes that were tracked in the old document version. Then insert a new line in the version table on the title page.

<![if !supportLists]>o<![endif]>There are three types of changes, which affect the version number as follows

<![if !supportLists]>§<![endif]>Status Changes:

<![if !supportLists]>·<![endif]>Draft versions prior to review meeting => starting with 1.0

<![if !supportLists]>·<![endif]>Version after action items of review meeting have been completed => starting with 2.0

<![if !supportLists]>·<![endif]>Version after implementation (starting with 3.0)

<![if !supportLists]>§<![endif]>Major Changes: Increment y-part of document version for complete revisions (e.g. 1.3 to 1.4)

<![if !supportLists]>§<![endif]>Minor Changes: Increment z-part of document version for minor corrections (e.g. 1.3 to 1.3.1)

<![if !supportLists]>§<![endif]>Changes after sign off of the document have to be aligned with the verifier(s) of the documents. If required a new review for the document has to be set up.

<![if !supportLists]>o<![endif]>Consider update of existing central documents, which could be affected by this design (blue book, Architecture documentation, …).

<![if !supportLists]>§<![endif]>To update the table of content of this document, mark it and press <F9>

<![if !supportLists]>§<![endif]>Template Owner: Juergen Heymann; last changed: March 2010

<![if !supportLists]>§<![endif]>Contact the template owner if you have any ideas to improve this template.

  

**Contents**

[1  General Information_ 4](#_Toc265049772)

[1.1  Stakeholders and Roles  4](#_Toc265049773)

[1.2  References  4](#_Toc265049774)

[1.3  IP Compliance and Patents  4](#_Toc265049775)

[2  Design_ 5](#_Toc265049776)

[2.1  Key Requirements and Design Goals  5](#_Toc265049777)

[2.2  Context  5](#_Toc265049778)

[2.3  Major Building Blocks  5](#_Toc265049779)

[2.4  Interfaces / Communication Handling_ 5](#_Toc265049780)

[2.5  Design Challenges resulting from Non-Functional Requirements  5](#_Toc265049781)

[2.6  User Interface  5](#_Toc265049782)

[2.7  Used Components and Frameworks  5](#_Toc265049783)

[2.8  Package/Development Component Concept  5](#_Toc265049784)

[2.9  Business Functions and Switches for EHPs  5](#_Toc265049785)

[2.10  Upgrade / Migration / Compatibility  6](#_Toc265049786)

[2.11  TCO Considerations  6](#_Toc265049787)

[2.12  Analytics / BI Content  6](#_Toc265049788)

[2.13  Compliance to Standards and Guidelines  7](#_Toc265049789)

[3  Design Details Documentation_ 8](#_Toc265049790)

[3.1  Database Design_ 8](#_Toc265049791)

[3.2  Testability and Test Environment  8](#_Toc265049792)

[3.3  Complex Algorithms and Applied Patterns  8](#_Toc265049793)

[3.4  Design Alternatives and Trade-Offs  8](#_Toc265049794)

[3.5  Guide to the Implementation_ 8](#_Toc265049795)

[4  Appendix_ 8](#_Toc265049796)

[4.1  Glossary  8](#_Toc265049797)

[4.2  Customizing_ 8](#_Toc265049798)

[4.3  Supportability Considerations  8](#_Toc265049799)

[4.4  Error Analysis  8](#_Toc265049800)

[4.5  Other  8](#_Toc265049801)

  

# <![if !supportLists]>1 <![endif]>General Information

## <![if !supportLists]>1.1 <![endif]>Stakeholders and Roles

List all people who were involved in the creation of this document and who should be involved in the final review and sign-off of this document.

**Role**

**Name**

Author(s)

Architect

Product Owner

Information Developer

Quality Responsible (QE/QPE)

IMS Representative

Test Developers

< other relevant roles>

## <![if !supportLists]>1.2 <![endif]>References

In this table give a list of all documents that are input / assigned to the design scope.

Typical references: ACDs and SRSs (mandatory), UI spec, Architecture guidelines, SOA content, work packages, naming conventions, …

**Document Title**

Title and version

**Date**

Enter document date

**Link**

document (preferably in cPro)

**Comments**

Enter the author/publishing organization responsible/reason for reference

## <![if !supportLists]>1.3 <![endif]>IP Compliance and Patents

You must always store architecture and design documents 'IP safe' (currently cPro) so that (if needed) SAP can prove that a certain idea / concept was invented / designed at a certain point in time.

In addition, consider patents: Does your design extend the current state-of-the-art in any way? If you think so, or even if you think it might, please go to the ['Patents@SAP'](https://wiki.wdf.sap.corp/display/patents/Home) Wiki and follow the process described there. Not only is it required of all employees to notify SAP if they make an invention, but participation in the SAP patent program is rewarded in several ways (including money) – so by taking part in the SAP patent program, you can help SAP protect its innovation and receive recognition along the way.

# <![if !supportLists]>2 <![endif]>Design

Give a brief overview of the component / feature design, i.e. of the rest of the document. A reader / reviewer should be able to decide from this overview if they need to read the rest.

## <![if !supportLists]>2.1 <![endif]>Key Requirements and Design Goals

Briefly describe the key requirements and design goals that drive this design. Consider the requirements from the release backlog but also **quality attributes and non-functional requirements** (they should all be in the backlog as well). The reference to the backlog / requirements is given in References above.

## <![if !supportLists]>2.2 <![endif]>Context

State the business context and technical context of the component, sub-component, or function designed in this document. What is its purpose? Refer to requirements defined in the related Software Requirements Specification to make clear, how this design fulfils them.

Explain how the components and functions which are designed in this document fit into the overall architecture (as described in the corresponding ACD) and how they fulfill functional requirements and quality attribute scenarios (as described in Software Requirements Specification). To do so, provide a block/component diagram which shows the main building blocks of your component together with surrounding components, with which it is integrated.

Note: the design has to comply with the boundary conditions given by the corresponding ACD, the corresponding unit architecture guideline(s), and the SAP Architecture Guideline.

<![if !vml]>![ERP_Overview_Example](file:///C:/Users/I077430/AppData/Local/Temp/msohtmlclip1/01/clip_image006.gif)<![endif]>

Figure 1: Architecture Context of Component X (please remove example when finalizing this document)

## <![if !supportLists]>2.3 <![endif]>Major Building Blocks

Deliver a holistic, easy-to-understand description of the design topic. Take an “outside view” and adjust the zoom to show the high-level structure.

Describe how the design topic is structured into major building blocks, which responsibilities each building block has, and how they relate to each other. Typical building blocks on this level are packages or (sub) components, and  important classes and interfaces.

It is good design practice to first focus on the most long-lived structures, which is typically the data / entity / business objects level (i.e. show the data model or the changes to the existing data model) and then describe the use cases / functions that use / traverse these objects.

Use TAM block diagrams (see [http://ency.wdf.sap.corp:1080/wiki/Modeling/Standard](http://ency.wdf.sap.corp:1080/wiki/Modeling/Standard)) and/or class diagrams to depict the building blocks and their relations. Additionally use prose to describe their responsibilities.

If helpful, visualize the desired behavior of the system and the interaction between the major building blocks as sequence diagrams or activity diagrams (“who is talking to whom in which order?”).

Describe typical interactions of client components with your component as sequence or activity diagrams and accompanying prose.

If helpful include business object models or entity-relationship diagrams of the most important database tables (table names, important fields only, no data types). A more detailed database design can be included in sections 3.x.2.

After reading this section your stakeholders must be able to understand:

<![if !supportLists]>·<![endif]>The scope and the problem described in the document,

<![if !supportLists]>·<![endif]>If the described solution appropriately solves the problem,

<![if !supportLists]>·<![endif]>Which parts of the component must be kept flexible and variable,

<![if !supportLists]>·<![endif]>The core principles of the component.,

<![if !supportLists]>·<![endif]>Potential future restrictions for extending the component.

Designers of client components should find all they need in this section.

<![if !vml]>![](file:///C:/Users/I077430/AppData/Local/Temp/msohtmlclip1/01/clip_image008.gif)<![endif]>

Figure 2: Constituents and relatives of Order (remove example when finalizing this document)

<![if !vml]>![](file:///C:/Users/I077430/AppData/Local/Temp/msohtmlclip1/01/clip_image010.gif)<![endif]>

Figure 3: Cancel Order (remove example when finalizing this document)

Use sequence diagrams for simple behavior, activity diagram for complex behavior:

<![if !vml]>![](file:///C:/Users/I077430/AppData/Local/Temp/msohtmlclip1/01/clip_image012.gif)<![endif]>

Figure 4: Bar interaction (remove example when finalizing this document)

Restrict entity-relationship diagrams here to the most important database tables and their relationships, depict only the most important fields, omit types:

<![if !vml]>![](file:///C:/Users/I077430/AppData/Local/Temp/msohtmlclip1/01/clip_image014.gif)<![endif]>

Figure 5: Order tables overview (remove example when finalizing this document)

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTUyOTA5OTQwMCw3ODAwOTI5ODhdfQ==
-->