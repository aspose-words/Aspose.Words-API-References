---
title: Field
second_title: Aspose.Words for Java API Reference
description: Represents a Microsoft Word document field.
type: docs
weight: 151
url: /java/com.aspose.words/field/
---

**Inheritance:**
java.lang.Object
```
public class Field
```

Represents a Microsoft Word document field.

To learn more, visit the [ Working with Fields ][Working with Fields] documentation article.

A field in a Word document is a complex structure consisting of multiple nodes that include field start, field code, field separator, field result and field end. Fields can be nested, contain rich content and span multiple paragraphs or sections in a document. The [Field](../../com.aspose.words/field) class is a "facade" object that provides properties and methods that allow to work with a field as a single object.

The [getStart()](../../com.aspose.words/field\#getStart--), [getSeparator()](../../com.aspose.words/field\#getSeparator--) and [getEnd()](../../com.aspose.words/field\#getEnd--) properties point to the field start, separator and end nodes of the field respectively.

The content between the field start and separator is the field code. The content between the field separator and field end is the field result. The field code typically consists of one or more [Run](../../com.aspose.words/run) objects that specify instructions. The processing application is expected to execute the field code to calculate the field result.

The process of calculating field results is called the field update. Aspose.Words can update field results of most of the field types in exactly the same way as Microsoft Word does it. Most notably, Aspose.Words can calculate results of even the most complex formula fields. To calculate the field result of a single field use the [update()](../../com.aspose.words/field\#update--) method. To update fields in the whole document use [Document.updateFields()](../../com.aspose.words/document\#updateFields--).

You can get the plain text version of the field code using the [getFieldCode(boolean)](../../com.aspose.words/field\#getFieldCode-boolean-) method. You can get and set the plain text version of the field result using the [getResult()](../../com.aspose.words/field\#getResult--) / [setResult(java.lang.String)](../../com.aspose.words/field\#setResult-java.lang.String-) property. Both the field code and field result can contain complex content, such as nested fields, paragraphs, shapes, tables and in this case you might want to work with the field nodes directly if you need more control.

You do not create instances of the [Field](../../com.aspose.words/field) class directly. To create a new field use the [DocumentBuilder.insertField(java.lang.String)](../../com.aspose.words/documentbuilder\#insertField-java.lang.String-) method.


[Working with Fields]: https://docs.aspose.com/words/java/working-with-fields/
## Methods

| Method | Description |
| --- | --- |
| [getFieldCode()](#getFieldCode--) | Returns text between field start and field separator (or field end if there is no separator). |
| [getFieldCode(boolean includeChildFieldCodes)](#getFieldCode-boolean-) | Returns text between field start and field separator (or field end if there is no separator). |
| [remove()](#remove--) | Removes the field from the document. |
| [update()](#update--) | Performs the field update. |
| [update(boolean ignoreMergeFormat)](#update-boolean-) | Performs a field update. |
| [unlink()](#unlink--) | Performs the field unlink. |
| [getStart()](#getStart--) | Gets the node that represents the start of the field. |
| [getSeparator()](#getSeparator--) | Gets the node that represents the field separator. |
| [getEnd()](#getEnd--) | Gets the node that represents the field end. |
| [getType()](#getType--) | Gets the Microsoft Word field type. |
| [getResult()](#getResult--) | Gets text that is between the field separator and field end. |
| [setResult(String value)](#setResult-java.lang.String-) | Sets text that is between the field separator and field end. |
| [getDisplayResult()](#getDisplayResult--) | Gets the text that represents the displayed field result. |
| [isLocked()](#isLocked--) | Gets whether the field is locked (should not recalculate its result). |
| [isLocked(boolean value)](#isLocked-boolean-) | Sets whether the field is locked (should not recalculate its result). |
| [isDirty()](#isDirty--) | Gets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [isDirty(boolean value)](#isDirty-boolean-) | Sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [getFormat()](#getFormat--) | Gets a [FieldFormat](../../com.aspose.words/fieldformat) object that provides typed access to field's formatting. |
| [getLocaleId()](#getLocaleId--) | Gets the LCID of the field. |
| [setLocaleId(int value)](#setLocaleId-int-) | Sets the LCID of the field. |
### getFieldCode() {#getFieldCode--}
```
public String getFieldCode()
```


Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included.

**Returns:**
java.lang.String
### getFieldCode(boolean includeChildFieldCodes) {#getFieldCode-boolean-}
```
public String getFieldCode(boolean includeChildFieldCodes)
```


Returns text between field start and field separator (or field end if there is no separator).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| includeChildFieldCodes | boolean | \{ True  if child field codes should be included. |

**Returns:**
java.lang.String
### remove() {#remove--}
```
public Node remove()
```


Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**.

**Returns:**
[Node](../../com.aspose.words/node)
### update() {#update--}
```
public void update()
```


Performs the field update. Throws if the field is being updated already.

### update(boolean ignoreMergeFormat) {#update-boolean-}
```
public void update(boolean ignoreMergeFormat)
```


Performs a field update. Throws if the field is being updated already.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| ignoreMergeFormat | boolean | If  true  then direct field result formatting is abandoned, regardless of the MERGEFORMAT switch, otherwise normal update is performed. |

### unlink() {#unlink--}
```
public boolean unlink()
```


Performs the field unlink.

Replaces the field with its most recent result.

Some fields, such as XE (Index Entry) fields and SEQ (Sequence) fields, cannot be unlinked.

**Returns:**
boolean - \{ True  if the field has been unlinked, otherwise  false .
### getStart() {#getStart--}
```
public FieldStart getStart()
```


Gets the node that represents the start of the field.

**Returns:**
[FieldStart](../../com.aspose.words/fieldstart) - The node that represents the start of the field.
### getSeparator() {#getSeparator--}
```
public FieldSeparator getSeparator()
```


Gets the node that represents the field separator. Can be null.

**Returns:**
[FieldSeparator](../../com.aspose.words/fieldseparator) - The node that represents the field separator.
### getEnd() {#getEnd--}
```
public FieldEnd getEnd()
```


Gets the node that represents the field end.

**Returns:**
[FieldEnd](../../com.aspose.words/fieldend) - The node that represents the field end.
### getType() {#getType--}
```
public int getType()
```


Gets the Microsoft Word field type.

**Returns:**
int - The Microsoft Word field type. The returned value is one of [FieldType](../../com.aspose.words/fieldtype) constants.
### getResult() {#getResult--}
```
public String getResult()
```


Gets text that is between the field separator and field end.

**Returns:**
java.lang.String - Text that is between the field separator and field end.
### setResult(String value) {#setResult-java.lang.String-}
```
public void setResult(String value)
```


Sets text that is between the field separator and field end.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | Text that is between the field separator and field end. |

### getDisplayResult() {#getDisplayResult--}
```
public String getDisplayResult()
```


Gets the text that represents the displayed field result. The [Document.updateListLabels()](../../com.aspose.words/document\#updateListLabels--) method must be called to obtain correct value for the [FieldListNum](../../com.aspose.words/fieldlistnum), [FieldAutoNum](../../com.aspose.words/fieldautonum), [FieldAutoNumOut](../../com.aspose.words/fieldautonumout) and [FieldAutoNumLgl](../../com.aspose.words/fieldautonumlgl) fields.

**Returns:**
java.lang.String - The text that represents the displayed field result.
### isLocked() {#isLocked--}
```
public boolean isLocked()
```


Gets whether the field is locked (should not recalculate its result).

**Returns:**
boolean - Whether the field is locked (should not recalculate its result).
### isLocked(boolean value) {#isLocked-boolean-}
```
public void isLocked(boolean value)
```


Sets whether the field is locked (should not recalculate its result).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether the field is locked (should not recalculate its result). |

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

### getFormat() {#getFormat--}
```
public FieldFormat getFormat()
```


Gets a [FieldFormat](../../com.aspose.words/fieldformat) object that provides typed access to field's formatting.

**Returns:**
[FieldFormat](../../com.aspose.words/fieldformat) - A [FieldFormat](../../com.aspose.words/fieldformat) object that provides typed access to field's formatting.
### getLocaleId() {#getLocaleId--}
```
public int getLocaleId()
```


Gets the LCID of the field.

**Returns:**
int - The LCID of the field.
### setLocaleId(int value) {#setLocaleId-int-}
```
public void setLocaleId(int value)
```


Sets the LCID of the field.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The LCID of the field. |

