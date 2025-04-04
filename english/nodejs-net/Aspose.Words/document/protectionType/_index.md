---
title: Document.protectionType property
linktitle: protectionType property
articleTitle: protectionType property
second_title: Aspose.Words for Node.js
description: "Document.protectionType property. Gets the currently active document protection type."
type: docs
weight: 320
url: /nodejs-net/aspose.words/document/protectionType/
---

## Document.protectionType property

Gets the currently active document protection type.


```js
get protectionType(): Aspose.Words.ProtectionType
```

### Remarks

This property allows to retrieve the currently set document protection type.
To change the document protection type use the [Document.protect()](../protect/#protectiontype_string)
and [Document.unprotect()](../unprotect/#default) methods.

When a document is protected, the user can make only limited changes,
such as adding annotations, making revisions, or completing a form.

Note that document protection is different from write protection.
Write protection is specified using the [Document.writeProtection](../writeProtection/)





### Examples

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

### See Also

* module [Aspose.Words](../../)
* class [Document](../)
* method [Document.protect()](../protect/#protectiontype_string)
* method [Document.unprotect()](../unprotect/#default)
* property [Document.writeProtection](../writeProtection/)

