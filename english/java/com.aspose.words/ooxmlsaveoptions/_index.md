---
title: OoxmlSaveOptions
second_title: Aspose.Words for Java API Reference
description: Can be used to specify additional options when saving a document into the     or  format.
type: docs
weight: 428
url: /java/com.aspose.words/ooxmlsaveoptions/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.SaveOptions](../../com.aspose.words/saveoptions)
```
public class OoxmlSaveOptions extends SaveOptions
```

Can be used to specify additional options when saving a document into the [SaveFormat.DOCX](../../com.aspose.words/saveformat\#DOCX), [SaveFormat.DOCM](../../com.aspose.words/saveformat\#DOCM), [SaveFormat.DOTX](../../com.aspose.words/saveformat\#DOTX), [SaveFormat.DOTM](../../com.aspose.words/saveformat\#DOTM) or [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat\#FLAT-OPC) format.

To learn more, visit the **Specify Save Options** documentation article.
## Constructors

| Constructor | Description |
| --- | --- |
| [OoxmlSaveOptions()](#OoxmlSaveOptions--) | Initializes a new instance of this class that can be used to save a document in the [SaveFormat.DOCX](../../com.aspose.words/saveformat\#DOCX) format. |
| [OoxmlSaveOptions(int saveFormat)](#OoxmlSaveOptions-int-) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [getSaveFormat()](#getSaveFormat--) | Specifies the format in which the document will be saved if this save options object is used. |
| [setSaveFormat(int value)](#setSaveFormat-int-) | Specifies the format in which the document will be saved if this save options object is used. |
| [getPassword()](#getPassword--) | Gets/sets a password to encrypt document using ECMA376 Standard encryption algorithm. |
| [setPassword(String value)](#setPassword-java.lang.String-) | Gets/sets a password to encrypt document using ECMA376 Standard encryption algorithm. |
| [getCompliance()](#getCompliance--) | Specifies the OOXML version for the output document. |
| [setCompliance(int value)](#setCompliance-int-) | Specifies the OOXML version for the output document. |
| [getKeepLegacyControlChars()](#getKeepLegacyControlChars--) | Keeps original representation of legacy control characters. |
| [setKeepLegacyControlChars(boolean value)](#setKeepLegacyControlChars-boolean-) | Keeps original representation of legacy control characters. |
| [getCompressionLevel()](#getCompressionLevel--) | Specifies the compression level used to save document. |
| [setCompressionLevel(int value)](#setCompressionLevel-int-) | Specifies the compression level used to save document. |
### OoxmlSaveOptions() {#OoxmlSaveOptions--}
```
public OoxmlSaveOptions()
```


Initializes a new instance of this class that can be used to save a document in the [SaveFormat.DOCX](../../com.aspose.words/saveformat\#DOCX) format.

### OoxmlSaveOptions(int saveFormat) {#OoxmlSaveOptions-int-}
```
public OoxmlSaveOptions(int saveFormat)
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


Specifies the format in which the document will be saved if this save options object is used. Can be [SaveFormat.DOCX](../../com.aspose.words/saveformat\#DOCX), [SaveFormat.DOCM](../../com.aspose.words/saveformat\#DOCM), [SaveFormat.DOTX](../../com.aspose.words/saveformat\#DOTX), [SaveFormat.DOTM](../../com.aspose.words/saveformat\#DOTM) or [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat\#FLAT-OPC).

**Returns:**
int - The corresponding  int  value. The returned value is one of [SaveFormat](../../com.aspose.words/saveformat) constants.
### setSaveFormat(int value) {#setSaveFormat-int-}
```
public void setSaveFormat(int value)
```


Specifies the format in which the document will be saved if this save options object is used. Can be [SaveFormat.DOCX](../../com.aspose.words/saveformat\#DOCX), [SaveFormat.DOCM](../../com.aspose.words/saveformat\#DOCM), [SaveFormat.DOTX](../../com.aspose.words/saveformat\#DOTX), [SaveFormat.DOTM](../../com.aspose.words/saveformat\#DOTM) or [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat\#FLAT-OPC).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [SaveFormat](../../com.aspose.words/saveformat) constants. |

### getPassword() {#getPassword--}
```
public String getPassword()
```


Gets/sets a password to encrypt document using ECMA376 Standard encryption algorithm.

In order to save document without encryption this property should be null or empty string.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setPassword(String value) {#setPassword-java.lang.String-}
```
public void setPassword(String value)
```


Gets/sets a password to encrypt document using ECMA376 Standard encryption algorithm.

In order to save document without encryption this property should be null or empty string.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### getCompliance() {#getCompliance--}
```
public int getCompliance()
```


Specifies the OOXML version for the output document. The default value is [OoxmlCompliance.ECMA\_376\_2006](../../com.aspose.words/ooxmlcompliance\#ECMA-376-2006).

**Returns:**
int - The corresponding  int  value. The returned value is one of [OoxmlCompliance](../../com.aspose.words/ooxmlcompliance) constants.
### setCompliance(int value) {#setCompliance-int-}
```
public void setCompliance(int value)
```


Specifies the OOXML version for the output document. The default value is [OoxmlCompliance.ECMA\_376\_2006](../../com.aspose.words/ooxmlcompliance\#ECMA-376-2006).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [OoxmlCompliance](../../com.aspose.words/ooxmlcompliance) constants. |

### getKeepLegacyControlChars() {#getKeepLegacyControlChars--}
```
public boolean getKeepLegacyControlChars()
```


Keeps original representation of legacy control characters.

**Returns:**
boolean - The corresponding  boolean  value.
### setKeepLegacyControlChars(boolean value) {#setKeepLegacyControlChars-boolean-}
```
public void setKeepLegacyControlChars(boolean value)
```


Keeps original representation of legacy control characters.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getCompressionLevel() {#getCompressionLevel--}
```
public int getCompressionLevel()
```


Specifies the compression level used to save document. The default value is [CompressionLevel.NORMAL](../../com.aspose.words/compressionlevel\#NORMAL).

**Returns:**
int - The corresponding  int  value. The returned value is one of [CompressionLevel](../../com.aspose.words/compressionlevel) constants.
### setCompressionLevel(int value) {#setCompressionLevel-int-}
```
public void setCompressionLevel(int value)
```


Specifies the compression level used to save document. The default value is [CompressionLevel.NORMAL](../../com.aspose.words/compressionlevel\#NORMAL).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [CompressionLevel](../../com.aspose.words/compressionlevel) constants. |

