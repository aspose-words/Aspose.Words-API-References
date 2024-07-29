---
title: HtmlFixedSaveOptions
linktitle: HtmlFixedSaveOptions
second_title: Aspose.Words for Java
description: Can be used to specify additional options when saving a document into the SaveFormat.HTML_FIXED format in Java.
type: docs
weight: 356
url: /java/com.aspose.words/htmlfixedsaveoptions/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.SaveOptions](../../com.aspose.words/saveoptions/), [com.aspose.words.FixedPageSaveOptions](../../com.aspose.words/fixedpagesaveoptions/)
```
public class HtmlFixedSaveOptions extends FixedPageSaveOptions
```

Can be used to specify additional options when saving a document into the [SaveFormat.HTML\_FIXED](../../com.aspose.words/saveformat/\#HTML-FIXED) format.

To learn more, visit the [ Specify Save Options ][Specify Save Options] documentation article.

 **Examples:** 

Shows how to use a callback to print the URIs of external resources created while converting a document to HTML.

```

 public void htmlFixedResourceFolder() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     ResourceUriPrinter callback = new ResourceUriPrinter();

     HtmlFixedSaveOptions options = new HtmlFixedSaveOptions();
     {
         options.setSaveFormat(SaveFormat.HTML_FIXED);
         options.setExportEmbeddedImages(false);
         options.setResourcesFolder(getArtifactsDir() + "HtmlFixedResourceFolder");
         options.setResourcesFolderAlias(getArtifactsDir() + "HtmlFixedResourceFolderAlias");
         options.setShowPageBorder(false);
         options.setResourceSavingCallback(callback);
     }

     // A folder specified by ResourcesFolderAlias will contain the resources instead of ResourcesFolder.
     // We must ensure the folder exists before the streams can put their resources into it.
     new File(options.getResourcesFolderAlias()).mkdir();

     doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.HtmlFixedResourceFolder.html", options);

     System.out.println(callback.getText());

     String[] resourceFiles = new File(getArtifactsDir() + "HtmlFixedResourceFolderAlias").list();

     Assert.assertFalse(new File(getArtifactsDir() + "HtmlFixedResourceFolder").exists());
     Assert.assertEquals(6, IterableUtils.countMatches(Arrays.asList(resourceFiles),
             f -> f.endsWith(".jpeg") || f.endsWith(".png") || f.endsWith(".css")));
 }

 /// 
 /// Counts and prints URIs of resources contained by as they are converted to fixed HTML.
 /// 
 private static class ResourceUriPrinter implements IResourceSavingCallback {
     public void resourceSaving(ResourceSavingArgs args) throws Exception {
         // If we set a folder alias in the SaveOptions object, we will be able to print it from here.
         mText.append(MessageFormat.format("Resource #{0} \"{1}\"", ++mSavedResourceCount, args.getResourceFileName()));

         String extension = FilenameUtils.getExtension(args.getResourceFileName());
         switch (extension) {
             case "ttf":
             case "woff": {
                 // By default, 'ResourceFileUri' uses system folder for fonts.
                 // To avoid problems in other platforms you must explicitly specify the path for the fonts.
                 args.setResourceFileUri(getArtifactsDir() + File.separatorChar + args.getResourceFileName());
                 break;
             }
         }

         mText.append("\t" + args.getResourceFileUri());

         // If we have specified a folder in the "ResourcesFolderAlias" property,
         // we will also need to redirect each stream to put its resource in that folder.
         args.setResourceStream(new FileOutputStream(args.getResourceFileUri()));
         args.setKeepResourceStreamOpen(false);
     }

     public String getText() {
         return mText.toString();
     }

     private int mSavedResourceCount;
     private final  StringBuilder mText = new StringBuilder();
 }
 
```


[Specify Save Options]: https://docs.aspose.com/words/java/specify-save-options/
## Methods

| Method | Description |
| --- | --- |
| [createSaveOptions(int saveFormat)](#createSaveOptions-int) |  |
| [createSaveOptions(String fileName)](#createSaveOptions-java.lang.String) | Creates a save options object of a class suitable for the file extension specified in the given file name. |
| [equals(Object obj)](#equals-java.lang.Object) | Determines whether the specified object is equal in value to the current object. |
| [getAllowEmbeddingPostScriptFonts()](#getAllowEmbeddingPostScriptFonts) | Gets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. |
| [getColorMode()](#getColorMode) | Gets a value determining how colors are rendered. |
| [getCssClassNamesPrefix()](#getCssClassNamesPrefix) | Specifies prefix which is added to all class names in style.css file. |
| [getDefaultTemplate()](#getDefaultTemplate) | Gets path to default template (including filename). |
| [getDml3DEffectsRenderingMode()](#getDml3DEffectsRenderingMode) | Gets a value determining how 3D effects are rendered. |
| [getDmlEffectsRenderingMode()](#getDmlEffectsRenderingMode) | Gets a value determining how DrawingML effects are rendered. |
| [getDmlRenderingMode()](#getDmlRenderingMode) | Gets a value determining how DrawingML shapes are rendered. |
| [getEncoding()](#getEncoding) |  |
| [getExportEmbeddedCss()](#getExportEmbeddedCss) | Specifies whether the CSS (Cascading Style Sheet) should be embedded into Html document. |
| [getExportEmbeddedFonts()](#getExportEmbeddedFonts) | Specifies whether fonts should be embedded into Html document in Base64 format. |
| [getExportEmbeddedImages()](#getExportEmbeddedImages) | Specifies whether images should be embedded into Html document in Base64 format. |
| [getExportEmbeddedSvg()](#getExportEmbeddedSvg) | Specifies whether SVG resources should be embedded into Html document. |
| [getExportFormFields()](#getExportFormFields) | Gets indication of whether form fields are exported as interactive items (as 'input' tag) rather than converted to text or graphics. |
| [getExportGeneratorName()](#getExportGeneratorName) | When  true , causes the name and version of Aspose.Words to be embedded into produced files. |
| [getFontFormat()](#getFontFormat) | Gets [ExportFontFormat](../../com.aspose.words/exportfontformat/) used for font exporting. |
| [getImlRenderingMode()](#getImlRenderingMode) | Gets a value determining how ink (InkML) objects are rendered. |
| [getJpegQuality()](#getJpegQuality) | Gets a value determining the quality of the JPEG images inside Html document. |
| [getMemoryOptimization()](#getMemoryOptimization) | Gets value determining if memory optimization should be performed before saving the document. |
| [getMetafileRenderingOptions()](#getMetafileRenderingOptions) | Allows to specify metafile rendering options. |
| [getNumeralFormat()](#getNumeralFormat) | Gets [NumeralFormat](../../com.aspose.words/numeralformat/) used for rendering of numerals. |
| [getOptimizeOutput()](#getOptimizeOutput) | Flag indicates whether it is required to optimize output. |
| [getPageHorizontalAlignment()](#getPageHorizontalAlignment) | Specifies the horizontal alignment of pages in an HTML document. |
| [getPageMargins()](#getPageMargins) | Specifies the margins around pages in an HTML document. |
| [getPageSavingCallback()](#getPageSavingCallback) | Allows to control how separate pages are saved when a document is exported to fixed page format. |
| [getPageSet()](#getPageSet) | Gets the pages to render. |
| [getPrettyFormat()](#getPrettyFormat) | When  true , pretty formats output where applicable. |
| [getProgressCallback()](#getProgressCallback) | Called during saving a document and accepts data about saving progress. |
| [getResourceSavingCallback()](#getResourceSavingCallback) | Allows to control how resources (images, fonts and css) are saved when a document is exported to fixed page Html format. |
| [getResourcesFolder()](#getResourcesFolder) | Specifies the physical folder where resources (images, fonts, css) are saved when exporting a document to Html format. |
| [getResourcesFolderAlias()](#getResourcesFolderAlias) | Specifies the name of the folder used to construct image URIs written into an Html document. |
| [getSaveFontFaceCssSeparately()](#getSaveFontFaceCssSeparately) | Flag indicates whether "@font-face" CSS rules should be placed into a separate file "fontFaces.css" when a document is being saved with external stylesheet (that is, when [getExportEmbeddedCss()](../../com.aspose.words/htmlfixedsaveoptions/\#getExportEmbeddedCss) / [setExportEmbeddedCss(boolean)](../../com.aspose.words/htmlfixedsaveoptions/\#setExportEmbeddedCss-boolean) is  false ). |
| [getSaveFormat()](#getSaveFormat) | Specifies the format in which the document will be saved if this save options object is used. |
| [getShowPageBorder()](#getShowPageBorder) | Specifies whether border around pages should be shown. |
| [getTempFolder()](#getTempFolder) | Specifies the folder for temporary files used when saving to a DOC or DOCX file. |
| [getUpdateCreatedTimeProperty()](#getUpdateCreatedTimeProperty) | Gets a value determining whether the [BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties/\#getCreatedTime) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setCreatedTime-java.util.Date) property is updated before saving. |
| [getUpdateFields()](#getUpdateFields) | Gets a value determining if fields of certain types should be updated before saving the document to a fixed page format. |
| [getUpdateLastPrintedProperty()](#getUpdateLastPrintedProperty) | Gets a value determining whether the [BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties/\#getLastPrinted) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastPrinted-java.util.Date) property is updated before saving. |
| [getUpdateLastSavedTimeProperty()](#getUpdateLastSavedTimeProperty) | Gets a value determining whether the [BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties/\#getLastSavedTime) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastSavedTime-java.util.Date) property is updated before saving. |
| [getUseAntiAliasing()](#getUseAntiAliasing) | Gets a value determining whether or not to use anti-aliasing for rendering. |
| [getUseHighQualityRendering()](#getUseHighQualityRendering) | Gets a value determining whether or not to use high quality (i.e. |
| [getUseTargetMachineFonts()](#getUseTargetMachineFonts) | Flag indicates whether fonts from target machine must be used to display the document. |
| [setAllowEmbeddingPostScriptFonts(boolean value)](#setAllowEmbeddingPostScriptFonts-boolean) | Sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. |
| [setColorMode(int value)](#setColorMode-int) | Sets a value determining how colors are rendered. |
| [setCssClassNamesPrefix(String value)](#setCssClassNamesPrefix-java.lang.String) | Specifies prefix which is added to all class names in style.css file. |
| [setDefaultTemplate(String value)](#setDefaultTemplate-java.lang.String) | Sets path to default template (including filename). |
| [setDml3DEffectsRenderingMode(int value)](#setDml3DEffectsRenderingMode-int) | Sets a value determining how 3D effects are rendered. |
| [setDmlEffectsRenderingMode(int value)](#setDmlEffectsRenderingMode-int) | Sets a value determining how DrawingML effects are rendered. |
| [setDmlRenderingMode(int value)](#setDmlRenderingMode-int) | Sets a value determining how DrawingML shapes are rendered. |
| [setEncoding(Charset value)](#setEncoding-java.nio.charset.Charset) |  |
| [setExportEmbeddedCss(boolean value)](#setExportEmbeddedCss-boolean) | Specifies whether the CSS (Cascading Style Sheet) should be embedded into Html document. |
| [setExportEmbeddedFonts(boolean value)](#setExportEmbeddedFonts-boolean) | Specifies whether fonts should be embedded into Html document in Base64 format. |
| [setExportEmbeddedImages(boolean value)](#setExportEmbeddedImages-boolean) | Specifies whether images should be embedded into Html document in Base64 format. |
| [setExportEmbeddedSvg(boolean value)](#setExportEmbeddedSvg-boolean) | Specifies whether SVG resources should be embedded into Html document. |
| [setExportFormFields(boolean value)](#setExportFormFields-boolean) | Sets indication of whether form fields are exported as interactive items (as 'input' tag) rather than converted to text or graphics. |
| [setExportGeneratorName(boolean value)](#setExportGeneratorName-boolean) | When  true , causes the name and version of Aspose.Words to be embedded into produced files. |
| [setFontFormat(int value)](#setFontFormat-int) | Sets [ExportFontFormat](../../com.aspose.words/exportfontformat/) used for font exporting. |
| [setImlRenderingMode(int value)](#setImlRenderingMode-int) | Sets a value determining how ink (InkML) objects are rendered. |
| [setJpegQuality(int value)](#setJpegQuality-int) | Sets a value determining the quality of the JPEG images inside Html document. |
| [setMemoryOptimization(boolean value)](#setMemoryOptimization-boolean) | Sets value determining if memory optimization should be performed before saving the document. |
| [setMetafileRenderingOptions(MetafileRenderingOptions value)](#setMetafileRenderingOptions-com.aspose.words.MetafileRenderingOptions) | Allows to specify metafile rendering options. |
| [setNumeralFormat(int value)](#setNumeralFormat-int) | Sets [NumeralFormat](../../com.aspose.words/numeralformat/) used for rendering of numerals. |
| [setOptimizeOutput(boolean value)](#setOptimizeOutput-boolean) | Flag indicates whether it is required to optimize output. |
| [setPageHorizontalAlignment(int value)](#setPageHorizontalAlignment-int) | Specifies the horizontal alignment of pages in an HTML document. |
| [setPageMargins(double value)](#setPageMargins-double) | Specifies the margins around pages in an HTML document. |
| [setPageSavingCallback(IPageSavingCallback value)](#setPageSavingCallback-com.aspose.words.IPageSavingCallback) | Allows to control how separate pages are saved when a document is exported to fixed page format. |
| [setPageSet(PageSet value)](#setPageSet-com.aspose.words.PageSet) | Sets the pages to render. |
| [setPrettyFormat(boolean value)](#setPrettyFormat-boolean) | When  true , pretty formats output where applicable. |
| [setProgressCallback(IDocumentSavingCallback value)](#setProgressCallback-com.aspose.words.IDocumentSavingCallback) | Called during saving a document and accepts data about saving progress. |
| [setResourceSavingCallback(IResourceSavingCallback value)](#setResourceSavingCallback-com.aspose.words.IResourceSavingCallback) | Allows to control how resources (images, fonts and css) are saved when a document is exported to fixed page Html format. |
| [setResourcesFolder(String value)](#setResourcesFolder-java.lang.String) | Specifies the physical folder where resources (images, fonts, css) are saved when exporting a document to Html format. |
| [setResourcesFolderAlias(String value)](#setResourcesFolderAlias-java.lang.String) | Specifies the name of the folder used to construct image URIs written into an Html document. |
| [setSaveFontFaceCssSeparately(boolean value)](#setSaveFontFaceCssSeparately-boolean) | Flag indicates whether "@font-face" CSS rules should be placed into a separate file "fontFaces.css" when a document is being saved with external stylesheet (that is, when [getExportEmbeddedCss()](../../com.aspose.words/htmlfixedsaveoptions/\#getExportEmbeddedCss) / [setExportEmbeddedCss(boolean)](../../com.aspose.words/htmlfixedsaveoptions/\#setExportEmbeddedCss-boolean) is  false ). |
| [setSaveFormat(int value)](#setSaveFormat-int) | Specifies the format in which the document will be saved if this save options object is used. |
| [setShowPageBorder(boolean value)](#setShowPageBorder-boolean) | Specifies whether border around pages should be shown. |
| [setTempFolder(String value)](#setTempFolder-java.lang.String) | Specifies the folder for temporary files used when saving to a DOC or DOCX file. |
| [setUpdateCreatedTimeProperty(boolean value)](#setUpdateCreatedTimeProperty-boolean) | Sets a value determining whether the [BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties/\#getCreatedTime) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setCreatedTime-java.util.Date) property is updated before saving. |
| [setUpdateFields(boolean value)](#setUpdateFields-boolean) | Sets a value determining if fields of certain types should be updated before saving the document to a fixed page format. |
| [setUpdateLastPrintedProperty(boolean value)](#setUpdateLastPrintedProperty-boolean) | Sets a value determining whether the [BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties/\#getLastPrinted) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastPrinted-java.util.Date) property is updated before saving. |
| [setUpdateLastSavedTimeProperty(boolean value)](#setUpdateLastSavedTimeProperty-boolean) | Sets a value determining whether the [BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties/\#getLastSavedTime) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastSavedTime-java.util.Date) property is updated before saving. |
| [setUseAntiAliasing(boolean value)](#setUseAntiAliasing-boolean) | Sets a value determining whether or not to use anti-aliasing for rendering. |
| [setUseHighQualityRendering(boolean value)](#setUseHighQualityRendering-boolean) | Sets a value determining whether or not to use high quality (i.e. |
| [setUseTargetMachineFonts(boolean value)](#setUseTargetMachineFonts-boolean) | Flag indicates whether fonts from target machine must be used to display the document. |
### createSaveOptions(int saveFormat) {#createSaveOptions-int}
```
public static SaveOptions createSaveOptions(int saveFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| saveFormat | int |  |

**Returns:**
[SaveOptions](../../com.aspose.words/saveoptions/)
### createSaveOptions(String fileName) {#createSaveOptions-java.lang.String}
```
public static SaveOptions createSaveOptions(String fileName)
```


Creates a save options object of a class suitable for the file extension specified in the given file name.

 **Examples:** 

Shows how to set a default template for documents that do not have attached templates.

```

 Document doc = new Document();

 // Enable automatic style updating, but do not attach a template document.
 doc.setAutomaticallyUpdateStyles(true);

 Assert.assertEquals("", doc.getAttachedTemplate());

 // Since there is no template document, the document had nowhere to track style changes.
 // Use a SaveOptions object to automatically set a template
 // if a document that we are saving does not have one.
 SaveOptions options = SaveOptions.createSaveOptions("Document.DefaultTemplate.docx");
 options.setDefaultTemplate(getMyDir() + "Business brochure.dotx");

 doc.save(getArtifactsDir() + "Document.DefaultTemplate.docx", options);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | The extension of this file name determines the class of the save options object to create. |

**Returns:**
[SaveOptions](../../com.aspose.words/saveoptions/) - An object of a class that derives from [SaveOptions](../../com.aspose.words/saveoptions/).
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


Determines whether the specified object is equal in value to the current object.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### getAllowEmbeddingPostScriptFonts() {#getAllowEmbeddingPostScriptFonts}
```
public boolean getAllowEmbeddingPostScriptFonts()
```


Gets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is  false .

 **Remarks:** 

Note, Word does not embed PostScript fonts, but can open documents with embedded fonts of this type.

This option only works when [FontInfoCollection.getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection/\#getEmbedTrueTypeFonts) / [FontInfoCollection.setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection/\#setEmbedTrueTypeFonts-boolean) of the [DocumentBase.getFontInfos()](../../com.aspose.words/documentbase/\#getFontInfos) property is set to  true .

 **Examples:** 

Shows how to save the document with PostScript font.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setName("PostScriptFont");
 builder.writeln("Some text with PostScript font.");

 // Load the font with PostScript to use in the document.
 MemoryFontSource otf = new MemoryFontSource(DocumentHelper.getBytesFromStream(new FileInputStream(getFontsDir() + "AllegroOpen.otf")));
 doc.setFontSettings(new FontSettings());
 doc.getFontSettings().setFontsSources(new FontSourceBase[]{otf});

 // Embed TrueType fonts.
 doc.getFontInfos().setEmbedTrueTypeFonts(true);

 // Allow embedding PostScript fonts while embedding TrueType fonts.
 // Microsoft Word does not embed PostScript fonts, but can open documents with embedded fonts of this type.
 SaveOptions saveOptions = SaveOptions.createSaveOptions(SaveFormat.DOCX);
 saveOptions.setAllowEmbeddingPostScriptFonts(true);

 doc.save(getArtifactsDir() + "Document.AllowEmbeddingPostScriptFonts.docx", saveOptions);
 
```

**Returns:**
boolean - A boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved.
### getColorMode() {#getColorMode}
```
public int getColorMode()
```


Gets a value determining how colors are rendered.

 **Remarks:** 

The default value is [ColorMode.NORMAL](../../com.aspose.words/colormode/\#NORMAL).

 **Examples:** 

Shows how to change image color with saving options property.

```

 Document doc = new Document(getMyDir() + "Images.docx");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 // Set the "ColorMode" property to "Grayscale" to render all images from the document in black and white.
 // The size of the output document may be larger with this setting.
 // Set the "ColorMode" property to "Normal" to render all images in color.
 PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
 {
     pdfSaveOptions.setColorMode(colorMode);
 }

 doc.save(getArtifactsDir() + "PdfSaveOptions.ColorRendering.pdf", pdfSaveOptions);
 
```

**Returns:**
int - A value determining how colors are rendered. The returned value is one of [ColorMode](../../com.aspose.words/colormode/) constants.
### getCssClassNamesPrefix() {#getCssClassNamesPrefix}
```
public String getCssClassNamesPrefix()
```


Specifies prefix which is added to all class names in style.css file. Default value is  "aw" .

 **Examples:** 

Shows how to place CSS into a separate file and add a prefix to all of its CSS class names.

```

 Document doc = new Document(getMyDir() + "Bookmarks.docx");

 HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();
 {
     htmlFixedSaveOptions.setCssClassNamesPrefix("myprefix");
     htmlFixedSaveOptions.setSaveFontFaceCssSeparately(true);
 }

 doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.AddCssClassNamesPrefix.html", htmlFixedSaveOptions);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlFixedSaveOptions.AddCssClassNamesPrefix.html"), StandardCharsets.UTF_8);

 Assert.assertTrue(Pattern.compile(
     " " +
     " " +
     "").matcher(outDocContents).find());

 outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlFixedSaveOptions.AddCssClassNamesPrefix/styles.css"), StandardCharsets.UTF_8);

 Assert.assertTrue(Pattern.compile(
     ".myprefixdiv [{] position:absolute; [}] " +
     ".myprefixspan [{] position:absolute; white-space:pre; color:#000000; font-size:12pt; [}]").matcher(outDocContents).find());
 
```

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getDefaultTemplate() {#getDefaultTemplate}
```
public String getDefaultTemplate()
```


Gets path to default template (including filename). Default value for this property is **empty string**.

 **Remarks:** 

If specified, this path is used to load template when [Document.getAutomaticallyUpdateStyles()](../../com.aspose.words/document/\#getAutomaticallyUpdateStyles) / [Document.setAutomaticallyUpdateStyles(boolean)](../../com.aspose.words/document/\#setAutomaticallyUpdateStyles-boolean) is  true , but [Document.getAttachedTemplate()](../../com.aspose.words/document/\#getAttachedTemplate) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document/\#setAttachedTemplate-java.lang.String) is empty.

 **Examples:** 

Shows how to set a default template for documents that do not have attached templates.

```

 Document doc = new Document();

 // Enable automatic style updating, but do not attach a template document.
 doc.setAutomaticallyUpdateStyles(true);

 Assert.assertEquals("", doc.getAttachedTemplate());

 // Since there is no template document, the document had nowhere to track style changes.
 // Use a SaveOptions object to automatically set a template
 // if a document that we are saving does not have one.
 SaveOptions options = SaveOptions.createSaveOptions("Document.DefaultTemplate.docx");
 options.setDefaultTemplate(getMyDir() + "Business brochure.dotx");

 doc.save(getArtifactsDir() + "Document.DefaultTemplate.docx", options);
 
```

**Returns:**
java.lang.String - Path to default template (including filename).
### getDml3DEffectsRenderingMode() {#getDml3DEffectsRenderingMode}
```
public int getDml3DEffectsRenderingMode()
```


Gets a value determining how 3D effects are rendered.

 **Remarks:** 

The default value is [Dml3DEffectsRenderingMode.BASIC](../../com.aspose.words/dml3deffectsrenderingmode/\#BASIC).

 **Examples:** 

Shows how 3D effects are rendered.

```

 Document doc = new Document(getMyDir() + "DrawingML shape 3D effects.docx");

 RenderCallback warningCallback = new RenderCallback();
 doc.setWarningCallback(warningCallback);

 PdfSaveOptions saveOptions = new PdfSaveOptions();
 saveOptions.setDml3DEffectsRenderingMode(Dml3DEffectsRenderingMode.ADVANCED);

 doc.save(getArtifactsDir() + "PdfSaveOptions.Dml3DEffectsRenderingModeTest.pdf", saveOptions);
 
```

**Returns:**
int - A value determining how 3D effects are rendered. The returned value is one of [Dml3DEffectsRenderingMode](../../com.aspose.words/dml3deffectsrenderingmode/) constants.
### getDmlEffectsRenderingMode() {#getDmlEffectsRenderingMode}
```
public int getDmlEffectsRenderingMode()
```


Gets a value determining how DrawingML effects are rendered.

 **Remarks:** 

The default value is [DmlEffectsRenderingMode.SIMPLIFIED](../../com.aspose.words/dmleffectsrenderingmode/\#SIMPLIFIED).

This property is used when the document is exported to fixed page formats.

 **Examples:** 

Shows how to configure the rendering quality of DrawingML effects in a document as we save it to PDF.

```

 Document doc = new Document(getMyDir() + "DrawingML shape effects.docx");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Set the "DmlEffectsRenderingMode" property to "DmlEffectsRenderingMode.None" to discard all DrawingML effects.
 // Set the "DmlEffectsRenderingMode" property to "DmlEffectsRenderingMode.Simplified"
 // to render a simplified version of DrawingML effects.
 // Set the "DmlEffectsRenderingMode" property to "DmlEffectsRenderingMode.Fine" to
 // render DrawingML effects with more accuracy and also with more processing cost.
 options.setDmlEffectsRenderingMode(effectsRenderingMode);

 Assert.assertEquals(DmlRenderingMode.DRAWING_ML, options.getDmlRenderingMode());

 doc.save(getArtifactsDir() + "PdfSaveOptions.DrawingMLEffects.pdf", options);
 
```

**Returns:**
int - A value determining how DrawingML effects are rendered. The returned value is one of [DmlEffectsRenderingMode](../../com.aspose.words/dmleffectsrenderingmode/) constants.
### getDmlRenderingMode() {#getDmlRenderingMode}
```
public int getDmlRenderingMode()
```


Gets a value determining how DrawingML shapes are rendered.

 **Remarks:** 

The default value is [DmlRenderingMode.FALLBACK](../../com.aspose.words/dmlrenderingmode/\#FALLBACK).

This property is used when the document is exported to fixed page formats.

 **Examples:** 

Shows how to render fallback shapes when saving to PDF.

```

 Document doc = new Document(getMyDir() + "DrawingML shape fallbacks.docx");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Set the "DmlRenderingMode" property to "DmlRenderingMode.Fallback"
 // to substitute DML shapes with their fallback shapes.
 // Set the "DmlRenderingMode" property to "DmlRenderingMode.DrawingML"
 // to render the DML shapes themselves.
 options.setDmlRenderingMode(dmlRenderingMode);

 doc.save(getArtifactsDir() + "PdfSaveOptions.DrawingMLFallback.pdf", options);
 
```

Shows how to configure the rendering quality of DrawingML effects in a document as we save it to PDF.

```

 Document doc = new Document(getMyDir() + "DrawingML shape effects.docx");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Set the "DmlEffectsRenderingMode" property to "DmlEffectsRenderingMode.None" to discard all DrawingML effects.
 // Set the "DmlEffectsRenderingMode" property to "DmlEffectsRenderingMode.Simplified"
 // to render a simplified version of DrawingML effects.
 // Set the "DmlEffectsRenderingMode" property to "DmlEffectsRenderingMode.Fine" to
 // render DrawingML effects with more accuracy and also with more processing cost.
 options.setDmlEffectsRenderingMode(effectsRenderingMode);

 Assert.assertEquals(DmlRenderingMode.DRAWING_ML, options.getDmlRenderingMode());

 doc.save(getArtifactsDir() + "PdfSaveOptions.DrawingMLEffects.pdf", options);
 
```

**Returns:**
int - A value determining how DrawingML shapes are rendered. The returned value is one of [DmlRenderingMode](../../com.aspose.words/dmlrenderingmode/) constants.
### getEncoding() {#getEncoding}
```
public Charset getEncoding()
```




**Returns:**
java.nio.charset.Charset
### getExportEmbeddedCss() {#getExportEmbeddedCss}
```
public boolean getExportEmbeddedCss()
```


Specifies whether the CSS (Cascading Style Sheet) should be embedded into Html document.

 **Examples:** 

Shows how to determine where to store CSS stylesheets when exporting a document to Html.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 // When we export a document to html, Aspose.Words will also create a CSS stylesheet to format the document with.
 // Setting the "ExportEmbeddedCss" flag to "true" save the CSS stylesheet to a .css file,
 // and link to the file from the html document using a  element.
 // Setting the flag to "false" will embed the CSS stylesheet within the Html document,
 // which will create only one file instead of two.
 HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();
 {
     htmlFixedSaveOptions.setExportEmbeddedCss(exportEmbeddedCss);
 }

 doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.ExportEmbeddedCss.html", htmlFixedSaveOptions);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlFixedSaveOptions.ExportEmbeddedCss.html"), "utf-8");

 if (exportEmbeddedCss) {
     Assert.assertTrue(outDocContents.contains("
```

**Returns:**
boolean - The corresponding  boolean  value.
### getExportEmbeddedFonts() {#getExportEmbeddedFonts}
```
public boolean getExportEmbeddedFonts()
```


Specifies whether fonts should be embedded into Html document in Base64 format. Note setting this flag can significantly increase size of output Html file.

 **Examples:** 

Shows how to determine where to store embedded fonts when exporting a document to Html.

```

 Document doc = new Document(getMyDir() + "Embedded font.docx");

 // When we export a document with embedded fonts to .html,
 // Aspose.Words can place the fonts in two possible locations.
 // Setting the "ExportEmbeddedFonts" flag to "true" will store the raw data for embedded fonts within the CSS stylesheet,
 // in the "url" property of the "@font-face" rule. This may create a huge CSS stylesheet file
 // and reduce the number of external files that this HTML conversion will create.
 // Setting this flag to "false" will create a file for each font.
 // The CSS stylesheet will link to each font file using the "url" property of the "@font-face" rule.
 HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();
 {
     htmlFixedSaveOptions.setExportEmbeddedFonts(exportEmbeddedFonts);
 }

 doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.ExportEmbeddedFonts.html", htmlFixedSaveOptions);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlFixedSaveOptions.ExportEmbeddedFonts/styles.css"), StandardCharsets.UTF_8);

 if (exportEmbeddedFonts)
 {
     Assert.assertTrue(Pattern.compile("@font-face [{] font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'\u263a'[)], url[(].+[)] format[(]'woff'[)]; [}]").matcher(outDocContents).find());
     Assert.assertEquals(0, DocumentHelper.directoryGetFiles(getArtifactsDir() + "HtmlFixedSaveOptions.ExportEmbeddedFonts", "*.woff").size());
 }
 else
 {
     Assert.assertTrue(Pattern.compile("@font-face [{] font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'\u263a'[)], url[(]'font001[.]woff'[)] format[(]'woff'[)]; [}]").matcher(outDocContents).find());
     Assert.assertEquals(2, DocumentHelper.directoryGetFiles(getArtifactsDir() + "HtmlFixedSaveOptions.ExportEmbeddedFonts", "*.woff").size());
 }
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getExportEmbeddedImages() {#getExportEmbeddedImages}
```
public boolean getExportEmbeddedImages()
```


Specifies whether images should be embedded into Html document in Base64 format. Note setting this flag can significantly increase size of output Html file.

 **Examples:** 

Shows how to determine where to store images when exporting a document to Html.

```

 Document doc = new Document(getMyDir() + "Images.docx");

 // When we export a document with embedded images to .html,
 // Aspose.Words can place the images in two possible locations.
 // Setting the "ExportEmbeddedImages" flag to "true" will store the raw data
 // for all images within the output HTML document, in the "src" attribute of  tags.
 // Setting this flag to "false" will create an image file in the local file system for every image,
 // and store all these files in a separate folder.
 HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();
 {
     htmlFixedSaveOptions.setExportEmbeddedImages(exportImages);
 }

 doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.ExportEmbeddedImages.html", htmlFixedSaveOptions);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlFixedSaveOptions.ExportEmbeddedImages.html"), StandardCharsets.UTF_8);

 if (exportImages)
 {
     Assert.assertFalse(new File(getArtifactsDir() + "HtmlFixedSaveOptions.ExportEmbeddedImages/image001.jpeg").exists());
     Assert.assertTrue(Pattern.compile("").matcher(outDocContents).find());
 }
 else
 {
     Assert.assertTrue(new File(getArtifactsDir() + "HtmlFixedSaveOptions.ExportEmbeddedImages/image001.jpeg").exists());
     Assert.assertTrue(Pattern.compile("").matcher(outDocContents).find());
 }
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getExportEmbeddedSvg() {#getExportEmbeddedSvg}
```
public boolean getExportEmbeddedSvg()
```


Specifies whether SVG resources should be embedded into Html document. Default value is  true .

 **Examples:** 

Shows how to determine where to store SVG objects when exporting a document to Html.

```

 Document doc = new Document(getMyDir() + "Images.docx");

 // When we export a document with SVG objects to .html,
 // Aspose.Words can place these objects in two possible locations.
 // Setting the "ExportEmbeddedSvg" flag to "true" will embed all SVG object raw data
 // within the output HTML, inside  tags.
 // Setting this flag to "false" will create a file in the local file system for each SVG object.
 // The HTML will link to each file using the "data" attribute of an  tag.
 HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();
 {
     htmlFixedSaveOptions.setExportEmbeddedSvg(exportSvgs);
 }

 doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.ExportEmbeddedSvgs.html", htmlFixedSaveOptions);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlFixedSaveOptions.ExportEmbeddedSvgs.html"), StandardCharsets.UTF_8);

 if (exportSvgs) {
     Assert.assertFalse(new File(getArtifactsDir() + "HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001.svg").exists());
     Assert.assertTrue(Pattern.compile("").matcher(outDocContents).find());
 } else {
     Assert.assertTrue(new File(getArtifactsDir() + "HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001.svg").exists());
     Assert.assertTrue(Pattern.compile("").matcher(outDocContents).find());
 }
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getExportFormFields() {#getExportFormFields}
```
public boolean getExportFormFields()
```


Gets indication of whether form fields are exported as interactive items (as 'input' tag) rather than converted to text or graphics.

 **Examples:** 

Shows how to export form fields to Html.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.insertCheckBox("CheckBox", false, 15);

 // When we export a document with form fields to .html,
 // there are two ways in which Aspose.Words can export form fields.
 // Setting the "ExportFormFields" flag to "true" will export them as interactive objects.
 // Setting this flag to "false" will display form fields as plain text.
 // This will freeze them at their current value, and prevent the reader of our HTML document
 // from being able to interact with them.
 HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();
 {
     htmlFixedSaveOptions.setExportFormFields(exportFormFields);
 }

 doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.ExportFormFields.html", htmlFixedSaveOptions);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlFixedSaveOptions.ExportFormFields.html"), StandardCharsets.UTF_8);

 if (exportFormFields)
 {
     Assert.assertTrue(Pattern.compile(
         "" +
         "").matcher(outDocContents).find());
 }
 else
 {
     Assert.assertTrue(Pattern.compile(
         "" +
         "
```

**Returns:**
boolean - Indication of whether form fields are exported as interactive items (as 'input' tag) rather than converted to text or graphics.
### getExportGeneratorName() {#getExportGeneratorName}
```
public boolean getExportGeneratorName()
```


When  true , causes the name and version of Aspose.Words to be embedded into produced files. Default value is  true .

 **Examples:** 

Shows how to disable adding name and version of Aspose.Words into produced files.

```

 Document doc = new Document();

 // Use https://docs.aspose.com/words/net/generator-or-producer-name-included-in-output-documents/ to know how to check the result.
 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(); { saveOptions.setExportGeneratorName(false); }

 doc.save(getArtifactsDir() + "OoxmlSaveOptions.ExportGeneratorName.docx", saveOptions);
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getFontFormat() {#getFontFormat}
```
public int getFontFormat()
```


Gets [ExportFontFormat](../../com.aspose.words/exportfontformat/) used for font exporting. Default value is [ExportFontFormat.WOFF](../../com.aspose.words/exportfontformat/\#WOFF).

 **Examples:** 

Shows how use fonts only from the target machine when saving a document to HTML.

```

 Document doc = new Document(getMyDir() + "Bullet points with alternative font.docx");

 HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions();
 {
     saveOptions.setExportEmbeddedCss(true);
     saveOptions.setUseTargetMachineFonts(useTargetMachineFonts);
     saveOptions.setFontFormat(ExportFontFormat.TTF);
     saveOptions.setExportEmbeddedFonts(false);
 }

 doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.UsingMachineFonts.html", saveOptions);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlFixedSaveOptions.UsingMachineFonts.html"), StandardCharsets.UTF_8);

 if (useTargetMachineFonts)
     Assert.assertFalse(Pattern.compile("@font-face").matcher(outDocContents).find());
 else
     Assert.assertTrue(Pattern.compile(
         "@font-face [{] font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'\u263a'[)], " +
         "url[(]'HtmlFixedSaveOptions.UsingMachineFonts/font001.ttf'[)] format[(]'truetype'[)]; [}]").matcher(outDocContents).find());
 
```

**Returns:**
int - [ExportFontFormat](../../com.aspose.words/exportfontformat/) used for font exporting. The returned value is one of [ExportFontFormat](../../com.aspose.words/exportfontformat/) constants.
### getImlRenderingMode() {#getImlRenderingMode}
```
public int getImlRenderingMode()
```


Gets a value determining how ink (InkML) objects are rendered.

 **Remarks:** 

The default value is [ImlRenderingMode.INK\_ML](../../com.aspose.words/imlrenderingmode/\#INK-ML).

This property is used when the document is exported to fixed page formats.

 **Examples:** 

Shows how to render Ink object.

```

 Document doc = new Document(getMyDir() + "Ink object.docx");

 // Set 'ImlRenderingMode.InkML' ignores fall-back shape of ink (InkML) object and renders InkML itself.
 // If the rendering result is unsatisfactory,
 // please use 'ImlRenderingMode.Fallback' to get a result similar to previous versions.
 ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.JPEG);
 {
     saveOptions.setImlRenderingMode(ImlRenderingMode.INK_ML);
 }

 doc.save(getArtifactsDir() + "ImageSaveOptions.RenderInkObject.jpeg", saveOptions);
 
```

**Returns:**
int - A value determining how ink (InkML) objects are rendered. The returned value is one of [ImlRenderingMode](../../com.aspose.words/imlrenderingmode/) constants.
### getJpegQuality() {#getJpegQuality}
```
public int getJpegQuality()
```


Gets a value determining the quality of the JPEG images inside Html document.

 **Remarks:** 

Has effect only when a document contains JPEG images.

Use this property to get or set the quality of the images inside a document when saving in fixed page format. The value may vary from 0 to 100 where 0 means worst quality but maximum compression and 100 means best quality but minimum compression.

The default value is 95.

 **Examples:** 

Shows how to configure compression while saving a document as a JPEG.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertImage(getImageDir() + "Logo.jpg");

 // Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
 // to modify the way in which that method renders the document into an image.
 ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.JPEG);

 // Set the "JpegQuality" property to "10" to use stronger compression when rendering the document.
 // This will reduce the file size of the document, but the image will display more prominent compression artifacts.
 imageOptions.setJpegQuality(10);

 doc.save(getArtifactsDir() + "ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

 Assert.assertTrue(new File(getArtifactsDir() + "ImageSaveOptions.JpegQuality.HighCompression.jpg").length() <= 20000);

 // Set the "JpegQuality" property to "100" to use weaker compression when rending the document.
 // This will improve the quality of the image at the cost of an increased file size.
 imageOptions.setJpegQuality(100);

 doc.save(getArtifactsDir() + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);

 Assert.assertTrue(new File(getArtifactsDir() + "ImageSaveOptions.JpegQuality.HighQuality.jpg").length() < 60000);
 
```

**Returns:**
int - A value determining the quality of the JPEG images inside Html document.
### getMemoryOptimization() {#getMemoryOptimization}
```
public boolean getMemoryOptimization()
```


Gets value determining if memory optimization should be performed before saving the document. Default value for this property is  false .

 **Remarks:** 

Setting this option to  true  can significantly decrease memory consumption while saving large documents at the cost of slower saving time.

 **Examples:** 

Shows an option to optimize memory consumption when rendering large documents to PDF.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 SaveOptions saveOptions = SaveOptions.createSaveOptions(SaveFormat.PDF);

 // Set the "MemoryOptimization" property to "true" to lower the memory footprint of large documents' saving operations
 // at the cost of increasing the duration of the operation.
 // Set the "MemoryOptimization" property to "false" to save the document as a PDF normally.
 saveOptions.setMemoryOptimization(memoryOptimization);

 doc.save(getArtifactsDir() + "PdfSaveOptions.MemoryOptimization.pdf", saveOptions);
 
```

**Returns:**
boolean - Value determining if memory optimization should be performed before saving the document.
### getMetafileRenderingOptions() {#getMetafileRenderingOptions}
```
public MetafileRenderingOptions getMetafileRenderingOptions()
```


Allows to specify metafile rendering options.

 **Examples:** 

Shows added a fallback to bitmap rendering and changing type of warnings about unsupported metafile records.

```

 public void handleBinaryRasterWarnings() throws Exception {
     Document doc = new Document(getMyDir() + "WMF with image.docx");

     MetafileRenderingOptions metafileRenderingOptions = new MetafileRenderingOptions();

     // Set the "EmulateRasterOperations" property to "false" to fall back to bitmap when
     // it encounters a metafile, which will require raster operations to render in the output PDF.
     metafileRenderingOptions.setEmulateRasterOperations(false);

     // Set the "RenderingMode" property to "VectorWithFallback" to try to render every metafile using vector graphics.
     metafileRenderingOptions.setRenderingMode(MetafileRenderingMode.VECTOR_WITH_FALLBACK);

     // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
     // to modify how that method converts the document to .PDF and applies the configuration
     // in our MetafileRenderingOptions object to the saving operation.
     PdfSaveOptions saveOptions = new PdfSaveOptions();
     saveOptions.setMetafileRenderingOptions(metafileRenderingOptions);

     HandleDocumentWarnings callback = new HandleDocumentWarnings();
     doc.setWarningCallback(callback);

     doc.save(getArtifactsDir() + "PdfSaveOptions.HandleBinaryRasterWarnings.pdf", saveOptions);

     Assert.assertEquals(1, callback.mWarnings.getCount());
     Assert.assertEquals("'R2_XORPEN' binary raster operation is not supported.",
             callback.mWarnings.get(0).getDescription());
 }

 /// 
 /// Prints and collects formatting loss-related warnings that occur upon saving a document.
 /// 
 public static class HandleDocumentWarnings implements IWarningCallback {
     public void warning(WarningInfo info) {
         if (info.getWarningType() == WarningType.MINOR_FORMATTING_LOSS) {
             System.out.println("Unsupported operation: " + info.getDescription());
             this.mWarnings.warning(info);
         }
     }

     public WarningInfoCollection mWarnings = new WarningInfoCollection();
 }
 
```

**Returns:**
[MetafileRenderingOptions](../../com.aspose.words/metafilerenderingoptions/) - The corresponding [MetafileRenderingOptions](../../com.aspose.words/metafilerenderingoptions/) value.
### getNumeralFormat() {#getNumeralFormat}
```
public int getNumeralFormat()
```


Gets [NumeralFormat](../../com.aspose.words/numeralformat/) used for rendering of numerals. European numerals are used by default.

 **Remarks:** 

If the value of this property is changed and page layout is already built then [Document.updatePageLayout()](../../com.aspose.words/document/\#updatePageLayout) is invoked automatically to update any changes.

 **Examples:** 

Shows how to set the numeral format used when saving to PDF.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setLocaleId(1025);
 builder.writeln("1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 50, 100");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Set the "NumeralFormat" property to "NumeralFormat.ArabicIndic" to
 // use glyphs from the U+0660 to U+0669 range as numbers.
 // Set the "NumeralFormat" property to "NumeralFormat.Context" to
 // look up the locale to determine what number of glyphs to use.
 // Set the "NumeralFormat" property to "NumeralFormat.EasternArabicIndic" to
 // use glyphs from the U+06F0 to U+06F9 range as numbers.
 // Set the "NumeralFormat" property to "NumeralFormat.European" to use european numerals.
 // Set the "NumeralFormat" property to "NumeralFormat.System" to determine the symbol set from regional settings.
 options.setNumeralFormat(numeralFormat);

 doc.save(getArtifactsDir() + "PdfSaveOptions.SetNumeralFormat.pdf", options);
 
```

**Returns:**
int - [NumeralFormat](../../com.aspose.words/numeralformat/) used for rendering of numerals. The returned value is one of [NumeralFormat](../../com.aspose.words/numeralformat/) constants.
### getOptimizeOutput() {#getOptimizeOutput}
```
public boolean getOptimizeOutput()
```


Flag indicates whether it is required to optimize output. If this flag is set redundant nested canvases and empty canvases are removed, also neighbor glyphs with the same formating are concatenated. Note: The accuracy of the content display may be affected if this property is set to  true . Default is  true .

 **Examples:** 

Shows how to simplify a document when saving it to HTML by removing various redundant objects.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions();
 {
     saveOptions.setOptimizeOutput(optimizeOutput);
 }

 doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html", saveOptions);

 // The size of the optimized version of the document is almost a third of the size of the unoptimized document.
 if (optimizeOutput)
     Assert.assertEquals(61889.0,
         new File(getArtifactsDir() + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html").length(), 200.0);
 else
     Assert.assertEquals(191770.0,
         new File(getArtifactsDir() + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html").length(), 200.0);
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getPageHorizontalAlignment() {#getPageHorizontalAlignment}
```
public int getPageHorizontalAlignment()
```


Specifies the horizontal alignment of pages in an HTML document. Default value is [HtmlFixedPageHorizontalAlignment.CENTER](../../com.aspose.words/htmlfixedpagehorizontalalignment/\#CENTER).

 **Examples:** 

Shows how to set the horizontal alignment of pages when saving a document to HTML.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();
 {
     htmlFixedSaveOptions.setPageHorizontalAlignment(pageHorizontalAlignment);
 }

 doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.HorizontalAlignment.html", htmlFixedSaveOptions);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlFixedSaveOptions.HorizontalAlignment/styles.css"), StandardCharsets.UTF_8);

 switch (pageHorizontalAlignment)
 {
     case HtmlFixedPageHorizontalAlignment.CENTER:
         Assert.assertTrue(Pattern.compile(
             "[.]awpage [{] position:relative; border:solid 1pt black; margin:10pt auto 10pt auto; overflow:hidden; [}]").matcher(outDocContents).find());
         break;
     case HtmlFixedPageHorizontalAlignment.LEFT:
         Assert.assertTrue(Pattern.compile(
             "[.]awpage [{] position:relative; border:solid 1pt black; margin:10pt auto 10pt 10pt; overflow:hidden; [}]").matcher(outDocContents).find());
         break;
     case HtmlFixedPageHorizontalAlignment.RIGHT:
         Assert.assertTrue(Pattern.compile(
             "[.]awpage [{] position:relative; border:solid 1pt black; margin:10pt 10pt 10pt auto; overflow:hidden; [}]").matcher(outDocContents).find());
         break;
 }
 
```

**Returns:**
int - The corresponding  int  value. The returned value is one of [HtmlFixedPageHorizontalAlignment](../../com.aspose.words/htmlfixedpagehorizontalalignment/) constants.
### getPageMargins() {#getPageMargins}
```
public double getPageMargins()
```


Specifies the margins around pages in an HTML document. The margins value is measured in points and should be equal to or greater than 0. Default value is 10 points.

 **Remarks:** 

Depends on the value of [getPageHorizontalAlignment()](../../com.aspose.words/htmlfixedsaveoptions/\#getPageHorizontalAlignment) / [setPageHorizontalAlignment(int)](../../com.aspose.words/htmlfixedsaveoptions/\#setPageHorizontalAlignment-int) property:

 *  Defines top, bottom and left page margins if the value is [HtmlFixedPageHorizontalAlignment.LEFT](../../com.aspose.words/htmlfixedpagehorizontalalignment/\#LEFT).
 *  Defines top, bottom and right page margins if the value is [HtmlFixedPageHorizontalAlignment.RIGHT](../../com.aspose.words/htmlfixedpagehorizontalalignment/\#RIGHT).
 *  Defines top and bottom page margins if the value is [HtmlFixedPageHorizontalAlignment.CENTER](../../com.aspose.words/htmlfixedpagehorizontalalignment/\#CENTER).

 **Examples:** 

Shows how to adjust page margins when saving a document to HTML.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions();
 {
     saveOptions.setPageMargins(15.0);
 }

 doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.PageMargins.html", saveOptions);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlFixedSaveOptions.PageMargins/styles.css"), StandardCharsets.UTF_8);

 Assert.assertTrue(Pattern.compile(
     "[.]awpage [{] position:relative; border:solid 1pt black; margin:15pt auto 15pt auto; overflow:hidden; [}]").matcher(outDocContents).find());
 
```

**Returns:**
double - The corresponding  double  value.
### getPageSavingCallback() {#getPageSavingCallback}
```
public IPageSavingCallback getPageSavingCallback()
```


Allows to control how separate pages are saved when a document is exported to fixed page format.

 **Examples:** 

Shows how to use a callback to save a document to HTML page by page.

```

 public void pageFileNames() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.writeln("Page 1.");
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.writeln("Page 2.");
     builder.insertImage(getImageDir() + "Logo.jpg");
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.writeln("Page 3.");

     // Create an "HtmlFixedSaveOptions" object, which we can pass to the document's "Save" method
     // to modify how we convert the document to HTML.
     HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();

     // We will save each page in this document to a separate HTML file in the local file system.
     // Set a callback that allows us to name each output HTML document.
     htmlFixedSaveOptions.setPageSavingCallback(new CustomFileNamePageSavingCallback());

     doc.save(getArtifactsDir() + "SavingCallback.PageFileNames.html", htmlFixedSaveOptions);

     String[] filePaths = DocumentHelper.directoryGetFiles(getArtifactsDir(), "SavingCallback.PageFileNames.Page_*").toArray(new String[0]);

     Assert.assertEquals(3, filePaths.length);
 }

 /// 
 /// Saves all pages to a file and directory specified within.
 /// 
 private static class CustomFileNamePageSavingCallback implements IPageSavingCallback {
     public void pageSaving(PageSavingArgs args) throws Exception {
         String outFileName = MessageFormat.format("{0}SavingCallback.PageFileNames.Page_{1}.html", getArtifactsDir(), args.getPageIndex());

         // Below are two ways of specifying where Aspose.Words will save each page of the document.
         // 1 -  Set a filename for the output page file:
         args.setPageFileName(outFileName);

         // 2 -  Create a custom stream for the output page file:
         try (FileOutputStream outputStream = new FileOutputStream(outFileName)) {
             args.setPageStream(outputStream);
         }

         Assert.assertFalse(args.getKeepPageStreamOpen());
     }
 }
 
```

**Returns:**
[IPageSavingCallback](../../com.aspose.words/ipagesavingcallback/) - The corresponding [IPageSavingCallback](../../com.aspose.words/ipagesavingcallback/) value.
### getPageSet() {#getPageSet}
```
public PageSet getPageSet()
```


Gets the pages to render. Default is all the pages in the document.

 **Examples:** 

Shows how to extract pages based on exact page indices.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add five pages to the document.
 for (int i = 1; i < 6; i++) {
     builder.write("Page " + i);
     builder.insertBreak(BreakType.PAGE_BREAK);
 }

 // Create an "XpsSaveOptions" object, which we can pass to the document's "Save" method
 // to modify how that method converts the document to .XPS.
 XpsSaveOptions xpsOptions = new XpsSaveOptions();

 // Use the "PageSet" property to select a set of the document's pages to save to output XPS.
 // In this case, we will choose, via a zero-based index, only three pages: page 1, page 2, and page 4.
 xpsOptions.setPageSet(new PageSet(0, 1, 3));

 doc.save(getArtifactsDir() + "XpsSaveOptions.ExportExactPages.xps", xpsOptions);
 
```

Shows how to convert only some of the pages in a document to PDF.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 3.");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Set the "PageIndex" to "1" to render a portion of the document starting from the second page.
 options.setPageSet(new PageSet(1));

 // This document will contain one page starting from page two, which will only contain the second page.
 doc.save(new FileOutputStream(getArtifactsDir() + "PdfSaveOptions.OnePage.pdf"), options);
 
```

Shows how to export Odd pages from the document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 for (int i = 0; i < 5; i++) {
     builder.writeln(MessageFormat.format("Page {0} ({1})", i + 1, (i % 2 == 0 ? "odd" : "even")));
     if (i < 4)
         builder.insertBreak(BreakType.PAGE_BREAK);
 }

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Below are three PageSet properties that we can use to filter out a set of pages from
 // our document to save in an output PDF document based on the parity of their page numbers.
 // 1 -  Save only the even-numbered pages:
 options.setPageSet(PageSet.getEven());

 doc.save(getArtifactsDir() + "PdfSaveOptions.ExportPageSet.Even.pdf", options);

 // 2 -  Save only the odd-numbered pages:
 options.setPageSet(PageSet.getOdd());

 doc.save(getArtifactsDir() + "PdfSaveOptions.ExportPageSet.Odd.pdf", options);

 // 3 -  Save every page:
 options.setPageSet(PageSet.getAll());

 doc.save(getArtifactsDir() + "PdfSaveOptions.ExportPageSet.All.pdf", options);
 
```

**Returns:**
[PageSet](../../com.aspose.words/pageset/) - The pages to render.
### getPrettyFormat() {#getPrettyFormat}
```
public boolean getPrettyFormat()
```


When  true , pretty formats output where applicable. Default value is  false .

 **Remarks:** 

Set to  true  to make HTML, MHTML, EPUB, WordML, RTF, DOCX and ODT output human readable. Useful for testing or debugging.

 **Examples:** 

Shows how to enhance the readability of the raw code of a saved .html document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 HtmlSaveOptions htmlOptions = new HtmlSaveOptions(SaveFormat.HTML);
 {
     htmlOptions.setPrettyFormat(usePrettyFormat);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.PrettyFormat.html", htmlOptions);

 // Enabling pretty format makes the raw html code more readable by adding tab stop and new line characters.
 String html = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlSaveOptions.PrettyFormat.html"), StandardCharsets.UTF_8);

 if (usePrettyFormat)
     Assert.assertEquals(
             "\r\n" +
                     "\t\r\n" +
                     "\t\t\r\n" +
                     "\t\t\r\n" +
                     MessageFormat.format("\t\t\r\n", BuildVersionInfo.getProduct(), BuildVersionInfo.getVersion()) +
                     "\t\t\r\n" +
                     "\t\t\r\n" +
                     "\t\r\n" +
                     "\t\r\n" +
                     "\t\t \r\n" +
                     "\t\t\t \r\n" +
                     "\t\t\t\tHello world!\r\n" +
                     "\t\t\t\r\n" +
                     "\t\t\t \r\n" +
                     "\t\t\t\t \r\n" +
                     "\t\t\t\r\n" +
                     "\t\t\r\n" +
                     "\t\r\n",
             html);
 else
     Assert.assertEquals(
             "" +
                     "" +
                     MessageFormat.format("", BuildVersionInfo.getProduct(), BuildVersionInfo.getVersion()) +
                     "" +
                     " Hello world!" +
                     "  ",
             html);
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getProgressCallback() {#getProgressCallback}
```
public IDocumentSavingCallback getProgressCallback()
```


Called during saving a document and accepts data about saving progress.

 **Remarks:** 

Progress is reported when saving to [SaveFormat.DOCX](../../com.aspose.words/saveformat/\#DOCX), [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat/\#FLAT-OPC), [SaveFormat.DOCM](../../com.aspose.words/saveformat/\#DOCM), [SaveFormat.DOTM](../../com.aspose.words/saveformat/\#DOTM), [SaveFormat.DOTX](../../com.aspose.words/saveformat/\#DOTX), [SaveFormat.DOC](../../com.aspose.words/saveformat/\#DOC), [SaveFormat.DOT](../../com.aspose.words/saveformat/\#DOT), [SaveFormat.HTML](../../com.aspose.words/saveformat/\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat/\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat/\#EPUB), [SaveFormat.XAML\_FLOW](../../com.aspose.words/saveformat/\#XAML-FLOW), or [SaveFormat.XAML\_FLOW\_PACK](../../com.aspose.words/saveformat/\#XAML-FLOW-PACK).

 **Examples:** 

Shows how to manage a document while saving to xamlflow.

```

 public void progressCallback(int saveFormat, String ext) throws Exception
 {
     Document doc = new Document(getMyDir() + "Big document.docx");

     // Following formats are supported: XamlFlow, XamlFlowPack.
     XamlFlowSaveOptions saveOptions = new XamlFlowSaveOptions(saveFormat);
     {
         saveOptions.setProgressCallback(new SavingProgressCallback());
     }

     try {
         doc.save(getArtifactsDir() + MessageFormat.format("XamlFlowSaveOptions.ProgressCallback.{0}", ext), saveOptions);
     }
     catch (IllegalStateException exception) {
         Assert.assertTrue(exception.getMessage().contains("EstimatedProgress"));
     }
 }

 public static Object[][] progressCallbackDataProvider() throws Exception
 {
     return new Object[][]
             {
                     {SaveFormat.XAML_FLOW,  "xamlflow"},
                     {SaveFormat.XAML_FLOW_PACK,  "xamlflowpack"},
             };
 }

 /// 
 /// Saving progress callback. Cancel a document saving after the "MaxDuration" seconds.
 /// 
 public static class SavingProgressCallback implements IDocumentSavingCallback
 {
     /// 
     /// Ctr.
     /// 
     public SavingProgressCallback()
     {
         mSavingStartedAt = new Date();
     }

     /// 
     /// Callback method which called during document saving.
     /// 
     /// Saving arguments.
     public void notify(DocumentSavingArgs args)
     {
         Date canceledAt = new Date();
         long diff = canceledAt.getTime() - mSavingStartedAt.getTime();
         long ellapsedSeconds = TimeUnit.MILLISECONDS.toSeconds(diff);

         if (ellapsedSeconds > MAX_DURATION)
             throw new IllegalStateException(MessageFormat.format("EstimatedProgress = {0}; CanceledAt = {1}", args.getEstimatedProgress(), canceledAt));
     }

     /// 
     /// Date and time when document saving is started.
     /// 
     private Date mSavingStartedAt;

     /// 
     /// Maximum allowed duration in sec.
     /// 
     private static final double MAX_DURATION = 0.01d;
 }
 
```

Shows how to manage a document while saving to html.

```

 public void progressCallback(int saveFormat, String ext) throws Exception
 {
     Document doc = new Document(getMyDir() + "Big document.docx");

     // Following formats are supported: Html, Mhtml, Epub.
     HtmlSaveOptions saveOptions = new HtmlSaveOptions(saveFormat);
     {
         saveOptions.setProgressCallback(new SavingProgressCallback());
     }

     try {
         doc.save(getArtifactsDir() + MessageFormat.format("HtmlSaveOptions.ProgressCallback.{0}", ext), saveOptions);
     }
     catch (IllegalStateException exception) {
         Assert.assertTrue(exception.getMessage().contains("EstimatedProgress"));
     }

 }

 public static Object[][] progressCallbackDataProvider() throws Exception
 {
     return new Object[][]
             {
                     {SaveFormat.HTML,  "html"},
                     {SaveFormat.MHTML,  "mhtml"},
                     {SaveFormat.EPUB,  "epub"},
             };
 }

 /// 
 /// Saving progress callback. Cancel a document saving after the "MaxDuration" seconds.
 /// 
 public static class SavingProgressCallback implements IDocumentSavingCallback
 {
     /// 
     /// Ctr.
     /// 
     public SavingProgressCallback()
     {
         mSavingStartedAt = new Date();
     }

     /// 
     /// Callback method which called during document saving.
     /// 
     /// Saving arguments.
     public void notify(DocumentSavingArgs args)
     {
         Date canceledAt = new Date();
         long diff = canceledAt.getTime() - mSavingStartedAt.getTime();
         long ellapsedSeconds = TimeUnit.MILLISECONDS.toSeconds(diff);

         if (ellapsedSeconds > MAX_DURATION)
             throw new IllegalStateException(MessageFormat.format("EstimatedProgress = {0}; CanceledAt = {1}", args.getEstimatedProgress(), canceledAt));
     }

     /// 
     /// Date and time when document saving is started.
     /// 
     private Date mSavingStartedAt;

     /// 
     /// Maximum allowed duration in sec.
     /// 
     private static final double MAX_DURATION = 0.01d;
 }
 
```

Shows how to manage a document while saving to docx.

```

 public void progressCallback(int saveFormat, String ext) throws Exception
 {
     Document doc = new Document(getMyDir() + "Big document.docx");

     // Following formats are supported: Docx, FlatOpc, Docm, Dotm, Dotx.
     OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(saveFormat);
     {
         saveOptions.setProgressCallback(new SavingProgressCallback());
     }

     try {
         doc.save(getArtifactsDir() + MessageFormat.format("OoxmlSaveOptions.ProgressCallback.{0}", ext), saveOptions);
     }
     catch (IllegalStateException exception) {
         Assert.assertTrue(exception.getMessage().contains("EstimatedProgress"));
     }
 }

 public static Object[][] progressCallbackDataProvider() throws Exception
 {
     return new Object[][]
             {
                     {SaveFormat.DOCX,  "docx"},
                     {SaveFormat.DOCM,  "docm"},
                     {SaveFormat.DOTM,  "dotm"},
                     {SaveFormat.DOTX,  "dotx"},
                     {SaveFormat.FLAT_OPC,  "flatopc"},
             };
 }

 /// 
 /// Saving progress callback. Cancel a document saving after the "MaxDuration" seconds.
 /// 
 public static class SavingProgressCallback implements IDocumentSavingCallback
 {
     /// 
     /// Ctr.
     /// 
     public SavingProgressCallback()
     {
         mSavingStartedAt = new Date();
     }

     /// 
     /// Callback method which called during document saving.
     /// 
     /// Saving arguments.
     public void notify(DocumentSavingArgs args)
     {
         Date canceledAt = new Date();
         long diff = canceledAt.getTime() - mSavingStartedAt.getTime();
         long ellapsedSeconds = TimeUnit.MILLISECONDS.toSeconds(diff);

         if (ellapsedSeconds > MAX_DURATION)
             throw new IllegalStateException(MessageFormat.format("EstimatedProgress = {0}; CanceledAt = {1}", args.getEstimatedProgress(), canceledAt));
     }

     /// 
     /// Date and time when document saving is started.
     /// 
     private Date mSavingStartedAt;

     /// 
     /// Maximum allowed duration in sec.
     /// 
     private static final double MAX_DURATION = 0.01d;
 }
 
```

**Returns:**
[IDocumentSavingCallback](../../com.aspose.words/idocumentsavingcallback/) - The corresponding [IDocumentSavingCallback](../../com.aspose.words/idocumentsavingcallback/) value.
### getResourceSavingCallback() {#getResourceSavingCallback}
```
public IResourceSavingCallback getResourceSavingCallback()
```


Allows to control how resources (images, fonts and css) are saved when a document is exported to fixed page Html format.

 **Examples:** 

Shows how to use a callback to print the URIs of external resources created while converting a document to HTML.

```

 public void htmlFixedResourceFolder() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     ResourceUriPrinter callback = new ResourceUriPrinter();

     HtmlFixedSaveOptions options = new HtmlFixedSaveOptions();
     {
         options.setSaveFormat(SaveFormat.HTML_FIXED);
         options.setExportEmbeddedImages(false);
         options.setResourcesFolder(getArtifactsDir() + "HtmlFixedResourceFolder");
         options.setResourcesFolderAlias(getArtifactsDir() + "HtmlFixedResourceFolderAlias");
         options.setShowPageBorder(false);
         options.setResourceSavingCallback(callback);
     }

     // A folder specified by ResourcesFolderAlias will contain the resources instead of ResourcesFolder.
     // We must ensure the folder exists before the streams can put their resources into it.
     new File(options.getResourcesFolderAlias()).mkdir();

     doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.HtmlFixedResourceFolder.html", options);

     System.out.println(callback.getText());

     String[] resourceFiles = new File(getArtifactsDir() + "HtmlFixedResourceFolderAlias").list();

     Assert.assertFalse(new File(getArtifactsDir() + "HtmlFixedResourceFolder").exists());
     Assert.assertEquals(6, IterableUtils.countMatches(Arrays.asList(resourceFiles),
             f -> f.endsWith(".jpeg") || f.endsWith(".png") || f.endsWith(".css")));
 }

 /// 
 /// Counts and prints URIs of resources contained by as they are converted to fixed HTML.
 /// 
 private static class ResourceUriPrinter implements IResourceSavingCallback {
     public void resourceSaving(ResourceSavingArgs args) throws Exception {
         // If we set a folder alias in the SaveOptions object, we will be able to print it from here.
         mText.append(MessageFormat.format("Resource #{0} \"{1}\"", ++mSavedResourceCount, args.getResourceFileName()));

         String extension = FilenameUtils.getExtension(args.getResourceFileName());
         switch (extension) {
             case "ttf":
             case "woff": {
                 // By default, 'ResourceFileUri' uses system folder for fonts.
                 // To avoid problems in other platforms you must explicitly specify the path for the fonts.
                 args.setResourceFileUri(getArtifactsDir() + File.separatorChar + args.getResourceFileName());
                 break;
             }
         }

         mText.append("\t" + args.getResourceFileUri());

         // If we have specified a folder in the "ResourcesFolderAlias" property,
         // we will also need to redirect each stream to put its resource in that folder.
         args.setResourceStream(new FileOutputStream(args.getResourceFileUri()));
         args.setKeepResourceStreamOpen(false);
     }

     public String getText() {
         return mText.toString();
     }

     private int mSavedResourceCount;
     private final  StringBuilder mText = new StringBuilder();
 }
 
```

**Returns:**
[IResourceSavingCallback](../../com.aspose.words/iresourcesavingcallback/) - The corresponding [IResourceSavingCallback](../../com.aspose.words/iresourcesavingcallback/) value.
### getResourcesFolder() {#getResourcesFolder}
```
public String getResourcesFolder()
```


Specifies the physical folder where resources (images, fonts, css) are saved when exporting a document to Html format. Default is  null .

 **Remarks:** 

Has effect only if [getExportEmbeddedImages()](../../com.aspose.words/htmlfixedsaveoptions/\#getExportEmbeddedImages) / [setExportEmbeddedImages(boolean)](../../com.aspose.words/htmlfixedsaveoptions/\#setExportEmbeddedImages-boolean) property is  false .

When you save a [Document](../../com.aspose.words/document/) in Html format, Aspose.Words needs to save all images embedded in the document as standalone files. [getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolder) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolder-java.lang.String) allows you to specify where the images will be saved and [getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolderAlias) / [setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolderAlias-java.lang.String) allows to specify how the image URIs will be constructed.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the images in the same folder where the document file is saved. Use [getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolder) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolder-java.lang.String) to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the images, but still needs to save the images somewhere. In this case, you need to specify an accessible folder by using the [getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolder) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolder-java.lang.String) property

 **Examples:** 

Shows how to use a callback to print the URIs of external resources created while converting a document to HTML.

```

 public void htmlFixedResourceFolder() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     ResourceUriPrinter callback = new ResourceUriPrinter();

     HtmlFixedSaveOptions options = new HtmlFixedSaveOptions();
     {
         options.setSaveFormat(SaveFormat.HTML_FIXED);
         options.setExportEmbeddedImages(false);
         options.setResourcesFolder(getArtifactsDir() + "HtmlFixedResourceFolder");
         options.setResourcesFolderAlias(getArtifactsDir() + "HtmlFixedResourceFolderAlias");
         options.setShowPageBorder(false);
         options.setResourceSavingCallback(callback);
     }

     // A folder specified by ResourcesFolderAlias will contain the resources instead of ResourcesFolder.
     // We must ensure the folder exists before the streams can put their resources into it.
     new File(options.getResourcesFolderAlias()).mkdir();

     doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.HtmlFixedResourceFolder.html", options);

     System.out.println(callback.getText());

     String[] resourceFiles = new File(getArtifactsDir() + "HtmlFixedResourceFolderAlias").list();

     Assert.assertFalse(new File(getArtifactsDir() + "HtmlFixedResourceFolder").exists());
     Assert.assertEquals(6, IterableUtils.countMatches(Arrays.asList(resourceFiles),
             f -> f.endsWith(".jpeg") || f.endsWith(".png") || f.endsWith(".css")));
 }

 /// 
 /// Counts and prints URIs of resources contained by as they are converted to fixed HTML.
 /// 
 private static class ResourceUriPrinter implements IResourceSavingCallback {
     public void resourceSaving(ResourceSavingArgs args) throws Exception {
         // If we set a folder alias in the SaveOptions object, we will be able to print it from here.
         mText.append(MessageFormat.format("Resource #{0} \"{1}\"", ++mSavedResourceCount, args.getResourceFileName()));

         String extension = FilenameUtils.getExtension(args.getResourceFileName());
         switch (extension) {
             case "ttf":
             case "woff": {
                 // By default, 'ResourceFileUri' uses system folder for fonts.
                 // To avoid problems in other platforms you must explicitly specify the path for the fonts.
                 args.setResourceFileUri(getArtifactsDir() + File.separatorChar + args.getResourceFileName());
                 break;
             }
         }

         mText.append("\t" + args.getResourceFileUri());

         // If we have specified a folder in the "ResourcesFolderAlias" property,
         // we will also need to redirect each stream to put its resource in that folder.
         args.setResourceStream(new FileOutputStream(args.getResourceFileUri()));
         args.setKeepResourceStreamOpen(false);
     }

     public String getText() {
         return mText.toString();
     }

     private int mSavedResourceCount;
     private final  StringBuilder mText = new StringBuilder();
 }
 
```

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getResourcesFolderAlias() {#getResourcesFolderAlias}
```
public String getResourcesFolderAlias()
```


Specifies the name of the folder used to construct image URIs written into an Html document. Default is  null .

 **Remarks:** 

When you save a [Document](../../com.aspose.words/document/) in Html format, Aspose.Words needs to save all images embedded in the document as standalone files. [getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolder) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolder-java.lang.String) allows you to specify where the images will be saved and [getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolderAlias) / [setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolderAlias-java.lang.String) allows to specify how the image URIs will be constructed.

 **Examples:** 

Shows how to use a callback to print the URIs of external resources created while converting a document to HTML.

```

 public void htmlFixedResourceFolder() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     ResourceUriPrinter callback = new ResourceUriPrinter();

     HtmlFixedSaveOptions options = new HtmlFixedSaveOptions();
     {
         options.setSaveFormat(SaveFormat.HTML_FIXED);
         options.setExportEmbeddedImages(false);
         options.setResourcesFolder(getArtifactsDir() + "HtmlFixedResourceFolder");
         options.setResourcesFolderAlias(getArtifactsDir() + "HtmlFixedResourceFolderAlias");
         options.setShowPageBorder(false);
         options.setResourceSavingCallback(callback);
     }

     // A folder specified by ResourcesFolderAlias will contain the resources instead of ResourcesFolder.
     // We must ensure the folder exists before the streams can put their resources into it.
     new File(options.getResourcesFolderAlias()).mkdir();

     doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.HtmlFixedResourceFolder.html", options);

     System.out.println(callback.getText());

     String[] resourceFiles = new File(getArtifactsDir() + "HtmlFixedResourceFolderAlias").list();

     Assert.assertFalse(new File(getArtifactsDir() + "HtmlFixedResourceFolder").exists());
     Assert.assertEquals(6, IterableUtils.countMatches(Arrays.asList(resourceFiles),
             f -> f.endsWith(".jpeg") || f.endsWith(".png") || f.endsWith(".css")));
 }

 /// 
 /// Counts and prints URIs of resources contained by as they are converted to fixed HTML.
 /// 
 private static class ResourceUriPrinter implements IResourceSavingCallback {
     public void resourceSaving(ResourceSavingArgs args) throws Exception {
         // If we set a folder alias in the SaveOptions object, we will be able to print it from here.
         mText.append(MessageFormat.format("Resource #{0} \"{1}\"", ++mSavedResourceCount, args.getResourceFileName()));

         String extension = FilenameUtils.getExtension(args.getResourceFileName());
         switch (extension) {
             case "ttf":
             case "woff": {
                 // By default, 'ResourceFileUri' uses system folder for fonts.
                 // To avoid problems in other platforms you must explicitly specify the path for the fonts.
                 args.setResourceFileUri(getArtifactsDir() + File.separatorChar + args.getResourceFileName());
                 break;
             }
         }

         mText.append("\t" + args.getResourceFileUri());

         // If we have specified a folder in the "ResourcesFolderAlias" property,
         // we will also need to redirect each stream to put its resource in that folder.
         args.setResourceStream(new FileOutputStream(args.getResourceFileUri()));
         args.setKeepResourceStreamOpen(false);
     }

     public String getText() {
         return mText.toString();
     }

     private int mSavedResourceCount;
     private final  StringBuilder mText = new StringBuilder();
 }
 
```

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getSaveFontFaceCssSeparately() {#getSaveFontFaceCssSeparately}
```
public boolean getSaveFontFaceCssSeparately()
```


Flag indicates whether "@font-face" CSS rules should be placed into a separate file "fontFaces.css" when a document is being saved with external stylesheet (that is, when [getExportEmbeddedCss()](../../com.aspose.words/htmlfixedsaveoptions/\#getExportEmbeddedCss) / [setExportEmbeddedCss(boolean)](../../com.aspose.words/htmlfixedsaveoptions/\#setExportEmbeddedCss-boolean) is  false ). Default value is  false , all CSS rules are written into single file "styles.css".

 **Remarks:** 

Setting this property to  true  restores the old behavior (separate files) for compatibility with legacy code.

 **Examples:** 

Shows how to place CSS into a separate file and add a prefix to all of its CSS class names.

```

 Document doc = new Document(getMyDir() + "Bookmarks.docx");

 HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();
 {
     htmlFixedSaveOptions.setCssClassNamesPrefix("myprefix");
     htmlFixedSaveOptions.setSaveFontFaceCssSeparately(true);
 }

 doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.AddCssClassNamesPrefix.html", htmlFixedSaveOptions);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlFixedSaveOptions.AddCssClassNamesPrefix.html"), StandardCharsets.UTF_8);

 Assert.assertTrue(Pattern.compile(
     " " +
     " " +
     "").matcher(outDocContents).find());

 outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlFixedSaveOptions.AddCssClassNamesPrefix/styles.css"), StandardCharsets.UTF_8);

 Assert.assertTrue(Pattern.compile(
     ".myprefixdiv [{] position:absolute; [}] " +
     ".myprefixspan [{] position:absolute; white-space:pre; color:#000000; font-size:12pt; [}]").matcher(outDocContents).find());
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getSaveFormat() {#getSaveFormat}
```
public int getSaveFormat()
```


Specifies the format in which the document will be saved if this save options object is used. Can only be [SaveFormat.HTML\_FIXED](../../com.aspose.words/saveformat/\#HTML-FIXED).

 **Examples:** 

Shows how to use a callback to print the URIs of external resources created while converting a document to HTML.

```

 public void htmlFixedResourceFolder() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     ResourceUriPrinter callback = new ResourceUriPrinter();

     HtmlFixedSaveOptions options = new HtmlFixedSaveOptions();
     {
         options.setSaveFormat(SaveFormat.HTML_FIXED);
         options.setExportEmbeddedImages(false);
         options.setResourcesFolder(getArtifactsDir() + "HtmlFixedResourceFolder");
         options.setResourcesFolderAlias(getArtifactsDir() + "HtmlFixedResourceFolderAlias");
         options.setShowPageBorder(false);
         options.setResourceSavingCallback(callback);
     }

     // A folder specified by ResourcesFolderAlias will contain the resources instead of ResourcesFolder.
     // We must ensure the folder exists before the streams can put their resources into it.
     new File(options.getResourcesFolderAlias()).mkdir();

     doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.HtmlFixedResourceFolder.html", options);

     System.out.println(callback.getText());

     String[] resourceFiles = new File(getArtifactsDir() + "HtmlFixedResourceFolderAlias").list();

     Assert.assertFalse(new File(getArtifactsDir() + "HtmlFixedResourceFolder").exists());
     Assert.assertEquals(6, IterableUtils.countMatches(Arrays.asList(resourceFiles),
             f -> f.endsWith(".jpeg") || f.endsWith(".png") || f.endsWith(".css")));
 }

 /// 
 /// Counts and prints URIs of resources contained by as they are converted to fixed HTML.
 /// 
 private static class ResourceUriPrinter implements IResourceSavingCallback {
     public void resourceSaving(ResourceSavingArgs args) throws Exception {
         // If we set a folder alias in the SaveOptions object, we will be able to print it from here.
         mText.append(MessageFormat.format("Resource #{0} \"{1}\"", ++mSavedResourceCount, args.getResourceFileName()));

         String extension = FilenameUtils.getExtension(args.getResourceFileName());
         switch (extension) {
             case "ttf":
             case "woff": {
                 // By default, 'ResourceFileUri' uses system folder for fonts.
                 // To avoid problems in other platforms you must explicitly specify the path for the fonts.
                 args.setResourceFileUri(getArtifactsDir() + File.separatorChar + args.getResourceFileName());
                 break;
             }
         }

         mText.append("\t" + args.getResourceFileUri());

         // If we have specified a folder in the "ResourcesFolderAlias" property,
         // we will also need to redirect each stream to put its resource in that folder.
         args.setResourceStream(new FileOutputStream(args.getResourceFileUri()));
         args.setKeepResourceStreamOpen(false);
     }

     public String getText() {
         return mText.toString();
     }

     private int mSavedResourceCount;
     private final  StringBuilder mText = new StringBuilder();
 }
 
```

**Returns:**
int - The corresponding  int  value. The returned value is one of [SaveFormat](../../com.aspose.words/saveformat/) constants.
### getShowPageBorder() {#getShowPageBorder}
```
public boolean getShowPageBorder()
```


Specifies whether border around pages should be shown. Default is  true .

 **Examples:** 

Shows how to use a callback to print the URIs of external resources created while converting a document to HTML.

```

 public void htmlFixedResourceFolder() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     ResourceUriPrinter callback = new ResourceUriPrinter();

     HtmlFixedSaveOptions options = new HtmlFixedSaveOptions();
     {
         options.setSaveFormat(SaveFormat.HTML_FIXED);
         options.setExportEmbeddedImages(false);
         options.setResourcesFolder(getArtifactsDir() + "HtmlFixedResourceFolder");
         options.setResourcesFolderAlias(getArtifactsDir() + "HtmlFixedResourceFolderAlias");
         options.setShowPageBorder(false);
         options.setResourceSavingCallback(callback);
     }

     // A folder specified by ResourcesFolderAlias will contain the resources instead of ResourcesFolder.
     // We must ensure the folder exists before the streams can put their resources into it.
     new File(options.getResourcesFolderAlias()).mkdir();

     doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.HtmlFixedResourceFolder.html", options);

     System.out.println(callback.getText());

     String[] resourceFiles = new File(getArtifactsDir() + "HtmlFixedResourceFolderAlias").list();

     Assert.assertFalse(new File(getArtifactsDir() + "HtmlFixedResourceFolder").exists());
     Assert.assertEquals(6, IterableUtils.countMatches(Arrays.asList(resourceFiles),
             f -> f.endsWith(".jpeg") || f.endsWith(".png") || f.endsWith(".css")));
 }

 /// 
 /// Counts and prints URIs of resources contained by as they are converted to fixed HTML.
 /// 
 private static class ResourceUriPrinter implements IResourceSavingCallback {
     public void resourceSaving(ResourceSavingArgs args) throws Exception {
         // If we set a folder alias in the SaveOptions object, we will be able to print it from here.
         mText.append(MessageFormat.format("Resource #{0} \"{1}\"", ++mSavedResourceCount, args.getResourceFileName()));

         String extension = FilenameUtils.getExtension(args.getResourceFileName());
         switch (extension) {
             case "ttf":
             case "woff": {
                 // By default, 'ResourceFileUri' uses system folder for fonts.
                 // To avoid problems in other platforms you must explicitly specify the path for the fonts.
                 args.setResourceFileUri(getArtifactsDir() + File.separatorChar + args.getResourceFileName());
                 break;
             }
         }

         mText.append("\t" + args.getResourceFileUri());

         // If we have specified a folder in the "ResourcesFolderAlias" property,
         // we will also need to redirect each stream to put its resource in that folder.
         args.setResourceStream(new FileOutputStream(args.getResourceFileUri()));
         args.setKeepResourceStreamOpen(false);
     }

     public String getText() {
         return mText.toString();
     }

     private int mSavedResourceCount;
     private final  StringBuilder mText = new StringBuilder();
 }
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getTempFolder() {#getTempFolder}
```
public String getTempFolder()
```


Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default this property is  null  and no temporary files are used.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getUpdateCreatedTimeProperty() {#getUpdateCreatedTimeProperty}
```
public boolean getUpdateCreatedTimeProperty()
```


Gets a value determining whether the [BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties/\#getCreatedTime) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setCreatedTime-java.util.Date) property is updated before saving. Default value is  false ;

 **Examples:** 

Shows how to update a document's "CreatedTime" property when saving.

```

 Document doc = new Document();

 Calendar calendar = Calendar.getInstance();
 calendar.set(2019, 11, 20);
 doc.getBuiltInDocumentProperties().setCreatedTime(calendar.getTime());

 // This flag determines whether the created time, which is a built-in property, is updated.
 // If so, then the date of the document's most recent save operation
 // with this SaveOptions object passed as a parameter is used as the created time.
 DocSaveOptions saveOptions = new DocSaveOptions();
 saveOptions.setUpdateCreatedTimeProperty(isUpdateCreatedTimeProperty);

 doc.save(getArtifactsDir() + "DocSaveOptions.UpdateCreatedTimeProperty.docx", saveOptions);
 
```

**Returns:**
boolean - A value determining whether the [BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties/\#getCreatedTime) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setCreatedTime-java.util.Date) property is updated before saving.
### getUpdateFields() {#getUpdateFields}
```
public boolean getUpdateFields()
```


Gets a value determining if fields of certain types should be updated before saving the document to a fixed page format. Default value for this property is  true .

 **Remarks:** 

Allows to specify whether to mimic or not MS Word behavior.

 **Examples:** 

Shows how to update all the fields in a document immediately before saving it to PDF.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert text with PAGE and NUMPAGES fields. These fields do not display the correct value in real time.
 // We will need to manually update them using updating methods such as "Field.Update()", and "Document.UpdateFields()"
 // each time we need them to display accurate values.
 builder.write("Page ");
 builder.insertField("PAGE", "");
 builder.write(" of ");
 builder.insertField("NUMPAGES", "");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Hello World!");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Set the "UpdateFields" property to "false" to not update all the fields in a document right before a save operation.
 // This is the preferable option if we know that all our fields will be up to date before saving.
 // Set the "UpdateFields" property to "true" to iterate through all the document
 // fields and update them before we save it as a PDF. This will make sure that all the fields will display
 // the most accurate values in the PDF.
 options.setUpdateFields(updateFields);

 // We can clone PdfSaveOptions objects.
 Assert.assertNotSame(options, options.deepClone());

 doc.save(getArtifactsDir() + "PdfSaveOptions.UpdateFields.pdf", options);
 
```

**Returns:**
boolean - A value determining if fields of certain types should be updated before saving the document to a fixed page format.
### getUpdateLastPrintedProperty() {#getUpdateLastPrintedProperty}
```
public boolean getUpdateLastPrintedProperty()
```


Gets a value determining whether the [BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties/\#getLastPrinted) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastPrinted-java.util.Date) property is updated before saving.

 **Examples:** 

Shows how to update a document's "Last printed" property when saving.

```

 Document doc = new Document();

 Calendar calendar = Calendar.getInstance();
 calendar.set(2019, 11, 20);
 doc.getBuiltInDocumentProperties().setLastPrinted(calendar.getTime());

 // This flag determines whether the last printed date, which is a built-in property, is updated.
 // If so, then the date of the document's most recent save operation
 // with this SaveOptions object passed as a parameter is used as the print date.
 DocSaveOptions saveOptions = new DocSaveOptions();
 saveOptions.setUpdateLastPrintedProperty(isUpdateLastPrintedProperty);

 // In Microsoft Word 2003, this property can be found via File -> Properties -> Statistics -> Printed.
 // It can also be displayed in the document's body by using a PRINTDATE field.
 doc.save(getArtifactsDir() + "DocSaveOptions.UpdateLastPrintedProperty.doc", saveOptions);
 
```

**Returns:**
boolean - A value determining whether the [BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties/\#getLastPrinted) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastPrinted-java.util.Date) property is updated before saving.
### getUpdateLastSavedTimeProperty() {#getUpdateLastSavedTimeProperty}
```
public boolean getUpdateLastSavedTimeProperty()
```


Gets a value determining whether the [BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties/\#getLastSavedTime) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastSavedTime-java.util.Date) property is updated before saving.

 **Examples:** 

Shows how to determine whether to preserve the document's "Last saved time" property when saving.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 // When we save the document to an OOXML format, we can create an OoxmlSaveOptions object
 // and then pass it to the document's saving method to modify how we save the document.
 // Set the "UpdateLastSavedTimeProperty" property to "true" to
 // set the output document's "Last saved time" built-in property to the current date/time.
 // Set the "UpdateLastSavedTimeProperty" property to "false" to
 // preserve the original value of the input document's "Last saved time" built-in property.
 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 saveOptions.setUpdateLastSavedTimeProperty(updateLastSavedTimeProperty);

 doc.save(getArtifactsDir() + "OoxmlSaveOptions.LastSavedTime.docx", saveOptions);
 
```

**Returns:**
boolean - A value determining whether the [BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties/\#getLastSavedTime) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastSavedTime-java.util.Date) property is updated before saving.
### getUseAntiAliasing() {#getUseAntiAliasing}
```
public boolean getUseAntiAliasing()
```


Gets a value determining whether or not to use anti-aliasing for rendering.

 **Remarks:** 

The default value is  false . When this value is set to  true  anti-aliasing is used for rendering.

This property is used when the document is exported to the following formats: [SaveFormat.TIFF](../../com.aspose.words/saveformat/\#TIFF), [SaveFormat.PNG](../../com.aspose.words/saveformat/\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat/\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat/\#JPEG), [SaveFormat.EMF](../../com.aspose.words/saveformat/\#EMF). When the document is exported to the [SaveFormat.HTML](../../com.aspose.words/saveformat/\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat/\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat/\#EPUB), [SaveFormat.AZW\_3](../../com.aspose.words/saveformat/\#AZW-3) or [SaveFormat.MOBI](../../com.aspose.words/saveformat/\#MOBI) formats this option is used for raster images.

 **Examples:** 

Shows how to improve the quality of a rendered document with SaveOptions.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(60.0);
 builder.writeln("Some text.");

 SaveOptions options = new ImageSaveOptions(SaveFormat.JPEG);
 doc.save(getArtifactsDir() + "Document.ImageSaveOptions.Default.jpg", options);

 options.setUseAntiAliasing(true);
 options.setUseHighQualityRendering(true);

 doc.save(getArtifactsDir() + "Document.ImageSaveOptions.HighQuality.jpg", options);
 
```

**Returns:**
boolean - A value determining whether or not to use anti-aliasing for rendering.
### getUseHighQualityRendering() {#getUseHighQualityRendering}
```
public boolean getUseHighQualityRendering()
```


Gets a value determining whether or not to use high quality (i.e. slow) rendering algorithms.

 **Remarks:** 

The default value is  false .

This property is used when the document is exported to image formats: [SaveFormat.TIFF](../../com.aspose.words/saveformat/\#TIFF), [SaveFormat.PNG](../../com.aspose.words/saveformat/\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat/\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat/\#JPEG), [SaveFormat.EMF](../../com.aspose.words/saveformat/\#EMF).

 **Examples:** 

Shows how to improve the quality of a rendered document with SaveOptions.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(60.0);
 builder.writeln("Some text.");

 SaveOptions options = new ImageSaveOptions(SaveFormat.JPEG);
 doc.save(getArtifactsDir() + "Document.ImageSaveOptions.Default.jpg", options);

 options.setUseAntiAliasing(true);
 options.setUseHighQualityRendering(true);

 doc.save(getArtifactsDir() + "Document.ImageSaveOptions.HighQuality.jpg", options);
 
```

**Returns:**
boolean - A value determining whether or not to use high quality (i.e.
### getUseTargetMachineFonts() {#getUseTargetMachineFonts}
```
public boolean getUseTargetMachineFonts()
```


Flag indicates whether fonts from target machine must be used to display the document. If this flag is set to  true , [getFontFormat()](../../com.aspose.words/htmlfixedsaveoptions/\#getFontFormat) / [setFontFormat(int)](../../com.aspose.words/htmlfixedsaveoptions/\#setFontFormat-int) and [getExportEmbeddedFonts()](../../com.aspose.words/htmlfixedsaveoptions/\#getExportEmbeddedFonts) / [setExportEmbeddedFonts(boolean)](../../com.aspose.words/htmlfixedsaveoptions/\#setExportEmbeddedFonts-boolean) properties do not have effect, also [getResourceSavingCallback()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourceSavingCallback) / [setResourceSavingCallback(com.aspose.words.IResourceSavingCallback)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourceSavingCallback-com.aspose.words.IResourceSavingCallback) is not fired for fonts. Default is  false .

 **Examples:** 

Shows how use fonts only from the target machine when saving a document to HTML.

```

 Document doc = new Document(getMyDir() + "Bullet points with alternative font.docx");

 HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions();
 {
     saveOptions.setExportEmbeddedCss(true);
     saveOptions.setUseTargetMachineFonts(useTargetMachineFonts);
     saveOptions.setFontFormat(ExportFontFormat.TTF);
     saveOptions.setExportEmbeddedFonts(false);
 }

 doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.UsingMachineFonts.html", saveOptions);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlFixedSaveOptions.UsingMachineFonts.html"), StandardCharsets.UTF_8);

 if (useTargetMachineFonts)
     Assert.assertFalse(Pattern.compile("@font-face").matcher(outDocContents).find());
 else
     Assert.assertTrue(Pattern.compile(
         "@font-face [{] font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'\u263a'[)], " +
         "url[(]'HtmlFixedSaveOptions.UsingMachineFonts/font001.ttf'[)] format[(]'truetype'[)]; [}]").matcher(outDocContents).find());
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### setAllowEmbeddingPostScriptFonts(boolean value) {#setAllowEmbeddingPostScriptFonts-boolean}
```
public void setAllowEmbeddingPostScriptFonts(boolean value)
```


Sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is  false .

 **Remarks:** 

Note, Word does not embed PostScript fonts, but can open documents with embedded fonts of this type.

This option only works when [FontInfoCollection.getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection/\#getEmbedTrueTypeFonts) / [FontInfoCollection.setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection/\#setEmbedTrueTypeFonts-boolean) of the [DocumentBase.getFontInfos()](../../com.aspose.words/documentbase/\#getFontInfos) property is set to  true .

 **Examples:** 

Shows how to save the document with PostScript font.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setName("PostScriptFont");
 builder.writeln("Some text with PostScript font.");

 // Load the font with PostScript to use in the document.
 MemoryFontSource otf = new MemoryFontSource(DocumentHelper.getBytesFromStream(new FileInputStream(getFontsDir() + "AllegroOpen.otf")));
 doc.setFontSettings(new FontSettings());
 doc.getFontSettings().setFontsSources(new FontSourceBase[]{otf});

 // Embed TrueType fonts.
 doc.getFontInfos().setEmbedTrueTypeFonts(true);

 // Allow embedding PostScript fonts while embedding TrueType fonts.
 // Microsoft Word does not embed PostScript fonts, but can open documents with embedded fonts of this type.
 SaveOptions saveOptions = SaveOptions.createSaveOptions(SaveFormat.DOCX);
 saveOptions.setAllowEmbeddingPostScriptFonts(true);

 doc.save(getArtifactsDir() + "Document.AllowEmbeddingPostScriptFonts.docx", saveOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. |

### setColorMode(int value) {#setColorMode-int}
```
public void setColorMode(int value)
```


Sets a value determining how colors are rendered.

 **Remarks:** 

The default value is [ColorMode.NORMAL](../../com.aspose.words/colormode/\#NORMAL).

 **Examples:** 

Shows how to change image color with saving options property.

```

 Document doc = new Document(getMyDir() + "Images.docx");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 // Set the "ColorMode" property to "Grayscale" to render all images from the document in black and white.
 // The size of the output document may be larger with this setting.
 // Set the "ColorMode" property to "Normal" to render all images in color.
 PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
 {
     pdfSaveOptions.setColorMode(colorMode);
 }

 doc.save(getArtifactsDir() + "PdfSaveOptions.ColorRendering.pdf", pdfSaveOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value determining how colors are rendered. The value must be one of [ColorMode](../../com.aspose.words/colormode/) constants. |

### setCssClassNamesPrefix(String value) {#setCssClassNamesPrefix-java.lang.String}
```
public void setCssClassNamesPrefix(String value)
```


Specifies prefix which is added to all class names in style.css file. Default value is  "aw" .

 **Examples:** 

Shows how to place CSS into a separate file and add a prefix to all of its CSS class names.

```

 Document doc = new Document(getMyDir() + "Bookmarks.docx");

 HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();
 {
     htmlFixedSaveOptions.setCssClassNamesPrefix("myprefix");
     htmlFixedSaveOptions.setSaveFontFaceCssSeparately(true);
 }

 doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.AddCssClassNamesPrefix.html", htmlFixedSaveOptions);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlFixedSaveOptions.AddCssClassNamesPrefix.html"), StandardCharsets.UTF_8);

 Assert.assertTrue(Pattern.compile(
     " " +
     " " +
     "").matcher(outDocContents).find());

 outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlFixedSaveOptions.AddCssClassNamesPrefix/styles.css"), StandardCharsets.UTF_8);

 Assert.assertTrue(Pattern.compile(
     ".myprefixdiv [{] position:absolute; [}] " +
     ".myprefixspan [{] position:absolute; white-space:pre; color:#000000; font-size:12pt; [}]").matcher(outDocContents).find());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setDefaultTemplate(String value) {#setDefaultTemplate-java.lang.String}
```
public void setDefaultTemplate(String value)
```


Sets path to default template (including filename). Default value for this property is **empty string**.

 **Remarks:** 

If specified, this path is used to load template when [Document.getAutomaticallyUpdateStyles()](../../com.aspose.words/document/\#getAutomaticallyUpdateStyles) / [Document.setAutomaticallyUpdateStyles(boolean)](../../com.aspose.words/document/\#setAutomaticallyUpdateStyles-boolean) is  true , but [Document.getAttachedTemplate()](../../com.aspose.words/document/\#getAttachedTemplate) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document/\#setAttachedTemplate-java.lang.String) is empty.

 **Examples:** 

Shows how to set a default template for documents that do not have attached templates.

```

 Document doc = new Document();

 // Enable automatic style updating, but do not attach a template document.
 doc.setAutomaticallyUpdateStyles(true);

 Assert.assertEquals("", doc.getAttachedTemplate());

 // Since there is no template document, the document had nowhere to track style changes.
 // Use a SaveOptions object to automatically set a template
 // if a document that we are saving does not have one.
 SaveOptions options = SaveOptions.createSaveOptions("Document.DefaultTemplate.docx");
 options.setDefaultTemplate(getMyDir() + "Business brochure.dotx");

 doc.save(getArtifactsDir() + "Document.DefaultTemplate.docx", options);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | Path to default template (including filename). |

### setDml3DEffectsRenderingMode(int value) {#setDml3DEffectsRenderingMode-int}
```
public void setDml3DEffectsRenderingMode(int value)
```


Sets a value determining how 3D effects are rendered.

 **Remarks:** 

The default value is [Dml3DEffectsRenderingMode.BASIC](../../com.aspose.words/dml3deffectsrenderingmode/\#BASIC).

 **Examples:** 

Shows how 3D effects are rendered.

```

 Document doc = new Document(getMyDir() + "DrawingML shape 3D effects.docx");

 RenderCallback warningCallback = new RenderCallback();
 doc.setWarningCallback(warningCallback);

 PdfSaveOptions saveOptions = new PdfSaveOptions();
 saveOptions.setDml3DEffectsRenderingMode(Dml3DEffectsRenderingMode.ADVANCED);

 doc.save(getArtifactsDir() + "PdfSaveOptions.Dml3DEffectsRenderingModeTest.pdf", saveOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value determining how 3D effects are rendered. The value must be one of [Dml3DEffectsRenderingMode](../../com.aspose.words/dml3deffectsrenderingmode/) constants. |

### setDmlEffectsRenderingMode(int value) {#setDmlEffectsRenderingMode-int}
```
public void setDmlEffectsRenderingMode(int value)
```


Sets a value determining how DrawingML effects are rendered.

 **Remarks:** 

The default value is [DmlEffectsRenderingMode.SIMPLIFIED](../../com.aspose.words/dmleffectsrenderingmode/\#SIMPLIFIED).

This property is used when the document is exported to fixed page formats.

 **Examples:** 

Shows how to configure the rendering quality of DrawingML effects in a document as we save it to PDF.

```

 Document doc = new Document(getMyDir() + "DrawingML shape effects.docx");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Set the "DmlEffectsRenderingMode" property to "DmlEffectsRenderingMode.None" to discard all DrawingML effects.
 // Set the "DmlEffectsRenderingMode" property to "DmlEffectsRenderingMode.Simplified"
 // to render a simplified version of DrawingML effects.
 // Set the "DmlEffectsRenderingMode" property to "DmlEffectsRenderingMode.Fine" to
 // render DrawingML effects with more accuracy and also with more processing cost.
 options.setDmlEffectsRenderingMode(effectsRenderingMode);

 Assert.assertEquals(DmlRenderingMode.DRAWING_ML, options.getDmlRenderingMode());

 doc.save(getArtifactsDir() + "PdfSaveOptions.DrawingMLEffects.pdf", options);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value determining how DrawingML effects are rendered. The value must be one of [DmlEffectsRenderingMode](../../com.aspose.words/dmleffectsrenderingmode/) constants. |

### setDmlRenderingMode(int value) {#setDmlRenderingMode-int}
```
public void setDmlRenderingMode(int value)
```


Sets a value determining how DrawingML shapes are rendered.

 **Remarks:** 

The default value is [DmlRenderingMode.FALLBACK](../../com.aspose.words/dmlrenderingmode/\#FALLBACK).

This property is used when the document is exported to fixed page formats.

 **Examples:** 

Shows how to render fallback shapes when saving to PDF.

```

 Document doc = new Document(getMyDir() + "DrawingML shape fallbacks.docx");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Set the "DmlRenderingMode" property to "DmlRenderingMode.Fallback"
 // to substitute DML shapes with their fallback shapes.
 // Set the "DmlRenderingMode" property to "DmlRenderingMode.DrawingML"
 // to render the DML shapes themselves.
 options.setDmlRenderingMode(dmlRenderingMode);

 doc.save(getArtifactsDir() + "PdfSaveOptions.DrawingMLFallback.pdf", options);
 
```

Shows how to configure the rendering quality of DrawingML effects in a document as we save it to PDF.

```

 Document doc = new Document(getMyDir() + "DrawingML shape effects.docx");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Set the "DmlEffectsRenderingMode" property to "DmlEffectsRenderingMode.None" to discard all DrawingML effects.
 // Set the "DmlEffectsRenderingMode" property to "DmlEffectsRenderingMode.Simplified"
 // to render a simplified version of DrawingML effects.
 // Set the "DmlEffectsRenderingMode" property to "DmlEffectsRenderingMode.Fine" to
 // render DrawingML effects with more accuracy and also with more processing cost.
 options.setDmlEffectsRenderingMode(effectsRenderingMode);

 Assert.assertEquals(DmlRenderingMode.DRAWING_ML, options.getDmlRenderingMode());

 doc.save(getArtifactsDir() + "PdfSaveOptions.DrawingMLEffects.pdf", options);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value determining how DrawingML shapes are rendered. The value must be one of [DmlRenderingMode](../../com.aspose.words/dmlrenderingmode/) constants. |

### setEncoding(Charset value) {#setEncoding-java.nio.charset.Charset}
```
public void setEncoding(Charset value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.nio.charset.Charset |  |

### setExportEmbeddedCss(boolean value) {#setExportEmbeddedCss-boolean}
```
public void setExportEmbeddedCss(boolean value)
```


Specifies whether the CSS (Cascading Style Sheet) should be embedded into Html document.

 **Examples:** 

Shows how to determine where to store CSS stylesheets when exporting a document to Html.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 // When we export a document to html, Aspose.Words will also create a CSS stylesheet to format the document with.
 // Setting the "ExportEmbeddedCss" flag to "true" save the CSS stylesheet to a .css file,
 // and link to the file from the html document using a  element.
 // Setting the flag to "false" will embed the CSS stylesheet within the Html document,
 // which will create only one file instead of two.
 HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();
 {
     htmlFixedSaveOptions.setExportEmbeddedCss(exportEmbeddedCss);
 }

 doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.ExportEmbeddedCss.html", htmlFixedSaveOptions);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlFixedSaveOptions.ExportEmbeddedCss.html"), "utf-8");

 if (exportEmbeddedCss) {
     Assert.assertTrue(outDocContents.contains("
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setExportEmbeddedFonts(boolean value) {#setExportEmbeddedFonts-boolean}
```
public void setExportEmbeddedFonts(boolean value)
```


Specifies whether fonts should be embedded into Html document in Base64 format. Note setting this flag can significantly increase size of output Html file.

 **Examples:** 

Shows how to determine where to store embedded fonts when exporting a document to Html.

```

 Document doc = new Document(getMyDir() + "Embedded font.docx");

 // When we export a document with embedded fonts to .html,
 // Aspose.Words can place the fonts in two possible locations.
 // Setting the "ExportEmbeddedFonts" flag to "true" will store the raw data for embedded fonts within the CSS stylesheet,
 // in the "url" property of the "@font-face" rule. This may create a huge CSS stylesheet file
 // and reduce the number of external files that this HTML conversion will create.
 // Setting this flag to "false" will create a file for each font.
 // The CSS stylesheet will link to each font file using the "url" property of the "@font-face" rule.
 HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();
 {
     htmlFixedSaveOptions.setExportEmbeddedFonts(exportEmbeddedFonts);
 }

 doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.ExportEmbeddedFonts.html", htmlFixedSaveOptions);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlFixedSaveOptions.ExportEmbeddedFonts/styles.css"), StandardCharsets.UTF_8);

 if (exportEmbeddedFonts)
 {
     Assert.assertTrue(Pattern.compile("@font-face [{] font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'\u263a'[)], url[(].+[)] format[(]'woff'[)]; [}]").matcher(outDocContents).find());
     Assert.assertEquals(0, DocumentHelper.directoryGetFiles(getArtifactsDir() + "HtmlFixedSaveOptions.ExportEmbeddedFonts", "*.woff").size());
 }
 else
 {
     Assert.assertTrue(Pattern.compile("@font-face [{] font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'\u263a'[)], url[(]'font001[.]woff'[)] format[(]'woff'[)]; [}]").matcher(outDocContents).find());
     Assert.assertEquals(2, DocumentHelper.directoryGetFiles(getArtifactsDir() + "HtmlFixedSaveOptions.ExportEmbeddedFonts", "*.woff").size());
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setExportEmbeddedImages(boolean value) {#setExportEmbeddedImages-boolean}
```
public void setExportEmbeddedImages(boolean value)
```


Specifies whether images should be embedded into Html document in Base64 format. Note setting this flag can significantly increase size of output Html file.

 **Examples:** 

Shows how to determine where to store images when exporting a document to Html.

```

 Document doc = new Document(getMyDir() + "Images.docx");

 // When we export a document with embedded images to .html,
 // Aspose.Words can place the images in two possible locations.
 // Setting the "ExportEmbeddedImages" flag to "true" will store the raw data
 // for all images within the output HTML document, in the "src" attribute of  tags.
 // Setting this flag to "false" will create an image file in the local file system for every image,
 // and store all these files in a separate folder.
 HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();
 {
     htmlFixedSaveOptions.setExportEmbeddedImages(exportImages);
 }

 doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.ExportEmbeddedImages.html", htmlFixedSaveOptions);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlFixedSaveOptions.ExportEmbeddedImages.html"), StandardCharsets.UTF_8);

 if (exportImages)
 {
     Assert.assertFalse(new File(getArtifactsDir() + "HtmlFixedSaveOptions.ExportEmbeddedImages/image001.jpeg").exists());
     Assert.assertTrue(Pattern.compile("").matcher(outDocContents).find());
 }
 else
 {
     Assert.assertTrue(new File(getArtifactsDir() + "HtmlFixedSaveOptions.ExportEmbeddedImages/image001.jpeg").exists());
     Assert.assertTrue(Pattern.compile("").matcher(outDocContents).find());
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setExportEmbeddedSvg(boolean value) {#setExportEmbeddedSvg-boolean}
```
public void setExportEmbeddedSvg(boolean value)
```


Specifies whether SVG resources should be embedded into Html document. Default value is  true .

 **Examples:** 

Shows how to determine where to store SVG objects when exporting a document to Html.

```

 Document doc = new Document(getMyDir() + "Images.docx");

 // When we export a document with SVG objects to .html,
 // Aspose.Words can place these objects in two possible locations.
 // Setting the "ExportEmbeddedSvg" flag to "true" will embed all SVG object raw data
 // within the output HTML, inside  tags.
 // Setting this flag to "false" will create a file in the local file system for each SVG object.
 // The HTML will link to each file using the "data" attribute of an  tag.
 HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();
 {
     htmlFixedSaveOptions.setExportEmbeddedSvg(exportSvgs);
 }

 doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.ExportEmbeddedSvgs.html", htmlFixedSaveOptions);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlFixedSaveOptions.ExportEmbeddedSvgs.html"), StandardCharsets.UTF_8);

 if (exportSvgs) {
     Assert.assertFalse(new File(getArtifactsDir() + "HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001.svg").exists());
     Assert.assertTrue(Pattern.compile("").matcher(outDocContents).find());
 } else {
     Assert.assertTrue(new File(getArtifactsDir() + "HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001.svg").exists());
     Assert.assertTrue(Pattern.compile("").matcher(outDocContents).find());
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setExportFormFields(boolean value) {#setExportFormFields-boolean}
```
public void setExportFormFields(boolean value)
```


Sets indication of whether form fields are exported as interactive items (as 'input' tag) rather than converted to text or graphics.

 **Examples:** 

Shows how to export form fields to Html.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.insertCheckBox("CheckBox", false, 15);

 // When we export a document with form fields to .html,
 // there are two ways in which Aspose.Words can export form fields.
 // Setting the "ExportFormFields" flag to "true" will export them as interactive objects.
 // Setting this flag to "false" will display form fields as plain text.
 // This will freeze them at their current value, and prevent the reader of our HTML document
 // from being able to interact with them.
 HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();
 {
     htmlFixedSaveOptions.setExportFormFields(exportFormFields);
 }

 doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.ExportFormFields.html", htmlFixedSaveOptions);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlFixedSaveOptions.ExportFormFields.html"), StandardCharsets.UTF_8);

 if (exportFormFields)
 {
     Assert.assertTrue(Pattern.compile(
         "" +
         "").matcher(outDocContents).find());
 }
 else
 {
     Assert.assertTrue(Pattern.compile(
         "" +
         "
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Indication of whether form fields are exported as interactive items (as 'input' tag) rather than converted to text or graphics. |

### setExportGeneratorName(boolean value) {#setExportGeneratorName-boolean}
```
public void setExportGeneratorName(boolean value)
```


When  true , causes the name and version of Aspose.Words to be embedded into produced files. Default value is  true .

 **Examples:** 

Shows how to disable adding name and version of Aspose.Words into produced files.

```

 Document doc = new Document();

 // Use https://docs.aspose.com/words/net/generator-or-producer-name-included-in-output-documents/ to know how to check the result.
 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(); { saveOptions.setExportGeneratorName(false); }

 doc.save(getArtifactsDir() + "OoxmlSaveOptions.ExportGeneratorName.docx", saveOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setFontFormat(int value) {#setFontFormat-int}
```
public void setFontFormat(int value)
```


Sets [ExportFontFormat](../../com.aspose.words/exportfontformat/) used for font exporting. Default value is [ExportFontFormat.WOFF](../../com.aspose.words/exportfontformat/\#WOFF).

 **Examples:** 

Shows how use fonts only from the target machine when saving a document to HTML.

```

 Document doc = new Document(getMyDir() + "Bullet points with alternative font.docx");

 HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions();
 {
     saveOptions.setExportEmbeddedCss(true);
     saveOptions.setUseTargetMachineFonts(useTargetMachineFonts);
     saveOptions.setFontFormat(ExportFontFormat.TTF);
     saveOptions.setExportEmbeddedFonts(false);
 }

 doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.UsingMachineFonts.html", saveOptions);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlFixedSaveOptions.UsingMachineFonts.html"), StandardCharsets.UTF_8);

 if (useTargetMachineFonts)
     Assert.assertFalse(Pattern.compile("@font-face").matcher(outDocContents).find());
 else
     Assert.assertTrue(Pattern.compile(
         "@font-face [{] font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'\u263a'[)], " +
         "url[(]'HtmlFixedSaveOptions.UsingMachineFonts/font001.ttf'[)] format[(]'truetype'[)]; [}]").matcher(outDocContents).find());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | [ExportFontFormat](../../com.aspose.words/exportfontformat/) used for font exporting. The value must be one of [ExportFontFormat](../../com.aspose.words/exportfontformat/) constants. |

### setImlRenderingMode(int value) {#setImlRenderingMode-int}
```
public void setImlRenderingMode(int value)
```


Sets a value determining how ink (InkML) objects are rendered.

 **Remarks:** 

The default value is [ImlRenderingMode.INK\_ML](../../com.aspose.words/imlrenderingmode/\#INK-ML).

This property is used when the document is exported to fixed page formats.

 **Examples:** 

Shows how to render Ink object.

```

 Document doc = new Document(getMyDir() + "Ink object.docx");

 // Set 'ImlRenderingMode.InkML' ignores fall-back shape of ink (InkML) object and renders InkML itself.
 // If the rendering result is unsatisfactory,
 // please use 'ImlRenderingMode.Fallback' to get a result similar to previous versions.
 ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.JPEG);
 {
     saveOptions.setImlRenderingMode(ImlRenderingMode.INK_ML);
 }

 doc.save(getArtifactsDir() + "ImageSaveOptions.RenderInkObject.jpeg", saveOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value determining how ink (InkML) objects are rendered. The value must be one of [ImlRenderingMode](../../com.aspose.words/imlrenderingmode/) constants. |

### setJpegQuality(int value) {#setJpegQuality-int}
```
public void setJpegQuality(int value)
```


Sets a value determining the quality of the JPEG images inside Html document.

 **Remarks:** 

Has effect only when a document contains JPEG images.

Use this property to get or set the quality of the images inside a document when saving in fixed page format. The value may vary from 0 to 100 where 0 means worst quality but maximum compression and 100 means best quality but minimum compression.

The default value is 95.

 **Examples:** 

Shows how to configure compression while saving a document as a JPEG.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertImage(getImageDir() + "Logo.jpg");

 // Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
 // to modify the way in which that method renders the document into an image.
 ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.JPEG);

 // Set the "JpegQuality" property to "10" to use stronger compression when rendering the document.
 // This will reduce the file size of the document, but the image will display more prominent compression artifacts.
 imageOptions.setJpegQuality(10);

 doc.save(getArtifactsDir() + "ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

 Assert.assertTrue(new File(getArtifactsDir() + "ImageSaveOptions.JpegQuality.HighCompression.jpg").length() <= 20000);

 // Set the "JpegQuality" property to "100" to use weaker compression when rending the document.
 // This will improve the quality of the image at the cost of an increased file size.
 imageOptions.setJpegQuality(100);

 doc.save(getArtifactsDir() + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);

 Assert.assertTrue(new File(getArtifactsDir() + "ImageSaveOptions.JpegQuality.HighQuality.jpg").length() < 60000);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value determining the quality of the JPEG images inside Html document. |

### setMemoryOptimization(boolean value) {#setMemoryOptimization-boolean}
```
public void setMemoryOptimization(boolean value)
```


Sets value determining if memory optimization should be performed before saving the document. Default value for this property is  false .

 **Remarks:** 

Setting this option to  true  can significantly decrease memory consumption while saving large documents at the cost of slower saving time.

 **Examples:** 

Shows an option to optimize memory consumption when rendering large documents to PDF.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 SaveOptions saveOptions = SaveOptions.createSaveOptions(SaveFormat.PDF);

 // Set the "MemoryOptimization" property to "true" to lower the memory footprint of large documents' saving operations
 // at the cost of increasing the duration of the operation.
 // Set the "MemoryOptimization" property to "false" to save the document as a PDF normally.
 saveOptions.setMemoryOptimization(memoryOptimization);

 doc.save(getArtifactsDir() + "PdfSaveOptions.MemoryOptimization.pdf", saveOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Value determining if memory optimization should be performed before saving the document. |

### setMetafileRenderingOptions(MetafileRenderingOptions value) {#setMetafileRenderingOptions-com.aspose.words.MetafileRenderingOptions}
```
public void setMetafileRenderingOptions(MetafileRenderingOptions value)
```


Allows to specify metafile rendering options.

 **Examples:** 

Shows added a fallback to bitmap rendering and changing type of warnings about unsupported metafile records.

```

 public void handleBinaryRasterWarnings() throws Exception {
     Document doc = new Document(getMyDir() + "WMF with image.docx");

     MetafileRenderingOptions metafileRenderingOptions = new MetafileRenderingOptions();

     // Set the "EmulateRasterOperations" property to "false" to fall back to bitmap when
     // it encounters a metafile, which will require raster operations to render in the output PDF.
     metafileRenderingOptions.setEmulateRasterOperations(false);

     // Set the "RenderingMode" property to "VectorWithFallback" to try to render every metafile using vector graphics.
     metafileRenderingOptions.setRenderingMode(MetafileRenderingMode.VECTOR_WITH_FALLBACK);

     // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
     // to modify how that method converts the document to .PDF and applies the configuration
     // in our MetafileRenderingOptions object to the saving operation.
     PdfSaveOptions saveOptions = new PdfSaveOptions();
     saveOptions.setMetafileRenderingOptions(metafileRenderingOptions);

     HandleDocumentWarnings callback = new HandleDocumentWarnings();
     doc.setWarningCallback(callback);

     doc.save(getArtifactsDir() + "PdfSaveOptions.HandleBinaryRasterWarnings.pdf", saveOptions);

     Assert.assertEquals(1, callback.mWarnings.getCount());
     Assert.assertEquals("'R2_XORPEN' binary raster operation is not supported.",
             callback.mWarnings.get(0).getDescription());
 }

 /// 
 /// Prints and collects formatting loss-related warnings that occur upon saving a document.
 /// 
 public static class HandleDocumentWarnings implements IWarningCallback {
     public void warning(WarningInfo info) {
         if (info.getWarningType() == WarningType.MINOR_FORMATTING_LOSS) {
             System.out.println("Unsupported operation: " + info.getDescription());
             this.mWarnings.warning(info);
         }
     }

     public WarningInfoCollection mWarnings = new WarningInfoCollection();
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [MetafileRenderingOptions](../../com.aspose.words/metafilerenderingoptions/) | The corresponding [MetafileRenderingOptions](../../com.aspose.words/metafilerenderingoptions/) value. |

### setNumeralFormat(int value) {#setNumeralFormat-int}
```
public void setNumeralFormat(int value)
```


Sets [NumeralFormat](../../com.aspose.words/numeralformat/) used for rendering of numerals. European numerals are used by default.

 **Remarks:** 

If the value of this property is changed and page layout is already built then [Document.updatePageLayout()](../../com.aspose.words/document/\#updatePageLayout) is invoked automatically to update any changes.

 **Examples:** 

Shows how to set the numeral format used when saving to PDF.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setLocaleId(1025);
 builder.writeln("1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 50, 100");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Set the "NumeralFormat" property to "NumeralFormat.ArabicIndic" to
 // use glyphs from the U+0660 to U+0669 range as numbers.
 // Set the "NumeralFormat" property to "NumeralFormat.Context" to
 // look up the locale to determine what number of glyphs to use.
 // Set the "NumeralFormat" property to "NumeralFormat.EasternArabicIndic" to
 // use glyphs from the U+06F0 to U+06F9 range as numbers.
 // Set the "NumeralFormat" property to "NumeralFormat.European" to use european numerals.
 // Set the "NumeralFormat" property to "NumeralFormat.System" to determine the symbol set from regional settings.
 options.setNumeralFormat(numeralFormat);

 doc.save(getArtifactsDir() + "PdfSaveOptions.SetNumeralFormat.pdf", options);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | [NumeralFormat](../../com.aspose.words/numeralformat/) used for rendering of numerals. The value must be one of [NumeralFormat](../../com.aspose.words/numeralformat/) constants. |

### setOptimizeOutput(boolean value) {#setOptimizeOutput-boolean}
```
public void setOptimizeOutput(boolean value)
```


Flag indicates whether it is required to optimize output. If this flag is set redundant nested canvases and empty canvases are removed, also neighbor glyphs with the same formating are concatenated. Note: The accuracy of the content display may be affected if this property is set to  true . Default is  true .

 **Examples:** 

Shows how to simplify a document when saving it to HTML by removing various redundant objects.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions();
 {
     saveOptions.setOptimizeOutput(optimizeOutput);
 }

 doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html", saveOptions);

 // The size of the optimized version of the document is almost a third of the size of the unoptimized document.
 if (optimizeOutput)
     Assert.assertEquals(61889.0,
         new File(getArtifactsDir() + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html").length(), 200.0);
 else
     Assert.assertEquals(191770.0,
         new File(getArtifactsDir() + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html").length(), 200.0);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setPageHorizontalAlignment(int value) {#setPageHorizontalAlignment-int}
```
public void setPageHorizontalAlignment(int value)
```


Specifies the horizontal alignment of pages in an HTML document. Default value is [HtmlFixedPageHorizontalAlignment.CENTER](../../com.aspose.words/htmlfixedpagehorizontalalignment/\#CENTER).

 **Examples:** 

Shows how to set the horizontal alignment of pages when saving a document to HTML.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();
 {
     htmlFixedSaveOptions.setPageHorizontalAlignment(pageHorizontalAlignment);
 }

 doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.HorizontalAlignment.html", htmlFixedSaveOptions);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlFixedSaveOptions.HorizontalAlignment/styles.css"), StandardCharsets.UTF_8);

 switch (pageHorizontalAlignment)
 {
     case HtmlFixedPageHorizontalAlignment.CENTER:
         Assert.assertTrue(Pattern.compile(
             "[.]awpage [{] position:relative; border:solid 1pt black; margin:10pt auto 10pt auto; overflow:hidden; [}]").matcher(outDocContents).find());
         break;
     case HtmlFixedPageHorizontalAlignment.LEFT:
         Assert.assertTrue(Pattern.compile(
             "[.]awpage [{] position:relative; border:solid 1pt black; margin:10pt auto 10pt 10pt; overflow:hidden; [}]").matcher(outDocContents).find());
         break;
     case HtmlFixedPageHorizontalAlignment.RIGHT:
         Assert.assertTrue(Pattern.compile(
             "[.]awpage [{] position:relative; border:solid 1pt black; margin:10pt 10pt 10pt auto; overflow:hidden; [}]").matcher(outDocContents).find());
         break;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [HtmlFixedPageHorizontalAlignment](../../com.aspose.words/htmlfixedpagehorizontalalignment/) constants. |

### setPageMargins(double value) {#setPageMargins-double}
```
public void setPageMargins(double value)
```


Specifies the margins around pages in an HTML document. The margins value is measured in points and should be equal to or greater than 0. Default value is 10 points.

 **Remarks:** 

Depends on the value of [getPageHorizontalAlignment()](../../com.aspose.words/htmlfixedsaveoptions/\#getPageHorizontalAlignment) / [setPageHorizontalAlignment(int)](../../com.aspose.words/htmlfixedsaveoptions/\#setPageHorizontalAlignment-int) property:

 *  Defines top, bottom and left page margins if the value is [HtmlFixedPageHorizontalAlignment.LEFT](../../com.aspose.words/htmlfixedpagehorizontalalignment/\#LEFT).
 *  Defines top, bottom and right page margins if the value is [HtmlFixedPageHorizontalAlignment.RIGHT](../../com.aspose.words/htmlfixedpagehorizontalalignment/\#RIGHT).
 *  Defines top and bottom page margins if the value is [HtmlFixedPageHorizontalAlignment.CENTER](../../com.aspose.words/htmlfixedpagehorizontalalignment/\#CENTER).

 **Examples:** 

Shows how to adjust page margins when saving a document to HTML.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions();
 {
     saveOptions.setPageMargins(15.0);
 }

 doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.PageMargins.html", saveOptions);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlFixedSaveOptions.PageMargins/styles.css"), StandardCharsets.UTF_8);

 Assert.assertTrue(Pattern.compile(
     "[.]awpage [{] position:relative; border:solid 1pt black; margin:15pt auto 15pt auto; overflow:hidden; [}]").matcher(outDocContents).find());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The corresponding  double  value. |

### setPageSavingCallback(IPageSavingCallback value) {#setPageSavingCallback-com.aspose.words.IPageSavingCallback}
```
public void setPageSavingCallback(IPageSavingCallback value)
```


Allows to control how separate pages are saved when a document is exported to fixed page format.

 **Examples:** 

Shows how to use a callback to save a document to HTML page by page.

```

 public void pageFileNames() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.writeln("Page 1.");
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.writeln("Page 2.");
     builder.insertImage(getImageDir() + "Logo.jpg");
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.writeln("Page 3.");

     // Create an "HtmlFixedSaveOptions" object, which we can pass to the document's "Save" method
     // to modify how we convert the document to HTML.
     HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();

     // We will save each page in this document to a separate HTML file in the local file system.
     // Set a callback that allows us to name each output HTML document.
     htmlFixedSaveOptions.setPageSavingCallback(new CustomFileNamePageSavingCallback());

     doc.save(getArtifactsDir() + "SavingCallback.PageFileNames.html", htmlFixedSaveOptions);

     String[] filePaths = DocumentHelper.directoryGetFiles(getArtifactsDir(), "SavingCallback.PageFileNames.Page_*").toArray(new String[0]);

     Assert.assertEquals(3, filePaths.length);
 }

 /// 
 /// Saves all pages to a file and directory specified within.
 /// 
 private static class CustomFileNamePageSavingCallback implements IPageSavingCallback {
     public void pageSaving(PageSavingArgs args) throws Exception {
         String outFileName = MessageFormat.format("{0}SavingCallback.PageFileNames.Page_{1}.html", getArtifactsDir(), args.getPageIndex());

         // Below are two ways of specifying where Aspose.Words will save each page of the document.
         // 1 -  Set a filename for the output page file:
         args.setPageFileName(outFileName);

         // 2 -  Create a custom stream for the output page file:
         try (FileOutputStream outputStream = new FileOutputStream(outFileName)) {
             args.setPageStream(outputStream);
         }

         Assert.assertFalse(args.getKeepPageStreamOpen());
     }
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IPageSavingCallback](../../com.aspose.words/ipagesavingcallback/) | The corresponding [IPageSavingCallback](../../com.aspose.words/ipagesavingcallback/) value. |

### setPageSet(PageSet value) {#setPageSet-com.aspose.words.PageSet}
```
public void setPageSet(PageSet value)
```


Sets the pages to render. Default is all the pages in the document.

 **Examples:** 

Shows how to extract pages based on exact page indices.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add five pages to the document.
 for (int i = 1; i < 6; i++) {
     builder.write("Page " + i);
     builder.insertBreak(BreakType.PAGE_BREAK);
 }

 // Create an "XpsSaveOptions" object, which we can pass to the document's "Save" method
 // to modify how that method converts the document to .XPS.
 XpsSaveOptions xpsOptions = new XpsSaveOptions();

 // Use the "PageSet" property to select a set of the document's pages to save to output XPS.
 // In this case, we will choose, via a zero-based index, only three pages: page 1, page 2, and page 4.
 xpsOptions.setPageSet(new PageSet(0, 1, 3));

 doc.save(getArtifactsDir() + "XpsSaveOptions.ExportExactPages.xps", xpsOptions);
 
```

Shows how to convert only some of the pages in a document to PDF.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 3.");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Set the "PageIndex" to "1" to render a portion of the document starting from the second page.
 options.setPageSet(new PageSet(1));

 // This document will contain one page starting from page two, which will only contain the second page.
 doc.save(new FileOutputStream(getArtifactsDir() + "PdfSaveOptions.OnePage.pdf"), options);
 
```

Shows how to export Odd pages from the document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 for (int i = 0; i < 5; i++) {
     builder.writeln(MessageFormat.format("Page {0} ({1})", i + 1, (i % 2 == 0 ? "odd" : "even")));
     if (i < 4)
         builder.insertBreak(BreakType.PAGE_BREAK);
 }

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Below are three PageSet properties that we can use to filter out a set of pages from
 // our document to save in an output PDF document based on the parity of their page numbers.
 // 1 -  Save only the even-numbered pages:
 options.setPageSet(PageSet.getEven());

 doc.save(getArtifactsDir() + "PdfSaveOptions.ExportPageSet.Even.pdf", options);

 // 2 -  Save only the odd-numbered pages:
 options.setPageSet(PageSet.getOdd());

 doc.save(getArtifactsDir() + "PdfSaveOptions.ExportPageSet.Odd.pdf", options);

 // 3 -  Save every page:
 options.setPageSet(PageSet.getAll());

 doc.save(getArtifactsDir() + "PdfSaveOptions.ExportPageSet.All.pdf", options);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [PageSet](../../com.aspose.words/pageset/) | The pages to render. |

### setPrettyFormat(boolean value) {#setPrettyFormat-boolean}
```
public void setPrettyFormat(boolean value)
```


When  true , pretty formats output where applicable. Default value is  false .

 **Remarks:** 

Set to  true  to make HTML, MHTML, EPUB, WordML, RTF, DOCX and ODT output human readable. Useful for testing or debugging.

 **Examples:** 

Shows how to enhance the readability of the raw code of a saved .html document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 HtmlSaveOptions htmlOptions = new HtmlSaveOptions(SaveFormat.HTML);
 {
     htmlOptions.setPrettyFormat(usePrettyFormat);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.PrettyFormat.html", htmlOptions);

 // Enabling pretty format makes the raw html code more readable by adding tab stop and new line characters.
 String html = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlSaveOptions.PrettyFormat.html"), StandardCharsets.UTF_8);

 if (usePrettyFormat)
     Assert.assertEquals(
             "\r\n" +
                     "\t\r\n" +
                     "\t\t\r\n" +
                     "\t\t\r\n" +
                     MessageFormat.format("\t\t\r\n", BuildVersionInfo.getProduct(), BuildVersionInfo.getVersion()) +
                     "\t\t\r\n" +
                     "\t\t\r\n" +
                     "\t\r\n" +
                     "\t\r\n" +
                     "\t\t \r\n" +
                     "\t\t\t \r\n" +
                     "\t\t\t\tHello world!\r\n" +
                     "\t\t\t\r\n" +
                     "\t\t\t \r\n" +
                     "\t\t\t\t \r\n" +
                     "\t\t\t\r\n" +
                     "\t\t\r\n" +
                     "\t\r\n",
             html);
 else
     Assert.assertEquals(
             "" +
                     "" +
                     MessageFormat.format("", BuildVersionInfo.getProduct(), BuildVersionInfo.getVersion()) +
                     "" +
                     " Hello world!" +
                     "  ",
             html);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setProgressCallback(IDocumentSavingCallback value) {#setProgressCallback-com.aspose.words.IDocumentSavingCallback}
```
public void setProgressCallback(IDocumentSavingCallback value)
```


Called during saving a document and accepts data about saving progress.

 **Remarks:** 

Progress is reported when saving to [SaveFormat.DOCX](../../com.aspose.words/saveformat/\#DOCX), [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat/\#FLAT-OPC), [SaveFormat.DOCM](../../com.aspose.words/saveformat/\#DOCM), [SaveFormat.DOTM](../../com.aspose.words/saveformat/\#DOTM), [SaveFormat.DOTX](../../com.aspose.words/saveformat/\#DOTX), [SaveFormat.DOC](../../com.aspose.words/saveformat/\#DOC), [SaveFormat.DOT](../../com.aspose.words/saveformat/\#DOT), [SaveFormat.HTML](../../com.aspose.words/saveformat/\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat/\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat/\#EPUB), [SaveFormat.XAML\_FLOW](../../com.aspose.words/saveformat/\#XAML-FLOW), or [SaveFormat.XAML\_FLOW\_PACK](../../com.aspose.words/saveformat/\#XAML-FLOW-PACK).

 **Examples:** 

Shows how to manage a document while saving to xamlflow.

```

 public void progressCallback(int saveFormat, String ext) throws Exception
 {
     Document doc = new Document(getMyDir() + "Big document.docx");

     // Following formats are supported: XamlFlow, XamlFlowPack.
     XamlFlowSaveOptions saveOptions = new XamlFlowSaveOptions(saveFormat);
     {
         saveOptions.setProgressCallback(new SavingProgressCallback());
     }

     try {
         doc.save(getArtifactsDir() + MessageFormat.format("XamlFlowSaveOptions.ProgressCallback.{0}", ext), saveOptions);
     }
     catch (IllegalStateException exception) {
         Assert.assertTrue(exception.getMessage().contains("EstimatedProgress"));
     }
 }

 public static Object[][] progressCallbackDataProvider() throws Exception
 {
     return new Object[][]
             {
                     {SaveFormat.XAML_FLOW,  "xamlflow"},
                     {SaveFormat.XAML_FLOW_PACK,  "xamlflowpack"},
             };
 }

 /// 
 /// Saving progress callback. Cancel a document saving after the "MaxDuration" seconds.
 /// 
 public static class SavingProgressCallback implements IDocumentSavingCallback
 {
     /// 
     /// Ctr.
     /// 
     public SavingProgressCallback()
     {
         mSavingStartedAt = new Date();
     }

     /// 
     /// Callback method which called during document saving.
     /// 
     /// Saving arguments.
     public void notify(DocumentSavingArgs args)
     {
         Date canceledAt = new Date();
         long diff = canceledAt.getTime() - mSavingStartedAt.getTime();
         long ellapsedSeconds = TimeUnit.MILLISECONDS.toSeconds(diff);

         if (ellapsedSeconds > MAX_DURATION)
             throw new IllegalStateException(MessageFormat.format("EstimatedProgress = {0}; CanceledAt = {1}", args.getEstimatedProgress(), canceledAt));
     }

     /// 
     /// Date and time when document saving is started.
     /// 
     private Date mSavingStartedAt;

     /// 
     /// Maximum allowed duration in sec.
     /// 
     private static final double MAX_DURATION = 0.01d;
 }
 
```

Shows how to manage a document while saving to html.

```

 public void progressCallback(int saveFormat, String ext) throws Exception
 {
     Document doc = new Document(getMyDir() + "Big document.docx");

     // Following formats are supported: Html, Mhtml, Epub.
     HtmlSaveOptions saveOptions = new HtmlSaveOptions(saveFormat);
     {
         saveOptions.setProgressCallback(new SavingProgressCallback());
     }

     try {
         doc.save(getArtifactsDir() + MessageFormat.format("HtmlSaveOptions.ProgressCallback.{0}", ext), saveOptions);
     }
     catch (IllegalStateException exception) {
         Assert.assertTrue(exception.getMessage().contains("EstimatedProgress"));
     }

 }

 public static Object[][] progressCallbackDataProvider() throws Exception
 {
     return new Object[][]
             {
                     {SaveFormat.HTML,  "html"},
                     {SaveFormat.MHTML,  "mhtml"},
                     {SaveFormat.EPUB,  "epub"},
             };
 }

 /// 
 /// Saving progress callback. Cancel a document saving after the "MaxDuration" seconds.
 /// 
 public static class SavingProgressCallback implements IDocumentSavingCallback
 {
     /// 
     /// Ctr.
     /// 
     public SavingProgressCallback()
     {
         mSavingStartedAt = new Date();
     }

     /// 
     /// Callback method which called during document saving.
     /// 
     /// Saving arguments.
     public void notify(DocumentSavingArgs args)
     {
         Date canceledAt = new Date();
         long diff = canceledAt.getTime() - mSavingStartedAt.getTime();
         long ellapsedSeconds = TimeUnit.MILLISECONDS.toSeconds(diff);

         if (ellapsedSeconds > MAX_DURATION)
             throw new IllegalStateException(MessageFormat.format("EstimatedProgress = {0}; CanceledAt = {1}", args.getEstimatedProgress(), canceledAt));
     }

     /// 
     /// Date and time when document saving is started.
     /// 
     private Date mSavingStartedAt;

     /// 
     /// Maximum allowed duration in sec.
     /// 
     private static final double MAX_DURATION = 0.01d;
 }
 
```

Shows how to manage a document while saving to docx.

```

 public void progressCallback(int saveFormat, String ext) throws Exception
 {
     Document doc = new Document(getMyDir() + "Big document.docx");

     // Following formats are supported: Docx, FlatOpc, Docm, Dotm, Dotx.
     OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(saveFormat);
     {
         saveOptions.setProgressCallback(new SavingProgressCallback());
     }

     try {
         doc.save(getArtifactsDir() + MessageFormat.format("OoxmlSaveOptions.ProgressCallback.{0}", ext), saveOptions);
     }
     catch (IllegalStateException exception) {
         Assert.assertTrue(exception.getMessage().contains("EstimatedProgress"));
     }
 }

 public static Object[][] progressCallbackDataProvider() throws Exception
 {
     return new Object[][]
             {
                     {SaveFormat.DOCX,  "docx"},
                     {SaveFormat.DOCM,  "docm"},
                     {SaveFormat.DOTM,  "dotm"},
                     {SaveFormat.DOTX,  "dotx"},
                     {SaveFormat.FLAT_OPC,  "flatopc"},
             };
 }

 /// 
 /// Saving progress callback. Cancel a document saving after the "MaxDuration" seconds.
 /// 
 public static class SavingProgressCallback implements IDocumentSavingCallback
 {
     /// 
     /// Ctr.
     /// 
     public SavingProgressCallback()
     {
         mSavingStartedAt = new Date();
     }

     /// 
     /// Callback method which called during document saving.
     /// 
     /// Saving arguments.
     public void notify(DocumentSavingArgs args)
     {
         Date canceledAt = new Date();
         long diff = canceledAt.getTime() - mSavingStartedAt.getTime();
         long ellapsedSeconds = TimeUnit.MILLISECONDS.toSeconds(diff);

         if (ellapsedSeconds > MAX_DURATION)
             throw new IllegalStateException(MessageFormat.format("EstimatedProgress = {0}; CanceledAt = {1}", args.getEstimatedProgress(), canceledAt));
     }

     /// 
     /// Date and time when document saving is started.
     /// 
     private Date mSavingStartedAt;

     /// 
     /// Maximum allowed duration in sec.
     /// 
     private static final double MAX_DURATION = 0.01d;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IDocumentSavingCallback](../../com.aspose.words/idocumentsavingcallback/) | The corresponding [IDocumentSavingCallback](../../com.aspose.words/idocumentsavingcallback/) value. |

### setResourceSavingCallback(IResourceSavingCallback value) {#setResourceSavingCallback-com.aspose.words.IResourceSavingCallback}
```
public void setResourceSavingCallback(IResourceSavingCallback value)
```


Allows to control how resources (images, fonts and css) are saved when a document is exported to fixed page Html format.

 **Examples:** 

Shows how to use a callback to print the URIs of external resources created while converting a document to HTML.

```

 public void htmlFixedResourceFolder() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     ResourceUriPrinter callback = new ResourceUriPrinter();

     HtmlFixedSaveOptions options = new HtmlFixedSaveOptions();
     {
         options.setSaveFormat(SaveFormat.HTML_FIXED);
         options.setExportEmbeddedImages(false);
         options.setResourcesFolder(getArtifactsDir() + "HtmlFixedResourceFolder");
         options.setResourcesFolderAlias(getArtifactsDir() + "HtmlFixedResourceFolderAlias");
         options.setShowPageBorder(false);
         options.setResourceSavingCallback(callback);
     }

     // A folder specified by ResourcesFolderAlias will contain the resources instead of ResourcesFolder.
     // We must ensure the folder exists before the streams can put their resources into it.
     new File(options.getResourcesFolderAlias()).mkdir();

     doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.HtmlFixedResourceFolder.html", options);

     System.out.println(callback.getText());

     String[] resourceFiles = new File(getArtifactsDir() + "HtmlFixedResourceFolderAlias").list();

     Assert.assertFalse(new File(getArtifactsDir() + "HtmlFixedResourceFolder").exists());
     Assert.assertEquals(6, IterableUtils.countMatches(Arrays.asList(resourceFiles),
             f -> f.endsWith(".jpeg") || f.endsWith(".png") || f.endsWith(".css")));
 }

 /// 
 /// Counts and prints URIs of resources contained by as they are converted to fixed HTML.
 /// 
 private static class ResourceUriPrinter implements IResourceSavingCallback {
     public void resourceSaving(ResourceSavingArgs args) throws Exception {
         // If we set a folder alias in the SaveOptions object, we will be able to print it from here.
         mText.append(MessageFormat.format("Resource #{0} \"{1}\"", ++mSavedResourceCount, args.getResourceFileName()));

         String extension = FilenameUtils.getExtension(args.getResourceFileName());
         switch (extension) {
             case "ttf":
             case "woff": {
                 // By default, 'ResourceFileUri' uses system folder for fonts.
                 // To avoid problems in other platforms you must explicitly specify the path for the fonts.
                 args.setResourceFileUri(getArtifactsDir() + File.separatorChar + args.getResourceFileName());
                 break;
             }
         }

         mText.append("\t" + args.getResourceFileUri());

         // If we have specified a folder in the "ResourcesFolderAlias" property,
         // we will also need to redirect each stream to put its resource in that folder.
         args.setResourceStream(new FileOutputStream(args.getResourceFileUri()));
         args.setKeepResourceStreamOpen(false);
     }

     public String getText() {
         return mText.toString();
     }

     private int mSavedResourceCount;
     private final  StringBuilder mText = new StringBuilder();
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IResourceSavingCallback](../../com.aspose.words/iresourcesavingcallback/) | The corresponding [IResourceSavingCallback](../../com.aspose.words/iresourcesavingcallback/) value. |

### setResourcesFolder(String value) {#setResourcesFolder-java.lang.String}
```
public void setResourcesFolder(String value)
```


Specifies the physical folder where resources (images, fonts, css) are saved when exporting a document to Html format. Default is  null .

 **Remarks:** 

Has effect only if [getExportEmbeddedImages()](../../com.aspose.words/htmlfixedsaveoptions/\#getExportEmbeddedImages) / [setExportEmbeddedImages(boolean)](../../com.aspose.words/htmlfixedsaveoptions/\#setExportEmbeddedImages-boolean) property is  false .

When you save a [Document](../../com.aspose.words/document/) in Html format, Aspose.Words needs to save all images embedded in the document as standalone files. [getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolder) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolder-java.lang.String) allows you to specify where the images will be saved and [getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolderAlias) / [setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolderAlias-java.lang.String) allows to specify how the image URIs will be constructed.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the images in the same folder where the document file is saved. Use [getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolder) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolder-java.lang.String) to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the images, but still needs to save the images somewhere. In this case, you need to specify an accessible folder by using the [getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolder) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolder-java.lang.String) property

 **Examples:** 

Shows how to use a callback to print the URIs of external resources created while converting a document to HTML.

```

 public void htmlFixedResourceFolder() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     ResourceUriPrinter callback = new ResourceUriPrinter();

     HtmlFixedSaveOptions options = new HtmlFixedSaveOptions();
     {
         options.setSaveFormat(SaveFormat.HTML_FIXED);
         options.setExportEmbeddedImages(false);
         options.setResourcesFolder(getArtifactsDir() + "HtmlFixedResourceFolder");
         options.setResourcesFolderAlias(getArtifactsDir() + "HtmlFixedResourceFolderAlias");
         options.setShowPageBorder(false);
         options.setResourceSavingCallback(callback);
     }

     // A folder specified by ResourcesFolderAlias will contain the resources instead of ResourcesFolder.
     // We must ensure the folder exists before the streams can put their resources into it.
     new File(options.getResourcesFolderAlias()).mkdir();

     doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.HtmlFixedResourceFolder.html", options);

     System.out.println(callback.getText());

     String[] resourceFiles = new File(getArtifactsDir() + "HtmlFixedResourceFolderAlias").list();

     Assert.assertFalse(new File(getArtifactsDir() + "HtmlFixedResourceFolder").exists());
     Assert.assertEquals(6, IterableUtils.countMatches(Arrays.asList(resourceFiles),
             f -> f.endsWith(".jpeg") || f.endsWith(".png") || f.endsWith(".css")));
 }

 /// 
 /// Counts and prints URIs of resources contained by as they are converted to fixed HTML.
 /// 
 private static class ResourceUriPrinter implements IResourceSavingCallback {
     public void resourceSaving(ResourceSavingArgs args) throws Exception {
         // If we set a folder alias in the SaveOptions object, we will be able to print it from here.
         mText.append(MessageFormat.format("Resource #{0} \"{1}\"", ++mSavedResourceCount, args.getResourceFileName()));

         String extension = FilenameUtils.getExtension(args.getResourceFileName());
         switch (extension) {
             case "ttf":
             case "woff": {
                 // By default, 'ResourceFileUri' uses system folder for fonts.
                 // To avoid problems in other platforms you must explicitly specify the path for the fonts.
                 args.setResourceFileUri(getArtifactsDir() + File.separatorChar + args.getResourceFileName());
                 break;
             }
         }

         mText.append("\t" + args.getResourceFileUri());

         // If we have specified a folder in the "ResourcesFolderAlias" property,
         // we will also need to redirect each stream to put its resource in that folder.
         args.setResourceStream(new FileOutputStream(args.getResourceFileUri()));
         args.setKeepResourceStreamOpen(false);
     }

     public String getText() {
         return mText.toString();
     }

     private int mSavedResourceCount;
     private final  StringBuilder mText = new StringBuilder();
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setResourcesFolderAlias(String value) {#setResourcesFolderAlias-java.lang.String}
```
public void setResourcesFolderAlias(String value)
```


Specifies the name of the folder used to construct image URIs written into an Html document. Default is  null .

 **Remarks:** 

When you save a [Document](../../com.aspose.words/document/) in Html format, Aspose.Words needs to save all images embedded in the document as standalone files. [getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolder) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolder-java.lang.String) allows you to specify where the images will be saved and [getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolderAlias) / [setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolderAlias-java.lang.String) allows to specify how the image URIs will be constructed.

 **Examples:** 

Shows how to use a callback to print the URIs of external resources created while converting a document to HTML.

```

 public void htmlFixedResourceFolder() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     ResourceUriPrinter callback = new ResourceUriPrinter();

     HtmlFixedSaveOptions options = new HtmlFixedSaveOptions();
     {
         options.setSaveFormat(SaveFormat.HTML_FIXED);
         options.setExportEmbeddedImages(false);
         options.setResourcesFolder(getArtifactsDir() + "HtmlFixedResourceFolder");
         options.setResourcesFolderAlias(getArtifactsDir() + "HtmlFixedResourceFolderAlias");
         options.setShowPageBorder(false);
         options.setResourceSavingCallback(callback);
     }

     // A folder specified by ResourcesFolderAlias will contain the resources instead of ResourcesFolder.
     // We must ensure the folder exists before the streams can put their resources into it.
     new File(options.getResourcesFolderAlias()).mkdir();

     doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.HtmlFixedResourceFolder.html", options);

     System.out.println(callback.getText());

     String[] resourceFiles = new File(getArtifactsDir() + "HtmlFixedResourceFolderAlias").list();

     Assert.assertFalse(new File(getArtifactsDir() + "HtmlFixedResourceFolder").exists());
     Assert.assertEquals(6, IterableUtils.countMatches(Arrays.asList(resourceFiles),
             f -> f.endsWith(".jpeg") || f.endsWith(".png") || f.endsWith(".css")));
 }

 /// 
 /// Counts and prints URIs of resources contained by as they are converted to fixed HTML.
 /// 
 private static class ResourceUriPrinter implements IResourceSavingCallback {
     public void resourceSaving(ResourceSavingArgs args) throws Exception {
         // If we set a folder alias in the SaveOptions object, we will be able to print it from here.
         mText.append(MessageFormat.format("Resource #{0} \"{1}\"", ++mSavedResourceCount, args.getResourceFileName()));

         String extension = FilenameUtils.getExtension(args.getResourceFileName());
         switch (extension) {
             case "ttf":
             case "woff": {
                 // By default, 'ResourceFileUri' uses system folder for fonts.
                 // To avoid problems in other platforms you must explicitly specify the path for the fonts.
                 args.setResourceFileUri(getArtifactsDir() + File.separatorChar + args.getResourceFileName());
                 break;
             }
         }

         mText.append("\t" + args.getResourceFileUri());

         // If we have specified a folder in the "ResourcesFolderAlias" property,
         // we will also need to redirect each stream to put its resource in that folder.
         args.setResourceStream(new FileOutputStream(args.getResourceFileUri()));
         args.setKeepResourceStreamOpen(false);
     }

     public String getText() {
         return mText.toString();
     }

     private int mSavedResourceCount;
     private final  StringBuilder mText = new StringBuilder();
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setSaveFontFaceCssSeparately(boolean value) {#setSaveFontFaceCssSeparately-boolean}
```
public void setSaveFontFaceCssSeparately(boolean value)
```


Flag indicates whether "@font-face" CSS rules should be placed into a separate file "fontFaces.css" when a document is being saved with external stylesheet (that is, when [getExportEmbeddedCss()](../../com.aspose.words/htmlfixedsaveoptions/\#getExportEmbeddedCss) / [setExportEmbeddedCss(boolean)](../../com.aspose.words/htmlfixedsaveoptions/\#setExportEmbeddedCss-boolean) is  false ). Default value is  false , all CSS rules are written into single file "styles.css".

 **Remarks:** 

Setting this property to  true  restores the old behavior (separate files) for compatibility with legacy code.

 **Examples:** 

Shows how to place CSS into a separate file and add a prefix to all of its CSS class names.

```

 Document doc = new Document(getMyDir() + "Bookmarks.docx");

 HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();
 {
     htmlFixedSaveOptions.setCssClassNamesPrefix("myprefix");
     htmlFixedSaveOptions.setSaveFontFaceCssSeparately(true);
 }

 doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.AddCssClassNamesPrefix.html", htmlFixedSaveOptions);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlFixedSaveOptions.AddCssClassNamesPrefix.html"), StandardCharsets.UTF_8);

 Assert.assertTrue(Pattern.compile(
     " " +
     " " +
     "").matcher(outDocContents).find());

 outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlFixedSaveOptions.AddCssClassNamesPrefix/styles.css"), StandardCharsets.UTF_8);

 Assert.assertTrue(Pattern.compile(
     ".myprefixdiv [{] position:absolute; [}] " +
     ".myprefixspan [{] position:absolute; white-space:pre; color:#000000; font-size:12pt; [}]").matcher(outDocContents).find());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setSaveFormat(int value) {#setSaveFormat-int}
```
public void setSaveFormat(int value)
```


Specifies the format in which the document will be saved if this save options object is used. Can only be [SaveFormat.HTML\_FIXED](../../com.aspose.words/saveformat/\#HTML-FIXED).

 **Examples:** 

Shows how to use a callback to print the URIs of external resources created while converting a document to HTML.

```

 public void htmlFixedResourceFolder() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     ResourceUriPrinter callback = new ResourceUriPrinter();

     HtmlFixedSaveOptions options = new HtmlFixedSaveOptions();
     {
         options.setSaveFormat(SaveFormat.HTML_FIXED);
         options.setExportEmbeddedImages(false);
         options.setResourcesFolder(getArtifactsDir() + "HtmlFixedResourceFolder");
         options.setResourcesFolderAlias(getArtifactsDir() + "HtmlFixedResourceFolderAlias");
         options.setShowPageBorder(false);
         options.setResourceSavingCallback(callback);
     }

     // A folder specified by ResourcesFolderAlias will contain the resources instead of ResourcesFolder.
     // We must ensure the folder exists before the streams can put their resources into it.
     new File(options.getResourcesFolderAlias()).mkdir();

     doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.HtmlFixedResourceFolder.html", options);

     System.out.println(callback.getText());

     String[] resourceFiles = new File(getArtifactsDir() + "HtmlFixedResourceFolderAlias").list();

     Assert.assertFalse(new File(getArtifactsDir() + "HtmlFixedResourceFolder").exists());
     Assert.assertEquals(6, IterableUtils.countMatches(Arrays.asList(resourceFiles),
             f -> f.endsWith(".jpeg") || f.endsWith(".png") || f.endsWith(".css")));
 }

 /// 
 /// Counts and prints URIs of resources contained by as they are converted to fixed HTML.
 /// 
 private static class ResourceUriPrinter implements IResourceSavingCallback {
     public void resourceSaving(ResourceSavingArgs args) throws Exception {
         // If we set a folder alias in the SaveOptions object, we will be able to print it from here.
         mText.append(MessageFormat.format("Resource #{0} \"{1}\"", ++mSavedResourceCount, args.getResourceFileName()));

         String extension = FilenameUtils.getExtension(args.getResourceFileName());
         switch (extension) {
             case "ttf":
             case "woff": {
                 // By default, 'ResourceFileUri' uses system folder for fonts.
                 // To avoid problems in other platforms you must explicitly specify the path for the fonts.
                 args.setResourceFileUri(getArtifactsDir() + File.separatorChar + args.getResourceFileName());
                 break;
             }
         }

         mText.append("\t" + args.getResourceFileUri());

         // If we have specified a folder in the "ResourcesFolderAlias" property,
         // we will also need to redirect each stream to put its resource in that folder.
         args.setResourceStream(new FileOutputStream(args.getResourceFileUri()));
         args.setKeepResourceStreamOpen(false);
     }

     public String getText() {
         return mText.toString();
     }

     private int mSavedResourceCount;
     private final  StringBuilder mText = new StringBuilder();
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [SaveFormat](../../com.aspose.words/saveformat/) constants. |

### setShowPageBorder(boolean value) {#setShowPageBorder-boolean}
```
public void setShowPageBorder(boolean value)
```


Specifies whether border around pages should be shown. Default is  true .

 **Examples:** 

Shows how to use a callback to print the URIs of external resources created while converting a document to HTML.

```

 public void htmlFixedResourceFolder() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     ResourceUriPrinter callback = new ResourceUriPrinter();

     HtmlFixedSaveOptions options = new HtmlFixedSaveOptions();
     {
         options.setSaveFormat(SaveFormat.HTML_FIXED);
         options.setExportEmbeddedImages(false);
         options.setResourcesFolder(getArtifactsDir() + "HtmlFixedResourceFolder");
         options.setResourcesFolderAlias(getArtifactsDir() + "HtmlFixedResourceFolderAlias");
         options.setShowPageBorder(false);
         options.setResourceSavingCallback(callback);
     }

     // A folder specified by ResourcesFolderAlias will contain the resources instead of ResourcesFolder.
     // We must ensure the folder exists before the streams can put their resources into it.
     new File(options.getResourcesFolderAlias()).mkdir();

     doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.HtmlFixedResourceFolder.html", options);

     System.out.println(callback.getText());

     String[] resourceFiles = new File(getArtifactsDir() + "HtmlFixedResourceFolderAlias").list();

     Assert.assertFalse(new File(getArtifactsDir() + "HtmlFixedResourceFolder").exists());
     Assert.assertEquals(6, IterableUtils.countMatches(Arrays.asList(resourceFiles),
             f -> f.endsWith(".jpeg") || f.endsWith(".png") || f.endsWith(".css")));
 }

 /// 
 /// Counts and prints URIs of resources contained by as they are converted to fixed HTML.
 /// 
 private static class ResourceUriPrinter implements IResourceSavingCallback {
     public void resourceSaving(ResourceSavingArgs args) throws Exception {
         // If we set a folder alias in the SaveOptions object, we will be able to print it from here.
         mText.append(MessageFormat.format("Resource #{0} \"{1}\"", ++mSavedResourceCount, args.getResourceFileName()));

         String extension = FilenameUtils.getExtension(args.getResourceFileName());
         switch (extension) {
             case "ttf":
             case "woff": {
                 // By default, 'ResourceFileUri' uses system folder for fonts.
                 // To avoid problems in other platforms you must explicitly specify the path for the fonts.
                 args.setResourceFileUri(getArtifactsDir() + File.separatorChar + args.getResourceFileName());
                 break;
             }
         }

         mText.append("\t" + args.getResourceFileUri());

         // If we have specified a folder in the "ResourcesFolderAlias" property,
         // we will also need to redirect each stream to put its resource in that folder.
         args.setResourceStream(new FileOutputStream(args.getResourceFileUri()));
         args.setKeepResourceStreamOpen(false);
     }

     public String getText() {
         return mText.toString();
     }

     private int mSavedResourceCount;
     private final  StringBuilder mText = new StringBuilder();
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setTempFolder(String value) {#setTempFolder-java.lang.String}
```
public void setTempFolder(String value)
```


Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default this property is  null  and no temporary files are used.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setUpdateCreatedTimeProperty(boolean value) {#setUpdateCreatedTimeProperty-boolean}
```
public void setUpdateCreatedTimeProperty(boolean value)
```


Sets a value determining whether the [BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties/\#getCreatedTime) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setCreatedTime-java.util.Date) property is updated before saving. Default value is  false ;

 **Examples:** 

Shows how to update a document's "CreatedTime" property when saving.

```

 Document doc = new Document();

 Calendar calendar = Calendar.getInstance();
 calendar.set(2019, 11, 20);
 doc.getBuiltInDocumentProperties().setCreatedTime(calendar.getTime());

 // This flag determines whether the created time, which is a built-in property, is updated.
 // If so, then the date of the document's most recent save operation
 // with this SaveOptions object passed as a parameter is used as the created time.
 DocSaveOptions saveOptions = new DocSaveOptions();
 saveOptions.setUpdateCreatedTimeProperty(isUpdateCreatedTimeProperty);

 doc.save(getArtifactsDir() + "DocSaveOptions.UpdateCreatedTimeProperty.docx", saveOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining whether the [BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties/\#getCreatedTime) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setCreatedTime-java.util.Date) property is updated before saving. |

### setUpdateFields(boolean value) {#setUpdateFields-boolean}
```
public void setUpdateFields(boolean value)
```


Sets a value determining if fields of certain types should be updated before saving the document to a fixed page format. Default value for this property is  true .

 **Remarks:** 

Allows to specify whether to mimic or not MS Word behavior.

 **Examples:** 

Shows how to update all the fields in a document immediately before saving it to PDF.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert text with PAGE and NUMPAGES fields. These fields do not display the correct value in real time.
 // We will need to manually update them using updating methods such as "Field.Update()", and "Document.UpdateFields()"
 // each time we need them to display accurate values.
 builder.write("Page ");
 builder.insertField("PAGE", "");
 builder.write(" of ");
 builder.insertField("NUMPAGES", "");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Hello World!");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Set the "UpdateFields" property to "false" to not update all the fields in a document right before a save operation.
 // This is the preferable option if we know that all our fields will be up to date before saving.
 // Set the "UpdateFields" property to "true" to iterate through all the document
 // fields and update them before we save it as a PDF. This will make sure that all the fields will display
 // the most accurate values in the PDF.
 options.setUpdateFields(updateFields);

 // We can clone PdfSaveOptions objects.
 Assert.assertNotSame(options, options.deepClone());

 doc.save(getArtifactsDir() + "PdfSaveOptions.UpdateFields.pdf", options);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining if fields of certain types should be updated before saving the document to a fixed page format. |

### setUpdateLastPrintedProperty(boolean value) {#setUpdateLastPrintedProperty-boolean}
```
public void setUpdateLastPrintedProperty(boolean value)
```


Sets a value determining whether the [BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties/\#getLastPrinted) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastPrinted-java.util.Date) property is updated before saving.

 **Examples:** 

Shows how to update a document's "Last printed" property when saving.

```

 Document doc = new Document();

 Calendar calendar = Calendar.getInstance();
 calendar.set(2019, 11, 20);
 doc.getBuiltInDocumentProperties().setLastPrinted(calendar.getTime());

 // This flag determines whether the last printed date, which is a built-in property, is updated.
 // If so, then the date of the document's most recent save operation
 // with this SaveOptions object passed as a parameter is used as the print date.
 DocSaveOptions saveOptions = new DocSaveOptions();
 saveOptions.setUpdateLastPrintedProperty(isUpdateLastPrintedProperty);

 // In Microsoft Word 2003, this property can be found via File -> Properties -> Statistics -> Printed.
 // It can also be displayed in the document's body by using a PRINTDATE field.
 doc.save(getArtifactsDir() + "DocSaveOptions.UpdateLastPrintedProperty.doc", saveOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining whether the [BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties/\#getLastPrinted) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastPrinted-java.util.Date) property is updated before saving. |

### setUpdateLastSavedTimeProperty(boolean value) {#setUpdateLastSavedTimeProperty-boolean}
```
public void setUpdateLastSavedTimeProperty(boolean value)
```


Sets a value determining whether the [BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties/\#getLastSavedTime) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastSavedTime-java.util.Date) property is updated before saving.

 **Examples:** 

Shows how to determine whether to preserve the document's "Last saved time" property when saving.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 // When we save the document to an OOXML format, we can create an OoxmlSaveOptions object
 // and then pass it to the document's saving method to modify how we save the document.
 // Set the "UpdateLastSavedTimeProperty" property to "true" to
 // set the output document's "Last saved time" built-in property to the current date/time.
 // Set the "UpdateLastSavedTimeProperty" property to "false" to
 // preserve the original value of the input document's "Last saved time" built-in property.
 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 saveOptions.setUpdateLastSavedTimeProperty(updateLastSavedTimeProperty);

 doc.save(getArtifactsDir() + "OoxmlSaveOptions.LastSavedTime.docx", saveOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining whether the [BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties/\#getLastSavedTime) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastSavedTime-java.util.Date) property is updated before saving. |

### setUseAntiAliasing(boolean value) {#setUseAntiAliasing-boolean}
```
public void setUseAntiAliasing(boolean value)
```


Sets a value determining whether or not to use anti-aliasing for rendering.

 **Remarks:** 

The default value is  false . When this value is set to  true  anti-aliasing is used for rendering.

This property is used when the document is exported to the following formats: [SaveFormat.TIFF](../../com.aspose.words/saveformat/\#TIFF), [SaveFormat.PNG](../../com.aspose.words/saveformat/\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat/\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat/\#JPEG), [SaveFormat.EMF](../../com.aspose.words/saveformat/\#EMF). When the document is exported to the [SaveFormat.HTML](../../com.aspose.words/saveformat/\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat/\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat/\#EPUB), [SaveFormat.AZW\_3](../../com.aspose.words/saveformat/\#AZW-3) or [SaveFormat.MOBI](../../com.aspose.words/saveformat/\#MOBI) formats this option is used for raster images.

 **Examples:** 

Shows how to improve the quality of a rendered document with SaveOptions.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(60.0);
 builder.writeln("Some text.");

 SaveOptions options = new ImageSaveOptions(SaveFormat.JPEG);
 doc.save(getArtifactsDir() + "Document.ImageSaveOptions.Default.jpg", options);

 options.setUseAntiAliasing(true);
 options.setUseHighQualityRendering(true);

 doc.save(getArtifactsDir() + "Document.ImageSaveOptions.HighQuality.jpg", options);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining whether or not to use anti-aliasing for rendering. |

### setUseHighQualityRendering(boolean value) {#setUseHighQualityRendering-boolean}
```
public void setUseHighQualityRendering(boolean value)
```


Sets a value determining whether or not to use high quality (i.e. slow) rendering algorithms.

 **Remarks:** 

The default value is  false .

This property is used when the document is exported to image formats: [SaveFormat.TIFF](../../com.aspose.words/saveformat/\#TIFF), [SaveFormat.PNG](../../com.aspose.words/saveformat/\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat/\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat/\#JPEG), [SaveFormat.EMF](../../com.aspose.words/saveformat/\#EMF).

 **Examples:** 

Shows how to improve the quality of a rendered document with SaveOptions.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(60.0);
 builder.writeln("Some text.");

 SaveOptions options = new ImageSaveOptions(SaveFormat.JPEG);
 doc.save(getArtifactsDir() + "Document.ImageSaveOptions.Default.jpg", options);

 options.setUseAntiAliasing(true);
 options.setUseHighQualityRendering(true);

 doc.save(getArtifactsDir() + "Document.ImageSaveOptions.HighQuality.jpg", options);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining whether or not to use high quality (i.e. |

### setUseTargetMachineFonts(boolean value) {#setUseTargetMachineFonts-boolean}
```
public void setUseTargetMachineFonts(boolean value)
```


Flag indicates whether fonts from target machine must be used to display the document. If this flag is set to  true , [getFontFormat()](../../com.aspose.words/htmlfixedsaveoptions/\#getFontFormat) / [setFontFormat(int)](../../com.aspose.words/htmlfixedsaveoptions/\#setFontFormat-int) and [getExportEmbeddedFonts()](../../com.aspose.words/htmlfixedsaveoptions/\#getExportEmbeddedFonts) / [setExportEmbeddedFonts(boolean)](../../com.aspose.words/htmlfixedsaveoptions/\#setExportEmbeddedFonts-boolean) properties do not have effect, also [getResourceSavingCallback()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourceSavingCallback) / [setResourceSavingCallback(com.aspose.words.IResourceSavingCallback)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourceSavingCallback-com.aspose.words.IResourceSavingCallback) is not fired for fonts. Default is  false .

 **Examples:** 

Shows how use fonts only from the target machine when saving a document to HTML.

```

 Document doc = new Document(getMyDir() + "Bullet points with alternative font.docx");

 HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions();
 {
     saveOptions.setExportEmbeddedCss(true);
     saveOptions.setUseTargetMachineFonts(useTargetMachineFonts);
     saveOptions.setFontFormat(ExportFontFormat.TTF);
     saveOptions.setExportEmbeddedFonts(false);
 }

 doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.UsingMachineFonts.html", saveOptions);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlFixedSaveOptions.UsingMachineFonts.html"), StandardCharsets.UTF_8);

 if (useTargetMachineFonts)
     Assert.assertFalse(Pattern.compile("@font-face").matcher(outDocContents).find());
 else
     Assert.assertTrue(Pattern.compile(
         "@font-face [{] font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'\u263a'[)], " +
         "url[(]'HtmlFixedSaveOptions.UsingMachineFonts/font001.ttf'[)] format[(]'truetype'[)]; [}]").matcher(outDocContents).find());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

