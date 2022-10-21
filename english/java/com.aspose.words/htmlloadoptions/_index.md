---
title: HtmlLoadOptions
second_title: Aspose.Words for Java API Reference
description: Allows to specify additional options when loading HTML document into a  object.
type: docs
weight: 328
url: /java/com.aspose.words/htmlloadoptions/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.LoadOptions](../../com.aspose.words/loadoptions)
```
public class HtmlLoadOptions extends LoadOptions
```

Allows to specify additional options when loading HTML document into a [Document](../../com.aspose.words/document) object.

To learn more, visit the **Specify Load Options** documentation article.
## Constructors

| Constructor | Description |
| --- | --- |
| [HtmlLoadOptions()](#HtmlLoadOptions--) | Initializes a new instance of this class with default values. |
| [HtmlLoadOptions(String password)](#HtmlLoadOptions-java.lang.String-) | A shortcut to initialize a new instance of this class with the specified password to load an encrypted document. |
| [HtmlLoadOptions(int loadFormat, String password, String baseUri)](#HtmlLoadOptions-int-java.lang.String-java.lang.String-) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [getSupportVml()](#getSupportVml--) | Gets a value indicating whether to support VML images. |
| [setSupportVml(boolean value)](#setSupportVml-boolean-) | Sets a value indicating whether to support VML images. |
| [getWebRequestTimeout()](#getWebRequestTimeout--) | The number of milliseconds to wait before the web request times out. |
| [setWebRequestTimeout(int value)](#setWebRequestTimeout-int-) | The number of milliseconds to wait before the web request times out. |
| [getPreferredControlType()](#getPreferredControlType--) | Gets preferred type of document nodes that will represent imported  and  elements. |
| [setPreferredControlType(int value)](#setPreferredControlType-int-) | Sets preferred type of document nodes that will represent imported  and  elements. |
| [getIgnoreNoscriptElements()](#getIgnoreNoscriptElements--) | Gets a value indicating whether to ignore  HTML elements. |
| [setIgnoreNoscriptElements(boolean value)](#setIgnoreNoscriptElements-boolean-) | Sets a value indicating whether to ignore  HTML elements. |
| [getConvertSvgToEmf()](#getConvertSvgToEmf--) | Gets a value indicating whether to convert loaded SVG images to the EMF format. |
| [setConvertSvgToEmf(boolean value)](#setConvertSvgToEmf-boolean-) | Sets a value indicating whether to convert loaded SVG images to the EMF format. |
| [getBlockImportMode()](#getBlockImportMode--) | Gets a value that specifies how properties of block-level elements are imported. |
| [setBlockImportMode(int value)](#setBlockImportMode-int-) | Sets a value that specifies how properties of block-level elements are imported. |
### HtmlLoadOptions() {#HtmlLoadOptions--}
```
public HtmlLoadOptions()
```


Initializes a new instance of this class with default values.

### HtmlLoadOptions(String password) {#HtmlLoadOptions-java.lang.String-}
```
public HtmlLoadOptions(String password)
```


A shortcut to initialize a new instance of this class with the specified password to load an encrypted document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| password | java.lang.String | The password to open an encrypted document. Can be null or empty string. |

### HtmlLoadOptions(int loadFormat, String password, String baseUri) {#HtmlLoadOptions-int-java.lang.String-java.lang.String-}
```
public HtmlLoadOptions(int loadFormat, String password, String baseUri)
```


Initializes a new instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| loadFormat | int |  |
| password | java.lang.String |  |
| baseUri | java.lang.String |  |

### getSupportVml() {#getSupportVml--}
```
public boolean getSupportVml()
```


Gets a value indicating whether to support VML images.

**Returns:**
boolean - A value indicating whether to support VML images.
### setSupportVml(boolean value) {#setSupportVml-boolean-}
```
public void setSupportVml(boolean value)
```


Sets a value indicating whether to support VML images.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value indicating whether to support VML images. |

### getWebRequestTimeout() {#getWebRequestTimeout--}
```
public int getWebRequestTimeout()
```


The number of milliseconds to wait before the web request times out. The default value is 100000 milliseconds (100 seconds). The number of milliseconds that Aspose.Words waits for a response, when loading external resources (images, style sheets) linked in HTML and MHTML documents.

**Returns:**
int - The corresponding  int  value.
### setWebRequestTimeout(int value) {#setWebRequestTimeout-int-}
```
public void setWebRequestTimeout(int value)
```


The number of milliseconds to wait before the web request times out. The default value is 100000 milliseconds (100 seconds). The number of milliseconds that Aspose.Words waits for a response, when loading external resources (images, style sheets) linked in HTML and MHTML documents.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### getPreferredControlType() {#getPreferredControlType--}
```
public int getPreferredControlType()
```


Gets preferred type of document nodes that will represent imported  and  elements. Default value is [HtmlControlType.FORM\_FIELD](../../com.aspose.words/htmlcontroltype\#FORM-FIELD). Please note that setting this property does not guarantee that all imported controls will be of the specified type. If an HTML control is not representable with document nodes of the preferred type, Aspose.Words will use a compatible [HtmlControlType](../../com.aspose.words/htmlcontroltype) for that control.

**Returns:**
int - Preferred type of document nodes that will represent imported  and  elements. The returned value is one of [HtmlControlType](../../com.aspose.words/htmlcontroltype) constants.
### setPreferredControlType(int value) {#setPreferredControlType-int-}
```
public void setPreferredControlType(int value)
```


Sets preferred type of document nodes that will represent imported  and  elements. Default value is [HtmlControlType.FORM\_FIELD](../../com.aspose.words/htmlcontroltype\#FORM-FIELD). Please note that setting this property does not guarantee that all imported controls will be of the specified type. If an HTML control is not representable with document nodes of the preferred type, Aspose.Words will use a compatible [HtmlControlType](../../com.aspose.words/htmlcontroltype) for that control.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | Preferred type of document nodes that will represent imported  and  elements. The value must be one of [HtmlControlType](../../com.aspose.words/htmlcontroltype) constants. |

### getIgnoreNoscriptElements() {#getIgnoreNoscriptElements--}
```
public boolean getIgnoreNoscriptElements()
```


Gets a value indicating whether to ignore  HTML elements. Default value is  false . Like MS Word, Aspose.Words does not support scripts and by default loads content of  elements into the resulting document. In most browsers, however, scripts are supported and content from  is not visible. Setting this property to  true  forces Aspose.Words to ignore all  elements and helps to produce documents that look closer to what is seen in browsers.

**Returns:**
boolean - A value indicating whether to ignore  HTML elements.
### setIgnoreNoscriptElements(boolean value) {#setIgnoreNoscriptElements-boolean-}
```
public void setIgnoreNoscriptElements(boolean value)
```


Sets a value indicating whether to ignore  HTML elements. Default value is  false . Like MS Word, Aspose.Words does not support scripts and by default loads content of  elements into the resulting document. In most browsers, however, scripts are supported and content from  is not visible. Setting this property to  true  forces Aspose.Words to ignore all  elements and helps to produce documents that look closer to what is seen in browsers.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value indicating whether to ignore  HTML elements. |

### getConvertSvgToEmf() {#getConvertSvgToEmf--}
```
public boolean getConvertSvgToEmf()
```


Gets a value indicating whether to convert loaded SVG images to the EMF format. Default value is  false  and, if possible, loaded SVG images are stored as is without conversion.

Newer versions of MS Word support SVG images natively. If the MS Word version specified in load options supports SVG, Aspose.Words will store SVG images as is without conversion. If SVG is not supported, loaded SVG images will be converted to the EMF format.

If, however, this option is set to  true , Aspose.Words will convert loaded SVG images to EMF even if SVG images are supported by the specified version of MS Word.

**Returns:**
boolean - A value indicating whether to convert loaded SVG images to the EMF format.
### setConvertSvgToEmf(boolean value) {#setConvertSvgToEmf-boolean-}
```
public void setConvertSvgToEmf(boolean value)
```


Sets a value indicating whether to convert loaded SVG images to the EMF format. Default value is  false  and, if possible, loaded SVG images are stored as is without conversion.

Newer versions of MS Word support SVG images natively. If the MS Word version specified in load options supports SVG, Aspose.Words will store SVG images as is without conversion. If SVG is not supported, loaded SVG images will be converted to the EMF format.

If, however, this option is set to  true , Aspose.Words will convert loaded SVG images to EMF even if SVG images are supported by the specified version of MS Word.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value indicating whether to convert loaded SVG images to the EMF format. |

### getBlockImportMode() {#getBlockImportMode--}
```
public int getBlockImportMode()
```


Gets a value that specifies how properties of block-level elements are imported. Default value is [BlockImportMode.MERGE](../../com.aspose.words/blockimportmode\#MERGE).

**Returns:**
int - A value that specifies how properties of block-level elements are imported. The returned value is one of [BlockImportMode](../../com.aspose.words/blockimportmode) constants.
### setBlockImportMode(int value) {#setBlockImportMode-int-}
```
public void setBlockImportMode(int value)
```


Sets a value that specifies how properties of block-level elements are imported. Default value is [BlockImportMode.MERGE](../../com.aspose.words/blockimportmode\#MERGE).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value that specifies how properties of block-level elements are imported. The value must be one of [BlockImportMode](../../com.aspose.words/blockimportmode) constants. |

