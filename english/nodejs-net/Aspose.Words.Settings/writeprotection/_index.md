---
title: WriteProtection class
linktitle: WriteProtection class
articleTitle: WriteProtection class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Settings.WriteProtection class. Specifies write protection settings for a document"
type: docs
weight: 210
url: /nodejs-net/Aspose.Words.Settings/writeprotection/
---

## WriteProtection class

Specifies write protection settings for a document.
To learn more, visit the [Protect or Encrypt a Document](https://docs.aspose.com/words/nodejs-net/protect-or-encrypt-a-document/) documentation article.




### Remarks

Write protection specifies whether the author has recommended that 
the document is to be opened as read-only and/or require a password to modify a document.

Write protection is different from document protection. Write protection is specified in 
Microsoft Word in the options of the Save As dialog box.

You do not create instances of this class directly. You access document protection settings
via the [Document.writeProtection](../../Aspose.Words/document/writeProtection/) property.




### Properties

| Name | Description |
| --- | --- |
| [isWriteProtected](./isWriteProtected/) | Returns ``True`` when a write protection password is set. |
| [readOnlyRecommended](./readOnlyRecommended/) | Specifies whether the document author has recommended that the document be opened as read-only. |

### Methods

| Name | Description |
| --- | --- |
|[ setPassword(password)](./setPassword/#string) | Sets the write protection password for the document. |
|[ validatePassword(password)](./validatePassword/#string) | Returns ``True`` if the specified password is the same as the write-protection password the document was protected with. If document is not write-protected with password then returns ``False``. |

### See Also

* module [Aspose.Words.Settings](../)

