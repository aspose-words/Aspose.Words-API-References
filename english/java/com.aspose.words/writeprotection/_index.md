---
title: WriteProtection
second_title: Aspose.Words for Java API Reference
description: Specifies write protection settings for a document.
type: docs
weight: 623
url: /java/com.aspose.words/writeprotection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class WriteProtection implements Cloneable
```

Specifies write protection settings for a document.

To learn more, visit the **Protect or Encrypt a Document** documentation article.

Write protection specifies whether the author has recommended that the document is to be opened as read-only and/or require a password to modify a document.

Write protection is different from document protection. Write protection is specified in Microsoft Word in the options of the Save As dialog box.

You do not create instances of this class directly. You access document protection settings via the [Document.getWriteProtection()](../../com.aspose.words/document\#getWriteProtection--) property.
## Methods

| Method | Description |
| --- | --- |
| [getReadOnlyRecommended()](#getReadOnlyRecommended--) | Specifies whether the document author has recommended that the document be opened as read-only. |
| [setReadOnlyRecommended(boolean value)](#setReadOnlyRecommended-boolean-) | Specifies whether the document author has recommended that the document be opened as read-only. |
| [setPassword(String password)](#setPassword-java.lang.String-) | Sets the write protection password for the document. |
| [validatePassword(String password)](#validatePassword-java.lang.String-) | Returns true if the specified password is the same as the write-protection password the document was protected with. |
| [isWriteProtected()](#isWriteProtected--) | Returns true when a write protection password is set. |
### getReadOnlyRecommended() {#getReadOnlyRecommended--}
```
public boolean getReadOnlyRecommended()
```


Specifies whether the document author has recommended that the document be opened as read-only.

**Returns:**
boolean - The corresponding  boolean  value.
### setReadOnlyRecommended(boolean value) {#setReadOnlyRecommended-boolean-}
```
public void setReadOnlyRecommended(boolean value)
```


Specifies whether the document author has recommended that the document be opened as read-only.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setPassword(String password) {#setPassword-java.lang.String-}
```
public void setPassword(String password)
```


Sets the write protection password for the document.

If a password is set, Microsoft Word will require the user to enter it or open the document as read-only.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| password | java.lang.String | The password to set. Cannot be null, but can be an empty string. |

### validatePassword(String password) {#validatePassword-java.lang.String-}
```
public boolean validatePassword(String password)
```


Returns true if the specified password is the same as the write-protection password the document was protected with. If document is not write-protected with password then returns false.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| password | java.lang.String |  |

**Returns:**
boolean
### isWriteProtected() {#isWriteProtected--}
```
public boolean isWriteProtected()
```


Returns true when a write protection password is set.

**Returns:**
boolean - True when a write protection password is set.
