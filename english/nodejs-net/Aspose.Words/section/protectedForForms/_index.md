---
title: Section.protectedForForms property
linktitle: protectedForForms property
articleTitle: protectedForForms property
second_title: Aspose.Words for NodeJs
description: "Section.protectedForForms property. True if the section is protected for forms"
type: docs
weight: 60
url: /nodejs-net/aspose.words/section/protectedForForms/
---

## Section.protectedForForms property

True if the section is protected for forms. When a section is protected for forms,
users can select and modify text only in form fields in Microsoft Word.


```js
get protectedForForms(): boolean
```

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

* module [Aspose.Words](../../)
* class [Section](../)

