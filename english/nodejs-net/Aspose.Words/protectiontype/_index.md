---
title: ProtectionType enumeration
linktitle: ProtectionType enumeration
articleTitle: ProtectionType enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.ProtectionType enumeration. Protection type for a document."
type: docs
weight: 1080
url: /nodejs-net/aspose.words/protectiontype/
---

## ProtectionType enumeration

Protection type for a document.


### Members

| Name | Description |
| --- | --- |
| AllowOnlyComments | User can only modify comments in the document. |
| AllowOnlyFormFields | User can only enter data in the form fields in the document. |
| AllowOnlyRevisions | User can only add revision marks to the document. |
| ReadOnly | No changes are allowed to the document. Available since Microsoft Word 2003. |
| NoProtection | The document is not protected. |

### Examples

Shows how to turn off protection for a section.

```js
let doc = new aw.Document();

let builder = new aw.DocumentBuilder(doc);
builder.writeln("Section 1. Hello world!");
builder.insertBreak(aw.BreakType.SectionBreakNewPage);

builder.writeln("Section 2. Hello again!");
builder.write("Please enter text here: ");
builder.insertTextInput("TextInput1", aw.Fields.TextFormFieldType.Regular, "", "Placeholder text", 0);

// Apply write protection to every section in the document.
doc.protect(aw.ProtectionType.AllowOnlyFormFields);

// Turn off write protection for the first section.
doc.sections.at(0).protectedForForms = false;

// In this output document, we will be able to edit the first section freely,
// and we will only be able to edit the contents of the form field in the second section.
doc.save(base.artifactsDir + "Section.protect.docx");
```

### See Also

* module [Aspose.Words](../)

