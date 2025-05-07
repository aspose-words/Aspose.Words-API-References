---
title: CustomPart class
linktitle: CustomPart class
articleTitle: CustomPart class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Markup.CustomPart class. Represents a custom (arbitrary content) part, that is not defined by the ISO/IEC 29500 standard"
type: docs
weight: 10
url: /nodejs-net/aspose.words.markup/custompart/
---

## CustomPart class

Represents a custom (arbitrary content) part, that is not defined by the ISO/IEC 29500 standard.
To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/nodejs-net/working-with-content-control-sdt/) documentation article.




### Remarks

This class represents an OOXML part that is a target of an "unknown relationship".
All relationships not defined within ISO/IEC 29500 are considered "unknown relationships".
Unknown relationships are permitted within an Office Open XML document provided that they 
conform to relationship markup guidelines.

Microsoft Word preserves custom parts during open/save cycles. Some additional info can be found 
here http://blogs.msdn.com/dmahugh/archive/2006/11/25/arbitrary-content-in-an-opc-package.aspx

Aspose.Words also roundtrips custom parts and in addition, allows to programmatically access 
such parts via the [CustomPart](./) and [CustomPartCollection](../custompartcollection/) objects.

Do not confuse custom parts with Custom XML Data. Use [CustomXmlPart](../customxmlpart/) if you need 
to access Custom XML Data.




### Constructors
| Name | Description |
| --- | --- |
| [CustomPart()](./constructor/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [contentType](./contentType/) | Specifies the content type of this custom part. |
| [data](./data/) | Contains the data of this custom part. |
| [isExternal](./isExternal/) | False if this custom part is stored inside the OOXML package. True if this custom part is an external target. |
| [name](./name/) | Gets or sets this part's absolute name within the OOXML package or the target URL. |
| [relationshipType](./relationshipType/) | Gets or sets the relationship type from the parent part to this custom part. |

### Methods

| Name | Description |
| --- | --- |
|[ clone()](./clone/#default) | Makes a "deep enough" copy of the object.  Does not duplicate the bytes of the [CustomPart.data](./data/) value. |

### See Also

* module [Aspose.Words.Markup](../)
* class [CustomPartCollection](../custompartcollection/)
* property [Document.packageCustomParts](../../aspose.words/document/packageCustomParts/)

