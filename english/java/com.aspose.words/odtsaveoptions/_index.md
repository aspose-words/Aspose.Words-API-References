---
title: OdtSaveOptions
second_title: Aspose.Words for Java API Reference
description: Can be used to specify additional options when saving a document into the  or  format.
type: docs
weight: 419
url: /java/com.aspose.words/odtsaveoptions/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.SaveOptions](../../com.aspose.words/saveoptions)
```
public class OdtSaveOptions extends SaveOptions
```

Can be used to specify additional options when saving a document into the [SaveFormat.ODT](../../com.aspose.words/saveformat\#ODT) or [SaveFormat.OTT](../../com.aspose.words/saveformat\#OTT) format.

To learn more, visit the **Specify Save Options** documentation article.

At the moment provides only the [getSaveFormat()](../../com.aspose.words/odtsaveoptions\#getSaveFormat--) / [setSaveFormat(int)](../../com.aspose.words/odtsaveoptions\#setSaveFormat-int-) property, but in the future will have other options added, such as an encryption password or digital signature settings.
## Constructors

| Constructor | Description |
| --- | --- |
| [OdtSaveOptions()](#OdtSaveOptions--) | Initializes a new instance of this class that can be used to save a document in the [SaveFormat.ODT](../../com.aspose.words/saveformat\#ODT) format. |
| [OdtSaveOptions(String password)](#OdtSaveOptions-java.lang.String-) | Initializes a new instance of this class that can be used to save a document in the [SaveFormat.ODT](../../com.aspose.words/saveformat\#ODT) format encrypted with a password. |
| [OdtSaveOptions(int saveFormat)](#OdtSaveOptions-int-) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [getSaveFormat()](#getSaveFormat--) | Specifies the format in which the document will be saved if this save options object is used. |
| [setSaveFormat(int value)](#setSaveFormat-int-) | Specifies the format in which the document will be saved if this save options object is used. |
| [isStrictSchema11()](#isStrictSchema11--) | Specifies whether export should correspond to ODT specification 1.1 strictly. |
| [isStrictSchema11(boolean value)](#isStrictSchema11-boolean-) | Specifies whether export should correspond to ODT specification 1.1 strictly. |
| [getMeasureUnit()](#getMeasureUnit--) | Allows to specify units of measure to apply to document content. |
| [setMeasureUnit(int value)](#setMeasureUnit-int-) | Allows to specify units of measure to apply to document content. |
| [getPassword()](#getPassword--) | Gets a password to encrypt document. |
| [setPassword(String value)](#setPassword-java.lang.String-) | Sets a password to encrypt document. |
### OdtSaveOptions() {#OdtSaveOptions--}
```
public OdtSaveOptions()
```


Initializes a new instance of this class that can be used to save a document in the [SaveFormat.ODT](../../com.aspose.words/saveformat\#ODT) format.

### OdtSaveOptions(String password) {#OdtSaveOptions-java.lang.String-}
```
public OdtSaveOptions(String password)
```


Initializes a new instance of this class that can be used to save a document in the [SaveFormat.ODT](../../com.aspose.words/saveformat\#ODT) format encrypted with a password.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| password | java.lang.String |  |

### OdtSaveOptions(int saveFormat) {#OdtSaveOptions-int-}
```
public OdtSaveOptions(int saveFormat)
```


Initializes a new instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| saveFormat | int |  |

### getSaveFormat() {#getSaveFormat--}
```
public int getSaveFormat()
```


Specifies the format in which the document will be saved if this save options object is used. Can be [SaveFormat.ODT](../../com.aspose.words/saveformat\#ODT) or [SaveFormat.OTT](../../com.aspose.words/saveformat\#OTT).

**Returns:**
int - The corresponding  int  value. The returned value is one of [SaveFormat](../../com.aspose.words/saveformat) constants.
### setSaveFormat(int value) {#setSaveFormat-int-}
```
public void setSaveFormat(int value)
```


Specifies the format in which the document will be saved if this save options object is used. Can be [SaveFormat.ODT](../../com.aspose.words/saveformat\#ODT) or [SaveFormat.OTT](../../com.aspose.words/saveformat\#OTT).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [SaveFormat](../../com.aspose.words/saveformat) constants. |

### isStrictSchema11() {#isStrictSchema11--}
```
public boolean isStrictSchema11()
```


Specifies whether export should correspond to ODT specification 1.1 strictly. OOo 3.0 displays files correctly when they contain elements and attributes of ODT 1.2. Use "false" for this purpose, or "true" for strict conformity of specification 1.1. The default value is **false**.

**Returns:**
boolean - The corresponding  boolean  value.
### isStrictSchema11(boolean value) {#isStrictSchema11-boolean-}
```
public void isStrictSchema11(boolean value)
```


Specifies whether export should correspond to ODT specification 1.1 strictly. OOo 3.0 displays files correctly when they contain elements and attributes of ODT 1.2. Use "false" for this purpose, or "true" for strict conformity of specification 1.1. The default value is **false**.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getMeasureUnit() {#getMeasureUnit--}
```
public int getMeasureUnit()
```


Allows to specify units of measure to apply to document content. The default value is [OdtSaveMeasureUnit.CENTIMETERS](../../com.aspose.words/odtsavemeasureunit\#CENTIMETERS) Open Office uses centimeters when specifying lengths, widths and other measurable formatting and content properties in documents whereas MS Office uses inches.

**Returns:**
int - The corresponding  int  value. The returned value is one of [OdtSaveMeasureUnit](../../com.aspose.words/odtsavemeasureunit) constants.
### setMeasureUnit(int value) {#setMeasureUnit-int-}
```
public void setMeasureUnit(int value)
```


Allows to specify units of measure to apply to document content. The default value is [OdtSaveMeasureUnit.CENTIMETERS](../../com.aspose.words/odtsavemeasureunit\#CENTIMETERS) Open Office uses centimeters when specifying lengths, widths and other measurable formatting and content properties in documents whereas MS Office uses inches.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [OdtSaveMeasureUnit](../../com.aspose.words/odtsavemeasureunit) constants. |

### getPassword() {#getPassword--}
```
public String getPassword()
```


Gets a password to encrypt document.

In order to save document without encryption this property should be null or empty string.

**Returns:**
java.lang.String - A password to encrypt document.
### setPassword(String value) {#setPassword-java.lang.String-}
```
public void setPassword(String value)
```


Sets a password to encrypt document.

In order to save document without encryption this property should be null or empty string.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | A password to encrypt document. |

