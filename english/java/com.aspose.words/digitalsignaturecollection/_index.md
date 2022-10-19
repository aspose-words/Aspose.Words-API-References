---
title: DigitalSignatureCollection
second_title: Aspose.Words for Java API Reference
description: Provides a read-only collection of digital signatures attached to a document.
type: docs
weight: 112
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

To learn more, visit the **Work with Digital Signatures** documentation article.

[Document.getDigitalSignatures()](../../com.aspose.words/document\#getDigitalSignatures--)
## Methods

| Method | Description |
| --- | --- |
| [isValid()](#isValid--) | Returns  true  if all digital signatures in this collection are valid and the document has not been tampered with Also returns  true  if there are no digital signatures. |
| [getCount()](#getCount--) | Gets the number of elements contained in the collection. |
| [get(int index)](#get-int-) | Gets a document signature at the specified index. |
| [iterator()](#iterator--) | Returns a dictionary iterator object that can be used to iterate over all items in the collection. |
### isValid() {#isValid--}
```
public boolean isValid()
```


Returns  true  if all digital signatures in this collection are valid and the document has not been tampered with Also returns  true  if there are no digital signatures. Returns  false  if at least one digital signature is invalid.

**Returns:**
boolean - \{ true  if all digital signatures in this collection are valid and the document has not been tampered with Also returns  true  if there are no digital signatures.
### getCount() {#getCount--}
```
public int getCount()
```


Gets the number of elements contained in the collection.

**Returns:**
int - The number of elements contained in the collection.
### get(int index) {#get-int-}
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
### iterator() {#iterator--}
```
public Iterator iterator()
```


Returns a dictionary iterator object that can be used to iterate over all items in the collection.

**Returns:**
java.util.Iterator
