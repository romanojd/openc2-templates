![OASIS Logo](http://docs.oasis-open.org/templates/OASISLogo.jpg)
***
<!--
Basic guidance
*****color tags:
red:
<span style="color:#FF0000">text</span> 
OASIS purple:
<span style="color:#3B006F">text</span> 
********** vertical spacing
EOL = LF or CRLF
- single spacing: terminate line with two* space characters and EOL
- double spacing: terminate line with two* EOL  (of course, second EOL is on a new line)
* actually two or more, but more than two are ignored
- bullet handling: AFAIK must have two EOL before bulleted line(s) - so no way to have a single vertical space before bullets
*********** cross-references and anchor points 
- basic structure:
-- hyperlink: [visible text](#target)
-- anchor point:  <a name="target"></a>

- example usage in links to References
-- hyperlink example: as described in [[RFC2119](#RFC2119)] and [[RFC8174](#RFC8174)]
-- anchor point example:  
**[RFC2119]<a name="RFC2119"></a>**  

Bradner, S., "Key words for use in RFCs to Indicate Requirement Levels", BCP 14, RFC 2119, DOI 10.17487/RFC2119, March 1997, <http://www.rfc-editor.org/info/rfc2119>.  

**** 
-->

# <span style="color:#3B006F">Specification for Transfer of OpenC2 Messages via HTTPS Version 1.0
<!--
TC Editors: Change text below to Committee Specification Draft 01, etc., for publication
-->
## <span style="color:#3B006F">Working Draft 01
## <span style="color:#3B006F">11 June 2018
#### <span style="color:#3B006F">Specification URIs

<span style="color:#3B006F">**This version:**</span>  
[http://docs.oasis-open.org/openc2/open-impl-https/v1.0/csd01/open-impl-https-v1.0-csd01.md](http://docs.oasis-open.org/openc2/open-impl-https/v1.0/csd01/open-impl-https-v1.0-csd01.md) (Authoritative)  
[http://docs.oasis-open.org/openc2/open-impl-https/v1.0/csd01/open-impl-https-v1.0-csd01.html](http://docs.oasis-open.org/openc2/open-impl-https/v1.0/csd01/open-impl-https-v1.0-csd01.html)  
[http://docs.oasis-open.org/openc2/open-impl-https/v1.0/csd01/open-impl-https-v1.0-csd01.pdf](http://docs.oasis-open.org/openc2/open-impl-https/v1.0/csd01/open-impl-https-v1.0-csd01.pdf)  

<span style="color:#3B006F">**Previous Version:**</span>  
N/A

<span style="color:#3B006F">**Latest Version:**</span>  
[http://docs.oasis-open.org/openc2/open-impl-https/v1.0/open-impl-https-v1.0.md](http://docs.oasis-open.org/openc2/open-impl-https/v1.0/open-impl-https-v1.0.md) (Authoritative)  
[http://docs.oasis-open.org/openc2/open-impl-https/v1.0/open-impl-https-v1.0.html](http://docs.oasis-open.org/openc2/open-impl-https/v1.0/open-impl-https-v1.0.html)  
[http://docs.oasis-open.org/openc2/open-impl-https/v1.0/open-impl-https-v1.0.pdf](http://docs.oasis-open.org/openc2/open-impl-https/v1.0/open-impl-https-v1.0.pdf)  

<span style="color:#3B006F">**Technical Committee:**</span>  
[OASIS Open Command and Control (OpenC2) TC](https://www.oasis-open.org/committees/openc2/)

<span style="color:#3B006F">**Chairs:**</span>  
Joe Brule ([jmbrule@nsa.gov](mailto:jmbrule@nsa.gov)), [National Security Agency](https://www.nsa.gov/)  
Sounil Yu ([sounil.yu@bankofamerica.com](mailto:sounil.yu@bankofamerica.com)), [Bank of America](http://www.bankofamerica.com/)  

<span style="color:#3B006F">**Editor:**</span>  
David Lemire ([dave.lemire@g2-inc.com](mailto:dave.lemire@g2-inc.com)), [G2, Inc.](http://www.g2-inc.com/)  

<span style="color:#3B006F">**Additional artifacts:**</span>  
This prose specification is one component of a Work Product that also includes:  

* XML schemas: http://docs.oasis-open.org/openc2/open-impl-https/v1.0/csd01/schemas/
<span style="color:#FF0000">(hyperlink, including terminating /)</span>
* Other parts 
<span style="color:#FF0000">(list full title and VISIBLE hyperlink, preferably to HTML version) 
(remove entire section if no entries - don't use "N/A")</span>

<span style="color:#3B006F">**Related work:**</span>  
This specification replaces or supersedes:  

* Specifications replaced by this specification 
<span style="color:#FF0000">(VISIBLE hyperlink, preferably to HTML version)</span>

This specification is related to:  

* Related specifications 
<span style="color:#FF0000">(VISIBLE hyperlink, preferably to HTML version)
(remove "Related work" section or the "replaces" or "related" subsections if no entries)</span>

<span style="color:#3B006F">**Declared XML namespaces:**</span>  

* list namespaces which are declared, not just referenced 
<span style="color:#FF0000">(hyperlink if HTTP-based URI)
(remove "Declared XML namespaces" section if no entries - don't use "N/A")</span>

<span style="color:#3B006F">**Abstract**</span>  
Summary of the technical purpose of the document.

<span style="color:#3B006F">**Status:**</span>  
This document was last revised or approved by the 
OASIS Open Command and Control (OpenC2) TC 
on the above date. The level of approval is also listed above. Check the "Latest version" location noted above for possible later revisions of this document. Any other numbered Versions and other technical work produced by the Technical Committee (TC) are listed at [https://www.oasis-open.org/committees/tc\_home.php?wg\_abbrev=openc2#technical](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=openc2#technical).  
TC members should send comments on this specification to the TC's email list. Others should send comments to the TC's public comment list, after subscribing to it by following the instructions at the "[Send A Comment](https://www.oasis-open.org/committees/comments/index.php?wg_abbrev=openc2)" button on the TC's web page at [https://www.oasis-open.org/committees/openc2/](https://www.oasis-open.org/committees/openc2/).  
This specification is provided under the 
[Non-Assertion](https://www.oasis-open.org/policies-guidelines/ipr#Non-Assertion-Mode) 
Mode of the [OASIS IPR Policy](https://www.oasis-open.org/policies-guidelines/ipr), the mode chosen when the Technical Committee was established. 
For information on whether any patents have been disclosed that may be essential to implementing this specification, and any offers of patent licensing terms, please refer to the Intellectual Property Rights section of the TC's web page 
([https://www.oasis-open.org/committees/openc2/ipr.php](https://www.oasis-open.org/committees/openc2/ipr.php)).  
Note that any machine-readable content ([Computer Language Definitions](https://www.oasis-open.org/policies-guidelines/tc-process#wpComponentsCompLang)) declared Normative for this Work Product is provided in separate plain text files. In the event of a discrepancy between any such plain text file and display content in the Work Product's prose narrative document(s), the content in the separate plain text file prevails.  

<span style="color:#3B006F">**Citation format:**</span>  
When referencing this specification the following citation format should be used:

**[OpenC2-HTTPS-v1.0]**

*Specification for Transfer of OpenC2 Messages via HTTPS Version 1.0*. Edited by David Lemire. 11 June 2018. OASIS Committee Specification Draft 01. [http://docs.oasis-open.org/openc2/open-impl-https/v1.0/csd01/open-impl-https-v1.0-csd01.html](http://docs.oasis-open.org/openc2/open-impl-https/v1.0/csd01/open-impl-https-v1.0-csd01.html). Latest version: [http://docs.oasis-open.org/openc2/open-impl-https/v1.0/open-impl-https-v1.0.html](http://docs.oasis-open.org/openc2/open-impl-https/v1.0/open-impl-https-v1.0.html).

-------
## <span style="color:#3B006F">Notices

Copyright © OASIS Open 2018. All Rights Reserved.
All capitalized terms in the following text have the meanings assigned to them in the OASIS Intellectual Property Rights Policy (the "OASIS IPR Policy"). The full [Policy](https://www.oasis-open.org/policies-guidelines/ipr) may be found at the OASIS website.

This document and translations of it may be copied and furnished to others, and derivative works that comment on or otherwise explain it or assist in its implementation may be prepared, copied, published, and distributed, in whole or in part, without restriction of any kind, provided that the above copyright notice and this section are included on all such copies and derivative works. However, this document itself may not be modified in any way, including by removing the copyright notice or references to OASIS, except as needed for the purpose of developing any document or deliverable produced by an OASIS Technical Committee (in which case the rules applicable to copyrights, as set forth in the OASIS IPR Policy, must be followed) or as required to translate it into languages other than English.

The limited permissions granted above are perpetual and will not be revoked by OASIS or its successors or assigns.

This document and the information contained herein is provided on an "AS IS" basis and OASIS DISCLAIMS ALL WARRANTIES, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO ANY WARRANTY THAT THE USE OF THE INFORMATION HEREIN WILL NOT INFRINGE ANY OWNERSHIP RIGHTS OR ANY IMPLIED WARRANTIES OF MERCHANTABILITY OR FITNESS FOR A PARTICULAR PURPOSE.

OASIS requests that any OASIS Party or any other party that believes it has patent claims that would necessarily be infringed by implementations of this OASIS Committee Specification or OASIS Standard, to notify OASIS TC Administrator and provide an indication of its willingness to grant patent licenses to such patent claims in a manner consistent with the IPR Mode of the OASIS Technical Committee that produced this specification.

OASIS invites any party to contact the OASIS TC Administrator if it is aware of a claim of ownership of any patent claims that would necessarily be infringed by implementations of this specification by a patent holder that is not willing to provide a license to such patent claims in a manner consistent with the IPR Mode of the OASIS Technical Committee that produced this specification. OASIS may include such claims on its website, but disclaims any obligation to do so.

OASIS takes no position regarding the validity or scope of any intellectual property or other rights that might be claimed to pertain to the implementation or use of the technology described in this document or the extent to which any license under such rights might or might not be available; neither does it represent that it has made any effort to identify any such rights. Information on OASIS' procedures with respect to rights in any document or deliverable produced by an OASIS Technical Committee can be found on the OASIS website. Copies of claims of rights made available for publication and any assurances of licenses to be made available, or the result of an attempt made to obtain a general license or permission for the use of such proprietary rights by implementers or users of this OASIS Committee Specification or OASIS Standard, can be obtained from the OASIS TC Administrator. OASIS makes no representation that any information or list of intellectual property rights will at any time be complete, or that any claims in such list are, in fact, Essential Claims.

The name "OASIS" is a trademark of [OASIS](https://www.oasis-open.org/), the owner and developer of this specification, and should be used only to refer to the organization and its official outputs. OASIS welcomes reference to, and implementation and use of, specifications, while reserving the right to enforce its marks against misleading uses. Please see [https://www.oasis-open.org/policies-guidelines/trademark](https://www.oasis-open.org/policies-guidelines/trademark) for above guidance.

## <span style="color:#3B006F">Table of Contents  
[TOC]

# <span style="color:#3B006F">1 Introduction  
Text.

## <span style="color:#3B006F">1.1 IPR Policy  
<!--
TC Editors: Please don't modify text in this section.
-->
This specification is provided under the 
[Non-Assertion](https://www.oasis-open.org/policies-guidelines/ipr#Non-Assertion-Mode) 
Mode of the [OASIS IPR Policy](https://www.oasis-open.org/policies-guidelines/ipr), the mode chosen when the Technical Committee was established. 
For information on whether any patents have been disclosed that may be essential to implementing this specification, and any offers of patent licensing terms, please refer to the Intellectual Property Rights section of the TC's web page 
([https://www.oasis-open.org/committees/openc2/ipr.php](https://www.oasis-open.org/committees/openc2/ipr.php)).  

##  <span style="color:#3B006F">1.2 Terminology
The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED", "MAY", and "OPTIONAL" in this document are to be interpreted as described in [[RFC2119](#RFC2119)] and [[RFC8174](#RFC8174)] when, and only when, they appear in all capitals, as shown here.

##  <span style="color:#3B006F">1.3 Normative References  
**[RFC2119]<a name="RFC2119"></a>**  
Bradner, S., "Key words for use in RFCs to Indicate Requirement Levels", BCP 14, RFC 2119, DOI 10.17487/RFC2119, March 1997, <http://www.rfc-editor.org/info/rfc2119>.  

**[RFC8174]<a name="RFC8174"></a>**  
Leiba, B., "Ambiguity of Uppercase vs Lowercase in RFC 2119 Key Words", BCP 14, RFC 8174, DOI 10.17487/RFC8174, May 2017, <http://www.rfc-editor.org/info/rfc8174>.  

**[Reference]**  
[Full reference citation]

##  <span style="color:#3B006F">1.4 Non-Normative References  
**[Reference]**  
[Full reference citation]

(<span style="color:#FF0000">**Note:**</span>  
_Reference sources:_  
For references to **IETF RFCs**, use the approved citation formats at:  
[http://docs.oasis-open.org/templates/ietf-rfc-list/ietf-rfc-list.html](http://docs.oasis-open.org/templates/ietf-rfc-list/ietf-rfc-list.html).  
For references to **W3C Recommendations**, use the approved citation formats at:  
[http://docs.oasis-open.org/templates/w3c-recommendations-list/w3c-recommendations-list.html](http://docs.oasis-open.org/templates/w3c-recommendations-list/w3c-recommendations-list.html).  
<span style="color:#FF0000">Remove this note before submitting for publication.</span>)

#  <span style="color:#3B006F">2 Section Title  
Text
##  <span style="color:#3B006F">2.1 Level 2 Section Title   
Text
###  <span style="color:#3B006F">2.1.1 Level 3 Section Title  
Text
#####  <span style="color:#3B006F">2.1.1.1 Level 4 Section Title  
Text
######  <span style="color:#3B006F">2.1.1.1.1 Level 5 Section Title  
Level 5 is the deepest available in Markdown.

#  <span style="color:#3B006F">3 Conformance  
(<span style="color:#FF0000">**Note:**</span> The [OASIS TC Process](https://www.oasis-open.org/policies-guidelines/tc-process#wpComponentsConfClause) requires that a specification approved by the TC at the Committee Specification Public Review Draft, Committee Specification or OASIS Standard level must include a separate section, listing a set of numbered conformance clauses, to which any implementation of the specification must adhere in order to claim conformance to the specification (or any optional portion thereof). This is done by listing the conformance clauses here.
For the definition of "conformance clause," see [OASIS Defined Terms](https://www.oasis-open.org/policies-guidelines/oasis-defined-terms-2017-05-26#dConformanceClause).  
See "Guidelines to Writing Conformance Clauses":  
[http://docs.oasis-open.org/templates/TCHandbook/ConformanceGuidelines.html](http://docs.oasis-open.org/templates/TCHandbook/ConformanceGuidelines.html).  
<span style="color:#FF0000">Remove this note before submitting for publication.</span>)

#  <span style="color:#3B006F">Appendix A. Acknowledgments
The following individuals have participated in the creation of this specification and are gratefully acknowledged:

**Participants**:


#  <span style="color:#3B006F">Appendix B. Revision History  

