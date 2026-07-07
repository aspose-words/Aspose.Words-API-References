---
title: Document.unprotect method
linktitle: unprotect method
articleTitle: unprotect method
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Document.unprotect method"
type: docs
weight: 740
url: /nodejs-net/aspose.words/document/unprotect/
---

## unprotect() {#default}

Removes protection from the document regardless of the password.


```js
unprotect()
```

### Remarks

This method unprotects the document even if it has a protection password.

Note that document protection is different from write protection.
Write protection is specified using the [Document.writeProtection](../writeProtection/).




## unprotect(password) {#string}

Removes protection from the document if a correct password is specified.


```js
unprotect(password: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| password | string | The password to unprotect the document with. |

### Remarks

This method unprotects the document only if a correct password is specified.

Note that document protection is different from write protection.
Write protection is specified using the [Document.writeProtection](../writeProtection/).




### Returns

``true`` if a correct password was specified and the document was unprotected.


## Examples

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

