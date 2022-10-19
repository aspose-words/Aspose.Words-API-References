---
title: DocSaveOptions
second_title: Aspose.Words for Java API Reference
description: Can be used to specify additional options when saving a document into the  or  format.
type: docs
weight: 119
url: /java/com.aspose.words/docsaveoptions/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.SaveOptions](../../com.aspose.words/saveoptions)
```
public class DocSaveOptions extends SaveOptions
```

Can be used to specify additional options when saving a document into the [SaveFormat.DOC](../../com.aspose.words/saveformat\#DOC) or [SaveFormat.DOT](../../com.aspose.words/saveformat\#DOT) format.

To learn more, visit the **Specify Save Options** documentation article.

At the moment provides only the [getSaveFormat()](../../com.aspose.words/docsaveoptions\#getSaveFormat--) / [setSaveFormat(int)](../../com.aspose.words/docsaveoptions\#setSaveFormat-int-) property, but in the future will have other options added, such as an encryption password or digital signature settings.
## Constructors

| Constructor | Description |
| --- | --- |
| [DocSaveOptions()](#DocSaveOptions--) | Initializes a new instance of this class that can be used to save a document in the [SaveFormat.DOC](../../com.aspose.words/saveformat\#DOC) format. |
| [DocSaveOptions(int saveFormat)](#DocSaveOptions-int-) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [getSaveFormat()](#getSaveFormat--) | Specifies the format in which the document will be saved if this save options object is used. |
| [setSaveFormat(int value)](#setSaveFormat-int-) | Specifies the format in which the document will be saved if this save options object is used. |
| [getPassword()](#getPassword--) | Gets/sets a password to encrypt document using RC4 encryption method. |
| [setPassword(String value)](#setPassword-java.lang.String-) | Gets/sets a password to encrypt document using RC4 encryption method. |
| [getSaveRoutingSlip()](#getSaveRoutingSlip--) | When  false , RoutingSlip data is not saved to output document. |
| [setSaveRoutingSlip(boolean value)](#setSaveRoutingSlip-boolean-) | When  false , RoutingSlip data is not saved to output document. |
| [getAlwaysCompressMetafiles()](#getAlwaysCompressMetafiles--) | When  false , small metafiles are not compressed for performance reason. |
| [setAlwaysCompressMetafiles(boolean value)](#setAlwaysCompressMetafiles-boolean-) | When  false , small metafiles are not compressed for performance reason. |
| [getSavePictureBullet()](#getSavePictureBullet--) | When  false , PictureBullet data is not saved to output document. |
| [setSavePictureBullet(boolean value)](#setSavePictureBullet-boolean-) | When  false , PictureBullet data is not saved to output document. |
### DocSaveOptions() {#DocSaveOptions--}
```
public DocSaveOptions()
```


Initializes a new instance of this class that can be used to save a document in the [SaveFormat.DOC](../../com.aspose.words/saveformat\#DOC) format.

### DocSaveOptions(int saveFormat) {#DocSaveOptions-int-}
```
public DocSaveOptions(int saveFormat)
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


Specifies the format in which the document will be saved if this save options object is used. Can be [SaveFormat.DOC](../../com.aspose.words/saveformat\#DOC) or [SaveFormat.DOT](../../com.aspose.words/saveformat\#DOT).

**Returns:**
int - The corresponding  int  value. The returned value is one of [SaveFormat](../../com.aspose.words/saveformat) constants.
### setSaveFormat(int value) {#setSaveFormat-int-}
```
public void setSaveFormat(int value)
```


Specifies the format in which the document will be saved if this save options object is used. Can be [SaveFormat.DOC](../../com.aspose.words/saveformat\#DOC) or [SaveFormat.DOT](../../com.aspose.words/saveformat\#DOT).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [SaveFormat](../../com.aspose.words/saveformat) constants. |

### getPassword() {#getPassword--}
```
public String getPassword()
```


Gets/sets a password to encrypt document using RC4 encryption method.

In order to save document without encryption this property should be null or empty string.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setPassword(String value) {#setPassword-java.lang.String-}
```
public void setPassword(String value)
```


Gets/sets a password to encrypt document using RC4 encryption method.

In order to save document without encryption this property should be null or empty string.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### getSaveRoutingSlip() {#getSaveRoutingSlip--}
```
public boolean getSaveRoutingSlip()
```


When  false , RoutingSlip data is not saved to output document. Default value is **true**.

**Returns:**
boolean - The corresponding  boolean  value.
### setSaveRoutingSlip(boolean value) {#setSaveRoutingSlip-boolean-}
```
public void setSaveRoutingSlip(boolean value)
```


When  false , RoutingSlip data is not saved to output document. Default value is **true**.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getAlwaysCompressMetafiles() {#getAlwaysCompressMetafiles--}
```
public boolean getAlwaysCompressMetafiles()
```


When  false , small metafiles are not compressed for performance reason. Default value is **true**, all metafiles are compressed regardless of its size.

**Returns:**
boolean - The corresponding  boolean  value.
### setAlwaysCompressMetafiles(boolean value) {#setAlwaysCompressMetafiles-boolean-}
```
public void setAlwaysCompressMetafiles(boolean value)
```


When  false , small metafiles are not compressed for performance reason. Default value is **true**, all metafiles are compressed regardless of its size.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getSavePictureBullet() {#getSavePictureBullet--}
```
public boolean getSavePictureBullet()
```


When  false , PictureBullet data is not saved to output document. Default value is **true**.

This option is provided for Word 97, which cannot work correctly with PictureBullet data. To remove PictureBullet data, set the option to "false".

**Returns:**
boolean - The corresponding  boolean  value.
### setSavePictureBullet(boolean value) {#setSavePictureBullet-boolean-}
```
public void setSavePictureBullet(boolean value)
```


When  false , PictureBullet data is not saved to output document. Default value is **true**.

This option is provided for Word 97, which cannot work correctly with PictureBullet data. To remove PictureBullet data, set the option to "false".

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

