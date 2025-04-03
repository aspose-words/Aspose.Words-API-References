---
title: Document.protect method
linktitle: protect method
articleTitle: protect method
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Document.protect method"
type: docs
weight: 660
url: /nodejs-net/Aspose.Words/document/protect/
---

## protect(type) {#protectiontype}

Protects the document from changes without changing the existing password or assigns a random password.


```js
protect(type: Aspose.Words.ProtectionType)
```

| Parameter | Type | Description |
| --- | --- | --- |
| type | [ProtectionType](../../protectiontype/) | Specifies the protection type for the document. |

### Remarks

When a document is protected, the user can make only limited changes,
such as adding annotations, making revisions, or completing a form.

When you protect a document, and the document already has a protection password,
the existing protection password is not changed.

When you protect a document, and the document does not have a protection password,
this method assigns a random password that makes it impossible to unprotect the document
in Microsoft Word, but you still can unprotect the document in Aspose.Words as it does not
require a password when unprotecting.




## protect(type, password) {#protectiontype_string}

Protects the document from changes and optionally sets a protection password.


```js
protect(type: Aspose.Words.ProtectionTypepassword: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| type | [ProtectionType](../../protectiontype/) | Specifies the protection type for the document. |
| password | string | The password to protect the document with. Specify ``null`` or empty string if you want to protect the document without a password. |

### Remarks

When a document is protected, the user can make only limited changes,
such as adding annotations, making revisions, or completing a form.

Note that document protection is different from write protection.
Write protection is specified using the [Document.writeProtection](../writeProtection/).




## Examples

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

Shows how to protect and unprotect a document.

```js
let doc = new aw.Document();
doc.protect(aw.ProtectionType.ReadOnly, "password");
expect(doc.protectionType).toEqual(aw.ProtectionType.ReadOnly);
// If we open this document with Microsoft Word intending to edit it,
// we will need to apply the password to get through the protection.
doc.save(base.artifactsDir + "Document.protect.docx");
// Note that the protection only applies to Microsoft Word users opening our document.
// We have not encrypted the document in any way, and we do not need the password to open and edit it programmatically.
let protectedDoc = new aw.Document(base.artifactsDir + "Document.protect.docx");
expect(protectedDoc.protectionType).toEqual(aw.ProtectionType.ReadOnly);
let builder = new aw.DocumentBuilder(protectedDoc);
builder.writeln("Text added to a protected document.");
expect(protectedDoc.range.text.trim()).toEqual("Text added to a protected document.");
// There are two ways of removing protection from a document.
// 1 - With no password:
doc.unprotect();
expect(doc.protectionType).toEqual(aw.ProtectionType.NoProtection);
doc.protect(aw.ProtectionType.ReadOnly, "NewPassword");
expect(doc.protectionType).toEqual(aw.ProtectionType.ReadOnly);
doc.unprotect("WrongPassword");
expect(doc.protectionType).toEqual(aw.ProtectionType.ReadOnly);
// 2 - With the correct password:
doc.unprotect("NewPassword");
expect(doc.protectionType).toEqual(aw.ProtectionType.NoProtection);
```

## See Also

* module [Aspose.Words](../../)
* class [Document](../)

