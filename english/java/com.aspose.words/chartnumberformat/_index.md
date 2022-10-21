---
title: ChartNumberFormat
second_title: Aspose.Words for Java API Reference
description: Represents number formatting of the parent element.
type: docs
weight: 67
url: /java/com.aspose.words/chartnumberformat/
---

**Inheritance:**
java.lang.Object
```
public class ChartNumberFormat
```

Represents number formatting of the parent element.

To learn more, visit the **Working with Charts** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [getFormatCode()](#getFormatCode--) | Gets the format code applied to a data label. |
| [setFormatCode(String value)](#setFormatCode-java.lang.String-) | Sets the format code applied to a data label. |
| [isLinkedToSource()](#isLinkedToSource--) | Specifies whether the format code is linked to a source cell. |
| [isLinkedToSource(boolean value)](#isLinkedToSource-boolean-) | Specifies whether the format code is linked to a source cell. |
### getFormatCode() {#getFormatCode--}
```
public String getFormatCode()
```


Gets the format code applied to a data label. Number formatting is used to change the way a value appears in data label and can be used in some very creative ways. The examples of number formats:

Number - "\#,\#\#0.00"

Currency - "\\"$\\"\#,\#\#0.00"

Time - "[$-x-systime]h:mm:ss AM/PM"

Date - "d/mm/yyyy"

Percentage - "0.00%"

Fraction - "\# ?/?"

Scientific - "0.00E+00"

Text - "@"

Accounting - "\_-\\"$\\"\* \#,\#\#0.00\_-;-\\"$\\"\* \#,\#\#0.00\_-;\_-\\"$\\"\* \\"-\\"??\_-;\_-@\_-"

Custom with color - "[Red]-\#,\#\#0.0"

**Returns:**
java.lang.String - The format code applied to a data label.
### setFormatCode(String value) {#setFormatCode-java.lang.String-}
```
public void setFormatCode(String value)
```


Sets the format code applied to a data label. Number formatting is used to change the way a value appears in data label and can be used in some very creative ways. The examples of number formats:

Number - "\#,\#\#0.00"

Currency - "\\"$\\"\#,\#\#0.00"

Time - "[$-x-systime]h:mm:ss AM/PM"

Date - "d/mm/yyyy"

Percentage - "0.00%"

Fraction - "\# ?/?"

Scientific - "0.00E+00"

Text - "@"

Accounting - "\_-\\"$\\"\* \#,\#\#0.00\_-;-\\"$\\"\* \#,\#\#0.00\_-;\_-\\"$\\"\* \\"-\\"??\_-;\_-@\_-"

Custom with color - "[Red]-\#,\#\#0.0"

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The format code applied to a data label. |

### isLinkedToSource() {#isLinkedToSource--}
```
public boolean isLinkedToSource()
```


Specifies whether the format code is linked to a source cell. Default is true. The NumberFormat will be reset to general if format code is linked to source.

**Returns:**
boolean - The corresponding  boolean  value.
### isLinkedToSource(boolean value) {#isLinkedToSource-boolean-}
```
public void isLinkedToSource(boolean value)
```


Specifies whether the format code is linked to a source cell. Default is true. The NumberFormat will be reset to general if format code is linked to source.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

