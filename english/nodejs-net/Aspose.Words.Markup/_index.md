---
title: Aspose.Words.Markup module
linktitle: Aspose.Words.Markup module
articleTitle: Aspose.Words.Markup module
second_title: Aspose.Words for Node.js
description: "The Aspose.Words.Markup module contains classes that represent customer defined semantics in a document: smart tags, custom XML and structured document tags (content controls)."
type: docs
weight: 160
url: /nodejs-net/aspose.words.markup/
---

The **Aspose.Words.Markup** module contains classes that
represent customer defined semantics in a document: smart tags, custom XML and
structured document tags (content controls).





## Classes

| Class | Description |
| --- | --- |
| [CustomPart](./custompart/) | Represents a custom (arbitrary content) part, that is not defined by the ISO/IEC 29500 standard. To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/nodejs-net/working-with-content-control-sdt/) documentation article. |
| [CustomPartCollection](./custompartcollection/) | Represents a collection of [CustomPart](./custompart/) objects. To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/nodejs-net/working-with-content-control-sdt/) documentation article. |
| [CustomXmlPart](./customxmlpart/) | Represents a Custom XML Data Storage Part (custom XML data within a package). To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/nodejs-net/working-with-content-control-sdt/) documentation article. |
| [CustomXmlPartCollection](./customxmlpartcollection/) | Represents a collection of Custom XML Parts. The items are [CustomXmlPart](./customxmlpart/) objects. To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/nodejs-net/working-with-content-control-sdt/) documentation article. |
| [CustomXmlProperty](./customxmlproperty/) | Represents a single custom XML attribute or a smart tag property. To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/nodejs-net/working-with-content-control-sdt/) documentation article. |
| [CustomXmlPropertyCollection](./customxmlpropertycollection/) | Represents a collection of custom XML attributes or smart tag properties. To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/nodejs-net/working-with-content-control-sdt/) documentation article. |
| [CustomXmlSchemaCollection](./customxmlschemacollection/) | A collection of strings that represent XML schemas that are associated with a custom XML part. To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/nodejs-net/working-with-content-control-sdt/) documentation article. |
| [SdtListItem](./sdtlistitem/) | This element specifies a single list item within a parent [SdtType.ComboBox](./sdttype/#ComboBox) or [SdtType.DropDownList](./sdttype/#DropDownList) structured document tag. To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/nodejs-net/working-with-content-control-sdt/) documentation article. |
| [SdtListItemCollection](./sdtlistitemcollection/) | Provides access to [SdtListItem](./sdtlistitem/) elements of a structured document tag. To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/nodejs-net/working-with-content-control-sdt/) documentation article. |
| [SmartTag](./smarttag/) | This element specifies the presence of a smart tag around one or more inline structures (runs, images, fields,etc.) within a paragraph. To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/nodejs-net/working-with-content-control-sdt/) documentation article. |
| [StructuredDocumentTag](./structureddocumenttag/) | Represents a structured document tag (SDT or content control) in a document. To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/nodejs-net/working-with-content-control-sdt/) documentation article. |
| [StructuredDocumentTagCollection](./structureddocumenttagcollection/) | A collection of [IStructuredDocumentTag](./istructureddocumenttag/) instances that represent the structured document tags in the specified range. To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/nodejs-net/working-with-content-control-sdt/) documentation article. |
| [StructuredDocumentTagRangeEnd](./structureddocumenttagrangeend/) | Represents an end of **ranged** structured document tag which accepts multi-sections content. See also [StructuredDocumentTagRangeStart](./structureddocumenttagrangestart/) node. To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/nodejs-net/working-with-content-control-sdt/) documentation article. |
| [StructuredDocumentTagRangeStart](./structureddocumenttagrangestart/) | Represents a start of **ranged** structured document tag which accepts multi-sections content. See also [StructuredDocumentTagRangeEnd](./structureddocumenttagrangeend/). To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/nodejs-net/working-with-content-control-sdt/) documentation article. |
| [XmlMapping](./xmlmapping/) | Specifies the information that is used to establish a mapping between the parent structured document tag and an XML element stored within a custom XML data part in the document. To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/nodejs-net/working-with-content-control-sdt/) documentation article. |
| [IStructuredDocumentTag](./istructureddocumenttag/) | Interface to define a common data for [StructuredDocumentTag](./structureddocumenttag/) and [StructuredDocumentTagRangeStart](./structureddocumenttagrangestart/). |

## Enumerations

| Enumeration | Description |
| --- | --- |
| [MarkupLevel](./markuplevel/) | Specifies the level in the document tree where a particular [StructuredDocumentTag](./structureddocumenttag/) can occur. |
| [SdtAppearance](./sdtappearance/) | Specifies the appearance of a structured document tag. |
| [SdtCalendarType](./sdtcalendartype/) | Specifies the possible types of calendars which can be used to specify [StructuredDocumentTag.calendarType](./structureddocumenttag/calendarType/) in an Office Open XML document. |
| [SdtDateStorageFormat](./sdtdatestorageformat/) | Specifies how the date for a date SDT is stored/retrieved when the SDT is bound to an XML node in the document's data store. |
| [SdtType](./sdttype/) | Specifies the type of a structured document tag (SDT) node. |

