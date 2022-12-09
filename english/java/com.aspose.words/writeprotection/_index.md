---
title: WriteProtection
second_title: Aspose.Words for Java API Reference
description: Specifies write protection settings for a document.
type: docs
weight: 626
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

To learn more, visit the [ Protect or Encrypt a Document ][Protect or Encrypt a Document] documentation article.

Write protection specifies whether the author has recommended that the document is to be opened as read-only and/or require a password to modify a document.

Write protection is different from document protection. Write protection is specified in Microsoft Word in the options of the Save As dialog box.

You do not create instances of this class directly. You access document protection settings via the [Document.getWriteProtection()](../../com.aspose.words/document\#getWriteProtection) property.


[Protect or Encrypt a Document]: https://docs.aspose.com/words/java/protect-or-encrypt-a-document/
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getClass()](#getClass) |  |
| [getReadOnlyRecommended()](#getReadOnlyRecommended) | Specifies whether the document author has recommended that the document be opened as read-only. |
| [hashCode()](#hashCode) |  |
| [isWriteProtected()](#isWriteProtected) | Returns  true  when a write protection password is set. |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [setPassword(String password)](#setPassword-java.lang.String) | Sets the write protection password for the document. |
| [setReadOnlyRecommended(boolean value)](#setReadOnlyRecommended-boolean) | Specifies whether the document author has recommended that the document be opened as read-only. |
| [toString()](#toString) |  |
| [validatePassword(String password)](#validatePassword-java.lang.String) | Returns  true  if the specified password is the same as the write-protection password the document was protected with. |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getReadOnlyRecommended() {#getReadOnlyRecommended}
```
public boolean getReadOnlyRecommended()
```


Specifies whether the document author has recommended that the document be opened as read-only.

**Returns:**
boolean - The corresponding  boolean  value.
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### isWriteProtected() {#isWriteProtected}
```
public boolean isWriteProtected()
```


Returns  true  when a write protection password is set.

**Returns:**
boolean - \{ true  when a write protection password is set.
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### setPassword(String password) {#setPassword-java.lang.String}
```
public void setPassword(String password)
```


Sets the write protection password for the document.

If a password is set, Microsoft Word will require the user to enter it or open the document as read-only.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| password | java.lang.String | The password to set. Cannot be  null , but can be an empty string. |

### setReadOnlyRecommended(boolean value) {#setReadOnlyRecommended-boolean}
```
public void setReadOnlyRecommended(boolean value)
```


Specifies whether the document author has recommended that the document be opened as read-only.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### validatePassword(String password) {#validatePassword-java.lang.String}
```
public boolean validatePassword(String password)
```


Returns  true  if the specified password is the same as the write-protection password the document was protected with. If document is not write-protected with password then returns  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| password | java.lang.String |  |

**Returns:**
boolean
### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

