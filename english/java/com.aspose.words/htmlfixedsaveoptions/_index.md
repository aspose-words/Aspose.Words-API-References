---
title: HtmlFixedSaveOptions
second_title: Aspose.Words for Java API Reference
description: Can be used to specify additional options when saving a document into the  format.
type: docs
weight: 326
url: /java/com.aspose.words/htmlfixedsaveoptions/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.SaveOptions](../../com.aspose.words/saveoptions), [com.aspose.words.FixedPageSaveOptions](../../com.aspose.words/fixedpagesaveoptions)
```
public class HtmlFixedSaveOptions extends FixedPageSaveOptions
```

Can be used to specify additional options when saving a document into the [SaveFormat.HTML\_FIXED](../../com.aspose.words/saveformat\#HTML-FIXED) format.

To learn more, visit the **Specify Save Options** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [getSaveFormat()](#getSaveFormat--) | Specifies the format in which the document will be saved if this save options object is used. |
| [setSaveFormat(int value)](#setSaveFormat-int-) | Specifies the format in which the document will be saved if this save options object is used. |
| [getShowPageBorder()](#getShowPageBorder--) | Specifies whether border around pages should be shown. |
| [setShowPageBorder(boolean value)](#setShowPageBorder-boolean-) | Specifies whether border around pages should be shown. |
| [getPageHorizontalAlignment()](#getPageHorizontalAlignment--) | Specifies the horizontal alignment of pages in an HTML document. |
| [setPageHorizontalAlignment(int value)](#setPageHorizontalAlignment-int-) | Specifies the horizontal alignment of pages in an HTML document. |
| [getPageMargins()](#getPageMargins--) | Specifies the margins around pages in an HTML document. |
| [setPageMargins(double value)](#setPageMargins-double-) | Specifies the margins around pages in an HTML document. |
| [getResourcesFolder()](#getResourcesFolder--) | Specifies the physical folder where resources (images, fonts, css) are saved when exporting a document to Html format. |
| [setResourcesFolder(String value)](#setResourcesFolder-java.lang.String-) | Specifies the physical folder where resources (images, fonts, css) are saved when exporting a document to Html format. |
| [getResourcesFolderAlias()](#getResourcesFolderAlias--) | Specifies the name of the folder used to construct image URIs written into an Html document. |
| [setResourcesFolderAlias(String value)](#setResourcesFolderAlias-java.lang.String-) | Specifies the name of the folder used to construct image URIs written into an Html document. |
| [getExportEmbeddedImages()](#getExportEmbeddedImages--) | Specifies whether images should be embedded into Html document in Base64 format. |
| [setExportEmbeddedImages(boolean value)](#setExportEmbeddedImages-boolean-) | Specifies whether images should be embedded into Html document in Base64 format. |
| [getExportEmbeddedFonts()](#getExportEmbeddedFonts--) | Specifies whether fonts should be embedded into Html document in Base64 format. |
| [setExportEmbeddedFonts(boolean value)](#setExportEmbeddedFonts-boolean-) | Specifies whether fonts should be embedded into Html document in Base64 format. |
| [getExportEmbeddedCss()](#getExportEmbeddedCss--) | Specifies whether the CSS (Cascading Style Sheet) should be embedded into Html document. |
| [setExportEmbeddedCss(boolean value)](#setExportEmbeddedCss-boolean-) | Specifies whether the CSS (Cascading Style Sheet) should be embedded into Html document. |
| [getExportEmbeddedSvg()](#getExportEmbeddedSvg--) | Specifies whether SVG resources should be embedded into Html document. |
| [setExportEmbeddedSvg(boolean value)](#setExportEmbeddedSvg-boolean-) | Specifies whether SVG resources should be embedded into Html document. |
| [getFontFormat()](#getFontFormat--) | Gets [ExportFontFormat](../../com.aspose.words/exportfontformat) used for font exporting. |
| [setFontFormat(int value)](#setFontFormat-int-) | Sets [ExportFontFormat](../../com.aspose.words/exportfontformat) used for font exporting. |
| [getCssClassNamesPrefix()](#getCssClassNamesPrefix--) | Specifies prefix which is added to all class names in style.css file. |
| [setCssClassNamesPrefix(String value)](#setCssClassNamesPrefix-java.lang.String-) | Specifies prefix which is added to all class names in style.css file. |
| [getResourceSavingCallback()](#getResourceSavingCallback--) | Allows to control how resources (images, fonts and css) are saved when a document is exported to fixed page Html format. |
| [setResourceSavingCallback(IResourceSavingCallback value)](#setResourceSavingCallback-com.aspose.words.IResourceSavingCallback-) | Allows to control how resources (images, fonts and css) are saved when a document is exported to fixed page Html format. |
| [getEncoding()](#getEncoding--) |  |
| [setEncoding(Charset value)](#setEncoding-java.nio.charset.Charset-) |  |
| [getExportFormFields()](#getExportFormFields--) | Gets indication of whether form fields are exported as interactive items (as 'input' tag) rather than converted to text or graphics. |
| [setExportFormFields(boolean value)](#setExportFormFields-boolean-) | Sets indication of whether form fields are exported as interactive items (as 'input' tag) rather than converted to text or graphics. |
| [getOptimizeOutput()](#getOptimizeOutput--) | Flag indicates whether it is required to optimize output. |
| [setOptimizeOutput(boolean value)](#setOptimizeOutput-boolean-) | Flag indicates whether it is required to optimize output. |
| [getUseTargetMachineFonts()](#getUseTargetMachineFonts--) | Flag indicates whether fonts from target machine must be used to display the document. |
| [setUseTargetMachineFonts(boolean value)](#setUseTargetMachineFonts-boolean-) | Flag indicates whether fonts from target machine must be used to display the document. |
| [getSaveFontFaceCssSeparately()](#getSaveFontFaceCssSeparately--) | Flag indicates whether "@font-face" CSS rules should be placed into a separate file "fontFaces.css" when a document is being saved with external stylesheet (that is, when [getExportEmbeddedCss()](../../com.aspose.words/htmlfixedsaveoptions\#getExportEmbeddedCss--) / [setExportEmbeddedCss(boolean)](../../com.aspose.words/htmlfixedsaveoptions\#setExportEmbeddedCss-boolean-) is  false ). |
| [setSaveFontFaceCssSeparately(boolean value)](#setSaveFontFaceCssSeparately-boolean-) | Flag indicates whether "@font-face" CSS rules should be placed into a separate file "fontFaces.css" when a document is being saved with external stylesheet (that is, when [getExportEmbeddedCss()](../../com.aspose.words/htmlfixedsaveoptions\#getExportEmbeddedCss--) / [setExportEmbeddedCss(boolean)](../../com.aspose.words/htmlfixedsaveoptions\#setExportEmbeddedCss-boolean-) is  false ). |
### getSaveFormat() {#getSaveFormat--}
```
public int getSaveFormat()
```


Specifies the format in which the document will be saved if this save options object is used. Can only be [SaveFormat.HTML\_FIXED](../../com.aspose.words/saveformat\#HTML-FIXED).

**Returns:**
int - The corresponding  int  value. The returned value is one of [SaveFormat](../../com.aspose.words/saveformat) constants.
### setSaveFormat(int value) {#setSaveFormat-int-}
```
public void setSaveFormat(int value)
```


Specifies the format in which the document will be saved if this save options object is used. Can only be [SaveFormat.HTML\_FIXED](../../com.aspose.words/saveformat\#HTML-FIXED).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [SaveFormat](../../com.aspose.words/saveformat) constants. |

### getShowPageBorder() {#getShowPageBorder--}
```
public boolean getShowPageBorder()
```


Specifies whether border around pages should be shown. Default is  true .

**Returns:**
boolean - The corresponding  boolean  value.
### setShowPageBorder(boolean value) {#setShowPageBorder-boolean-}
```
public void setShowPageBorder(boolean value)
```


Specifies whether border around pages should be shown. Default is  true .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getPageHorizontalAlignment() {#getPageHorizontalAlignment--}
```
public int getPageHorizontalAlignment()
```


Specifies the horizontal alignment of pages in an HTML document. Default value is  HtmlFixedHorizontalPageAlignment.Center .

**Returns:**
int - The corresponding  int  value. The returned value is one of [HtmlFixedPageHorizontalAlignment](../../com.aspose.words/htmlfixedpagehorizontalalignment) constants.
### setPageHorizontalAlignment(int value) {#setPageHorizontalAlignment-int-}
```
public void setPageHorizontalAlignment(int value)
```


Specifies the horizontal alignment of pages in an HTML document. Default value is  HtmlFixedHorizontalPageAlignment.Center .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [HtmlFixedPageHorizontalAlignment](../../com.aspose.words/htmlfixedpagehorizontalalignment) constants. |

### getPageMargins() {#getPageMargins--}
```
public double getPageMargins()
```


Specifies the margins around pages in an HTML document. The margins value is measured in points and should be equal to or greater than 0. Default value is 10 points.

Depends on the value of [getPageHorizontalAlignment()](../../com.aspose.words/htmlfixedsaveoptions\#getPageHorizontalAlignment--) / [setPageHorizontalAlignment(int)](../../com.aspose.words/htmlfixedsaveoptions\#setPageHorizontalAlignment-int-) property:

 *  Defines top, bottom and left page margins if the value is [HtmlFixedPageHorizontalAlignment.LEFT](../../com.aspose.words/htmlfixedpagehorizontalalignment\#LEFT).
 *  Defines top, bottom and right page margins if the value is [HtmlFixedPageHorizontalAlignment.RIGHT](../../com.aspose.words/htmlfixedpagehorizontalalignment\#RIGHT).
 *  Defines top and bottom page margins if the value is [HtmlFixedPageHorizontalAlignment.CENTER](../../com.aspose.words/htmlfixedpagehorizontalalignment\#CENTER).

**Returns:**
double - The corresponding  double  value.
### setPageMargins(double value) {#setPageMargins-double-}
```
public void setPageMargins(double value)
```


Specifies the margins around pages in an HTML document. The margins value is measured in points and should be equal to or greater than 0. Default value is 10 points.

Depends on the value of [getPageHorizontalAlignment()](../../com.aspose.words/htmlfixedsaveoptions\#getPageHorizontalAlignment--) / [setPageHorizontalAlignment(int)](../../com.aspose.words/htmlfixedsaveoptions\#setPageHorizontalAlignment-int-) property:

 *  Defines top, bottom and left page margins if the value is [HtmlFixedPageHorizontalAlignment.LEFT](../../com.aspose.words/htmlfixedpagehorizontalalignment\#LEFT).
 *  Defines top, bottom and right page margins if the value is [HtmlFixedPageHorizontalAlignment.RIGHT](../../com.aspose.words/htmlfixedpagehorizontalalignment\#RIGHT).
 *  Defines top and bottom page margins if the value is [HtmlFixedPageHorizontalAlignment.CENTER](../../com.aspose.words/htmlfixedpagehorizontalalignment\#CENTER).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The corresponding  double  value. |

### getResourcesFolder() {#getResourcesFolder--}
```
public String getResourcesFolder()
```


Specifies the physical folder where resources (images, fonts, css) are saved when exporting a document to Html format. Default is  null .

Has effect only if [getExportEmbeddedImages()](../../com.aspose.words/htmlfixedsaveoptions\#getExportEmbeddedImages--) / [setExportEmbeddedImages(boolean)](../../com.aspose.words/htmlfixedsaveoptions\#setExportEmbeddedImages-boolean-) property is false.

When you save a [Document](../../com.aspose.words/document) in Html format, Aspose.Words needs to save all images embedded in the document as standalone files. [getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolder--) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolder-java.lang.String-) allows you to specify where the images will be saved and [getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolderAlias--) / [setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolderAlias-java.lang.String-) allows to specify how the image URIs will be constructed.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the images in the same folder where the document file is saved. Use [getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolder--) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolder-java.lang.String-) to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the images, but still needs to save the images somewhere. In this case, you need to specify an accessible folder by using the [getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolder--) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolder-java.lang.String-) property

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setResourcesFolder(String value) {#setResourcesFolder-java.lang.String-}
```
public void setResourcesFolder(String value)
```


Specifies the physical folder where resources (images, fonts, css) are saved when exporting a document to Html format. Default is  null .

Has effect only if [getExportEmbeddedImages()](../../com.aspose.words/htmlfixedsaveoptions\#getExportEmbeddedImages--) / [setExportEmbeddedImages(boolean)](../../com.aspose.words/htmlfixedsaveoptions\#setExportEmbeddedImages-boolean-) property is false.

When you save a [Document](../../com.aspose.words/document) in Html format, Aspose.Words needs to save all images embedded in the document as standalone files. [getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolder--) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolder-java.lang.String-) allows you to specify where the images will be saved and [getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolderAlias--) / [setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolderAlias-java.lang.String-) allows to specify how the image URIs will be constructed.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the images in the same folder where the document file is saved. Use [getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolder--) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolder-java.lang.String-) to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the images, but still needs to save the images somewhere. In this case, you need to specify an accessible folder by using the [getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolder--) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolder-java.lang.String-) property

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### getResourcesFolderAlias() {#getResourcesFolderAlias--}
```
public String getResourcesFolderAlias()
```


Specifies the name of the folder used to construct image URIs written into an Html document. Default is  null .

When you save a [Document](../../com.aspose.words/document) in Html format, Aspose.Words needs to save all images embedded in the document as standalone files. [getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolder--) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolder-java.lang.String-) allows you to specify where the images will be saved and [getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolderAlias--) / [setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolderAlias-java.lang.String-) allows to specify how the image URIs will be constructed.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setResourcesFolderAlias(String value) {#setResourcesFolderAlias-java.lang.String-}
```
public void setResourcesFolderAlias(String value)
```


Specifies the name of the folder used to construct image URIs written into an Html document. Default is  null .

When you save a [Document](../../com.aspose.words/document) in Html format, Aspose.Words needs to save all images embedded in the document as standalone files. [getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolder--) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolder-java.lang.String-) allows you to specify where the images will be saved and [getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolderAlias--) / [setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolderAlias-java.lang.String-) allows to specify how the image URIs will be constructed.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### getExportEmbeddedImages() {#getExportEmbeddedImages--}
```
public boolean getExportEmbeddedImages()
```


Specifies whether images should be embedded into Html document in Base64 format. Note setting this flag can significantly increase size of output Html file.

**Returns:**
boolean - The corresponding  boolean  value.
### setExportEmbeddedImages(boolean value) {#setExportEmbeddedImages-boolean-}
```
public void setExportEmbeddedImages(boolean value)
```


Specifies whether images should be embedded into Html document in Base64 format. Note setting this flag can significantly increase size of output Html file.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getExportEmbeddedFonts() {#getExportEmbeddedFonts--}
```
public boolean getExportEmbeddedFonts()
```


Specifies whether fonts should be embedded into Html document in Base64 format. Note setting this flag can significantly increase size of output Html file.

**Returns:**
boolean - The corresponding  boolean  value.
### setExportEmbeddedFonts(boolean value) {#setExportEmbeddedFonts-boolean-}
```
public void setExportEmbeddedFonts(boolean value)
```


Specifies whether fonts should be embedded into Html document in Base64 format. Note setting this flag can significantly increase size of output Html file.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getExportEmbeddedCss() {#getExportEmbeddedCss--}
```
public boolean getExportEmbeddedCss()
```


Specifies whether the CSS (Cascading Style Sheet) should be embedded into Html document.

**Returns:**
boolean - The corresponding  boolean  value.
### setExportEmbeddedCss(boolean value) {#setExportEmbeddedCss-boolean-}
```
public void setExportEmbeddedCss(boolean value)
```


Specifies whether the CSS (Cascading Style Sheet) should be embedded into Html document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getExportEmbeddedSvg() {#getExportEmbeddedSvg--}
```
public boolean getExportEmbeddedSvg()
```


Specifies whether SVG resources should be embedded into Html document. Default value is  true .

**Returns:**
boolean - The corresponding  boolean  value.
### setExportEmbeddedSvg(boolean value) {#setExportEmbeddedSvg-boolean-}
```
public void setExportEmbeddedSvg(boolean value)
```


Specifies whether SVG resources should be embedded into Html document. Default value is  true .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getFontFormat() {#getFontFormat--}
```
public int getFontFormat()
```


Gets [ExportFontFormat](../../com.aspose.words/exportfontformat) used for font exporting. Default value is [ExportFontFormat.WOFF](../../com.aspose.words/exportfontformat\#WOFF).

**Returns:**
int - \{[ExportFontFormat](../../com.aspose.words/exportfontformat) used for font exporting. The returned value is one of [ExportFontFormat](../../com.aspose.words/exportfontformat) constants.
### setFontFormat(int value) {#setFontFormat-int-}
```
public void setFontFormat(int value)
```


Sets [ExportFontFormat](../../com.aspose.words/exportfontformat) used for font exporting. Default value is [ExportFontFormat.WOFF](../../com.aspose.words/exportfontformat\#WOFF).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | \{[ExportFontFormat](../../com.aspose.words/exportfontformat) used for font exporting. The value must be one of [ExportFontFormat](../../com.aspose.words/exportfontformat) constants. |

### getCssClassNamesPrefix() {#getCssClassNamesPrefix--}
```
public String getCssClassNamesPrefix()
```


Specifies prefix which is added to all class names in style.css file. Default value is  "aw" .

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setCssClassNamesPrefix(String value) {#setCssClassNamesPrefix-java.lang.String-}
```
public void setCssClassNamesPrefix(String value)
```


Specifies prefix which is added to all class names in style.css file. Default value is  "aw" .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### getResourceSavingCallback() {#getResourceSavingCallback--}
```
public IResourceSavingCallback getResourceSavingCallback()
```


Allows to control how resources (images, fonts and css) are saved when a document is exported to fixed page Html format.

**Returns:**
[IResourceSavingCallback](../../com.aspose.words/iresourcesavingcallback) - The corresponding [IResourceSavingCallback](../../com.aspose.words/iresourcesavingcallback) value.
### setResourceSavingCallback(IResourceSavingCallback value) {#setResourceSavingCallback-com.aspose.words.IResourceSavingCallback-}
```
public void setResourceSavingCallback(IResourceSavingCallback value)
```


Allows to control how resources (images, fonts and css) are saved when a document is exported to fixed page Html format.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IResourceSavingCallback](../../com.aspose.words/iresourcesavingcallback) | The corresponding [IResourceSavingCallback](../../com.aspose.words/iresourcesavingcallback) value. |

### getEncoding() {#getEncoding--}
```
public Charset getEncoding()
```




**Returns:**
java.nio.charset.Charset
### setEncoding(Charset value) {#setEncoding-java.nio.charset.Charset-}
```
public void setEncoding(Charset value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.nio.charset.Charset |  |

### getExportFormFields() {#getExportFormFields--}
```
public boolean getExportFormFields()
```


Gets indication of whether form fields are exported as interactive items (as 'input' tag) rather than converted to text or graphics.

**Returns:**
boolean - Indication of whether form fields are exported as interactive items (as 'input' tag) rather than converted to text or graphics.
### setExportFormFields(boolean value) {#setExportFormFields-boolean-}
```
public void setExportFormFields(boolean value)
```


Sets indication of whether form fields are exported as interactive items (as 'input' tag) rather than converted to text or graphics.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Indication of whether form fields are exported as interactive items (as 'input' tag) rather than converted to text or graphics. |

### getOptimizeOutput() {#getOptimizeOutput--}
```
public boolean getOptimizeOutput()
```


Flag indicates whether it is required to optimize output. If this flag is set redundant nested canvases and empty canvases are removed, also neighbor glyphs with the same formating are concatenated. Note: The accuracy of the content display may be affected if this property is set to true. Default is true.

**Returns:**
boolean - The corresponding  boolean  value.
### setOptimizeOutput(boolean value) {#setOptimizeOutput-boolean-}
```
public void setOptimizeOutput(boolean value)
```


Flag indicates whether it is required to optimize output. If this flag is set redundant nested canvases and empty canvases are removed, also neighbor glyphs with the same formating are concatenated. Note: The accuracy of the content display may be affected if this property is set to true. Default is true.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getUseTargetMachineFonts() {#getUseTargetMachineFonts--}
```
public boolean getUseTargetMachineFonts()
```


Flag indicates whether fonts from target machine must be used to display the document. If this flag is set to true, [getFontFormat()](../../com.aspose.words/htmlfixedsaveoptions\#getFontFormat--) / [setFontFormat(int)](../../com.aspose.words/htmlfixedsaveoptions\#setFontFormat-int-) and [getExportEmbeddedFonts()](../../com.aspose.words/htmlfixedsaveoptions\#getExportEmbeddedFonts--) / [setExportEmbeddedFonts(boolean)](../../com.aspose.words/htmlfixedsaveoptions\#setExportEmbeddedFonts-boolean-) properties do not have effect, also [getResourceSavingCallback()](../../com.aspose.words/htmlfixedsaveoptions\#getResourceSavingCallback--) / [setResourceSavingCallback(com.aspose.words.IResourceSavingCallback)](../../com.aspose.words/htmlfixedsaveoptions\#setResourceSavingCallback-com.aspose.words.IResourceSavingCallback-) is not fired for fonts. Default is false.

**Returns:**
boolean - The corresponding  boolean  value.
### setUseTargetMachineFonts(boolean value) {#setUseTargetMachineFonts-boolean-}
```
public void setUseTargetMachineFonts(boolean value)
```


Flag indicates whether fonts from target machine must be used to display the document. If this flag is set to true, [getFontFormat()](../../com.aspose.words/htmlfixedsaveoptions\#getFontFormat--) / [setFontFormat(int)](../../com.aspose.words/htmlfixedsaveoptions\#setFontFormat-int-) and [getExportEmbeddedFonts()](../../com.aspose.words/htmlfixedsaveoptions\#getExportEmbeddedFonts--) / [setExportEmbeddedFonts(boolean)](../../com.aspose.words/htmlfixedsaveoptions\#setExportEmbeddedFonts-boolean-) properties do not have effect, also [getResourceSavingCallback()](../../com.aspose.words/htmlfixedsaveoptions\#getResourceSavingCallback--) / [setResourceSavingCallback(com.aspose.words.IResourceSavingCallback)](../../com.aspose.words/htmlfixedsaveoptions\#setResourceSavingCallback-com.aspose.words.IResourceSavingCallback-) is not fired for fonts. Default is false.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getSaveFontFaceCssSeparately() {#getSaveFontFaceCssSeparately--}
```
public boolean getSaveFontFaceCssSeparately()
```


Flag indicates whether "@font-face" CSS rules should be placed into a separate file "fontFaces.css" when a document is being saved with external stylesheet (that is, when [getExportEmbeddedCss()](../../com.aspose.words/htmlfixedsaveoptions\#getExportEmbeddedCss--) / [setExportEmbeddedCss(boolean)](../../com.aspose.words/htmlfixedsaveoptions\#setExportEmbeddedCss-boolean-) is  false ). Default value is  false , all CSS rules are written into single file "styles.css". Setting this property to  true  restores the old behavior (separate files) for compatibility with legacy code.

**Returns:**
boolean - The corresponding  boolean  value.
### setSaveFontFaceCssSeparately(boolean value) {#setSaveFontFaceCssSeparately-boolean-}
```
public void setSaveFontFaceCssSeparately(boolean value)
```


Flag indicates whether "@font-face" CSS rules should be placed into a separate file "fontFaces.css" when a document is being saved with external stylesheet (that is, when [getExportEmbeddedCss()](../../com.aspose.words/htmlfixedsaveoptions\#getExportEmbeddedCss--) / [setExportEmbeddedCss(boolean)](../../com.aspose.words/htmlfixedsaveoptions\#setExportEmbeddedCss-boolean-) is  false ). Default value is  false , all CSS rules are written into single file "styles.css". Setting this property to  true  restores the old behavior (separate files) for compatibility with legacy code.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

