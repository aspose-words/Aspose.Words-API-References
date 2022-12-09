---
title: DigitalSignatureCollection
second_title: Aspose.Words for Java API Reference
description: Provides a read-only collection of digital signatures attached to a document.
type: docs
weight: 113
url: /java/com.aspose.words/digitalsignaturecollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class DigitalSignatureCollection implements Iterable
```

Provides a read-only collection of digital signatures attached to a document.

To learn more, visit the [ Work with Digital Signatures ][Work with Digital Signatures] documentation article.

[Document.getDigitalSignatures()](../../com.aspose.words/document\#getDigitalSignatures)


[Work with Digital Signatures]: https://docs.aspose.com/words/java/working-with-digital-signatures/
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [get(int index)](#get-int) | Gets a document signature at the specified index. |
| [getClass()](#getClass) |  |
| [getCount()](#getCount) | Gets the number of elements contained in the collection. |
| [hashCode()](#hashCode) |  |
| [isValid()](#isValid) | Returns  true  if all digital signatures in this collection are valid and the document has not been tampered with Also returns  true  if there are no digital signatures. |
| [iterator()](#iterator) | Returns a dictionary iterator object that can be used to iterate over all items in the collection. |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
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
### get(int index) {#get-int}
```
public DigitalSignature get(int index)
```


Gets a document signature at the specified index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | Zero-based index of the signature. |

**Returns:**
[DigitalSignature](../../com.aspose.words/digitalsignature) - A document signature at the specified index.
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getCount() {#getCount}
```
public int getCount()
```


Gets the number of elements contained in the collection.

**Returns:**
int - The number of elements contained in the collection.
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### isValid() {#isValid}
```
public boolean isValid()
```


Returns  true  if all digital signatures in this collection are valid and the document has not been tampered with Also returns  true  if there are no digital signatures. Returns  false  if at least one digital signature is invalid.

**Returns:**
boolean - \{ true  if all digital signatures in this collection are valid and the document has not been tampered with Also returns  true  if there are no digital signatures.
### iterator() {#iterator}
```
public Iterator iterator()
```


Returns a dictionary iterator object that can be used to iterate over all items in the collection.

**Returns:**
java.util.Iterator
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
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

