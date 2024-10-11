---
title: MarkdownSaveOptions
linktitle: MarkdownSaveOptions
second_title: Aspose.Words for Java
description: Class to specify additional options when saving a document into the SaveFormat.MARKDOWN format in Java.
type: docs
weight: 432
url: /java/com.aspose.words/markdownsaveoptions/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.SaveOptions](../../com.aspose.words/saveoptions/), [com.aspose.words.TxtSaveOptionsBase](../../com.aspose.words/txtsaveoptionsbase/)
```
public class MarkdownSaveOptions extends TxtSaveOptionsBase
```

Class to specify additional options when saving a document into the [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat/\#MARKDOWN) format.

To learn more, visit the [ Specify Save Options ][Specify Save Options] documentation article.

 **Examples:** 

Shows how to rename the image name during saving into Markdown document.

```

 public void renameImages() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
     // If we convert a document that contains images into Markdown, we will end up with one Markdown file which links to several images.
     // Each image will be in the form of a file in the local file system.
     // There is also a callback that can customize the name and file system location of each image.
     saveOptions.setImageSavingCallback(new SavedImageRename("MarkdownSaveOptions.HandleDocument.md"));
     saveOptions.setSaveFormat(SaveFormat.MARKDOWN);

     // The ImageSaving() method of our callback will be run at this time.
     doc.save(getArtifactsDir() + "MarkdownSaveOptions.HandleDocument.md", saveOptions);

     Supplier> filteredShapes = () -> DocumentHelper.directoryGetFiles(
             getArtifactsDir(), "*").stream().
             filter(s -> s.startsWith(getArtifactsDir() + "MarkdownSaveOptions.HandleDocument.md shape"));

     Assert.assertEquals(1, filteredShapes.get().filter(f -> f.endsWith(".jpeg")).count());
     Assert.assertEquals(8, filteredShapes.get().filter(f -> f.endsWith(".png")).count());
 }

 /// 
 /// Renames saved images that are produced when an Markdown document is saved.
 /// 
 public static class SavedImageRename implements IImageSavingCallback
 {
     public SavedImageRename(String outFileName)
     {
         mOutFileName = outFileName;
     }

     public void imageSaving(ImageSavingArgs args) throws Exception
     {
         String imageFileName = MessageFormat.format("{0} shape {1}, of type {2}.{3}",
                 mOutFileName, ++mCount, args.getCurrentShape().getShapeType(),
                 FilenameUtils.getExtension(args.getImageFileName()));

         args.setImageFileName(imageFileName);
         args.setImageStream(new FileOutputStream(getArtifactsDir() + imageFileName));

         Assert.assertTrue(args.isImageAvailable());
         Assert.assertFalse(args.getKeepImageStreamOpen());
     }

     private int mCount;
     private String mOutFileName;
 }
 
```


[Specify Save Options]: https://docs.aspose.com/words/java/specify-save-options/
## Constructors

| Constructor | Description |
| --- | --- |
| [MarkdownSaveOptions()](#MarkdownSaveOptions) | Initializes a new instance of this class that can be used to save a document in the [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat/\#MARKDOWN) format. |
## Methods

| Method | Description |
| --- | --- |
| [createSaveOptions(int saveFormat)](#createSaveOptions-int) |  |
| [createSaveOptions(String fileName)](#createSaveOptions-java.lang.String) | Creates a save options object of a class suitable for the file extension specified in the given file name. |
| [getAllowEmbeddingPostScriptFonts()](#getAllowEmbeddingPostScriptFonts) | Gets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. |
| [getDefaultTemplate()](#getDefaultTemplate) | Gets path to default template (including filename). |
| [getDml3DEffectsRenderingMode()](#getDml3DEffectsRenderingMode) | Gets a value determining how 3D effects are rendered. |
| [getDmlEffectsRenderingMode()](#getDmlEffectsRenderingMode) | Gets a value determining how DrawingML effects are rendered. |
| [getDmlRenderingMode()](#getDmlRenderingMode) | Gets a value determining how DrawingML shapes are rendered. |
| [getEncoding()](#getEncoding) |  |
| [getExportAsHtml()](#getExportAsHtml) | Allows to specify the elements to be exported to Markdown as raw HTML. |
| [getExportGeneratorName()](#getExportGeneratorName) | When  true , causes the name and version of Aspose.Words to be embedded into produced files. |
| [getExportHeadersFootersMode()](#getExportHeadersFootersMode) | Specifies the way headers and footers are exported to the text formats. |
| [getExportImagesAsBase64()](#getExportImagesAsBase64) | Specifies whether images are saved in Base64 format to the output file. |
| [getExportUnderlineFormatting()](#getExportUnderlineFormatting) | Gets a boolean value indicating either to export underline text formatting as sequence of two plus characters "++". |
| [getForcePageBreaks()](#getForcePageBreaks) | Allows to specify whether the page breaks should be preserved during export. |
| [getImageSavingCallback()](#getImageSavingCallback) | Allows to control how images are saved when a document is saved to [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat/\#MARKDOWN) format. |
| [getImagesFolder()](#getImagesFolder) | Specifies the physical folder where images are saved when exporting a document to the [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat/\#MARKDOWN) format. |
| [getImagesFolderAlias()](#getImagesFolderAlias) | Specifies the name of the folder used to construct image URIs written into a document. |
| [getImlRenderingMode()](#getImlRenderingMode) | Gets a value determining how ink (InkML) objects are rendered. |
| [getLinkExportMode()](#getLinkExportMode) | Specifies how links will be written to the output file. |
| [getListExportMode()](#getListExportMode) | Specifies how list items will be written to the output file. |
| [getMemoryOptimization()](#getMemoryOptimization) | Gets value determining if memory optimization should be performed before saving the document. |
| [getParagraphBreak()](#getParagraphBreak) | Specifies the string to use as a paragraph break when exporting in text formats. |
| [getPrettyFormat()](#getPrettyFormat) | When  true , pretty formats output where applicable. |
| [getProgressCallback()](#getProgressCallback) | Called during saving a document and accepts data about saving progress. |
| [getSaveFormat()](#getSaveFormat) | Specifies the format in which the document will be saved if this save options object is used. |
| [getTableContentAlignment()](#getTableContentAlignment) | Gets a value that specifies how to align contents in tables when exporting into the [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat/\#MARKDOWN) format. |
| [getTempFolder()](#getTempFolder) | Specifies the folder for temporary files used when saving to a DOC or DOCX file. |
| [getUpdateCreatedTimeProperty()](#getUpdateCreatedTimeProperty) | Gets a value determining whether the [BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties/\#getCreatedTime) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setCreatedTime-java.util.Date) property is updated before saving. |
| [getUpdateFields()](#getUpdateFields) | Gets a value determining if fields of certain types should be updated before saving the document to a fixed page format. |
| [getUpdateLastPrintedProperty()](#getUpdateLastPrintedProperty) | Gets a value determining whether the [BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties/\#getLastPrinted) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastPrinted-java.util.Date) property is updated before saving. |
| [getUpdateLastSavedTimeProperty()](#getUpdateLastSavedTimeProperty) | Gets a value determining whether the [BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties/\#getLastSavedTime) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastSavedTime-java.util.Date) property is updated before saving. |
| [getUseAntiAliasing()](#getUseAntiAliasing) | Gets a value determining whether or not to use anti-aliasing for rendering. |
| [getUseHighQualityRendering()](#getUseHighQualityRendering) | Gets a value determining whether or not to use high quality (i.e. |
| [setAllowEmbeddingPostScriptFonts(boolean value)](#setAllowEmbeddingPostScriptFonts-boolean) | Sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. |
| [setDefaultTemplate(String value)](#setDefaultTemplate-java.lang.String) | Sets path to default template (including filename). |
| [setDml3DEffectsRenderingMode(int value)](#setDml3DEffectsRenderingMode-int) | Sets a value determining how 3D effects are rendered. |
| [setDmlEffectsRenderingMode(int value)](#setDmlEffectsRenderingMode-int) | Sets a value determining how DrawingML effects are rendered. |
| [setDmlRenderingMode(int value)](#setDmlRenderingMode-int) | Sets a value determining how DrawingML shapes are rendered. |
| [setEncoding(Charset value)](#setEncoding-java.nio.charset.Charset) |  |
| [setExportAsHtml(int value)](#setExportAsHtml-int) | Allows to specify the elements to be exported to Markdown as raw HTML. |
| [setExportGeneratorName(boolean value)](#setExportGeneratorName-boolean) | When  true , causes the name and version of Aspose.Words to be embedded into produced files. |
| [setExportHeadersFootersMode(int value)](#setExportHeadersFootersMode-int) | Specifies the way headers and footers are exported to the text formats. |
| [setExportImagesAsBase64(boolean value)](#setExportImagesAsBase64-boolean) | Specifies whether images are saved in Base64 format to the output file. |
| [setExportUnderlineFormatting(boolean value)](#setExportUnderlineFormatting-boolean) | Sets a boolean value indicating either to export underline text formatting as sequence of two plus characters "++". |
| [setForcePageBreaks(boolean value)](#setForcePageBreaks-boolean) | Allows to specify whether the page breaks should be preserved during export. |
| [setImageSavingCallback(IImageSavingCallback value)](#setImageSavingCallback-com.aspose.words.IImageSavingCallback) | Allows to control how images are saved when a document is saved to [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat/\#MARKDOWN) format. |
| [setImagesFolder(String value)](#setImagesFolder-java.lang.String) | Specifies the physical folder where images are saved when exporting a document to the [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat/\#MARKDOWN) format. |
| [setImagesFolderAlias(String value)](#setImagesFolderAlias-java.lang.String) | Specifies the name of the folder used to construct image URIs written into a document. |
| [setImlRenderingMode(int value)](#setImlRenderingMode-int) | Sets a value determining how ink (InkML) objects are rendered. |
| [setLinkExportMode(int value)](#setLinkExportMode-int) | Specifies how links will be written to the output file. |
| [setListExportMode(int value)](#setListExportMode-int) | Specifies how list items will be written to the output file. |
| [setMemoryOptimization(boolean value)](#setMemoryOptimization-boolean) | Sets value determining if memory optimization should be performed before saving the document. |
| [setParagraphBreak(String value)](#setParagraphBreak-java.lang.String) | Specifies the string to use as a paragraph break when exporting in text formats. |
| [setPrettyFormat(boolean value)](#setPrettyFormat-boolean) | When  true , pretty formats output where applicable. |
| [setProgressCallback(IDocumentSavingCallback value)](#setProgressCallback-com.aspose.words.IDocumentSavingCallback) | Called during saving a document and accepts data about saving progress. |
| [setSaveFormat(int value)](#setSaveFormat-int) | Specifies the format in which the document will be saved if this save options object is used. |
| [setTableContentAlignment(int value)](#setTableContentAlignment-int) | Sets a value that specifies how to align contents in tables when exporting into the [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat/\#MARKDOWN) format. |
| [setTempFolder(String value)](#setTempFolder-java.lang.String) | Specifies the folder for temporary files used when saving to a DOC or DOCX file. |
| [setUpdateCreatedTimeProperty(boolean value)](#setUpdateCreatedTimeProperty-boolean) | Sets a value determining whether the [BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties/\#getCreatedTime) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setCreatedTime-java.util.Date) property is updated before saving. |
| [setUpdateFields(boolean value)](#setUpdateFields-boolean) | Sets a value determining if fields of certain types should be updated before saving the document to a fixed page format. |
| [setUpdateLastPrintedProperty(boolean value)](#setUpdateLastPrintedProperty-boolean) | Sets a value determining whether the [BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties/\#getLastPrinted) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastPrinted-java.util.Date) property is updated before saving. |
| [setUpdateLastSavedTimeProperty(boolean value)](#setUpdateLastSavedTimeProperty-boolean) | Sets a value determining whether the [BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties/\#getLastSavedTime) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastSavedTime-java.util.Date) property is updated before saving. |
| [setUseAntiAliasing(boolean value)](#setUseAntiAliasing-boolean) | Sets a value determining whether or not to use anti-aliasing for rendering. |
| [setUseHighQualityRendering(boolean value)](#setUseHighQualityRendering-boolean) | Sets a value determining whether or not to use high quality (i.e. |
### MarkdownSaveOptions() {#MarkdownSaveOptions}
```
public MarkdownSaveOptions()
```


Initializes a new instance of this class that can be used to save a document in the [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat/\#MARKDOWN) format.

 **Examples:** 

Shows how to rename the image name during saving into Markdown document.

```

 public void renameImages() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
     // If we convert a document that contains images into Markdown, we will end up with one Markdown file which links to several images.
     // Each image will be in the form of a file in the local file system.
     // There is also a callback that can customize the name and file system location of each image.
     saveOptions.setImageSavingCallback(new SavedImageRename("MarkdownSaveOptions.HandleDocument.md"));
     saveOptions.setSaveFormat(SaveFormat.MARKDOWN);

     // The ImageSaving() method of our callback will be run at this time.
     doc.save(getArtifactsDir() + "MarkdownSaveOptions.HandleDocument.md", saveOptions);

     Supplier> filteredShapes = () -> DocumentHelper.directoryGetFiles(
             getArtifactsDir(), "*").stream().
             filter(s -> s.startsWith(getArtifactsDir() + "MarkdownSaveOptions.HandleDocument.md shape"));

     Assert.assertEquals(1, filteredShapes.get().filter(f -> f.endsWith(".jpeg")).count());
     Assert.assertEquals(8, filteredShapes.get().filter(f -> f.endsWith(".png")).count());
 }

 /// 
 /// Renames saved images that are produced when an Markdown document is saved.
 /// 
 public static class SavedImageRename implements IImageSavingCallback
 {
     public SavedImageRename(String outFileName)
     {
         mOutFileName = outFileName;
     }

     public void imageSaving(ImageSavingArgs args) throws Exception
     {
         String imageFileName = MessageFormat.format("{0} shape {1}, of type {2}.{3}",
                 mOutFileName, ++mCount, args.getCurrentShape().getShapeType(),
                 FilenameUtils.getExtension(args.getImageFileName()));

         args.setImageFileName(imageFileName);
         args.setImageStream(new FileOutputStream(getArtifactsDir() + imageFileName));

         Assert.assertTrue(args.isImageAvailable());
         Assert.assertFalse(args.getKeepImageStreamOpen());
     }

     private int mCount;
     private String mOutFileName;
 }
 
```

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
### getExportAsHtml() {#getExportAsHtml}
```
public int getExportAsHtml()
```


Allows to specify the elements to be exported to Markdown as raw HTML. Default value is [MarkdownExportAsHtml.NONE](../../com.aspose.words/markdownexportashtml/\#NONE).

 **Examples:** 

Shows how to export a table to Markdown as raw HTML.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Sample table:");

 // Create table.
 builder.insertCell();
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.RIGHT);
 builder.write("Cell1");
 builder.insertCell();
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.write("Cell2");

 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 saveOptions.setExportAsHtml(MarkdownExportAsHtml.TABLES);

 doc.save(getArtifactsDir() + "MarkdownSaveOptions.ExportTableAsHtml.md", saveOptions);
 
```

**Returns:**
int - The corresponding  int  value. The returned value is a bitwise combination of [MarkdownExportAsHtml](../../com.aspose.words/markdownexportashtml/) constants.
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
### getExportHeadersFootersMode() {#getExportHeadersFootersMode}
```
public int getExportHeadersFootersMode()
```


Specifies the way headers and footers are exported to the text formats. Default value is [TxtExportHeadersFootersMode.PRIMARY\_ONLY](../../com.aspose.words/txtexportheadersfootersmode/\#PRIMARY-ONLY).

 **Examples:** 

Shows how to specify how to export headers and footers to plain text format.

```

 Document doc = new Document();

 // Insert even and primary headers/footers into the document.
 // The primary header/footers will override the even headers/footers.
 doc.getFirstSection().getHeadersFooters().add(new HeaderFooter(doc, HeaderFooterType.HEADER_EVEN));
 doc.getFirstSection().getHeadersFooters().getByHeaderFooterType(HeaderFooterType.HEADER_EVEN).appendParagraph("Even header");
 doc.getFirstSection().getHeadersFooters().add(new HeaderFooter(doc, HeaderFooterType.FOOTER_EVEN));
 doc.getFirstSection().getHeadersFooters().getByHeaderFooterType(HeaderFooterType.FOOTER_EVEN).appendParagraph("Even footer");
 doc.getFirstSection().getHeadersFooters().add(new HeaderFooter(doc, HeaderFooterType.HEADER_PRIMARY));
 doc.getFirstSection().getHeadersFooters().getByHeaderFooterType(HeaderFooterType.HEADER_PRIMARY).appendParagraph("Primary header");
 doc.getFirstSection().getHeadersFooters().add(new HeaderFooter(doc, HeaderFooterType.FOOTER_PRIMARY));
 doc.getFirstSection().getHeadersFooters().getByHeaderFooterType(HeaderFooterType.FOOTER_PRIMARY).appendParagraph("Primary footer");

 // Insert pages to display these headers and footers.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Page 1");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 2");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.write("Page 3");

 // Create a "TxtSaveOptions" object, which we can pass to the document's "Save" method
 // to modify how we save the document to plaintext.
 TxtSaveOptions saveOptions = new TxtSaveOptions();

 // Set the "ExportHeadersFootersMode" property to "TxtExportHeadersFootersMode.None"
 // to not export any headers/footers.
 // Set the "ExportHeadersFootersMode" property to "TxtExportHeadersFootersMode.PrimaryOnly"
 // to only export primary headers/footers.
 // Set the "ExportHeadersFootersMode" property to "TxtExportHeadersFootersMode.AllAtEnd"
 // to place all headers and footers for all section bodies at the end of the document.
 saveOptions.setExportHeadersFootersMode(txtExportHeadersFootersMode);

 doc.save(getArtifactsDir() + "TxtSaveOptions.ExportHeadersFooters.txt", saveOptions);

 String docText = new Document(getArtifactsDir() + "TxtSaveOptions.ExportHeadersFooters.txt").getText().trim();

 switch (txtExportHeadersFootersMode) {
     case TxtExportHeadersFootersMode.ALL_AT_END:
         Assert.assertEquals("Page 1\r" +
                 "Page 2\r" +
                 "Page 3\r" +
                 "Even header\r\r" +
                 "Primary header\r\r" +
                 "Even footer\r\r" +
                 "Primary footer", docText);

         break;
     case TxtExportHeadersFootersMode.PRIMARY_ONLY:
         Assert.assertEquals("Primary header\r" +
                 "Page 1\r" +
                 "Page 2\r" +
                 "Page 3\r" +
                 "Primary footer", docText);
         break;
     case TxtExportHeadersFootersMode.NONE:
         Assert.assertEquals("Page 1\r" +
                 "Page 2\r" +
                 "Page 3", docText);
         break;
 }
 
```

**Returns:**
int - The corresponding  int  value. The returned value is one of [TxtExportHeadersFootersMode](../../com.aspose.words/txtexportheadersfootersmode/) constants.
### getExportImagesAsBase64() {#getExportImagesAsBase64}
```
public boolean getExportImagesAsBase64()
```


Specifies whether images are saved in Base64 format to the output file. Default value is  false .

 **Remarks:** 

When this property is set to  true  images data are exported directly into the **img** elements and separate files are not created.

 **Examples:** 

Shows how to save a .md document with images embedded inside it.

```

 Document doc = new Document(getMyDir() + "Images.docx");

 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions(); { saveOptions.setExportImagesAsBase64(exportImagesAsBase64); }

 doc.save(getArtifactsDir() + "MarkdownSaveOptions.ExportImagesAsBase64.md", saveOptions);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "MarkdownSaveOptions.ExportImagesAsBase64.md"), Charset.forName("UTF-8"));

 Assert.assertTrue(exportImagesAsBase64
     ? outDocContents.contains("data:image/jpeg;base64")
     : outDocContents.contains("MarkdownSaveOptions.ExportImagesAsBase64.001.jpeg"));
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getExportUnderlineFormatting() {#getExportUnderlineFormatting}
```
public boolean getExportUnderlineFormatting()
```


Gets a boolean value indicating either to export underline text formatting as sequence of two plus characters "++". The default value is  false .

 **Examples:** 

Shows how to export underline formatting as ++.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.setUnderline(Underline.SINGLE);
 builder.write("Lorem ipsum. Dolor sit amet.");

 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 saveOptions.setExportUnderlineFormatting(true);
 doc.save(getArtifactsDir() + "MarkdownSaveOptions.ExportUnderlineFormatting.md", saveOptions);
 
```

**Returns:**
boolean - A boolean value indicating either to export underline text formatting as sequence of two plus characters "++".
### getForcePageBreaks() {#getForcePageBreaks}
```
public boolean getForcePageBreaks()
```


Allows to specify whether the page breaks should be preserved during export.

The default value is  false .

 **Remarks:** 

The property affects only page breaks that are inserted explicitly into a document. It is not related to page breaks that MS Word automatically inserts at the end of each page.

 **Examples:** 

Shows how to specify whether to preserve page breaks when exporting a document to plaintext.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Page 1");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 2");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 3");

 // Create a "TxtSaveOptions" object, which we can pass to the document's "Save"
 // method to modify how we save the document to plaintext.
 TxtSaveOptions saveOptions = new TxtSaveOptions();

 // The Aspose.Words "Document" objects have page breaks, just like Microsoft Word documents.
 // Save formats such as ".txt" are one continuous body of text without page breaks.
 // Set the "ForcePageBreaks" property to "true" to preserve all page breaks in the form of '\f' characters.
 // Set the "ForcePageBreaks" property to "false" to discard all page breaks.
 saveOptions.setForcePageBreaks(forcePageBreaks);

 doc.save(getArtifactsDir() + "TxtSaveOptions.PageBreaks.txt", saveOptions);

 // If we load a plaintext document with page breaks,
 // the "Document" object will use them to split the body into pages.
 doc = new Document(getArtifactsDir() + "TxtSaveOptions.PageBreaks.txt");

 Assert.assertEquals(forcePageBreaks ? 3 : 1, doc.getPageCount());
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getImageSavingCallback() {#getImageSavingCallback}
```
public IImageSavingCallback getImageSavingCallback()
```


Allows to control how images are saved when a document is saved to [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat/\#MARKDOWN) format.

 **Examples:** 

Shows how to rename the image name during saving into Markdown document.

```

 public void renameImages() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
     // If we convert a document that contains images into Markdown, we will end up with one Markdown file which links to several images.
     // Each image will be in the form of a file in the local file system.
     // There is also a callback that can customize the name and file system location of each image.
     saveOptions.setImageSavingCallback(new SavedImageRename("MarkdownSaveOptions.HandleDocument.md"));
     saveOptions.setSaveFormat(SaveFormat.MARKDOWN);

     // The ImageSaving() method of our callback will be run at this time.
     doc.save(getArtifactsDir() + "MarkdownSaveOptions.HandleDocument.md", saveOptions);

     Supplier> filteredShapes = () -> DocumentHelper.directoryGetFiles(
             getArtifactsDir(), "*").stream().
             filter(s -> s.startsWith(getArtifactsDir() + "MarkdownSaveOptions.HandleDocument.md shape"));

     Assert.assertEquals(1, filteredShapes.get().filter(f -> f.endsWith(".jpeg")).count());
     Assert.assertEquals(8, filteredShapes.get().filter(f -> f.endsWith(".png")).count());
 }

 /// 
 /// Renames saved images that are produced when an Markdown document is saved.
 /// 
 public static class SavedImageRename implements IImageSavingCallback
 {
     public SavedImageRename(String outFileName)
     {
         mOutFileName = outFileName;
     }

     public void imageSaving(ImageSavingArgs args) throws Exception
     {
         String imageFileName = MessageFormat.format("{0} shape {1}, of type {2}.{3}",
                 mOutFileName, ++mCount, args.getCurrentShape().getShapeType(),
                 FilenameUtils.getExtension(args.getImageFileName()));

         args.setImageFileName(imageFileName);
         args.setImageStream(new FileOutputStream(getArtifactsDir() + imageFileName));

         Assert.assertTrue(args.isImageAvailable());
         Assert.assertFalse(args.getKeepImageStreamOpen());
     }

     private int mCount;
     private String mOutFileName;
 }
 
```

**Returns:**
[IImageSavingCallback](../../com.aspose.words/iimagesavingcallback/) - The corresponding [IImageSavingCallback](../../com.aspose.words/iimagesavingcallback/) value.
### getImagesFolder() {#getImagesFolder}
```
public String getImagesFolder()
```


Specifies the physical folder where images are saved when exporting a document to the [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat/\#MARKDOWN) format. Default is an empty string.

 **Remarks:** 

When you save a [Document](../../com.aspose.words/document/) in [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat/\#MARKDOWN) format, Aspose.Words needs to save all images embedded in the document as standalone files. [getImagesFolder()](../../com.aspose.words/markdownsaveoptions/\#getImagesFolder) / [setImagesFolder(java.lang.String)](../../com.aspose.words/markdownsaveoptions/\#setImagesFolder-java.lang.String) allows you to specify where the images will be saved.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the images in the same folder where the document file is saved. Use [getImagesFolder()](../../com.aspose.words/markdownsaveoptions/\#getImagesFolder) / [setImagesFolder(java.lang.String)](../../com.aspose.words/markdownsaveoptions/\#setImagesFolder-java.lang.String) to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the images, but still needs to save the images somewhere. In this case, you need to specify an accessible folder in the [getImagesFolder()](../../com.aspose.words/markdownsaveoptions/\#getImagesFolder) / [setImagesFolder(java.lang.String)](../../com.aspose.words/markdownsaveoptions/\#setImagesFolder-java.lang.String) property.

If the folder specified by [getImagesFolder()](../../com.aspose.words/markdownsaveoptions/\#getImagesFolder) / [setImagesFolder(java.lang.String)](../../com.aspose.words/markdownsaveoptions/\#setImagesFolder-java.lang.String) doesn't exist, it will be created automatically.

 **Examples:** 

Shows how to specifies the name of the folder used to construct image URIs.

```

 DocumentBuilder builder = new DocumentBuilder();

 builder.writeln("Some image below:");
 builder.insertImage(getImageDir() + "Logo.jpg");

 String imagesFolder = Paths.get(getArtifactsDir(), "ImagesDir").toString();
 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 // Use the "ImagesFolder" property to assign a folder in the local file system into which
 // Aspose.Words will save all the document's linked images.
 saveOptions.setImagesFolder(imagesFolder);
 // Use the "ImagesFolderAlias" property to use this folder
 // when constructing image URIs instead of the images folder's name.
 saveOptions.setImagesFolderAlias("http://example.com/images");

 builder.getDocument().save(getArtifactsDir() + "MarkdownSaveOptions.ImagesFolder.md", saveOptions);
 
```

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getImagesFolderAlias() {#getImagesFolderAlias}
```
public String getImagesFolderAlias()
```


Specifies the name of the folder used to construct image URIs written into a document. Default is an empty string.

 **Remarks:** 

When you save a [Document](../../com.aspose.words/document/) in [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat/\#MARKDOWN) format, Aspose.Words needs to save all images embedded in the document as standalone files. [getImagesFolder()](../../com.aspose.words/markdownsaveoptions/\#getImagesFolder) / [setImagesFolder(java.lang.String)](../../com.aspose.words/markdownsaveoptions/\#setImagesFolder-java.lang.String) allows you to specify where the images will be saved and [getImagesFolderAlias()](../../com.aspose.words/markdownsaveoptions/\#getImagesFolderAlias) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/markdownsaveoptions/\#setImagesFolderAlias-java.lang.String) allows to specify how the image URIs will be constructed.

If [getImagesFolderAlias()](../../com.aspose.words/markdownsaveoptions/\#getImagesFolderAlias) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/markdownsaveoptions/\#setImagesFolderAlias-java.lang.String) is not an empty string, then the image URI written to Markdown will be *ImagesFolderAlias + ![Image 1][]*.

If [getImagesFolderAlias()](../../com.aspose.words/markdownsaveoptions/\#getImagesFolderAlias) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/markdownsaveoptions/\#setImagesFolderAlias-java.lang.String) is an empty string, then the image URI written to Markdown will be *ImagesFolder + ![Image 1][]*.

If [getImagesFolderAlias()](../../com.aspose.words/markdownsaveoptions/\#getImagesFolderAlias) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/markdownsaveoptions/\#setImagesFolderAlias-java.lang.String) is set to '.' (dot), then the image file name will be written to Markdown without path regardless of other options.

 **Examples:** 

Shows how to specifies the name of the folder used to construct image URIs.

```

 DocumentBuilder builder = new DocumentBuilder();

 builder.writeln("Some image below:");
 builder.insertImage(getImageDir() + "Logo.jpg");

 String imagesFolder = Paths.get(getArtifactsDir(), "ImagesDir").toString();
 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 // Use the "ImagesFolder" property to assign a folder in the local file system into which
 // Aspose.Words will save all the document's linked images.
 saveOptions.setImagesFolder(imagesFolder);
 // Use the "ImagesFolderAlias" property to use this folder
 // when constructing image URIs instead of the images folder's name.
 saveOptions.setImagesFolderAlias("http://example.com/images");

 builder.getDocument().save(getArtifactsDir() + "MarkdownSaveOptions.ImagesFolder.md", saveOptions);
 
```


[Image 1]: 

**Returns:**
java.lang.String - The corresponding java.lang.String value.
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
### getLinkExportMode() {#getLinkExportMode}
```
public int getLinkExportMode()
```


Specifies how links will be written to the output file. Default value is [MarkdownLinkExportMode.AUTO](../../com.aspose.words/markdownlinkexportmode/\#AUTO).

 **Examples:** 

Shows how to links will be written to the .md file.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertShape(ShapeType.BALLOON, 100.0, 100.0);

 // Image will be written as reference:
 // ![ref1]
 //
 // [ref1]: aw_ref.001.png
 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 saveOptions.setLinkExportMode(MarkdownLinkExportMode.REFERENCE);
 doc.save(getArtifactsDir() + "MarkdownSaveOptions.LinkExportMode.Reference.md", saveOptions);

 // Image will be written as inline:
 // ![](../aw_inline.001.png)
 saveOptions.setLinkExportMode(MarkdownLinkExportMode.INLINE);
 doc.save(getArtifactsDir() + "MarkdownSaveOptions.LinkExportMode.Inline.md", saveOptions);
 
```

**Returns:**
int - The corresponding  int  value. The returned value is one of [MarkdownLinkExportMode](../../com.aspose.words/markdownlinkexportmode/) constants.
### getListExportMode() {#getListExportMode}
```
public int getListExportMode()
```


Specifies how list items will be written to the output file. Default value is [MarkdownListExportMode.MARKDOWN\_SYNTAX](../../com.aspose.words/markdownlistexportmode/\#MARKDOWN-SYNTAX).

 **Remarks:** 

When this property is set to [MarkdownListExportMode.PLAIN\_TEXT](../../com.aspose.words/markdownlistexportmode/\#PLAIN-TEXT) all list labels are updated using [Document.updateListLabels()](../../com.aspose.words/document/\#updateListLabels) and exported with their actual values. Such lists can be non-compatible with Markdown format and will be recognized as plain text upon importing in this case.

When this property is set to [MarkdownListExportMode.MARKDOWN\_SYNTAX](../../com.aspose.words/markdownlistexportmode/\#MARKDOWN-SYNTAX), writer tries to export list items in manner that allows to numerate list items in automatic mode by Markdown.

 **Examples:** 

Shows how to list items will be written to the markdown document.

```

 Document doc = new Document(getMyDir() + "List item.docx");

 // Use MarkdownListExportMode.PlainText or MarkdownListExportMode.MarkdownSyntax to export list.
 MarkdownSaveOptions options = new MarkdownSaveOptions(); { options.setListExportMode(markdownListExportMode); }
 doc.save(getArtifactsDir() + "MarkdownSaveOptions.ListExportMode.md", options);
 
```

**Returns:**
int - The corresponding  int  value. The returned value is one of [MarkdownListExportMode](../../com.aspose.words/markdownlistexportmode/) constants.
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
### getParagraphBreak() {#getParagraphBreak}
```
public String getParagraphBreak()
```


Specifies the string to use as a paragraph break when exporting in text formats.

 **Remarks:** 

The default value is [ControlChar.CR\_LF](../../com.aspose.words/controlchar/\#CR-LF).

 **Examples:** 

Shows how to save a .txt document with a custom paragraph break.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Paragraph 1.");
 builder.writeln("Paragraph 2.");
 builder.write("Paragraph 3.");

 // Create a "TxtSaveOptions" object, which we can pass to the document's "Save" method
 // to modify how we save the document to plaintext.
 TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

 Assert.assertEquals(SaveFormat.TEXT, txtSaveOptions.getSaveFormat());

 // Set the "ParagraphBreak" to a custom value that we wish to put at the end of every paragraph.
 txtSaveOptions.setParagraphBreak(" End of paragraph.\r\r\t");

 doc.save(getArtifactsDir() + "TxtSaveOptions.ParagraphBreak.txt", txtSaveOptions);

 String docText = new Document(getArtifactsDir() + "TxtSaveOptions.ParagraphBreak.txt").getText().trim();

 Assert.assertEquals("Paragraph 1. End of paragraph.\r\r\t" +
         "Paragraph 2. End of paragraph.\r\r\t" +
         "Paragraph 3. End of paragraph.", docText);
 
```

**Returns:**
java.lang.String - The corresponding java.lang.String value.
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
### getSaveFormat() {#getSaveFormat}
```
public int getSaveFormat()
```


Specifies the format in which the document will be saved if this save options object is used. Can only be [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat/\#MARKDOWN).

 **Examples:** 

Shows how to rename the image name during saving into Markdown document.

```

 public void renameImages() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
     // If we convert a document that contains images into Markdown, we will end up with one Markdown file which links to several images.
     // Each image will be in the form of a file in the local file system.
     // There is also a callback that can customize the name and file system location of each image.
     saveOptions.setImageSavingCallback(new SavedImageRename("MarkdownSaveOptions.HandleDocument.md"));
     saveOptions.setSaveFormat(SaveFormat.MARKDOWN);

     // The ImageSaving() method of our callback will be run at this time.
     doc.save(getArtifactsDir() + "MarkdownSaveOptions.HandleDocument.md", saveOptions);

     Supplier> filteredShapes = () -> DocumentHelper.directoryGetFiles(
             getArtifactsDir(), "*").stream().
             filter(s -> s.startsWith(getArtifactsDir() + "MarkdownSaveOptions.HandleDocument.md shape"));

     Assert.assertEquals(1, filteredShapes.get().filter(f -> f.endsWith(".jpeg")).count());
     Assert.assertEquals(8, filteredShapes.get().filter(f -> f.endsWith(".png")).count());
 }

 /// 
 /// Renames saved images that are produced when an Markdown document is saved.
 /// 
 public static class SavedImageRename implements IImageSavingCallback
 {
     public SavedImageRename(String outFileName)
     {
         mOutFileName = outFileName;
     }

     public void imageSaving(ImageSavingArgs args) throws Exception
     {
         String imageFileName = MessageFormat.format("{0} shape {1}, of type {2}.{3}",
                 mOutFileName, ++mCount, args.getCurrentShape().getShapeType(),
                 FilenameUtils.getExtension(args.getImageFileName()));

         args.setImageFileName(imageFileName);
         args.setImageStream(new FileOutputStream(getArtifactsDir() + imageFileName));

         Assert.assertTrue(args.isImageAvailable());
         Assert.assertFalse(args.getKeepImageStreamOpen());
     }

     private int mCount;
     private String mOutFileName;
 }
 
```

**Returns:**
int - The corresponding  int  value. The returned value is one of [SaveFormat](../../com.aspose.words/saveformat/) constants.
### getTableContentAlignment() {#getTableContentAlignment}
```
public int getTableContentAlignment()
```


Gets a value that specifies how to align contents in tables when exporting into the [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat/\#MARKDOWN) format. The default value is [TableContentAlignment.AUTO](../../com.aspose.words/tablecontentalignment/\#AUTO).

 **Examples:** 

Shows how to align contents in tables.

```

 DocumentBuilder builder = new DocumentBuilder();

 builder.insertCell();
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.RIGHT);
 builder.write("Cell1");
 builder.insertCell();
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.write("Cell2");

 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions(); { saveOptions.setTableContentAlignment(tableContentAlignment); }

 builder.getDocument().save(getArtifactsDir() + "MarkdownSaveOptions.MarkdownDocumentTableContentAlignment.md", saveOptions);

 Document doc = new Document(getArtifactsDir() + "MarkdownSaveOptions.MarkdownDocumentTableContentAlignment.md");
 Table table = doc.getFirstSection().getBody().getTables().get(0);

 switch (tableContentAlignment)
 {
     case TableContentAlignment.AUTO:
         Assert.assertEquals(ParagraphAlignment.RIGHT,
             table.getFirstRow().getCells().get(0).getFirstParagraph().getParagraphFormat().getAlignment());
         Assert.assertEquals(ParagraphAlignment.CENTER,
             table.getFirstRow().getCells().get(1).getFirstParagraph().getParagraphFormat().getAlignment());
         break;
     case TableContentAlignment.LEFT:
         Assert.assertEquals(ParagraphAlignment.LEFT,
             table.getFirstRow().getCells().get(0).getFirstParagraph().getParagraphFormat().getAlignment());
         Assert.assertEquals(ParagraphAlignment.LEFT,
             table.getFirstRow().getCells().get(1).getFirstParagraph().getParagraphFormat().getAlignment());
         break;
     case TableContentAlignment.CENTER:
         Assert.assertEquals(ParagraphAlignment.CENTER,
             table.getFirstRow().getCells().get(0).getFirstParagraph().getParagraphFormat().getAlignment());
         Assert.assertEquals(ParagraphAlignment.CENTER,
             table.getFirstRow().getCells().get(1).getFirstParagraph().getParagraphFormat().getAlignment());
         break;
     case TableContentAlignment.RIGHT:
         Assert.assertEquals(ParagraphAlignment.RIGHT,
             table.getFirstRow().getCells().get(0).getFirstParagraph().getParagraphFormat().getAlignment());
         Assert.assertEquals(ParagraphAlignment.RIGHT,
             table.getFirstRow().getCells().get(1).getFirstParagraph().getParagraphFormat().getAlignment());
         break;
 }
 
```

**Returns:**
int - A value that specifies how to align contents in tables when exporting into the [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat/\#MARKDOWN) format. The returned value is one of [TableContentAlignment](../../com.aspose.words/tablecontentalignment/) constants.
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

### setExportAsHtml(int value) {#setExportAsHtml-int}
```
public void setExportAsHtml(int value)
```


Allows to specify the elements to be exported to Markdown as raw HTML. Default value is [MarkdownExportAsHtml.NONE](../../com.aspose.words/markdownexportashtml/\#NONE).

 **Examples:** 

Shows how to export a table to Markdown as raw HTML.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Sample table:");

 // Create table.
 builder.insertCell();
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.RIGHT);
 builder.write("Cell1");
 builder.insertCell();
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.write("Cell2");

 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 saveOptions.setExportAsHtml(MarkdownExportAsHtml.TABLES);

 doc.save(getArtifactsDir() + "MarkdownSaveOptions.ExportTableAsHtml.md", saveOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be a bitwise combination of [MarkdownExportAsHtml](../../com.aspose.words/markdownexportashtml/) constants. |

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

### setExportHeadersFootersMode(int value) {#setExportHeadersFootersMode-int}
```
public void setExportHeadersFootersMode(int value)
```


Specifies the way headers and footers are exported to the text formats. Default value is [TxtExportHeadersFootersMode.PRIMARY\_ONLY](../../com.aspose.words/txtexportheadersfootersmode/\#PRIMARY-ONLY).

 **Examples:** 

Shows how to specify how to export headers and footers to plain text format.

```

 Document doc = new Document();

 // Insert even and primary headers/footers into the document.
 // The primary header/footers will override the even headers/footers.
 doc.getFirstSection().getHeadersFooters().add(new HeaderFooter(doc, HeaderFooterType.HEADER_EVEN));
 doc.getFirstSection().getHeadersFooters().getByHeaderFooterType(HeaderFooterType.HEADER_EVEN).appendParagraph("Even header");
 doc.getFirstSection().getHeadersFooters().add(new HeaderFooter(doc, HeaderFooterType.FOOTER_EVEN));
 doc.getFirstSection().getHeadersFooters().getByHeaderFooterType(HeaderFooterType.FOOTER_EVEN).appendParagraph("Even footer");
 doc.getFirstSection().getHeadersFooters().add(new HeaderFooter(doc, HeaderFooterType.HEADER_PRIMARY));
 doc.getFirstSection().getHeadersFooters().getByHeaderFooterType(HeaderFooterType.HEADER_PRIMARY).appendParagraph("Primary header");
 doc.getFirstSection().getHeadersFooters().add(new HeaderFooter(doc, HeaderFooterType.FOOTER_PRIMARY));
 doc.getFirstSection().getHeadersFooters().getByHeaderFooterType(HeaderFooterType.FOOTER_PRIMARY).appendParagraph("Primary footer");

 // Insert pages to display these headers and footers.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Page 1");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 2");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.write("Page 3");

 // Create a "TxtSaveOptions" object, which we can pass to the document's "Save" method
 // to modify how we save the document to plaintext.
 TxtSaveOptions saveOptions = new TxtSaveOptions();

 // Set the "ExportHeadersFootersMode" property to "TxtExportHeadersFootersMode.None"
 // to not export any headers/footers.
 // Set the "ExportHeadersFootersMode" property to "TxtExportHeadersFootersMode.PrimaryOnly"
 // to only export primary headers/footers.
 // Set the "ExportHeadersFootersMode" property to "TxtExportHeadersFootersMode.AllAtEnd"
 // to place all headers and footers for all section bodies at the end of the document.
 saveOptions.setExportHeadersFootersMode(txtExportHeadersFootersMode);

 doc.save(getArtifactsDir() + "TxtSaveOptions.ExportHeadersFooters.txt", saveOptions);

 String docText = new Document(getArtifactsDir() + "TxtSaveOptions.ExportHeadersFooters.txt").getText().trim();

 switch (txtExportHeadersFootersMode) {
     case TxtExportHeadersFootersMode.ALL_AT_END:
         Assert.assertEquals("Page 1\r" +
                 "Page 2\r" +
                 "Page 3\r" +
                 "Even header\r\r" +
                 "Primary header\r\r" +
                 "Even footer\r\r" +
                 "Primary footer", docText);

         break;
     case TxtExportHeadersFootersMode.PRIMARY_ONLY:
         Assert.assertEquals("Primary header\r" +
                 "Page 1\r" +
                 "Page 2\r" +
                 "Page 3\r" +
                 "Primary footer", docText);
         break;
     case TxtExportHeadersFootersMode.NONE:
         Assert.assertEquals("Page 1\r" +
                 "Page 2\r" +
                 "Page 3", docText);
         break;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [TxtExportHeadersFootersMode](../../com.aspose.words/txtexportheadersfootersmode/) constants. |

### setExportImagesAsBase64(boolean value) {#setExportImagesAsBase64-boolean}
```
public void setExportImagesAsBase64(boolean value)
```


Specifies whether images are saved in Base64 format to the output file. Default value is  false .

 **Remarks:** 

When this property is set to  true  images data are exported directly into the **img** elements and separate files are not created.

 **Examples:** 

Shows how to save a .md document with images embedded inside it.

```

 Document doc = new Document(getMyDir() + "Images.docx");

 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions(); { saveOptions.setExportImagesAsBase64(exportImagesAsBase64); }

 doc.save(getArtifactsDir() + "MarkdownSaveOptions.ExportImagesAsBase64.md", saveOptions);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "MarkdownSaveOptions.ExportImagesAsBase64.md"), Charset.forName("UTF-8"));

 Assert.assertTrue(exportImagesAsBase64
     ? outDocContents.contains("data:image/jpeg;base64")
     : outDocContents.contains("MarkdownSaveOptions.ExportImagesAsBase64.001.jpeg"));
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setExportUnderlineFormatting(boolean value) {#setExportUnderlineFormatting-boolean}
```
public void setExportUnderlineFormatting(boolean value)
```


Sets a boolean value indicating either to export underline text formatting as sequence of two plus characters "++". The default value is  false .

 **Examples:** 

Shows how to export underline formatting as ++.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.setUnderline(Underline.SINGLE);
 builder.write("Lorem ipsum. Dolor sit amet.");

 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 saveOptions.setExportUnderlineFormatting(true);
 doc.save(getArtifactsDir() + "MarkdownSaveOptions.ExportUnderlineFormatting.md", saveOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A boolean value indicating either to export underline text formatting as sequence of two plus characters "++". |

### setForcePageBreaks(boolean value) {#setForcePageBreaks-boolean}
```
public void setForcePageBreaks(boolean value)
```


Allows to specify whether the page breaks should be preserved during export.

The default value is  false .

 **Remarks:** 

The property affects only page breaks that are inserted explicitly into a document. It is not related to page breaks that MS Word automatically inserts at the end of each page.

 **Examples:** 

Shows how to specify whether to preserve page breaks when exporting a document to plaintext.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Page 1");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 2");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 3");

 // Create a "TxtSaveOptions" object, which we can pass to the document's "Save"
 // method to modify how we save the document to plaintext.
 TxtSaveOptions saveOptions = new TxtSaveOptions();

 // The Aspose.Words "Document" objects have page breaks, just like Microsoft Word documents.
 // Save formats such as ".txt" are one continuous body of text without page breaks.
 // Set the "ForcePageBreaks" property to "true" to preserve all page breaks in the form of '\f' characters.
 // Set the "ForcePageBreaks" property to "false" to discard all page breaks.
 saveOptions.setForcePageBreaks(forcePageBreaks);

 doc.save(getArtifactsDir() + "TxtSaveOptions.PageBreaks.txt", saveOptions);

 // If we load a plaintext document with page breaks,
 // the "Document" object will use them to split the body into pages.
 doc = new Document(getArtifactsDir() + "TxtSaveOptions.PageBreaks.txt");

 Assert.assertEquals(forcePageBreaks ? 3 : 1, doc.getPageCount());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setImageSavingCallback(IImageSavingCallback value) {#setImageSavingCallback-com.aspose.words.IImageSavingCallback}
```
public void setImageSavingCallback(IImageSavingCallback value)
```


Allows to control how images are saved when a document is saved to [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat/\#MARKDOWN) format.

 **Examples:** 

Shows how to rename the image name during saving into Markdown document.

```

 public void renameImages() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
     // If we convert a document that contains images into Markdown, we will end up with one Markdown file which links to several images.
     // Each image will be in the form of a file in the local file system.
     // There is also a callback that can customize the name and file system location of each image.
     saveOptions.setImageSavingCallback(new SavedImageRename("MarkdownSaveOptions.HandleDocument.md"));
     saveOptions.setSaveFormat(SaveFormat.MARKDOWN);

     // The ImageSaving() method of our callback will be run at this time.
     doc.save(getArtifactsDir() + "MarkdownSaveOptions.HandleDocument.md", saveOptions);

     Supplier> filteredShapes = () -> DocumentHelper.directoryGetFiles(
             getArtifactsDir(), "*").stream().
             filter(s -> s.startsWith(getArtifactsDir() + "MarkdownSaveOptions.HandleDocument.md shape"));

     Assert.assertEquals(1, filteredShapes.get().filter(f -> f.endsWith(".jpeg")).count());
     Assert.assertEquals(8, filteredShapes.get().filter(f -> f.endsWith(".png")).count());
 }

 /// 
 /// Renames saved images that are produced when an Markdown document is saved.
 /// 
 public static class SavedImageRename implements IImageSavingCallback
 {
     public SavedImageRename(String outFileName)
     {
         mOutFileName = outFileName;
     }

     public void imageSaving(ImageSavingArgs args) throws Exception
     {
         String imageFileName = MessageFormat.format("{0} shape {1}, of type {2}.{3}",
                 mOutFileName, ++mCount, args.getCurrentShape().getShapeType(),
                 FilenameUtils.getExtension(args.getImageFileName()));

         args.setImageFileName(imageFileName);
         args.setImageStream(new FileOutputStream(getArtifactsDir() + imageFileName));

         Assert.assertTrue(args.isImageAvailable());
         Assert.assertFalse(args.getKeepImageStreamOpen());
     }

     private int mCount;
     private String mOutFileName;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IImageSavingCallback](../../com.aspose.words/iimagesavingcallback/) | The corresponding [IImageSavingCallback](../../com.aspose.words/iimagesavingcallback/) value. |

### setImagesFolder(String value) {#setImagesFolder-java.lang.String}
```
public void setImagesFolder(String value)
```


Specifies the physical folder where images are saved when exporting a document to the [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat/\#MARKDOWN) format. Default is an empty string.

 **Remarks:** 

When you save a [Document](../../com.aspose.words/document/) in [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat/\#MARKDOWN) format, Aspose.Words needs to save all images embedded in the document as standalone files. [getImagesFolder()](../../com.aspose.words/markdownsaveoptions/\#getImagesFolder) / [setImagesFolder(java.lang.String)](../../com.aspose.words/markdownsaveoptions/\#setImagesFolder-java.lang.String) allows you to specify where the images will be saved.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the images in the same folder where the document file is saved. Use [getImagesFolder()](../../com.aspose.words/markdownsaveoptions/\#getImagesFolder) / [setImagesFolder(java.lang.String)](../../com.aspose.words/markdownsaveoptions/\#setImagesFolder-java.lang.String) to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the images, but still needs to save the images somewhere. In this case, you need to specify an accessible folder in the [getImagesFolder()](../../com.aspose.words/markdownsaveoptions/\#getImagesFolder) / [setImagesFolder(java.lang.String)](../../com.aspose.words/markdownsaveoptions/\#setImagesFolder-java.lang.String) property.

If the folder specified by [getImagesFolder()](../../com.aspose.words/markdownsaveoptions/\#getImagesFolder) / [setImagesFolder(java.lang.String)](../../com.aspose.words/markdownsaveoptions/\#setImagesFolder-java.lang.String) doesn't exist, it will be created automatically.

 **Examples:** 

Shows how to specifies the name of the folder used to construct image URIs.

```

 DocumentBuilder builder = new DocumentBuilder();

 builder.writeln("Some image below:");
 builder.insertImage(getImageDir() + "Logo.jpg");

 String imagesFolder = Paths.get(getArtifactsDir(), "ImagesDir").toString();
 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 // Use the "ImagesFolder" property to assign a folder in the local file system into which
 // Aspose.Words will save all the document's linked images.
 saveOptions.setImagesFolder(imagesFolder);
 // Use the "ImagesFolderAlias" property to use this folder
 // when constructing image URIs instead of the images folder's name.
 saveOptions.setImagesFolderAlias("http://example.com/images");

 builder.getDocument().save(getArtifactsDir() + "MarkdownSaveOptions.ImagesFolder.md", saveOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setImagesFolderAlias(String value) {#setImagesFolderAlias-java.lang.String}
```
public void setImagesFolderAlias(String value)
```


Specifies the name of the folder used to construct image URIs written into a document. Default is an empty string.

 **Remarks:** 

When you save a [Document](../../com.aspose.words/document/) in [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat/\#MARKDOWN) format, Aspose.Words needs to save all images embedded in the document as standalone files. [getImagesFolder()](../../com.aspose.words/markdownsaveoptions/\#getImagesFolder) / [setImagesFolder(java.lang.String)](../../com.aspose.words/markdownsaveoptions/\#setImagesFolder-java.lang.String) allows you to specify where the images will be saved and [getImagesFolderAlias()](../../com.aspose.words/markdownsaveoptions/\#getImagesFolderAlias) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/markdownsaveoptions/\#setImagesFolderAlias-java.lang.String) allows to specify how the image URIs will be constructed.

If [getImagesFolderAlias()](../../com.aspose.words/markdownsaveoptions/\#getImagesFolderAlias) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/markdownsaveoptions/\#setImagesFolderAlias-java.lang.String) is not an empty string, then the image URI written to Markdown will be *ImagesFolderAlias + ![Image 1][]*.

If [getImagesFolderAlias()](../../com.aspose.words/markdownsaveoptions/\#getImagesFolderAlias) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/markdownsaveoptions/\#setImagesFolderAlias-java.lang.String) is an empty string, then the image URI written to Markdown will be *ImagesFolder + ![Image 1][]*.

If [getImagesFolderAlias()](../../com.aspose.words/markdownsaveoptions/\#getImagesFolderAlias) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/markdownsaveoptions/\#setImagesFolderAlias-java.lang.String) is set to '.' (dot), then the image file name will be written to Markdown without path regardless of other options.

 **Examples:** 

Shows how to specifies the name of the folder used to construct image URIs.

```

 DocumentBuilder builder = new DocumentBuilder();

 builder.writeln("Some image below:");
 builder.insertImage(getImageDir() + "Logo.jpg");

 String imagesFolder = Paths.get(getArtifactsDir(), "ImagesDir").toString();
 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 // Use the "ImagesFolder" property to assign a folder in the local file system into which
 // Aspose.Words will save all the document's linked images.
 saveOptions.setImagesFolder(imagesFolder);
 // Use the "ImagesFolderAlias" property to use this folder
 // when constructing image URIs instead of the images folder's name.
 saveOptions.setImagesFolderAlias("http://example.com/images");

 builder.getDocument().save(getArtifactsDir() + "MarkdownSaveOptions.ImagesFolder.md", saveOptions);
 
```


[Image 1]: 

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

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

### setLinkExportMode(int value) {#setLinkExportMode-int}
```
public void setLinkExportMode(int value)
```


Specifies how links will be written to the output file. Default value is [MarkdownLinkExportMode.AUTO](../../com.aspose.words/markdownlinkexportmode/\#AUTO).

 **Examples:** 

Shows how to links will be written to the .md file.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertShape(ShapeType.BALLOON, 100.0, 100.0);

 // Image will be written as reference:
 // ![ref1]
 //
 // [ref1]: aw_ref.001.png
 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 saveOptions.setLinkExportMode(MarkdownLinkExportMode.REFERENCE);
 doc.save(getArtifactsDir() + "MarkdownSaveOptions.LinkExportMode.Reference.md", saveOptions);

 // Image will be written as inline:
 // ![](../aw_inline.001.png)
 saveOptions.setLinkExportMode(MarkdownLinkExportMode.INLINE);
 doc.save(getArtifactsDir() + "MarkdownSaveOptions.LinkExportMode.Inline.md", saveOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [MarkdownLinkExportMode](../../com.aspose.words/markdownlinkexportmode/) constants. |

### setListExportMode(int value) {#setListExportMode-int}
```
public void setListExportMode(int value)
```


Specifies how list items will be written to the output file. Default value is [MarkdownListExportMode.MARKDOWN\_SYNTAX](../../com.aspose.words/markdownlistexportmode/\#MARKDOWN-SYNTAX).

 **Remarks:** 

When this property is set to [MarkdownListExportMode.PLAIN\_TEXT](../../com.aspose.words/markdownlistexportmode/\#PLAIN-TEXT) all list labels are updated using [Document.updateListLabels()](../../com.aspose.words/document/\#updateListLabels) and exported with their actual values. Such lists can be non-compatible with Markdown format and will be recognized as plain text upon importing in this case.

When this property is set to [MarkdownListExportMode.MARKDOWN\_SYNTAX](../../com.aspose.words/markdownlistexportmode/\#MARKDOWN-SYNTAX), writer tries to export list items in manner that allows to numerate list items in automatic mode by Markdown.

 **Examples:** 

Shows how to list items will be written to the markdown document.

```

 Document doc = new Document(getMyDir() + "List item.docx");

 // Use MarkdownListExportMode.PlainText or MarkdownListExportMode.MarkdownSyntax to export list.
 MarkdownSaveOptions options = new MarkdownSaveOptions(); { options.setListExportMode(markdownListExportMode); }
 doc.save(getArtifactsDir() + "MarkdownSaveOptions.ListExportMode.md", options);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [MarkdownListExportMode](../../com.aspose.words/markdownlistexportmode/) constants. |

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

### setParagraphBreak(String value) {#setParagraphBreak-java.lang.String}
```
public void setParagraphBreak(String value)
```


Specifies the string to use as a paragraph break when exporting in text formats.

 **Remarks:** 

The default value is [ControlChar.CR\_LF](../../com.aspose.words/controlchar/\#CR-LF).

 **Examples:** 

Shows how to save a .txt document with a custom paragraph break.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Paragraph 1.");
 builder.writeln("Paragraph 2.");
 builder.write("Paragraph 3.");

 // Create a "TxtSaveOptions" object, which we can pass to the document's "Save" method
 // to modify how we save the document to plaintext.
 TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

 Assert.assertEquals(SaveFormat.TEXT, txtSaveOptions.getSaveFormat());

 // Set the "ParagraphBreak" to a custom value that we wish to put at the end of every paragraph.
 txtSaveOptions.setParagraphBreak(" End of paragraph.\r\r\t");

 doc.save(getArtifactsDir() + "TxtSaveOptions.ParagraphBreak.txt", txtSaveOptions);

 String docText = new Document(getArtifactsDir() + "TxtSaveOptions.ParagraphBreak.txt").getText().trim();

 Assert.assertEquals("Paragraph 1. End of paragraph.\r\r\t" +
         "Paragraph 2. End of paragraph.\r\r\t" +
         "Paragraph 3. End of paragraph.", docText);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

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

### setSaveFormat(int value) {#setSaveFormat-int}
```
public void setSaveFormat(int value)
```


Specifies the format in which the document will be saved if this save options object is used. Can only be [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat/\#MARKDOWN).

 **Examples:** 

Shows how to rename the image name during saving into Markdown document.

```

 public void renameImages() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
     // If we convert a document that contains images into Markdown, we will end up with one Markdown file which links to several images.
     // Each image will be in the form of a file in the local file system.
     // There is also a callback that can customize the name and file system location of each image.
     saveOptions.setImageSavingCallback(new SavedImageRename("MarkdownSaveOptions.HandleDocument.md"));
     saveOptions.setSaveFormat(SaveFormat.MARKDOWN);

     // The ImageSaving() method of our callback will be run at this time.
     doc.save(getArtifactsDir() + "MarkdownSaveOptions.HandleDocument.md", saveOptions);

     Supplier> filteredShapes = () -> DocumentHelper.directoryGetFiles(
             getArtifactsDir(), "*").stream().
             filter(s -> s.startsWith(getArtifactsDir() + "MarkdownSaveOptions.HandleDocument.md shape"));

     Assert.assertEquals(1, filteredShapes.get().filter(f -> f.endsWith(".jpeg")).count());
     Assert.assertEquals(8, filteredShapes.get().filter(f -> f.endsWith(".png")).count());
 }

 /// 
 /// Renames saved images that are produced when an Markdown document is saved.
 /// 
 public static class SavedImageRename implements IImageSavingCallback
 {
     public SavedImageRename(String outFileName)
     {
         mOutFileName = outFileName;
     }

     public void imageSaving(ImageSavingArgs args) throws Exception
     {
         String imageFileName = MessageFormat.format("{0} shape {1}, of type {2}.{3}",
                 mOutFileName, ++mCount, args.getCurrentShape().getShapeType(),
                 FilenameUtils.getExtension(args.getImageFileName()));

         args.setImageFileName(imageFileName);
         args.setImageStream(new FileOutputStream(getArtifactsDir() + imageFileName));

         Assert.assertTrue(args.isImageAvailable());
         Assert.assertFalse(args.getKeepImageStreamOpen());
     }

     private int mCount;
     private String mOutFileName;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [SaveFormat](../../com.aspose.words/saveformat/) constants. |

### setTableContentAlignment(int value) {#setTableContentAlignment-int}
```
public void setTableContentAlignment(int value)
```


Sets a value that specifies how to align contents in tables when exporting into the [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat/\#MARKDOWN) format. The default value is [TableContentAlignment.AUTO](../../com.aspose.words/tablecontentalignment/\#AUTO).

 **Examples:** 

Shows how to align contents in tables.

```

 DocumentBuilder builder = new DocumentBuilder();

 builder.insertCell();
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.RIGHT);
 builder.write("Cell1");
 builder.insertCell();
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.write("Cell2");

 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions(); { saveOptions.setTableContentAlignment(tableContentAlignment); }

 builder.getDocument().save(getArtifactsDir() + "MarkdownSaveOptions.MarkdownDocumentTableContentAlignment.md", saveOptions);

 Document doc = new Document(getArtifactsDir() + "MarkdownSaveOptions.MarkdownDocumentTableContentAlignment.md");
 Table table = doc.getFirstSection().getBody().getTables().get(0);

 switch (tableContentAlignment)
 {
     case TableContentAlignment.AUTO:
         Assert.assertEquals(ParagraphAlignment.RIGHT,
             table.getFirstRow().getCells().get(0).getFirstParagraph().getParagraphFormat().getAlignment());
         Assert.assertEquals(ParagraphAlignment.CENTER,
             table.getFirstRow().getCells().get(1).getFirstParagraph().getParagraphFormat().getAlignment());
         break;
     case TableContentAlignment.LEFT:
         Assert.assertEquals(ParagraphAlignment.LEFT,
             table.getFirstRow().getCells().get(0).getFirstParagraph().getParagraphFormat().getAlignment());
         Assert.assertEquals(ParagraphAlignment.LEFT,
             table.getFirstRow().getCells().get(1).getFirstParagraph().getParagraphFormat().getAlignment());
         break;
     case TableContentAlignment.CENTER:
         Assert.assertEquals(ParagraphAlignment.CENTER,
             table.getFirstRow().getCells().get(0).getFirstParagraph().getParagraphFormat().getAlignment());
         Assert.assertEquals(ParagraphAlignment.CENTER,
             table.getFirstRow().getCells().get(1).getFirstParagraph().getParagraphFormat().getAlignment());
         break;
     case TableContentAlignment.RIGHT:
         Assert.assertEquals(ParagraphAlignment.RIGHT,
             table.getFirstRow().getCells().get(0).getFirstParagraph().getParagraphFormat().getAlignment());
         Assert.assertEquals(ParagraphAlignment.RIGHT,
             table.getFirstRow().getCells().get(1).getFirstParagraph().getParagraphFormat().getAlignment());
         break;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value that specifies how to align contents in tables when exporting into the [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat/\#MARKDOWN) format. The value must be one of [TableContentAlignment](../../com.aspose.words/tablecontentalignment/) constants. |

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

