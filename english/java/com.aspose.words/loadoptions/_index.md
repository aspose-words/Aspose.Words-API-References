---
title: LoadOptions
second_title: Aspose.Words for Java API Reference
description: Allows to specify additional options such as password or base URI when loading a document into a  object.
type: docs
weight: 378
url: /java/com.aspose.words/loadoptions/
---

**Inheritance:**
java.lang.Object
```
public class LoadOptions
```

Allows to specify additional options (such as password or base URI) when loading a document into a [Document](../../com.aspose.words/document) object.

To learn more, visit the **Specify Load Options** documentation article.
## Constructors

| Constructor | Description |
| --- | --- |
| [LoadOptions()](#LoadOptions--) | Initializes a new instance of this class with default values. |
| [LoadOptions(String password)](#LoadOptions-java.lang.String-) | A shortcut to initialize a new instance of this class with the specified password to load an encrypted document. |
| [LoadOptions(int loadFormat, String password, String baseUri)](#LoadOptions-int-java.lang.String-java.lang.String-) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [getLoadFormat()](#getLoadFormat--) | Specifies the format of the document to be loaded. |
| [setLoadFormat(int value)](#setLoadFormat-int-) | Specifies the format of the document to be loaded. |
| [getPassword()](#getPassword--) | Gets the password for opening an encrypted document. |
| [setPassword(String value)](#setPassword-java.lang.String-) | Sets the password for opening an encrypted document. |
| [getBaseUri()](#getBaseUri--) | Gets the string that will be used to resolve relative URIs found in the document into absolute URIs when required. |
| [setBaseUri(String value)](#setBaseUri-java.lang.String-) | Sets the string that will be used to resolve relative URIs found in the document into absolute URIs when required. |
| [getEncoding()](#getEncoding--) | Gets the encoding that will be used to load an HTML, TXT, or CHM document if the encoding is not specified inside the document. |
| [setEncoding(Charset value)](#setEncoding-java.nio.charset.Charset-) | Sets the encoding that will be used to load an HTML, TXT, or CHM document if the encoding is not specified inside the document. |
| [getResourceLoadingCallback()](#getResourceLoadingCallback--) | Allows to control how external resources (images, style sheets) are loaded when a document is imported from HTML, MHTML. |
| [setResourceLoadingCallback(IResourceLoadingCallback value)](#setResourceLoadingCallback-com.aspose.words.IResourceLoadingCallback-) | Allows to control how external resources (images, style sheets) are loaded when a document is imported from HTML, MHTML. |
| [getWarningCallback()](#getWarningCallback--) | Called during a load operation, when an issue is detected that might result in data or formatting fidelity loss. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback-) | Called during a load operation, when an issue is detected that might result in data or formatting fidelity loss. |
| [getProgressCallback()](#getProgressCallback--) | Called during loading a document and accepts data about loading progress. |
| [setProgressCallback(IDocumentLoadingCallback value)](#setProgressCallback-com.aspose.words.IDocumentLoadingCallback-) | Called during loading a document and accepts data about loading progress. |
| [getPreserveIncludePictureField()](#getPreserveIncludePictureField--) | Gets whether to preserve the INCLUDEPICTURE field when reading Microsoft Word formats. |
| [setPreserveIncludePictureField(boolean value)](#setPreserveIncludePictureField-boolean-) | Sets whether to preserve the INCLUDEPICTURE field when reading Microsoft Word formats. |
| [getConvertShapeToOfficeMath()](#getConvertShapeToOfficeMath--) | Gets whether to convert shapes with EquationXML to Office Math objects. |
| [setConvertShapeToOfficeMath(boolean value)](#setConvertShapeToOfficeMath-boolean-) | Sets whether to convert shapes with EquationXML to Office Math objects. |
| [getFontSettings()](#getFontSettings--) | Allows to specify document font settings. |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings-) | Allows to specify document font settings. |
| [getTempFolder()](#getTempFolder--) | Allows to use temporary files when reading document. |
| [setTempFolder(String value)](#setTempFolder-java.lang.String-) | Allows to use temporary files when reading document. |
| [getConvertMetafilesToPng()](#getConvertMetafilesToPng--) | Gets whether to convert metafile ( **F:Aspose.FileFormat.Wmf** or **F:Aspose.FileFormat.Emf**) images to **F:Aspose.FileFormat.Png** image format. |
| [setConvertMetafilesToPng(boolean value)](#setConvertMetafilesToPng-boolean-) | Sets whether to convert metafile ( **F:Aspose.FileFormat.Wmf** or **F:Aspose.FileFormat.Emf**) images to **F:Aspose.FileFormat.Png** image format. |
| [getMswVersion()](#getMswVersion--) | Allows to specify that the document loading process should match a specific MS Word version. |
| [setMswVersion(int value)](#setMswVersion-int-) | Allows to specify that the document loading process should match a specific MS Word version. |
| [getUpdateDirtyFields()](#getUpdateDirtyFields--) | Specifies whether to update the fields with the  dirty  attribute. |
| [setUpdateDirtyFields(boolean value)](#setUpdateDirtyFields-boolean-) | Specifies whether to update the fields with the  dirty  attribute. |
| [getLanguagePreferences()](#getLanguagePreferences--) | Gets language preferences that will be used when document is loading. |
### LoadOptions() {#LoadOptions--}
```
public LoadOptions()
```


Initializes a new instance of this class with default values.

### LoadOptions(String password) {#LoadOptions-java.lang.String-}
```
public LoadOptions(String password)
```


A shortcut to initialize a new instance of this class with the specified password to load an encrypted document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| password | java.lang.String | The password to open an encrypted document. Can be null or empty string. |

### LoadOptions(int loadFormat, String password, String baseUri) {#LoadOptions-int-java.lang.String-java.lang.String-}
```
public LoadOptions(int loadFormat, String password, String baseUri)
```


Initializes a new instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| loadFormat | int |  |
| password | java.lang.String |  |
| baseUri | java.lang.String |  |

### getLoadFormat() {#getLoadFormat--}
```
public int getLoadFormat()
```


Specifies the format of the document to be loaded. Default is [LoadFormat.AUTO](../../com.aspose.words/loadformat\#AUTO).

It is recommended that you specify the [LoadFormat.AUTO](../../com.aspose.words/loadformat\#AUTO) value and let Aspose.Words detect the file format automatically. If you know the format of the document you are about to load, you can specify the format explicitly and this will slightly reduce the loading time by the overhead associated with auto detecting the format. If you specify an explicit load format and it will turn out to be wrong, the auto detection will be invoked and a second attempt to load the file will be made.

**Returns:**
int - The corresponding  int  value. The returned value is one of [LoadFormat](../../com.aspose.words/loadformat) constants.
### setLoadFormat(int value) {#setLoadFormat-int-}
```
public void setLoadFormat(int value)
```


Specifies the format of the document to be loaded. Default is [LoadFormat.AUTO](../../com.aspose.words/loadformat\#AUTO).

It is recommended that you specify the [LoadFormat.AUTO](../../com.aspose.words/loadformat\#AUTO) value and let Aspose.Words detect the file format automatically. If you know the format of the document you are about to load, you can specify the format explicitly and this will slightly reduce the loading time by the overhead associated with auto detecting the format. If you specify an explicit load format and it will turn out to be wrong, the auto detection will be invoked and a second attempt to load the file will be made.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [LoadFormat](../../com.aspose.words/loadformat) constants. |

### getPassword() {#getPassword--}
```
public String getPassword()
```


Gets the password for opening an encrypted document. Can be null or empty string. Default is null.

You need to know the password to open an encrypted document. If the document is not encrypted, set this to null or empty string.

**Returns:**
java.lang.String - The password for opening an encrypted document.
### setPassword(String value) {#setPassword-java.lang.String-}
```
public void setPassword(String value)
```


Sets the password for opening an encrypted document. Can be null or empty string. Default is null.

You need to know the password to open an encrypted document. If the document is not encrypted, set this to null or empty string.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The password for opening an encrypted document. |

### getBaseUri() {#getBaseUri--}
```
public String getBaseUri()
```


Gets the string that will be used to resolve relative URIs found in the document into absolute URIs when required. Can be null or empty string. Default is null.

This property is used to resolve relative URIs into absolute in the following cases:

1.  When loading an HTML document from a stream and the document contains images with relative URIs and does not have a base URI specified in the BASE HTML element.
2.  When saving a document to PDF and other formats, to retrieve images linked using relative URIs so the images can be saved into the output document.

**Returns:**
java.lang.String - The string that will be used to resolve relative URIs found in the document into absolute URIs when required.
### setBaseUri(String value) {#setBaseUri-java.lang.String-}
```
public void setBaseUri(String value)
```


Sets the string that will be used to resolve relative URIs found in the document into absolute URIs when required. Can be null or empty string. Default is null.

This property is used to resolve relative URIs into absolute in the following cases:

1.  When loading an HTML document from a stream and the document contains images with relative URIs and does not have a base URI specified in the BASE HTML element.
2.  When saving a document to PDF and other formats, to retrieve images linked using relative URIs so the images can be saved into the output document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The string that will be used to resolve relative URIs found in the document into absolute URIs when required. |

### getEncoding() {#getEncoding--}
```
public Charset getEncoding()
```


Gets the encoding that will be used to load an HTML, TXT, or CHM document if the encoding is not specified inside the document. Can be null. Default is null.

This property is used only when loading HTML, TXT, or CHM documents.

If encoding is not specified inside the document and this property is  null , then the system will try to automatically detect the encoding.

**Returns:**
java.nio.charset.Charset - The encoding that will be used to load an HTML, TXT, or CHM document if the encoding is not specified inside the document.
### setEncoding(Charset value) {#setEncoding-java.nio.charset.Charset-}
```
public void setEncoding(Charset value)
```


Sets the encoding that will be used to load an HTML, TXT, or CHM document if the encoding is not specified inside the document. Can be null. Default is null.

This property is used only when loading HTML, TXT, or CHM documents.

If encoding is not specified inside the document and this property is  null , then the system will try to automatically detect the encoding.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.nio.charset.Charset | The encoding that will be used to load an HTML, TXT, or CHM document if the encoding is not specified inside the document. |

### getResourceLoadingCallback() {#getResourceLoadingCallback--}
```
public IResourceLoadingCallback getResourceLoadingCallback()
```


Allows to control how external resources (images, style sheets) are loaded when a document is imported from HTML, MHTML.

**Returns:**
[IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback) - The corresponding [IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback) value.
### setResourceLoadingCallback(IResourceLoadingCallback value) {#setResourceLoadingCallback-com.aspose.words.IResourceLoadingCallback-}
```
public void setResourceLoadingCallback(IResourceLoadingCallback value)
```


Allows to control how external resources (images, style sheets) are loaded when a document is imported from HTML, MHTML.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback) | The corresponding [IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback) value. |

### getWarningCallback() {#getWarningCallback--}
```
public IWarningCallback getWarningCallback()
```


Called during a load operation, when an issue is detected that might result in data or formatting fidelity loss.

**Returns:**
[IWarningCallback](../../com.aspose.words/iwarningcallback) - The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback) value.
### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback-}
```
public void setWarningCallback(IWarningCallback value)
```


Called during a load operation, when an issue is detected that might result in data or formatting fidelity loss.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback) | The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback) value. |

### getProgressCallback() {#getProgressCallback--}
```
public IDocumentLoadingCallback getProgressCallback()
```


Called during loading a document and accepts data about loading progress.

[LoadFormat.DOCX](../../com.aspose.words/loadformat\#DOCX), [LoadFormat.FLAT\_OPC](../../com.aspose.words/loadformat\#FLAT-OPC), [LoadFormat.DOCM](../../com.aspose.words/loadformat\#DOCM), [LoadFormat.DOTM](../../com.aspose.words/loadformat\#DOTM), [LoadFormat.DOTX](../../com.aspose.words/loadformat\#DOTX), [LoadFormat.MARKDOWN](../../com.aspose.words/loadformat\#MARKDOWN), [LoadFormat.RTF](../../com.aspose.words/loadformat\#RTF), [LoadFormat.WORD\_ML](../../com.aspose.words/loadformat\#WORD-ML), [LoadFormat.DOC](../../com.aspose.words/loadformat\#DOC), [LoadFormat.DOT](../../com.aspose.words/loadformat\#DOT), [LoadFormat.ODT](../../com.aspose.words/loadformat\#ODT), [LoadFormat.OTT](../../com.aspose.words/loadformat\#OTT) formats supported.

**Returns:**
[IDocumentLoadingCallback](../../com.aspose.words/idocumentloadingcallback) - The corresponding [IDocumentLoadingCallback](../../com.aspose.words/idocumentloadingcallback) value.
### setProgressCallback(IDocumentLoadingCallback value) {#setProgressCallback-com.aspose.words.IDocumentLoadingCallback-}
```
public void setProgressCallback(IDocumentLoadingCallback value)
```


Called during loading a document and accepts data about loading progress.

[LoadFormat.DOCX](../../com.aspose.words/loadformat\#DOCX), [LoadFormat.FLAT\_OPC](../../com.aspose.words/loadformat\#FLAT-OPC), [LoadFormat.DOCM](../../com.aspose.words/loadformat\#DOCM), [LoadFormat.DOTM](../../com.aspose.words/loadformat\#DOTM), [LoadFormat.DOTX](../../com.aspose.words/loadformat\#DOTX), [LoadFormat.MARKDOWN](../../com.aspose.words/loadformat\#MARKDOWN), [LoadFormat.RTF](../../com.aspose.words/loadformat\#RTF), [LoadFormat.WORD\_ML](../../com.aspose.words/loadformat\#WORD-ML), [LoadFormat.DOC](../../com.aspose.words/loadformat\#DOC), [LoadFormat.DOT](../../com.aspose.words/loadformat\#DOT), [LoadFormat.ODT](../../com.aspose.words/loadformat\#ODT), [LoadFormat.OTT](../../com.aspose.words/loadformat\#OTT) formats supported.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IDocumentLoadingCallback](../../com.aspose.words/idocumentloadingcallback) | The corresponding [IDocumentLoadingCallback](../../com.aspose.words/idocumentloadingcallback) value. |

### getPreserveIncludePictureField() {#getPreserveIncludePictureField--}
```
public boolean getPreserveIncludePictureField()
```


Gets whether to preserve the INCLUDEPICTURE field when reading Microsoft Word formats. The default value is false.

By default, the INCLUDEPICTURE field is converted into a shape object. You can override that if you need the field to be preserved, for example, if you wish to update it programmatically. Note however that this approach is not common for Aspose.Words. Use it on your own risk.

One of the possible use cases may be using a MERGEFIELD as a child field to dynamically change the source path of the picture. In this case you need the INCLUDEPICTURE to be preserved in the model.

**Returns:**
boolean - Whether to preserve the INCLUDEPICTURE field when reading Microsoft Word formats.
### setPreserveIncludePictureField(boolean value) {#setPreserveIncludePictureField-boolean-}
```
public void setPreserveIncludePictureField(boolean value)
```


Sets whether to preserve the INCLUDEPICTURE field when reading Microsoft Word formats. The default value is false.

By default, the INCLUDEPICTURE field is converted into a shape object. You can override that if you need the field to be preserved, for example, if you wish to update it programmatically. Note however that this approach is not common for Aspose.Words. Use it on your own risk.

One of the possible use cases may be using a MERGEFIELD as a child field to dynamically change the source path of the picture. In this case you need the INCLUDEPICTURE to be preserved in the model.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to preserve the INCLUDEPICTURE field when reading Microsoft Word formats. |

### getConvertShapeToOfficeMath() {#getConvertShapeToOfficeMath--}
```
public boolean getConvertShapeToOfficeMath()
```


Gets whether to convert shapes with EquationXML to Office Math objects.

**Returns:**
boolean - Whether to convert shapes with EquationXML to Office Math objects.
### setConvertShapeToOfficeMath(boolean value) {#setConvertShapeToOfficeMath-boolean-}
```
public void setConvertShapeToOfficeMath(boolean value)
```


Sets whether to convert shapes with EquationXML to Office Math objects.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to convert shapes with EquationXML to Office Math objects. |

### getFontSettings() {#getFontSettings--}
```
public FontSettings getFontSettings()
```


Allows to specify document font settings.

When loading some formats, Aspose.Words may require to resolve the fonts. For example, when loading HTML documents Aspose.Words may resolve the fonts to perform font fallback.

If set to null, default static font settings [FontSettings.getDefaultInstance()](../../com.aspose.words/fontsettings\#getDefaultInstance--) will be used.

The default value is null.

**Returns:**
[FontSettings](../../com.aspose.words/fontsettings) - The corresponding [FontSettings](../../com.aspose.words/fontsettings) value.
### setFontSettings(FontSettings value) {#setFontSettings-com.aspose.words.FontSettings-}
```
public void setFontSettings(FontSettings value)
```


Allows to specify document font settings.

When loading some formats, Aspose.Words may require to resolve the fonts. For example, when loading HTML documents Aspose.Words may resolve the fonts to perform font fallback.

If set to null, default static font settings [FontSettings.getDefaultInstance()](../../com.aspose.words/fontsettings\#getDefaultInstance--) will be used.

The default value is null.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [FontSettings](../../com.aspose.words/fontsettings) | The corresponding [FontSettings](../../com.aspose.words/fontsettings) value. |

### getTempFolder() {#getTempFolder--}
```
public String getTempFolder()
```


Allows to use temporary files when reading document. By default this property is  null  and no temporary files are used.

The folder must exist and be writable, otherwise an exception will be thrown.

Aspose.Words automatically deletes all temporary files when reading is complete.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setTempFolder(String value) {#setTempFolder-java.lang.String-}
```
public void setTempFolder(String value)
```


Allows to use temporary files when reading document. By default this property is  null  and no temporary files are used.

The folder must exist and be writable, otherwise an exception will be thrown.

Aspose.Words automatically deletes all temporary files when reading is complete.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### getConvertMetafilesToPng() {#getConvertMetafilesToPng--}
```
public boolean getConvertMetafilesToPng()
```


Gets whether to convert metafile ( **F:Aspose.FileFormat.Wmf** or **F:Aspose.FileFormat.Emf**) images to **F:Aspose.FileFormat.Png** image format. Metafiles ( **F:Aspose.FileFormat.Wmf** or **F:Aspose.FileFormat.Emf**) is an uncompressed image format and sometimes requires to much RAM to hold and process document. This option allows to convert all metafile images to **F:Aspose.FileFormat.Png** on document loading. Please note - conversion vector graphics to raster decreases quality of the images.

**Returns:**
boolean - Whether to convert metafile ( **F:Aspose.FileFormat.Wmf** or **F:Aspose.FileFormat.Emf**) images to **F:Aspose.FileFormat.Png** image format.
### setConvertMetafilesToPng(boolean value) {#setConvertMetafilesToPng-boolean-}
```
public void setConvertMetafilesToPng(boolean value)
```


Sets whether to convert metafile ( **F:Aspose.FileFormat.Wmf** or **F:Aspose.FileFormat.Emf**) images to **F:Aspose.FileFormat.Png** image format. Metafiles ( **F:Aspose.FileFormat.Wmf** or **F:Aspose.FileFormat.Emf**) is an uncompressed image format and sometimes requires to much RAM to hold and process document. This option allows to convert all metafile images to **F:Aspose.FileFormat.Png** on document loading. Please note - conversion vector graphics to raster decreases quality of the images.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to convert metafile ( **F:Aspose.FileFormat.Wmf** or **F:Aspose.FileFormat.Emf**) images to **F:Aspose.FileFormat.Png** image format. |

### getMswVersion() {#getMswVersion--}
```
public int getMswVersion()
```


Allows to specify that the document loading process should match a specific MS Word version. Default value is [MsWordVersion.WORD\_2019](../../com.aspose.words/mswordversion\#WORD-2019) Different Word versions may handle certain aspects of document content and formatting slightly differently during the loading process, which may result in minor differences in Document Object Model.

**Returns:**
int - The corresponding  int  value. The returned value is one of [MsWordVersion](../../com.aspose.words/mswordversion) constants.
### setMswVersion(int value) {#setMswVersion-int-}
```
public void setMswVersion(int value)
```


Allows to specify that the document loading process should match a specific MS Word version. Default value is [MsWordVersion.WORD\_2019](../../com.aspose.words/mswordversion\#WORD-2019) Different Word versions may handle certain aspects of document content and formatting slightly differently during the loading process, which may result in minor differences in Document Object Model.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [MsWordVersion](../../com.aspose.words/mswordversion) constants. |

### getUpdateDirtyFields() {#getUpdateDirtyFields--}
```
public boolean getUpdateDirtyFields()
```


Specifies whether to update the fields with the  dirty  attribute.

**Returns:**
boolean - The corresponding  boolean  value.
### setUpdateDirtyFields(boolean value) {#setUpdateDirtyFields-boolean-}
```
public void setUpdateDirtyFields(boolean value)
```


Specifies whether to update the fields with the  dirty  attribute.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getLanguagePreferences() {#getLanguagePreferences--}
```
public LanguagePreferences getLanguagePreferences()
```


Gets language preferences that will be used when document is loading.

**Returns:**
[LanguagePreferences](../../com.aspose.words/languagepreferences) - Language preferences that will be used when document is loading.