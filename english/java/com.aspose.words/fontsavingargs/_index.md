---
title: FontSavingArgs
second_title: Aspose.Words for Java API Reference
description: Provides data for the  event.
type: docs
weight: 285
url: /java/com.aspose.words/fontsavingargs/
---

**Inheritance:**
java.lang.Object
```
public class FontSavingArgs
```

Provides data for the [IFontSavingCallback.fontSaving(com.aspose.words.FontSavingArgs)](../../com.aspose.words/ifontsavingcallback\#fontSaving-com.aspose.words.FontSavingArgs-) event.

To learn more, visit the **Save a Document** documentation article.

When Aspose.Words saves a document to HTML or related formats and [HtmlSaveOptions.getExportFontResources()](../../com.aspose.words/htmlsaveoptions\#getExportFontResources--) / [HtmlSaveOptions.setExportFontResources(boolean)](../../com.aspose.words/htmlsaveoptions\#setExportFontResources-boolean-) is set to **true**, it saves each font subject for export into a separate file.

[FontSavingArgs](../../com.aspose.words/fontsavingargs) controls whether particular font resource should be exported and how.

[FontSavingArgs](../../com.aspose.words/fontsavingargs) also allows to redefine how font file names are generated or to completely circumvent saving of fonts into files by providing your own stream objects.

To decide whether to save a particular font resource, use the [isExportNeeded()](../../com.aspose.words/fontsavingargs\#isExportNeeded--) / [isExportNeeded(boolean)](../../com.aspose.words/fontsavingargs\#isExportNeeded-boolean-) property.

To save fonts into streams instead of files, use the **P:Aspose.Words.Saving.FontSavingArgs.FontStream** property.
## Methods

| Method | Description |
| --- | --- |
| [getDocument()](#getDocument--) | Gets the document object that is being saved. |
| [getFontFamilyName()](#getFontFamilyName--) | Indicates the current font family name. |
| [getBold()](#getBold--) | Indicates whether the current font is bold. |
| [getItalic()](#getItalic--) | Indicates whether the current font is italic. |
| [getOriginalFileName()](#getOriginalFileName--) | Gets the original font file name with an extension. |
| [getOriginalFileSize()](#getOriginalFileSize--) | Gets the original font file size. |
| [isExportNeeded()](#isExportNeeded--) | Allows to specify whether the current font will be exported as a font resource. |
| [isExportNeeded(boolean value)](#isExportNeeded-boolean-) | Allows to specify whether the current font will be exported as a font resource. |
| [isSubsettingNeeded()](#isSubsettingNeeded--) | Allows to specify whether the current font will be subsetted before exporting as a font resource. |
| [isSubsettingNeeded(boolean value)](#isSubsettingNeeded-boolean-) | Allows to specify whether the current font will be subsetted before exporting as a font resource. |
| [getFontFileName()](#getFontFileName--) | Gets the file name (without path) where the font will be saved to. |
| [setFontFileName(String value)](#setFontFileName-java.lang.String-) | Sets the file name (without path) where the font will be saved to. |
| [getKeepFontStreamOpen()](#getKeepFontStreamOpen--) | Specifies whether Aspose.Words should keep the stream open or close it after saving a font. |
| [setKeepFontStreamOpen(boolean value)](#setKeepFontStreamOpen-boolean-) | Specifies whether Aspose.Words should keep the stream open or close it after saving a font. |
| [getFontStream()](#getFontStream--) |  |
| [setFontStream(OutputStream value)](#setFontStream-java.io.OutputStream-) |  |
### getDocument() {#getDocument--}
```
public Document getDocument()
```


Gets the document object that is being saved.

**Returns:**
[Document](../../com.aspose.words/document) - The document object that is being saved.
### getFontFamilyName() {#getFontFamilyName--}
```
public String getFontFamilyName()
```


Indicates the current font family name.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getBold() {#getBold--}
```
public boolean getBold()
```


Indicates whether the current font is bold.

**Returns:**
boolean - The corresponding  boolean  value.
### getItalic() {#getItalic--}
```
public boolean getItalic()
```


Indicates whether the current font is italic.

**Returns:**
boolean - The corresponding  boolean  value.
### getOriginalFileName() {#getOriginalFileName--}
```
public String getOriginalFileName()
```


Gets the original font file name with an extension.

This property contains the original file name of the current font if it is known. Otherwise it can be an empty string.

**Returns:**
java.lang.String - The original font file name with an extension.
### getOriginalFileSize() {#getOriginalFileSize--}
```
public int getOriginalFileSize()
```


Gets the original font file size.

This property contains the original file size of the current font if it is known. Otherwise it can be zero.

**Returns:**
int - The original font file size.
### isExportNeeded() {#isExportNeeded--}
```
public boolean isExportNeeded()
```


Allows to specify whether the current font will be exported as a font resource. Default is  true .

**Returns:**
boolean - The corresponding  boolean  value.
### isExportNeeded(boolean value) {#isExportNeeded-boolean-}
```
public void isExportNeeded(boolean value)
```


Allows to specify whether the current font will be exported as a font resource. Default is  true .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### isSubsettingNeeded() {#isSubsettingNeeded--}
```
public boolean isSubsettingNeeded()
```


Allows to specify whether the current font will be subsetted before exporting as a font resource.

Fonts can be exported as complete original font files or subsetted to include only the characters that are used in the document. Subsetting allows to reduce the resulting font resource size.

By default, Aspose.Words decides whether to perform subsetting or not by comparing the original font file size with the one specified in [HtmlSaveOptions.getFontResourcesSubsettingSizeThreshold()](../../com.aspose.words/htmlsaveoptions\#getFontResourcesSubsettingSizeThreshold--) / [HtmlSaveOptions.setFontResourcesSubsettingSizeThreshold(int)](../../com.aspose.words/htmlsaveoptions\#setFontResourcesSubsettingSizeThreshold-int-). You can override this behavior for individual fonts by setting the [isSubsettingNeeded()](../../com.aspose.words/fontsavingargs\#isSubsettingNeeded--) / [isSubsettingNeeded(boolean)](../../com.aspose.words/fontsavingargs\#isSubsettingNeeded-boolean-) property.

**Returns:**
boolean - The corresponding  boolean  value.
### isSubsettingNeeded(boolean value) {#isSubsettingNeeded-boolean-}
```
public void isSubsettingNeeded(boolean value)
```


Allows to specify whether the current font will be subsetted before exporting as a font resource.

Fonts can be exported as complete original font files or subsetted to include only the characters that are used in the document. Subsetting allows to reduce the resulting font resource size.

By default, Aspose.Words decides whether to perform subsetting or not by comparing the original font file size with the one specified in [HtmlSaveOptions.getFontResourcesSubsettingSizeThreshold()](../../com.aspose.words/htmlsaveoptions\#getFontResourcesSubsettingSizeThreshold--) / [HtmlSaveOptions.setFontResourcesSubsettingSizeThreshold(int)](../../com.aspose.words/htmlsaveoptions\#setFontResourcesSubsettingSizeThreshold-int-). You can override this behavior for individual fonts by setting the [isSubsettingNeeded()](../../com.aspose.words/fontsavingargs\#isSubsettingNeeded--) / [isSubsettingNeeded(boolean)](../../com.aspose.words/fontsavingargs\#isSubsettingNeeded-boolean-) property.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getFontFileName() {#getFontFileName--}
```
public String getFontFileName()
```


Gets the file name (without path) where the font will be saved to.

This property allows you to redefine how the font file names are generated during export to HTML.

When the event is fired, this property contains the file name that was generated by Aspose.Words. You can change the value of this property to save the font into a different file. Note that file names must be unique.

Aspose.Words automatically generates a unique file name for every embedded font when exporting to HTML format. How the font file name is generated depends on whether you save the document to a file or to a stream.

When saving a document to a file, the generated font file name looks like *..*.

When saving a document to a stream, the generated font file name looks like *Aspose.Words...*.

[getFontFileName()](../../com.aspose.words/fontsavingargs\#getFontFileName--) / [setFontFileName(java.lang.String)](../../com.aspose.words/fontsavingargs\#setFontFileName-java.lang.String-) must contain only the file name without the path. Aspose.Words determines the path for saving using the document file name, the [HtmlSaveOptions.getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [HtmlSaveOptions.setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-) and [HtmlSaveOptions.getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [HtmlSaveOptions.setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-) properties.

**P:Aspose.Words.Saving.FontSavingArgs.FontStream**

**Returns:**
java.lang.String - The file name (without path) where the font will be saved to.
### setFontFileName(String value) {#setFontFileName-java.lang.String-}
```
public void setFontFileName(String value)
```


Sets the file name (without path) where the font will be saved to.

This property allows you to redefine how the font file names are generated during export to HTML.

When the event is fired, this property contains the file name that was generated by Aspose.Words. You can change the value of this property to save the font into a different file. Note that file names must be unique.

Aspose.Words automatically generates a unique file name for every embedded font when exporting to HTML format. How the font file name is generated depends on whether you save the document to a file or to a stream.

When saving a document to a file, the generated font file name looks like *..*.

When saving a document to a stream, the generated font file name looks like *Aspose.Words...*.

[getFontFileName()](../../com.aspose.words/fontsavingargs\#getFontFileName--) / [setFontFileName(java.lang.String)](../../com.aspose.words/fontsavingargs\#setFontFileName-java.lang.String-) must contain only the file name without the path. Aspose.Words determines the path for saving using the document file name, the [HtmlSaveOptions.getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [HtmlSaveOptions.setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-) and [HtmlSaveOptions.getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [HtmlSaveOptions.setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-) properties.

**P:Aspose.Words.Saving.FontSavingArgs.FontStream**

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The file name (without path) where the font will be saved to. |

### getKeepFontStreamOpen() {#getKeepFontStreamOpen--}
```
public boolean getKeepFontStreamOpen()
```


Specifies whether Aspose.Words should keep the stream open or close it after saving a font.

Default is  false  and Aspose.Words will close the stream you provided in the **P:Aspose.Words.Saving.FontSavingArgs.FontStream** property after writing a font into it. Specify  true  to keep the stream open.

**P:Aspose.Words.Saving.FontSavingArgs.FontStream**

**Returns:**
boolean - The corresponding  boolean  value.
### setKeepFontStreamOpen(boolean value) {#setKeepFontStreamOpen-boolean-}
```
public void setKeepFontStreamOpen(boolean value)
```


Specifies whether Aspose.Words should keep the stream open or close it after saving a font.

Default is  false  and Aspose.Words will close the stream you provided in the **P:Aspose.Words.Saving.FontSavingArgs.FontStream** property after writing a font into it. Specify  true  to keep the stream open.

**P:Aspose.Words.Saving.FontSavingArgs.FontStream**

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getFontStream() {#getFontStream--}
```
public OutputStream getFontStream()
```




**Returns:**
java.io.OutputStream
### setFontStream(OutputStream value) {#setFontStream-java.io.OutputStream-}
```
public void setFontStream(OutputStream value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.io.OutputStream |  |

