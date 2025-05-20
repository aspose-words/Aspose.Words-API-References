---
title: XamlFixedSaveOptions
linktitle: XamlFixedSaveOptions
second_title: Aspose.Words for Java
description: Can be used to specify additional options when saving a document into the SaveFormat.XAML_FIXED format in Java.
type: docs
weight: 728
url: /java/com.aspose.words/xamlfixedsaveoptions/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.SaveOptions](../../com.aspose.words/saveoptions/), [com.aspose.words.FixedPageSaveOptions](../../com.aspose.words/fixedpagesaveoptions/)
```
public class XamlFixedSaveOptions extends FixedPageSaveOptions
```

Can be used to specify additional options when saving a document into the [SaveFormat.XAML\_FIXED](../../com.aspose.words/saveformat/\#XAML-FIXED) format.

To learn more, visit the [ Specify Save Options ][Specify Save Options] documentation article.

 **Examples:** 

Shows how to print the URIs of linked resources created while converting a document to fixed-form .xaml.

```

 public void resourceFolder() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");
     ResourceUriPrinter callback = new ResourceUriPrinter();

     // Create a "XamlFixedSaveOptions" object, which we can pass to the document's "Save" method
     // to modify how we save the document to the XAML save format.
     XamlFixedSaveOptions options = new XamlFixedSaveOptions();

     Assert.assertEquals(SaveFormat.XAML_FIXED, options.getSaveFormat());

     // Use the "ResourcesFolder" property to assign a folder in the local file system into which
     // Aspose.Words will save all the document's linked resources, such as images and fonts.
     options.setResourcesFolder(getArtifactsDir() + "XamlFixedResourceFolder");

     // Use the "ResourcesFolderAlias" property to use this folder
     // when constructing image URIs instead of the resources folder's name.
     options.setResourcesFolderAlias(getArtifactsDir() + "XamlFixedFolderAlias");

     options.setResourceSavingCallback(callback);

     // A folder specified by "ResourcesFolderAlias" will need to contain the resources instead of "ResourcesFolder".
     // We must ensure the folder exists before the callback's streams can put their resources into it.
     new File(options.getResourcesFolderAlias()).mkdir();

     doc.save(getArtifactsDir() + "XamlFixedSaveOptions.ResourceFolder.xaml", options);

     for (String resource : callback.getResources())
         System.out.println(resource);
 }

 /// 
 /// Counts and prints URIs of resources created during conversion to fixed .xaml.
 /// 
 private static class ResourceUriPrinter implements IResourceSavingCallback {
     public ResourceUriPrinter() {
         mResources = new ArrayList<>();
     }

     public void resourceSaving(ResourceSavingArgs args) throws Exception {
         getResources().add(MessageFormat.format("Resource \"{0}\"\n\t{1}", args.getResourceFileName(), args.getResourceFileUri()));

         // If we specified a resource folder alias, we would also need
         // to redirect each stream to put its resource in the alias folder.
         args.setResourceStream(new FileOutputStream(args.getResourceFileUri()));
         args.setKeepResourceStreamOpen(false);
     }

     public ArrayList getResources() {
         return mResources;
     }

     private final ArrayList mResources;
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
| [getDefaultTemplate()](#getDefaultTemplate) | Gets path to default template (including filename). |
| [getDml3DEffectsRenderingMode()](#getDml3DEffectsRenderingMode) | Gets a value determining how 3D effects are rendered. |
| [getDmlEffectsRenderingMode()](#getDmlEffectsRenderingMode) | Gets a value determining how DrawingML effects are rendered. |
| [getDmlRenderingMode()](#getDmlRenderingMode) | Gets a value determining how DrawingML shapes are rendered. |
| [getExportGeneratorName()](#getExportGeneratorName) | When  true , causes the name and version of Aspose.Words to be embedded into produced files. |
| [getImlRenderingMode()](#getImlRenderingMode) | Gets a value determining how ink (InkML) objects are rendered. |
| [getJpegQuality()](#getJpegQuality) | Gets a value determining the quality of the JPEG images inside Html document. |
| [getMemoryOptimization()](#getMemoryOptimization) | Gets value determining if memory optimization should be performed before saving the document. |
| [getMetafileRenderingOptions()](#getMetafileRenderingOptions) | Allows to specify metafile rendering options. |
| [getNumeralFormat()](#getNumeralFormat) | Gets [NumeralFormat](../../com.aspose.words/numeralformat/) used for rendering of numerals. |
| [getOptimizeOutput()](#getOptimizeOutput) | Flag indicates whether it is required to optimize output. |
| [getPageSavingCallback()](#getPageSavingCallback) | Allows to control how separate pages are saved when a document is exported to fixed page format. |
| [getPageSet()](#getPageSet) | Gets the pages to render. |
| [getPrettyFormat()](#getPrettyFormat) | When  true , pretty formats output where applicable. |
| [getProgressCallback()](#getProgressCallback) | Called during saving a document and accepts data about saving progress. |
| [getResourceSavingCallback()](#getResourceSavingCallback) | Allows to control how resources (images and fonts) are saved when a document is exported to fixed page Xaml format. |
| [getResourcesFolder()](#getResourcesFolder) | Specifies the physical folder where resources (images and fonts) are saved when exporting a document to fixed page Xaml format. |
| [getResourcesFolderAlias()](#getResourcesFolderAlias) | Specifies the name of the folder used to construct image URIs written into an fixed page Xaml document. |
| [getSaveFormat()](#getSaveFormat) | Specifies the format in which the document will be saved if this save options object is used. |
| [getTempFolder()](#getTempFolder) | Specifies the folder for temporary files used when saving to a DOC or DOCX file. |
| [getUpdateAmbiguousTextFont()](#getUpdateAmbiguousTextFont) | Determines whether the font attributes will be changed according to the character code being used. |
| [getUpdateCreatedTimeProperty()](#getUpdateCreatedTimeProperty) | Gets a value determining whether the [BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties/\#getCreatedTime) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setCreatedTime-java.util.Date) property is updated before saving. |
| [getUpdateFields()](#getUpdateFields) | Gets a value determining if fields of certain types should be updated before saving the document to a fixed page format. |
| [getUpdateLastPrintedProperty()](#getUpdateLastPrintedProperty) | Gets a value determining whether the [BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties/\#getLastPrinted) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastPrinted-java.util.Date) property is updated before saving. |
| [getUpdateLastSavedTimeProperty()](#getUpdateLastSavedTimeProperty) | Gets a value determining whether the [BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties/\#getLastSavedTime) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastSavedTime-java.util.Date) property is updated before saving. |
| [getUseAntiAliasing()](#getUseAntiAliasing) | Gets a value determining whether or not to use anti-aliasing for rendering. |
| [getUseHighQualityRendering()](#getUseHighQualityRendering) | Gets a value determining whether or not to use high quality (i.e. |
| [getUseJAIImageRendering()](#getUseJAIImageRendering) | Gets a value that determines whether JAI is employed during the rendering of document images. |
| [setAllowEmbeddingPostScriptFonts(boolean value)](#setAllowEmbeddingPostScriptFonts-boolean) | Sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. |
| [setColorMode(int value)](#setColorMode-int) | Sets a value determining how colors are rendered. |
| [setDefaultTemplate(String value)](#setDefaultTemplate-java.lang.String) | Sets path to default template (including filename). |
| [setDml3DEffectsRenderingMode(int value)](#setDml3DEffectsRenderingMode-int) | Sets a value determining how 3D effects are rendered. |
| [setDmlEffectsRenderingMode(int value)](#setDmlEffectsRenderingMode-int) | Sets a value determining how DrawingML effects are rendered. |
| [setDmlRenderingMode(int value)](#setDmlRenderingMode-int) | Sets a value determining how DrawingML shapes are rendered. |
| [setExportGeneratorName(boolean value)](#setExportGeneratorName-boolean) | When  true , causes the name and version of Aspose.Words to be embedded into produced files. |
| [setImlRenderingMode(int value)](#setImlRenderingMode-int) | Sets a value determining how ink (InkML) objects are rendered. |
| [setJpegQuality(int value)](#setJpegQuality-int) | Sets a value determining the quality of the JPEG images inside Html document. |
| [setMemoryOptimization(boolean value)](#setMemoryOptimization-boolean) | Sets value determining if memory optimization should be performed before saving the document. |
| [setMetafileRenderingOptions(MetafileRenderingOptions value)](#setMetafileRenderingOptions-com.aspose.words.MetafileRenderingOptions) | Allows to specify metafile rendering options. |
| [setNumeralFormat(int value)](#setNumeralFormat-int) | Sets [NumeralFormat](../../com.aspose.words/numeralformat/) used for rendering of numerals. |
| [setOptimizeOutput(boolean value)](#setOptimizeOutput-boolean) | Flag indicates whether it is required to optimize output. |
| [setPageSavingCallback(IPageSavingCallback value)](#setPageSavingCallback-com.aspose.words.IPageSavingCallback) | Allows to control how separate pages are saved when a document is exported to fixed page format. |
| [setPageSet(PageSet value)](#setPageSet-com.aspose.words.PageSet) | Sets the pages to render. |
| [setPrettyFormat(boolean value)](#setPrettyFormat-boolean) | When  true , pretty formats output where applicable. |
| [setProgressCallback(IDocumentSavingCallback value)](#setProgressCallback-com.aspose.words.IDocumentSavingCallback) | Called during saving a document and accepts data about saving progress. |
| [setResourceSavingCallback(IResourceSavingCallback value)](#setResourceSavingCallback-com.aspose.words.IResourceSavingCallback) | Allows to control how resources (images and fonts) are saved when a document is exported to fixed page Xaml format. |
| [setResourcesFolder(String value)](#setResourcesFolder-java.lang.String) | Specifies the physical folder where resources (images and fonts) are saved when exporting a document to fixed page Xaml format. |
| [setResourcesFolderAlias(String value)](#setResourcesFolderAlias-java.lang.String) | Specifies the name of the folder used to construct image URIs written into an fixed page Xaml document. |
| [setSaveFormat(int value)](#setSaveFormat-int) | Specifies the format in which the document will be saved if this save options object is used. |
| [setTempFolder(String value)](#setTempFolder-java.lang.String) | Specifies the folder for temporary files used when saving to a DOC or DOCX file. |
| [setUpdateAmbiguousTextFont(boolean value)](#setUpdateAmbiguousTextFont-boolean) | Determines whether the font attributes will be changed according to the character code being used. |
| [setUpdateCreatedTimeProperty(boolean value)](#setUpdateCreatedTimeProperty-boolean) | Sets a value determining whether the [BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties/\#getCreatedTime) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setCreatedTime-java.util.Date) property is updated before saving. |
| [setUpdateFields(boolean value)](#setUpdateFields-boolean) | Sets a value determining if fields of certain types should be updated before saving the document to a fixed page format. |
| [setUpdateLastPrintedProperty(boolean value)](#setUpdateLastPrintedProperty-boolean) | Sets a value determining whether the [BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties/\#getLastPrinted) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastPrinted-java.util.Date) property is updated before saving. |
| [setUpdateLastSavedTimeProperty(boolean value)](#setUpdateLastSavedTimeProperty-boolean) | Sets a value determining whether the [BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties/\#getLastSavedTime) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastSavedTime-java.util.Date) property is updated before saving. |
| [setUseAntiAliasing(boolean value)](#setUseAntiAliasing-boolean) | Sets a value determining whether or not to use anti-aliasing for rendering. |
| [setUseHighQualityRendering(boolean value)](#setUseHighQualityRendering-boolean) | Sets a value determining whether or not to use high quality (i.e. |
| [setUseJAIImageRendering(boolean value)](#setUseJAIImageRendering-boolean) | Sets a value that determines whether JAI is employed during the rendering of document images. |
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


Flag indicates whether it is required to optimize output. If this flag is set redundant nested canvases and empty canvases are removed, also neighbor glyphs with the same formatting are concatenated. Note: The accuracy of the content display may be affected if this property is set to  true . Default is  false .

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
     Assert.assertEquals(60385.0,
         new File(getArtifactsDir() + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html").length(), 200.0);
 else
     Assert.assertEquals(191000.0,
         new File(getArtifactsDir() + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html").length(), 200.0);
 
```

Shows how to optimize document objects while saving to xps.

```

 Document doc = new Document(getMyDir() + "Unoptimized document.docx");

 // Create an "XpsSaveOptions" object to pass to the document's "Save" method
 // to modify how that method converts the document to .XPS.
 XpsSaveOptions saveOptions = new XpsSaveOptions();

 // Set the "OptimizeOutput" property to "true" to take measures such as removing nested or empty canvases
 // and concatenating adjacent runs with identical formatting to optimize the output document's content.
 // This may affect the appearance of the document.
 // Set the "OptimizeOutput" property to "false" to save the document normally.
 saveOptions.setOptimizeOutput(optimizeOutput);

 doc.save(getArtifactsDir() + "XpsSaveOptions.OptimizeOutput.xps", saveOptions);
 
```

**Returns:**
boolean - The corresponding  boolean  value.
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


Allows to control how resources (images and fonts) are saved when a document is exported to fixed page Xaml format.

 **Examples:** 

Shows how to print the URIs of linked resources created while converting a document to fixed-form .xaml.

```

 public void resourceFolder() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");
     ResourceUriPrinter callback = new ResourceUriPrinter();

     // Create a "XamlFixedSaveOptions" object, which we can pass to the document's "Save" method
     // to modify how we save the document to the XAML save format.
     XamlFixedSaveOptions options = new XamlFixedSaveOptions();

     Assert.assertEquals(SaveFormat.XAML_FIXED, options.getSaveFormat());

     // Use the "ResourcesFolder" property to assign a folder in the local file system into which
     // Aspose.Words will save all the document's linked resources, such as images and fonts.
     options.setResourcesFolder(getArtifactsDir() + "XamlFixedResourceFolder");

     // Use the "ResourcesFolderAlias" property to use this folder
     // when constructing image URIs instead of the resources folder's name.
     options.setResourcesFolderAlias(getArtifactsDir() + "XamlFixedFolderAlias");

     options.setResourceSavingCallback(callback);

     // A folder specified by "ResourcesFolderAlias" will need to contain the resources instead of "ResourcesFolder".
     // We must ensure the folder exists before the callback's streams can put their resources into it.
     new File(options.getResourcesFolderAlias()).mkdir();

     doc.save(getArtifactsDir() + "XamlFixedSaveOptions.ResourceFolder.xaml", options);

     for (String resource : callback.getResources())
         System.out.println(resource);
 }

 /// 
 /// Counts and prints URIs of resources created during conversion to fixed .xaml.
 /// 
 private static class ResourceUriPrinter implements IResourceSavingCallback {
     public ResourceUriPrinter() {
         mResources = new ArrayList<>();
     }

     public void resourceSaving(ResourceSavingArgs args) throws Exception {
         getResources().add(MessageFormat.format("Resource \"{0}\"\n\t{1}", args.getResourceFileName(), args.getResourceFileUri()));

         // If we specified a resource folder alias, we would also need
         // to redirect each stream to put its resource in the alias folder.
         args.setResourceStream(new FileOutputStream(args.getResourceFileUri()));
         args.setKeepResourceStreamOpen(false);
     }

     public ArrayList getResources() {
         return mResources;
     }

     private final ArrayList mResources;
 }
 
```

**Returns:**
[IResourceSavingCallback](../../com.aspose.words/iresourcesavingcallback/) - The corresponding [IResourceSavingCallback](../../com.aspose.words/iresourcesavingcallback/) value.
### getResourcesFolder() {#getResourcesFolder}
```
public String getResourcesFolder()
```


Specifies the physical folder where resources (images and fonts) are saved when exporting a document to fixed page Xaml format. Default is  null .

 **Remarks:** 

When you save a [Document](../../com.aspose.words/document/) in fixed page Xaml format, Aspose.Words needs to save all images embedded in the document as standalone files. [getResourcesFolder()](../../com.aspose.words/xamlfixedsaveoptions/\#getResourcesFolder) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/xamlfixedsaveoptions/\#setResourcesFolder-java.lang.String) allows you to specify where the images will be saved and [getResourcesFolderAlias()](../../com.aspose.words/xamlfixedsaveoptions/\#getResourcesFolderAlias) / [setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/xamlfixedsaveoptions/\#setResourcesFolderAlias-java.lang.String) allows to specify how the image URIs will be constructed.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the images in the same folder where the document file is saved. Use [getResourcesFolder()](../../com.aspose.words/xamlfixedsaveoptions/\#getResourcesFolder) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/xamlfixedsaveoptions/\#setResourcesFolder-java.lang.String) to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the images, but still needs to save the images somewhere. In this case, you need to specify an accessible folder by using the [getResourcesFolder()](../../com.aspose.words/xamlfixedsaveoptions/\#getResourcesFolder) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/xamlfixedsaveoptions/\#setResourcesFolder-java.lang.String) property

 **Examples:** 

Shows how to print the URIs of linked resources created while converting a document to fixed-form .xaml.

```

 public void resourceFolder() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");
     ResourceUriPrinter callback = new ResourceUriPrinter();

     // Create a "XamlFixedSaveOptions" object, which we can pass to the document's "Save" method
     // to modify how we save the document to the XAML save format.
     XamlFixedSaveOptions options = new XamlFixedSaveOptions();

     Assert.assertEquals(SaveFormat.XAML_FIXED, options.getSaveFormat());

     // Use the "ResourcesFolder" property to assign a folder in the local file system into which
     // Aspose.Words will save all the document's linked resources, such as images and fonts.
     options.setResourcesFolder(getArtifactsDir() + "XamlFixedResourceFolder");

     // Use the "ResourcesFolderAlias" property to use this folder
     // when constructing image URIs instead of the resources folder's name.
     options.setResourcesFolderAlias(getArtifactsDir() + "XamlFixedFolderAlias");

     options.setResourceSavingCallback(callback);

     // A folder specified by "ResourcesFolderAlias" will need to contain the resources instead of "ResourcesFolder".
     // We must ensure the folder exists before the callback's streams can put their resources into it.
     new File(options.getResourcesFolderAlias()).mkdir();

     doc.save(getArtifactsDir() + "XamlFixedSaveOptions.ResourceFolder.xaml", options);

     for (String resource : callback.getResources())
         System.out.println(resource);
 }

 /// 
 /// Counts and prints URIs of resources created during conversion to fixed .xaml.
 /// 
 private static class ResourceUriPrinter implements IResourceSavingCallback {
     public ResourceUriPrinter() {
         mResources = new ArrayList<>();
     }

     public void resourceSaving(ResourceSavingArgs args) throws Exception {
         getResources().add(MessageFormat.format("Resource \"{0}\"\n\t{1}", args.getResourceFileName(), args.getResourceFileUri()));

         // If we specified a resource folder alias, we would also need
         // to redirect each stream to put its resource in the alias folder.
         args.setResourceStream(new FileOutputStream(args.getResourceFileUri()));
         args.setKeepResourceStreamOpen(false);
     }

     public ArrayList getResources() {
         return mResources;
     }

     private final ArrayList mResources;
 }
 
```

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getResourcesFolderAlias() {#getResourcesFolderAlias}
```
public String getResourcesFolderAlias()
```


Specifies the name of the folder used to construct image URIs written into an fixed page Xaml document. Default is  null .

 **Remarks:** 

When you save a [Document](../../com.aspose.words/document/) in fixed page Xaml format, Aspose.Words needs to save all images embedded in the document as standalone files. [getResourcesFolder()](../../com.aspose.words/xamlfixedsaveoptions/\#getResourcesFolder) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/xamlfixedsaveoptions/\#setResourcesFolder-java.lang.String) allows you to specify where the images will be saved and [getResourcesFolderAlias()](../../com.aspose.words/xamlfixedsaveoptions/\#getResourcesFolderAlias) / [setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/xamlfixedsaveoptions/\#setResourcesFolderAlias-java.lang.String) allows to specify how the image URIs will be constructed.

 **Examples:** 

Shows how to print the URIs of linked resources created while converting a document to fixed-form .xaml.

```

 public void resourceFolder() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");
     ResourceUriPrinter callback = new ResourceUriPrinter();

     // Create a "XamlFixedSaveOptions" object, which we can pass to the document's "Save" method
     // to modify how we save the document to the XAML save format.
     XamlFixedSaveOptions options = new XamlFixedSaveOptions();

     Assert.assertEquals(SaveFormat.XAML_FIXED, options.getSaveFormat());

     // Use the "ResourcesFolder" property to assign a folder in the local file system into which
     // Aspose.Words will save all the document's linked resources, such as images and fonts.
     options.setResourcesFolder(getArtifactsDir() + "XamlFixedResourceFolder");

     // Use the "ResourcesFolderAlias" property to use this folder
     // when constructing image URIs instead of the resources folder's name.
     options.setResourcesFolderAlias(getArtifactsDir() + "XamlFixedFolderAlias");

     options.setResourceSavingCallback(callback);

     // A folder specified by "ResourcesFolderAlias" will need to contain the resources instead of "ResourcesFolder".
     // We must ensure the folder exists before the callback's streams can put their resources into it.
     new File(options.getResourcesFolderAlias()).mkdir();

     doc.save(getArtifactsDir() + "XamlFixedSaveOptions.ResourceFolder.xaml", options);

     for (String resource : callback.getResources())
         System.out.println(resource);
 }

 /// 
 /// Counts and prints URIs of resources created during conversion to fixed .xaml.
 /// 
 private static class ResourceUriPrinter implements IResourceSavingCallback {
     public ResourceUriPrinter() {
         mResources = new ArrayList<>();
     }

     public void resourceSaving(ResourceSavingArgs args) throws Exception {
         getResources().add(MessageFormat.format("Resource \"{0}\"\n\t{1}", args.getResourceFileName(), args.getResourceFileUri()));

         // If we specified a resource folder alias, we would also need
         // to redirect each stream to put its resource in the alias folder.
         args.setResourceStream(new FileOutputStream(args.getResourceFileUri()));
         args.setKeepResourceStreamOpen(false);
     }

     public ArrayList getResources() {
         return mResources;
     }

     private final ArrayList mResources;
 }
 
```

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getSaveFormat() {#getSaveFormat}
```
public int getSaveFormat()
```


Specifies the format in which the document will be saved if this save options object is used. Can only be [SaveFormat.XAML\_FIXED](../../com.aspose.words/saveformat/\#XAML-FIXED).

 **Examples:** 

Shows how to print the URIs of linked resources created while converting a document to fixed-form .xaml.

```

 public void resourceFolder() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");
     ResourceUriPrinter callback = new ResourceUriPrinter();

     // Create a "XamlFixedSaveOptions" object, which we can pass to the document's "Save" method
     // to modify how we save the document to the XAML save format.
     XamlFixedSaveOptions options = new XamlFixedSaveOptions();

     Assert.assertEquals(SaveFormat.XAML_FIXED, options.getSaveFormat());

     // Use the "ResourcesFolder" property to assign a folder in the local file system into which
     // Aspose.Words will save all the document's linked resources, such as images and fonts.
     options.setResourcesFolder(getArtifactsDir() + "XamlFixedResourceFolder");

     // Use the "ResourcesFolderAlias" property to use this folder
     // when constructing image URIs instead of the resources folder's name.
     options.setResourcesFolderAlias(getArtifactsDir() + "XamlFixedFolderAlias");

     options.setResourceSavingCallback(callback);

     // A folder specified by "ResourcesFolderAlias" will need to contain the resources instead of "ResourcesFolder".
     // We must ensure the folder exists before the callback's streams can put their resources into it.
     new File(options.getResourcesFolderAlias()).mkdir();

     doc.save(getArtifactsDir() + "XamlFixedSaveOptions.ResourceFolder.xaml", options);

     for (String resource : callback.getResources())
         System.out.println(resource);
 }

 /// 
 /// Counts and prints URIs of resources created during conversion to fixed .xaml.
 /// 
 private static class ResourceUriPrinter implements IResourceSavingCallback {
     public ResourceUriPrinter() {
         mResources = new ArrayList<>();
     }

     public void resourceSaving(ResourceSavingArgs args) throws Exception {
         getResources().add(MessageFormat.format("Resource \"{0}\"\n\t{1}", args.getResourceFileName(), args.getResourceFileUri()));

         // If we specified a resource folder alias, we would also need
         // to redirect each stream to put its resource in the alias folder.
         args.setResourceStream(new FileOutputStream(args.getResourceFileUri()));
         args.setKeepResourceStreamOpen(false);
     }

     public ArrayList getResources() {
         return mResources;
     }

     private final ArrayList mResources;
 }
 
```

**Returns:**
int - The corresponding  int  value. The returned value is one of [SaveFormat](../../com.aspose.words/saveformat/) constants.
### getTempFolder() {#getTempFolder}
```
public String getTempFolder()
```


Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default this property is  null  and no temporary files are used.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getUpdateAmbiguousTextFont() {#getUpdateAmbiguousTextFont}
```
public boolean getUpdateAmbiguousTextFont()
```


Determines whether the font attributes will be changed according to the character code being used.

 **Examples:** 

Shows how to update the font to match the character code being used.

```

 Document doc = new Document(getMyDir() + "Special symbol.docx");
 Run run = doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0);
 System.out.println(run.getText()); // \u0e3f
 System.out.println(run.getFont().getName()); // Arial

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 saveOptions.setUpdateAmbiguousTextFont(true);
 doc.save(getArtifactsDir() + "OoxmlSaveOptions.UpdateAmbiguousTextFont.docx", saveOptions);

 doc = new Document(getArtifactsDir() + "OoxmlSaveOptions.UpdateAmbiguousTextFont.docx");
 run = doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0);
 System.out.println(run.getText()); // \u0e3f
 System.out.println(run.getFont().getName()); // Angsana New
 
```

**Returns:**
boolean - The corresponding  boolean  value.
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
### getUseJAIImageRendering() {#getUseJAIImageRendering}
```
public boolean getUseJAIImageRendering()
```


Gets a value that determines whether JAI is employed during the rendering of document images. In some cases, this may improve performance.

 **Remarks:** 

The default value is  true .

JAI will only be utilized if it is included as a dependency. Certain images might not render correctly if JAI is disabled.

**Returns:**
boolean
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


Flag indicates whether it is required to optimize output. If this flag is set redundant nested canvases and empty canvases are removed, also neighbor glyphs with the same formatting are concatenated. Note: The accuracy of the content display may be affected if this property is set to  true . Default is  false .

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
     Assert.assertEquals(60385.0,
         new File(getArtifactsDir() + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html").length(), 200.0);
 else
     Assert.assertEquals(191000.0,
         new File(getArtifactsDir() + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html").length(), 200.0);
 
```

Shows how to optimize document objects while saving to xps.

```

 Document doc = new Document(getMyDir() + "Unoptimized document.docx");

 // Create an "XpsSaveOptions" object to pass to the document's "Save" method
 // to modify how that method converts the document to .XPS.
 XpsSaveOptions saveOptions = new XpsSaveOptions();

 // Set the "OptimizeOutput" property to "true" to take measures such as removing nested or empty canvases
 // and concatenating adjacent runs with identical formatting to optimize the output document's content.
 // This may affect the appearance of the document.
 // Set the "OptimizeOutput" property to "false" to save the document normally.
 saveOptions.setOptimizeOutput(optimizeOutput);

 doc.save(getArtifactsDir() + "XpsSaveOptions.OptimizeOutput.xps", saveOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

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


Allows to control how resources (images and fonts) are saved when a document is exported to fixed page Xaml format.

 **Examples:** 

Shows how to print the URIs of linked resources created while converting a document to fixed-form .xaml.

```

 public void resourceFolder() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");
     ResourceUriPrinter callback = new ResourceUriPrinter();

     // Create a "XamlFixedSaveOptions" object, which we can pass to the document's "Save" method
     // to modify how we save the document to the XAML save format.
     XamlFixedSaveOptions options = new XamlFixedSaveOptions();

     Assert.assertEquals(SaveFormat.XAML_FIXED, options.getSaveFormat());

     // Use the "ResourcesFolder" property to assign a folder in the local file system into which
     // Aspose.Words will save all the document's linked resources, such as images and fonts.
     options.setResourcesFolder(getArtifactsDir() + "XamlFixedResourceFolder");

     // Use the "ResourcesFolderAlias" property to use this folder
     // when constructing image URIs instead of the resources folder's name.
     options.setResourcesFolderAlias(getArtifactsDir() + "XamlFixedFolderAlias");

     options.setResourceSavingCallback(callback);

     // A folder specified by "ResourcesFolderAlias" will need to contain the resources instead of "ResourcesFolder".
     // We must ensure the folder exists before the callback's streams can put their resources into it.
     new File(options.getResourcesFolderAlias()).mkdir();

     doc.save(getArtifactsDir() + "XamlFixedSaveOptions.ResourceFolder.xaml", options);

     for (String resource : callback.getResources())
         System.out.println(resource);
 }

 /// 
 /// Counts and prints URIs of resources created during conversion to fixed .xaml.
 /// 
 private static class ResourceUriPrinter implements IResourceSavingCallback {
     public ResourceUriPrinter() {
         mResources = new ArrayList<>();
     }

     public void resourceSaving(ResourceSavingArgs args) throws Exception {
         getResources().add(MessageFormat.format("Resource \"{0}\"\n\t{1}", args.getResourceFileName(), args.getResourceFileUri()));

         // If we specified a resource folder alias, we would also need
         // to redirect each stream to put its resource in the alias folder.
         args.setResourceStream(new FileOutputStream(args.getResourceFileUri()));
         args.setKeepResourceStreamOpen(false);
     }

     public ArrayList getResources() {
         return mResources;
     }

     private final ArrayList mResources;
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


Specifies the physical folder where resources (images and fonts) are saved when exporting a document to fixed page Xaml format. Default is  null .

 **Remarks:** 

When you save a [Document](../../com.aspose.words/document/) in fixed page Xaml format, Aspose.Words needs to save all images embedded in the document as standalone files. [getResourcesFolder()](../../com.aspose.words/xamlfixedsaveoptions/\#getResourcesFolder) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/xamlfixedsaveoptions/\#setResourcesFolder-java.lang.String) allows you to specify where the images will be saved and [getResourcesFolderAlias()](../../com.aspose.words/xamlfixedsaveoptions/\#getResourcesFolderAlias) / [setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/xamlfixedsaveoptions/\#setResourcesFolderAlias-java.lang.String) allows to specify how the image URIs will be constructed.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the images in the same folder where the document file is saved. Use [getResourcesFolder()](../../com.aspose.words/xamlfixedsaveoptions/\#getResourcesFolder) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/xamlfixedsaveoptions/\#setResourcesFolder-java.lang.String) to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the images, but still needs to save the images somewhere. In this case, you need to specify an accessible folder by using the [getResourcesFolder()](../../com.aspose.words/xamlfixedsaveoptions/\#getResourcesFolder) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/xamlfixedsaveoptions/\#setResourcesFolder-java.lang.String) property

 **Examples:** 

Shows how to print the URIs of linked resources created while converting a document to fixed-form .xaml.

```

 public void resourceFolder() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");
     ResourceUriPrinter callback = new ResourceUriPrinter();

     // Create a "XamlFixedSaveOptions" object, which we can pass to the document's "Save" method
     // to modify how we save the document to the XAML save format.
     XamlFixedSaveOptions options = new XamlFixedSaveOptions();

     Assert.assertEquals(SaveFormat.XAML_FIXED, options.getSaveFormat());

     // Use the "ResourcesFolder" property to assign a folder in the local file system into which
     // Aspose.Words will save all the document's linked resources, such as images and fonts.
     options.setResourcesFolder(getArtifactsDir() + "XamlFixedResourceFolder");

     // Use the "ResourcesFolderAlias" property to use this folder
     // when constructing image URIs instead of the resources folder's name.
     options.setResourcesFolderAlias(getArtifactsDir() + "XamlFixedFolderAlias");

     options.setResourceSavingCallback(callback);

     // A folder specified by "ResourcesFolderAlias" will need to contain the resources instead of "ResourcesFolder".
     // We must ensure the folder exists before the callback's streams can put their resources into it.
     new File(options.getResourcesFolderAlias()).mkdir();

     doc.save(getArtifactsDir() + "XamlFixedSaveOptions.ResourceFolder.xaml", options);

     for (String resource : callback.getResources())
         System.out.println(resource);
 }

 /// 
 /// Counts and prints URIs of resources created during conversion to fixed .xaml.
 /// 
 private static class ResourceUriPrinter implements IResourceSavingCallback {
     public ResourceUriPrinter() {
         mResources = new ArrayList<>();
     }

     public void resourceSaving(ResourceSavingArgs args) throws Exception {
         getResources().add(MessageFormat.format("Resource \"{0}\"\n\t{1}", args.getResourceFileName(), args.getResourceFileUri()));

         // If we specified a resource folder alias, we would also need
         // to redirect each stream to put its resource in the alias folder.
         args.setResourceStream(new FileOutputStream(args.getResourceFileUri()));
         args.setKeepResourceStreamOpen(false);
     }

     public ArrayList getResources() {
         return mResources;
     }

     private final ArrayList mResources;
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


Specifies the name of the folder used to construct image URIs written into an fixed page Xaml document. Default is  null .

 **Remarks:** 

When you save a [Document](../../com.aspose.words/document/) in fixed page Xaml format, Aspose.Words needs to save all images embedded in the document as standalone files. [getResourcesFolder()](../../com.aspose.words/xamlfixedsaveoptions/\#getResourcesFolder) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/xamlfixedsaveoptions/\#setResourcesFolder-java.lang.String) allows you to specify where the images will be saved and [getResourcesFolderAlias()](../../com.aspose.words/xamlfixedsaveoptions/\#getResourcesFolderAlias) / [setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/xamlfixedsaveoptions/\#setResourcesFolderAlias-java.lang.String) allows to specify how the image URIs will be constructed.

 **Examples:** 

Shows how to print the URIs of linked resources created while converting a document to fixed-form .xaml.

```

 public void resourceFolder() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");
     ResourceUriPrinter callback = new ResourceUriPrinter();

     // Create a "XamlFixedSaveOptions" object, which we can pass to the document's "Save" method
     // to modify how we save the document to the XAML save format.
     XamlFixedSaveOptions options = new XamlFixedSaveOptions();

     Assert.assertEquals(SaveFormat.XAML_FIXED, options.getSaveFormat());

     // Use the "ResourcesFolder" property to assign a folder in the local file system into which
     // Aspose.Words will save all the document's linked resources, such as images and fonts.
     options.setResourcesFolder(getArtifactsDir() + "XamlFixedResourceFolder");

     // Use the "ResourcesFolderAlias" property to use this folder
     // when constructing image URIs instead of the resources folder's name.
     options.setResourcesFolderAlias(getArtifactsDir() + "XamlFixedFolderAlias");

     options.setResourceSavingCallback(callback);

     // A folder specified by "ResourcesFolderAlias" will need to contain the resources instead of "ResourcesFolder".
     // We must ensure the folder exists before the callback's streams can put their resources into it.
     new File(options.getResourcesFolderAlias()).mkdir();

     doc.save(getArtifactsDir() + "XamlFixedSaveOptions.ResourceFolder.xaml", options);

     for (String resource : callback.getResources())
         System.out.println(resource);
 }

 /// 
 /// Counts and prints URIs of resources created during conversion to fixed .xaml.
 /// 
 private static class ResourceUriPrinter implements IResourceSavingCallback {
     public ResourceUriPrinter() {
         mResources = new ArrayList<>();
     }

     public void resourceSaving(ResourceSavingArgs args) throws Exception {
         getResources().add(MessageFormat.format("Resource \"{0}\"\n\t{1}", args.getResourceFileName(), args.getResourceFileUri()));

         // If we specified a resource folder alias, we would also need
         // to redirect each stream to put its resource in the alias folder.
         args.setResourceStream(new FileOutputStream(args.getResourceFileUri()));
         args.setKeepResourceStreamOpen(false);
     }

     public ArrayList getResources() {
         return mResources;
     }

     private final ArrayList mResources;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setSaveFormat(int value) {#setSaveFormat-int}
```
public void setSaveFormat(int value)
```


Specifies the format in which the document will be saved if this save options object is used. Can only be [SaveFormat.XAML\_FIXED](../../com.aspose.words/saveformat/\#XAML-FIXED).

 **Examples:** 

Shows how to print the URIs of linked resources created while converting a document to fixed-form .xaml.

```

 public void resourceFolder() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");
     ResourceUriPrinter callback = new ResourceUriPrinter();

     // Create a "XamlFixedSaveOptions" object, which we can pass to the document's "Save" method
     // to modify how we save the document to the XAML save format.
     XamlFixedSaveOptions options = new XamlFixedSaveOptions();

     Assert.assertEquals(SaveFormat.XAML_FIXED, options.getSaveFormat());

     // Use the "ResourcesFolder" property to assign a folder in the local file system into which
     // Aspose.Words will save all the document's linked resources, such as images and fonts.
     options.setResourcesFolder(getArtifactsDir() + "XamlFixedResourceFolder");

     // Use the "ResourcesFolderAlias" property to use this folder
     // when constructing image URIs instead of the resources folder's name.
     options.setResourcesFolderAlias(getArtifactsDir() + "XamlFixedFolderAlias");

     options.setResourceSavingCallback(callback);

     // A folder specified by "ResourcesFolderAlias" will need to contain the resources instead of "ResourcesFolder".
     // We must ensure the folder exists before the callback's streams can put their resources into it.
     new File(options.getResourcesFolderAlias()).mkdir();

     doc.save(getArtifactsDir() + "XamlFixedSaveOptions.ResourceFolder.xaml", options);

     for (String resource : callback.getResources())
         System.out.println(resource);
 }

 /// 
 /// Counts and prints URIs of resources created during conversion to fixed .xaml.
 /// 
 private static class ResourceUriPrinter implements IResourceSavingCallback {
     public ResourceUriPrinter() {
         mResources = new ArrayList<>();
     }

     public void resourceSaving(ResourceSavingArgs args) throws Exception {
         getResources().add(MessageFormat.format("Resource \"{0}\"\n\t{1}", args.getResourceFileName(), args.getResourceFileUri()));

         // If we specified a resource folder alias, we would also need
         // to redirect each stream to put its resource in the alias folder.
         args.setResourceStream(new FileOutputStream(args.getResourceFileUri()));
         args.setKeepResourceStreamOpen(false);
     }

     public ArrayList getResources() {
         return mResources;
     }

     private final ArrayList mResources;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [SaveFormat](../../com.aspose.words/saveformat/) constants. |

### setTempFolder(String value) {#setTempFolder-java.lang.String}
```
public void setTempFolder(String value)
```


Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default this property is  null  and no temporary files are used.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setUpdateAmbiguousTextFont(boolean value) {#setUpdateAmbiguousTextFont-boolean}
```
public void setUpdateAmbiguousTextFont(boolean value)
```


Determines whether the font attributes will be changed according to the character code being used.

 **Examples:** 

Shows how to update the font to match the character code being used.

```

 Document doc = new Document(getMyDir() + "Special symbol.docx");
 Run run = doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0);
 System.out.println(run.getText()); // \u0e3f
 System.out.println(run.getFont().getName()); // Arial

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 saveOptions.setUpdateAmbiguousTextFont(true);
 doc.save(getArtifactsDir() + "OoxmlSaveOptions.UpdateAmbiguousTextFont.docx", saveOptions);

 doc = new Document(getArtifactsDir() + "OoxmlSaveOptions.UpdateAmbiguousTextFont.docx");
 run = doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0);
 System.out.println(run.getText()); // \u0e3f
 System.out.println(run.getFont().getName()); // Angsana New
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

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

### setUseJAIImageRendering(boolean value) {#setUseJAIImageRendering-boolean}
```
public void setUseJAIImageRendering(boolean value)
```


Sets a value that determines whether JAI is employed during the rendering of document images. In some cases, this may improve performance.

 **Remarks:** 

The default value is  true .

JAI will only be utilized if it is included as a dependency. Certain images might not render correctly if JAI is disabled.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean |  |

