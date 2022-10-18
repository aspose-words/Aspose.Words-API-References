---
title: FieldMergeField
second_title: Aspose.Words for Java API Reference
description: Implements the MERGEFIELD field.
type: docs
weight: 215
url: /java/com.aspose.words/fieldmergefield/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field)
```
public class FieldMergeField extends Field
```

Implements the MERGEFIELD field.

To learn more, visit the **Working with Fields** documentation article.

Retrieves the name of a data field within the merge characters in a mail merge main document. When the main document is merged with the selected data source, information from the specified data field is inserted in place of the merge field.
## Methods

| Method | Description |
| --- | --- |
| [getType()](#getType--) | Gets the Microsoft Word field type. |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String-) |  |
| [getFieldNameNoPrefix()](#getFieldNameNoPrefix--) | Returns just the name of the data field. |
| [getFieldName()](#getFieldName--) | Gets the name of a data field. |
| [setFieldName(String value)](#setFieldName-java.lang.String-) | Sets the name of a data field. |
| [getTextBefore()](#getTextBefore--) | Gets the text to be inserted before the field if the field is not blank. |
| [setTextBefore(String value)](#setTextBefore-java.lang.String-) | Sets the text to be inserted before the field if the field is not blank. |
| [getTextAfter()](#getTextAfter--) | Gets the text to be inserted after the field if the field is not blank. |
| [setTextAfter(String value)](#setTextAfter-java.lang.String-) | Sets the text to be inserted after the field if the field is not blank. |
| [isMapped()](#isMapped--) | Gets whether this field is a mapped field. |
| [isMapped(boolean value)](#isMapped-boolean-) | Sets whether this field is a mapped field. |
| [isVerticalFormatting()](#isVerticalFormatting--) | Gets whether to enable character conversion for vertical formatting. |
| [isVerticalFormatting(boolean value)](#isVerticalFormatting-boolean-) | Sets whether to enable character conversion for vertical formatting. |
### getType() {#getType--}
```
public int getType()
```


Gets the Microsoft Word field type.

**Returns:**
int - The Microsoft Word field type. The returned value is one of [FieldType](../../com.aspose.words/fieldtype) constants.
### getSwitchType(String switchName) {#getSwitchType-java.lang.String-}
```
public int getSwitchType(String switchName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| switchName | java.lang.String |  |

**Returns:**
int
### getFieldNameNoPrefix() {#getFieldNameNoPrefix--}
```
public String getFieldNameNoPrefix()
```


Returns just the name of the data field. Any prefix is stripped to the prefix property.

**Returns:**
java.lang.String - Just the name of the data field.
### getFieldName() {#getFieldName--}
```
public String getFieldName()
```


Gets the name of a data field.

**Returns:**
java.lang.String - The name of a data field.
### setFieldName(String value) {#setFieldName-java.lang.String-}
```
public void setFieldName(String value)
```


Sets the name of a data field.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The name of a data field. |

### getTextBefore() {#getTextBefore--}
```
public String getTextBefore()
```


Gets the text to be inserted before the field if the field is not blank.

**Returns:**
java.lang.String - The text to be inserted before the field if the field is not blank.
### setTextBefore(String value) {#setTextBefore-java.lang.String-}
```
public void setTextBefore(String value)
```


Sets the text to be inserted before the field if the field is not blank.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The text to be inserted before the field if the field is not blank. |

### getTextAfter() {#getTextAfter--}
```
public String getTextAfter()
```


Gets the text to be inserted after the field if the field is not blank.

**Returns:**
java.lang.String - The text to be inserted after the field if the field is not blank.
### setTextAfter(String value) {#setTextAfter-java.lang.String-}
```
public void setTextAfter(String value)
```


Sets the text to be inserted after the field if the field is not blank.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The text to be inserted after the field if the field is not blank. |

### isMapped() {#isMapped--}
```
public boolean isMapped()
```


Gets whether this field is a mapped field.

**Returns:**
boolean - Whether this field is a mapped field.
### isMapped(boolean value) {#isMapped-boolean-}
```
public void isMapped(boolean value)
```


Sets whether this field is a mapped field.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether this field is a mapped field. |

### isVerticalFormatting() {#isVerticalFormatting--}
```
public boolean isVerticalFormatting()
```


Gets whether to enable character conversion for vertical formatting.

**Returns:**
boolean - Whether to enable character conversion for vertical formatting.
### isVerticalFormatting(boolean value) {#isVerticalFormatting-boolean-}
```
public void isVerticalFormatting(boolean value)
```


Sets whether to enable character conversion for vertical formatting.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to enable character conversion for vertical formatting. |

