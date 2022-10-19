---
title: FieldChar
second_title: Aspose.Words for Java API Reference
description: Base class for nodes that represent field characters in a document.
type: docs
weight: 167
url: /java/com.aspose.words/fieldchar/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.Inline](../../com.aspose.words/inline), [com.aspose.words.SpecialChar](../../com.aspose.words/specialchar)
```
public abstract class FieldChar extends SpecialChar
```

Base class for nodes that represent field characters in a document.

To learn more, visit the **Working with Fields** documentation article.

A complete field in a Microsoft Word document is a complex structure consisting of a field start character, field code, field separator character, field result and field end character. Some fields only have field start, field code and field end.

To easily insert a new field into a document, use the [DocumentBuilder.insertField(java.lang.String)](../../com.aspose.words/documentbuilder\#insertField-java.lang.String-) method.
## Constructors

| Constructor | Description |
| --- | --- |
| [FieldChar()](#FieldChar--) |  |
## Methods

| Method | Description |
| --- | --- |
| [getField()](#getField--) | Returns a field for the field char. |
| [getFieldType()](#getFieldType--) | Returns the type of the field. |
| [isLocked()](#isLocked--) | Gets whether the parent field is locked (should not recalculate its result). |
| [isLocked(boolean value)](#isLocked-boolean-) | Sets whether the parent field is locked (should not recalculate its result). |
| [isDirty()](#isDirty--) | Gets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [isDirty(boolean value)](#isDirty-boolean-) | Sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
### FieldChar() {#FieldChar--}
```
public FieldChar()
```


### getField() {#getField--}
```
public Field getField()
```


Returns a field for the field char. A new [Field](../../com.aspose.words/field) object is created each time the method is called.

**Returns:**
[Field](../../com.aspose.words/field) - A field for the field char.
### getFieldType() {#getFieldType--}
```
public int getFieldType()
```


Returns the type of the field.

**Returns:**
int - The type of the field. The returned value is one of [FieldType](../../com.aspose.words/fieldtype) constants.
### isLocked() {#isLocked--}
```
public boolean isLocked()
```


Gets whether the parent field is locked (should not recalculate its result).

**Returns:**
boolean - Whether the parent field is locked (should not recalculate its result).
### isLocked(boolean value) {#isLocked-boolean-}
```
public void isLocked(boolean value)
```


Sets whether the parent field is locked (should not recalculate its result).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether the parent field is locked (should not recalculate its result). |

### isDirty() {#isDirty--}
```
public boolean isDirty()
```


Gets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.

**Returns:**
boolean - Whether the current result of the field is no longer correct (stale) due to other modifications made to the document.
### isDirty(boolean value) {#isDirty-boolean-}
```
public void isDirty(boolean value)
```


Sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |

