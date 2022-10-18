---
title: SdtListItem
second_title: Aspose.Words for Java API Reference
description: This element specifies a single list item within a parent  or  structured document tag.
type: docs
weight: 506
url: /java/com.aspose.words/sdtlistitem/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class SdtListItem implements Cloneable
```

This element specifies a single list item within a parent [SdtType.COMBO\_BOX](../../com.aspose.words/sdttype\#COMBO-BOX) or [SdtType.DROP\_DOWN\_LIST](../../com.aspose.words/sdttype\#DROP-DOWN-LIST) structured document tag.

To learn more, visit the **Structured Document Tags or Content Control** documentation article.
## Constructors

| Constructor | Description |
| --- | --- |
| [SdtListItem(String displayText, String value)](#SdtListItem-java.lang.String-java.lang.String-) | Initializes a new instance of this class. |
| [SdtListItem(String value)](#SdtListItem-java.lang.String-) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [getDisplayText()](#getDisplayText--) | Gets the text to display in the run content in place of the [getValue()](../../com.aspose.words/sdtlistitem\#getValue--) attribute contents for this list item. |
| [getValue()](#getValue--) | Gets the value of this list item. |
### SdtListItem(String displayText, String value) {#SdtListItem-java.lang.String-java.lang.String-}
```
public SdtListItem(String displayText, String value)
```


Initializes a new instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| displayText | java.lang.String |  |
| value | java.lang.String |  |

### SdtListItem(String value) {#SdtListItem-java.lang.String-}
```
public SdtListItem(String value)
```


Initializes a new instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String |  |

### getDisplayText() {#getDisplayText--}
```
public String getDisplayText()
```


Gets the text to display in the run content in place of the [getValue()](../../com.aspose.words/sdtlistitem\#getValue--) attribute contents for this list item.

Cannot be null and cannot be an empty string.

**Returns:**
java.lang.String - The text to display in the run content in place of the [getValue()](../../com.aspose.words/sdtlistitem\#getValue--) attribute contents for this list item.
### getValue() {#getValue--}
```
public String getValue()
```


Gets the value of this list item.

Cannot be null and cannot be an empty string.

**Returns:**
java.lang.String - The value of this list item.
