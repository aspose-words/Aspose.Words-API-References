---
title: HtmlSaveOptions
linktitle: HtmlSaveOptions
second_title: Aspose.Words for Java
description: Can be used to specify additional options when saving a document into the SaveFormat.HTML SaveFormat.MHTML SaveFormat.EPUB SaveFormat.AZW_3 or SaveFormat.MOBI format in Java.
type: docs
weight: 380
url: /java/com.aspose.words/htmlsaveoptions/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.SaveOptions](../../com.aspose.words/saveoptions/)

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class HtmlSaveOptions extends SaveOptions implements Cloneable
```

Can be used to specify additional options when saving a document into the [SaveFormat.HTML](../../com.aspose.words/saveformat/\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat/\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat/\#EPUB), [SaveFormat.AZW\_3](../../com.aspose.words/saveformat/\#AZW-3) or [SaveFormat.MOBI](../../com.aspose.words/saveformat/\#MOBI) format.

To learn more, visit the [ Specify Save Options ][Specify Save Options] documentation article.

 **Examples:** 

Shows how to specify the folder for storing linked images after saving to .html.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 File imagesDir = new File(getArtifactsDir() + "SaveHtmlWithOptions");

 if (imagesDir.exists())
     imagesDir.delete();

 imagesDir.mkdir();

 // Set an option to export form fields as plain text instead of HTML input elements.
 HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.HTML);
 options.setExportTextInputFormFieldAsText(true);
 options.setImagesFolder(imagesDir.getPath());

 doc.save(getArtifactsDir() + "HtmlSaveOptions.SaveHtmlWithOptions.html", options);
 
```

Shows how to use a specific encoding when saving a document to .epub.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 // Use a SaveOptions object to specify the encoding for a document that we will save.
 HtmlSaveOptions saveOptions = new HtmlSaveOptions();
 saveOptions.setSaveFormat(SaveFormat.EPUB);
 saveOptions.setEncoding(StandardCharsets.UTF_8);

 // By default, an output .epub document will have all of its contents in one HTML part.
 // A split criterion allows us to segment the document into several HTML parts.
 // We will set the criteria to split the document into heading paragraphs.
 // This is useful for readers who cannot read HTML files more significant than a specific size.
 saveOptions.setDocumentSplitCriteria(DocumentSplitCriteria.HEADING_PARAGRAPH);

 // Specify that we want to export document properties.
 saveOptions.setExportDocumentProperties(true);

 doc.save(getArtifactsDir() + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
 
```

Shows how to split a document into parts and save them.

```

 public void documentPartsFileNames() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");
     String outFileName = "SavingCallback.DocumentPartsFileNames.html";

     // Create an "HtmlFixedSaveOptions" object, which we can pass to the document's "Save" method
     // to modify how we convert the document to HTML.
     HtmlSaveOptions options = new HtmlSaveOptions();

     // If we save the document normally, there will be one output HTML
     // document with all the source document's contents.
     // Set the "DocumentSplitCriteria" property to "DocumentSplitCriteria.SectionBreak" to
     // save our document to multiple HTML files: one for each section.
     options.setDocumentSplitCriteria(DocumentSplitCriteria.SECTION_BREAK);

     // Assign a custom callback to the "DocumentPartSavingCallback" property to alter the document part saving logic.
     options.setDocumentPartSavingCallback(new SavedDocumentPartRename(outFileName, options.getDocumentSplitCriteria()));

     // If we convert a document that contains images into html, we will end up with one html file which links to several images.
     // Each image will be in the form of a file in the local file system.
     // There is also a callback that can customize the name and file system location of each image.
     options.setImageSavingCallback(new SavedImageRename(outFileName));

     doc.save(getArtifactsDir() + outFileName, options);
 }

 /// 
 /// Sets custom filenames for output documents that the saving operation splits a document into.
 /// 
 private static class SavedDocumentPartRename implements IDocumentPartSavingCallback {
     public SavedDocumentPartRename(String outFileName, int documentSplitCriteria) {
         mOutFileName = outFileName;
         mDocumentSplitCriteria = documentSplitCriteria;
     }

     public void documentPartSaving(DocumentPartSavingArgs args) throws Exception {
         // We can access the entire source document via the "Document" property.
         Assert.assertTrue(args.getDocument().getOriginalFileName().endsWith("Rendering.docx"));

         String partType = "";

         switch (mDocumentSplitCriteria) {
             case DocumentSplitCriteria.PAGE_BREAK:
                 partType = "Page";
                 break;
             case DocumentSplitCriteria.COLUMN_BREAK:
                 partType = "Column";
                 break;
             case DocumentSplitCriteria.SECTION_BREAK:
                 partType = "Section";
                 break;
             case DocumentSplitCriteria.HEADING_PARAGRAPH:
                 partType = "Paragraph from heading";
                 break;
         }

         String partFileName = MessageFormat.format("{0} part {1}, of type {2}.{3}", mOutFileName, ++mCount, partType, FilenameUtils.getExtension(args.getDocumentPartFileName()));

         // Below are two ways of specifying where Aspose.Words will save each part of the document.
         // 1 -  Set a filename for the output part file:
         args.setDocumentPartFileName(partFileName);

         // 2 -  Create a custom stream for the output part file:
         try (FileOutputStream outputStream = new FileOutputStream(getArtifactsDir() + partFileName)) {
             args.setDocumentPartStream(outputStream);
         }

         Assert.assertNotNull(args.getDocumentPartStream());
         Assert.assertFalse(args.getKeepDocumentPartStreamOpen());
     }

     private int mCount;
     private final String mOutFileName;
     private final int mDocumentSplitCriteria;
 }

 /// 
 /// Sets custom filenames for image files that an HTML conversion creates.
 /// 
 public static class SavedImageRename implements IImageSavingCallback {
     public SavedImageRename(String outFileName) {
         mOutFileName = outFileName;
     }

     public void imageSaving(ImageSavingArgs args) throws Exception {
         String imageFileName = MessageFormat.format("{0} shape {1}, of type {2}.{3}", mOutFileName, ++mCount, args.getCurrentShape().getShapeType(), FilenameUtils.getExtension(args.getImageFileName()));

         // Below are two ways of specifying where Aspose.Words will save each part of the document.
         // 1 -  Set a filename for the output image file:
         args.setImageFileName(imageFileName);

         // 2 -  Create a custom stream for the output image file:
         args.setImageStream(new FileOutputStream(getArtifactsDir() + imageFileName));

         Assert.assertNotNull(args.getImageStream());
         Assert.assertTrue(args.isImageAvailable());
         Assert.assertFalse(args.getKeepImageStreamOpen());
     }

     private int mCount;
     private final String mOutFileName;
 }
 
```


[Specify Save Options]: https://docs.aspose.com/words/java/specify-save-options/
## Constructors

| Constructor | Description |
| --- | --- |
| [HtmlSaveOptions()](#HtmlSaveOptions) | Initializes a new instance of this class that can be used to save a document in the [SaveFormat.HTML](../../com.aspose.words/saveformat/\#HTML) format. |
| [HtmlSaveOptions(int saveFormat)](#HtmlSaveOptions-int) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [createSaveOptions(int saveFormat)](#createSaveOptions-int) |  |
| [createSaveOptions(String fileName)](#createSaveOptions-java.lang.String) | Creates a save options object of a class suitable for the file extension specified in the given file name. |
| [getAllowEmbeddingPostScriptFonts()](#getAllowEmbeddingPostScriptFonts) | Gets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. |
| [getAllowNegativeIndent()](#getAllowNegativeIndent) | Specifies whether negative left and right indents of paragraphs are normalized when saving to HTML, MHTML or EPUB. |
| [getCssClassNamePrefix()](#getCssClassNamePrefix) | Specifies a prefix which is added to all CSS class names. |
| [getCssSavingCallback()](#getCssSavingCallback) | Allows to control how CSS styles are saved when a document is saved to HTML, MHTML or EPUB. |
| [getCssStyleSheetFileName()](#getCssStyleSheetFileName) | Specifies the path and the name of the Cascading Style Sheet (CSS) file written when a document is exported to HTML. |
| [getCssStyleSheetType()](#getCssStyleSheetType) | Specifies how CSS (Cascading Style Sheet) styles are exported to HTML, MHTML or EPUB. |
| [getDefaultTemplate()](#getDefaultTemplate) | Gets path to default template (including filename). |
| [getDml3DEffectsRenderingMode()](#getDml3DEffectsRenderingMode) | Gets a value determining how 3D effects are rendered. |
| [getDmlEffectsRenderingMode()](#getDmlEffectsRenderingMode) | Gets a value determining how DrawingML effects are rendered. |
| [getDmlRenderingMode()](#getDmlRenderingMode) | Gets a value determining how DrawingML shapes are rendered. |
| [getDocumentPartSavingCallback()](#getDocumentPartSavingCallback) | Allows to control how document parts are saved when a document is saved to HTML or EPUB. |
| [getDocumentSplitCriteria()](#getDocumentSplitCriteria) | Specifies how the document should be split when saving to [SaveFormat.HTML](../../com.aspose.words/saveformat/\#HTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat/\#EPUB) or [SaveFormat.AZW\_3](../../com.aspose.words/saveformat/\#AZW-3) format. |
| [getDocumentSplitHeadingLevel()](#getDocumentSplitHeadingLevel) | Specifies the maximum level of headings at which to split the document. |
| [getEncoding()](#getEncoding) |  |
| [getExportCidUrlsForMhtmlResources()](#getExportCidUrlsForMhtmlResources) | Specifies whether to use CID (Content-ID) URLs to reference resources (images, fonts, CSS) included in MHTML documents. |
| [getExportDocumentProperties()](#getExportDocumentProperties) | Specifies whether to export built-in and custom document properties to HTML, MHTML or EPUB. |
| [getExportDropDownFormFieldAsText()](#getExportDropDownFormFieldAsText) | Controls how drop-down form fields are saved to HTML or MHTML. |
| [getExportFontResources()](#getExportFontResources) | Specifies whether font resources should be exported to HTML, MHTML or EPUB. |
| [getExportFontsAsBase64()](#getExportFontsAsBase64) | Specifies whether fonts resources should be embedded to HTML in Base64 encoding. |
| [getExportGeneratorName()](#getExportGeneratorName) | When  true , causes the name and version of Aspose.Words to be embedded into produced files. |
| [getExportHeadersFootersMode()](#getExportHeadersFootersMode) | Specifies how headers and footers are output to HTML, MHTML or EPUB. |
| [getExportImagesAsBase64()](#getExportImagesAsBase64) | Specifies whether images are saved in Base64 format to the output HTML, MHTML or EPUB. |
| [getExportLanguageInformation()](#getExportLanguageInformation) | Specifies whether language information is exported to HTML, MHTML or EPUB. |
| [getExportListLabels()](#getExportListLabels) | Controls how list labels are output to HTML, MHTML or EPUB. |
| [getExportOriginalUrlForLinkedImages()](#getExportOriginalUrlForLinkedImages) | Specifies whether original URL should be used as the URL of the linked images. |
| [getExportPageMargins()](#getExportPageMargins) | Specifies whether page margins is exported to HTML, MHTML or EPUB. |
| [getExportPageSetup()](#getExportPageSetup) | Specifies whether page setup is exported to HTML, MHTML or EPUB. |
| [getExportRelativeFontSize()](#getExportRelativeFontSize) | Specifies whether font sizes should be output in relative units when saving to HTML, MHTML or EPUB. |
| [getExportRoundtripInformation()](#getExportRoundtripInformation) | Specifies whether to write the roundtrip information when saving to HTML, MHTML or EPUB. |
| [getExportShapesAsSvg()](#getExportShapesAsSvg) | Controls whether [Shape](../../com.aspose.words/shape/) nodes are converted to SVG images when saving to HTML, MHTML, EPUB or AZW3. |
| [getExportTextInputFormFieldAsText()](#getExportTextInputFormFieldAsText) | Controls how text input form fields are saved to HTML or MHTML. |
| [getExportTocPageNumbers()](#getExportTocPageNumbers) | Specifies whether to write page numbers to table of contents when saving HTML, MHTML and EPUB. |
| [getExportXhtmlTransitional()](#getExportXhtmlTransitional) | Specifies whether to write the DOCTYPE declaration when saving to HTML or MHTML. |
| [getFontResourcesSubsettingSizeThreshold()](#getFontResourcesSubsettingSizeThreshold) | Controls which font resources need subsetting when saving to HTML, MHTML or EPUB. |
| [getFontSavingCallback()](#getFontSavingCallback) | Allows to control how fonts are saved when a document is saved to HTML, MHTML or EPUB. |
| [getFontsFolder()](#getFontsFolder) | Specifies the physical folder where fonts are saved when exporting a document to HTML. |
| [getFontsFolderAlias()](#getFontsFolderAlias) | Specifies the name of the folder used to construct font URIs written into an HTML document. |
| [getHtmlVersion()](#getHtmlVersion) | Specifies version of HTML standard that should be used when saving the document to HTML or MHTML. |
| [getImageResolution()](#getImageResolution) | Specifies the output resolution for images when exporting to HTML, MHTML or EPUB. |
| [getImageSavingCallback()](#getImageSavingCallback) | Allows to control how images are saved when a document is saved to HTML, MHTML or EPUB. |
| [getImagesFolder()](#getImagesFolder) | Specifies the physical folder where images are saved when exporting a document to HTML format. |
| [getImagesFolderAlias()](#getImagesFolderAlias) | Specifies the name of the folder used to construct image URIs written into an HTML document. |
| [getImlRenderingMode()](#getImlRenderingMode) | Gets a value determining how ink (InkML) objects are rendered. |
| [getMemoryOptimization()](#getMemoryOptimization) | Gets value determining if memory optimization should be performed before saving the document. |
| [getMetafileFormat()](#getMetafileFormat) | Specifies in what format metafiles are saved when exporting to HTML, MHTML, or EPUB. |
| [getNavigationMapLevel()](#getNavigationMapLevel) | Specifies the maximum level of headings populated to the navigation map when exporting to EPUB, MOBI, or AZW3 formats. |
| [getOfficeMathOutputMode()](#getOfficeMathOutputMode) | Controls how OfficeMath objects are exported to HTML, MHTML or EPUB. |
| [getPrettyFormat()](#getPrettyFormat) | When  true , pretty formats output where applicable. |
| [getProgressCallback()](#getProgressCallback) | Called during saving a document and accepts data about saving progress. |
| [getRemoveJavaScriptFromLinks()](#getRemoveJavaScriptFromLinks) | Specifies whether JavaScript will be removed from links. |
| [getReplaceBackslashWithYenSign()](#getReplaceBackslashWithYenSign) | Specifies whether backslash characters should be replaced with yen signs. |
| [getResolveFontNames()](#getResolveFontNames) | Specifies whether font family names used in the document are resolved and substituted according to [Document.getFontSettings()](../../com.aspose.words/document/\#getFontSettings) / [Document.setFontSettings(com.aspose.words.FontSettings)](../../com.aspose.words/document/\#setFontSettings-com.aspose.words.FontSettings) when being written into HTML-based formats. |
| [getResourceFolder()](#getResourceFolder) | Specifies a physical folder where all resources like images, fonts, and external CSS are saved when a document is exported to HTML. |
| [getResourceFolderAlias()](#getResourceFolderAlias) | Specifies the name of the folder used to construct URIs of all resources written into an HTML document. |
| [getSaveFormat()](#getSaveFormat) | Specifies the format in which the document will be saved if this save options object is used. |
| [getScaleImageToShapeSize()](#getScaleImageToShapeSize) | Specifies whether images are scaled by Aspose.Words to the bounding shape size when exporting to HTML, MHTML or EPUB. |
| [getTableWidthOutputMode()](#getTableWidthOutputMode) | Controls how table, row and cell widths are exported to HTML, MHTML or EPUB. |
| [getTempFolder()](#getTempFolder) | Specifies the folder for temporary files used when saving to a DOC or DOCX file. |
| [getUpdateAmbiguousTextFont()](#getUpdateAmbiguousTextFont) | Determines whether the font attributes will be changed according to the character code being used. |
| [getUpdateCreatedTimeProperty()](#getUpdateCreatedTimeProperty) | Gets a value determining whether the [BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties/\#getCreatedTime) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setCreatedTime-java.util.Date) property is updated before saving. |
| [getUpdateFields()](#getUpdateFields) | Gets a value determining if fields of certain types should be updated before saving the document to a fixed page format. |
| [getUpdateLastPrintedProperty()](#getUpdateLastPrintedProperty) | Gets a value determining whether the [BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties/\#getLastPrinted) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastPrinted-java.util.Date) property is updated before saving. |
| [getUpdateLastSavedTimeProperty()](#getUpdateLastSavedTimeProperty) | Gets a value determining whether the [BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties/\#getLastSavedTime) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastSavedTime-java.util.Date) property is updated before saving. |
| [getUseAntiAliasing()](#getUseAntiAliasing) | Gets a value determining whether or not to use anti-aliasing for rendering. |
| [getUseHighQualityRendering()](#getUseHighQualityRendering) | Gets a value determining whether or not to use high quality (i.e. |
| [setAllowEmbeddingPostScriptFonts(boolean value)](#setAllowEmbeddingPostScriptFonts-boolean) | Sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. |
| [setAllowNegativeIndent(boolean value)](#setAllowNegativeIndent-boolean) | Specifies whether negative left and right indents of paragraphs are normalized when saving to HTML, MHTML or EPUB. |
| [setCssClassNamePrefix(String value)](#setCssClassNamePrefix-java.lang.String) | Specifies a prefix which is added to all CSS class names. |
| [setCssSavingCallback(ICssSavingCallback value)](#setCssSavingCallback-com.aspose.words.ICssSavingCallback) | Allows to control how CSS styles are saved when a document is saved to HTML, MHTML or EPUB. |
| [setCssStyleSheetFileName(String value)](#setCssStyleSheetFileName-java.lang.String) | Specifies the path and the name of the Cascading Style Sheet (CSS) file written when a document is exported to HTML. |
| [setCssStyleSheetType(int value)](#setCssStyleSheetType-int) | Specifies how CSS (Cascading Style Sheet) styles are exported to HTML, MHTML or EPUB. |
| [setDefaultTemplate(String value)](#setDefaultTemplate-java.lang.String) | Sets path to default template (including filename). |
| [setDml3DEffectsRenderingMode(int value)](#setDml3DEffectsRenderingMode-int) | Sets a value determining how 3D effects are rendered. |
| [setDmlEffectsRenderingMode(int value)](#setDmlEffectsRenderingMode-int) | Sets a value determining how DrawingML effects are rendered. |
| [setDmlRenderingMode(int value)](#setDmlRenderingMode-int) | Sets a value determining how DrawingML shapes are rendered. |
| [setDocumentPartSavingCallback(IDocumentPartSavingCallback value)](#setDocumentPartSavingCallback-com.aspose.words.IDocumentPartSavingCallback) | Allows to control how document parts are saved when a document is saved to HTML or EPUB. |
| [setDocumentSplitCriteria(int value)](#setDocumentSplitCriteria-int) | Specifies how the document should be split when saving to [SaveFormat.HTML](../../com.aspose.words/saveformat/\#HTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat/\#EPUB) or [SaveFormat.AZW\_3](../../com.aspose.words/saveformat/\#AZW-3) format. |
| [setDocumentSplitHeadingLevel(int value)](#setDocumentSplitHeadingLevel-int) | Specifies the maximum level of headings at which to split the document. |
| [setEncoding(Charset value)](#setEncoding-java.nio.charset.Charset) |  |
| [setExportCidUrlsForMhtmlResources(boolean value)](#setExportCidUrlsForMhtmlResources-boolean) | Specifies whether to use CID (Content-ID) URLs to reference resources (images, fonts, CSS) included in MHTML documents. |
| [setExportDocumentProperties(boolean value)](#setExportDocumentProperties-boolean) | Specifies whether to export built-in and custom document properties to HTML, MHTML or EPUB. |
| [setExportDropDownFormFieldAsText(boolean value)](#setExportDropDownFormFieldAsText-boolean) | Controls how drop-down form fields are saved to HTML or MHTML. |
| [setExportFontResources(boolean value)](#setExportFontResources-boolean) | Specifies whether font resources should be exported to HTML, MHTML or EPUB. |
| [setExportFontsAsBase64(boolean value)](#setExportFontsAsBase64-boolean) | Specifies whether fonts resources should be embedded to HTML in Base64 encoding. |
| [setExportGeneratorName(boolean value)](#setExportGeneratorName-boolean) | When  true , causes the name and version of Aspose.Words to be embedded into produced files. |
| [setExportHeadersFootersMode(int value)](#setExportHeadersFootersMode-int) | Specifies how headers and footers are output to HTML, MHTML or EPUB. |
| [setExportImagesAsBase64(boolean value)](#setExportImagesAsBase64-boolean) | Specifies whether images are saved in Base64 format to the output HTML, MHTML or EPUB. |
| [setExportLanguageInformation(boolean value)](#setExportLanguageInformation-boolean) | Specifies whether language information is exported to HTML, MHTML or EPUB. |
| [setExportListLabels(int value)](#setExportListLabels-int) | Controls how list labels are output to HTML, MHTML or EPUB. |
| [setExportOriginalUrlForLinkedImages(boolean value)](#setExportOriginalUrlForLinkedImages-boolean) | Specifies whether original URL should be used as the URL of the linked images. |
| [setExportPageMargins(boolean value)](#setExportPageMargins-boolean) | Specifies whether page margins is exported to HTML, MHTML or EPUB. |
| [setExportPageSetup(boolean value)](#setExportPageSetup-boolean) | Specifies whether page setup is exported to HTML, MHTML or EPUB. |
| [setExportRelativeFontSize(boolean value)](#setExportRelativeFontSize-boolean) | Specifies whether font sizes should be output in relative units when saving to HTML, MHTML or EPUB. |
| [setExportRoundtripInformation(boolean value)](#setExportRoundtripInformation-boolean) | Specifies whether to write the roundtrip information when saving to HTML, MHTML or EPUB. |
| [setExportShapesAsSvg(boolean value)](#setExportShapesAsSvg-boolean) | Controls whether [Shape](../../com.aspose.words/shape/) nodes are converted to SVG images when saving to HTML, MHTML, EPUB or AZW3. |
| [setExportTextInputFormFieldAsText(boolean value)](#setExportTextInputFormFieldAsText-boolean) | Controls how text input form fields are saved to HTML or MHTML. |
| [setExportTocPageNumbers(boolean value)](#setExportTocPageNumbers-boolean) | Specifies whether to write page numbers to table of contents when saving HTML, MHTML and EPUB. |
| [setExportXhtmlTransitional(boolean value)](#setExportXhtmlTransitional-boolean) | Specifies whether to write the DOCTYPE declaration when saving to HTML or MHTML. |
| [setFontResourcesSubsettingSizeThreshold(int value)](#setFontResourcesSubsettingSizeThreshold-int) | Controls which font resources need subsetting when saving to HTML, MHTML or EPUB. |
| [setFontSavingCallback(IFontSavingCallback value)](#setFontSavingCallback-com.aspose.words.IFontSavingCallback) | Allows to control how fonts are saved when a document is saved to HTML, MHTML or EPUB. |
| [setFontsFolder(String value)](#setFontsFolder-java.lang.String) | Specifies the physical folder where fonts are saved when exporting a document to HTML. |
| [setFontsFolderAlias(String value)](#setFontsFolderAlias-java.lang.String) | Specifies the name of the folder used to construct font URIs written into an HTML document. |
| [setHtmlVersion(int value)](#setHtmlVersion-int) | Specifies version of HTML standard that should be used when saving the document to HTML or MHTML. |
| [setImageResolution(int value)](#setImageResolution-int) | Specifies the output resolution for images when exporting to HTML, MHTML or EPUB. |
| [setImageSavingCallback(IImageSavingCallback value)](#setImageSavingCallback-com.aspose.words.IImageSavingCallback) | Allows to control how images are saved when a document is saved to HTML, MHTML or EPUB. |
| [setImagesFolder(String value)](#setImagesFolder-java.lang.String) | Specifies the physical folder where images are saved when exporting a document to HTML format. |
| [setImagesFolderAlias(String value)](#setImagesFolderAlias-java.lang.String) | Specifies the name of the folder used to construct image URIs written into an HTML document. |
| [setImlRenderingMode(int value)](#setImlRenderingMode-int) | Sets a value determining how ink (InkML) objects are rendered. |
| [setMemoryOptimization(boolean value)](#setMemoryOptimization-boolean) | Sets value determining if memory optimization should be performed before saving the document. |
| [setMetafileFormat(int value)](#setMetafileFormat-int) | Specifies in what format metafiles are saved when exporting to HTML, MHTML, or EPUB. |
| [setNavigationMapLevel(int value)](#setNavigationMapLevel-int) | Specifies the maximum level of headings populated to the navigation map when exporting to EPUB, MOBI, or AZW3 formats. |
| [setOfficeMathOutputMode(int value)](#setOfficeMathOutputMode-int) | Controls how OfficeMath objects are exported to HTML, MHTML or EPUB. |
| [setPrettyFormat(boolean value)](#setPrettyFormat-boolean) | When  true , pretty formats output where applicable. |
| [setProgressCallback(IDocumentSavingCallback value)](#setProgressCallback-com.aspose.words.IDocumentSavingCallback) | Called during saving a document and accepts data about saving progress. |
| [setRemoveJavaScriptFromLinks(boolean value)](#setRemoveJavaScriptFromLinks-boolean) | Specifies whether JavaScript will be removed from links. |
| [setReplaceBackslashWithYenSign(boolean value)](#setReplaceBackslashWithYenSign-boolean) | Specifies whether backslash characters should be replaced with yen signs. |
| [setResolveFontNames(boolean value)](#setResolveFontNames-boolean) | Specifies whether font family names used in the document are resolved and substituted according to [Document.getFontSettings()](../../com.aspose.words/document/\#getFontSettings) / [Document.setFontSettings(com.aspose.words.FontSettings)](../../com.aspose.words/document/\#setFontSettings-com.aspose.words.FontSettings) when being written into HTML-based formats. |
| [setResourceFolder(String value)](#setResourceFolder-java.lang.String) | Specifies a physical folder where all resources like images, fonts, and external CSS are saved when a document is exported to HTML. |
| [setResourceFolderAlias(String value)](#setResourceFolderAlias-java.lang.String) | Specifies the name of the folder used to construct URIs of all resources written into an HTML document. |
| [setSaveFormat(int value)](#setSaveFormat-int) | Specifies the format in which the document will be saved if this save options object is used. |
| [setScaleImageToShapeSize(boolean value)](#setScaleImageToShapeSize-boolean) | Specifies whether images are scaled by Aspose.Words to the bounding shape size when exporting to HTML, MHTML or EPUB. |
| [setTableWidthOutputMode(int value)](#setTableWidthOutputMode-int) | Controls how table, row and cell widths are exported to HTML, MHTML or EPUB. |
| [setTempFolder(String value)](#setTempFolder-java.lang.String) | Specifies the folder for temporary files used when saving to a DOC or DOCX file. |
| [setUpdateAmbiguousTextFont(boolean value)](#setUpdateAmbiguousTextFont-boolean) | Determines whether the font attributes will be changed according to the character code being used. |
| [setUpdateCreatedTimeProperty(boolean value)](#setUpdateCreatedTimeProperty-boolean) | Sets a value determining whether the [BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties/\#getCreatedTime) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setCreatedTime-java.util.Date) property is updated before saving. |
| [setUpdateFields(boolean value)](#setUpdateFields-boolean) | Sets a value determining if fields of certain types should be updated before saving the document to a fixed page format. |
| [setUpdateLastPrintedProperty(boolean value)](#setUpdateLastPrintedProperty-boolean) | Sets a value determining whether the [BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties/\#getLastPrinted) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastPrinted-java.util.Date) property is updated before saving. |
| [setUpdateLastSavedTimeProperty(boolean value)](#setUpdateLastSavedTimeProperty-boolean) | Sets a value determining whether the [BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties/\#getLastSavedTime) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastSavedTime-java.util.Date) property is updated before saving. |
| [setUseAntiAliasing(boolean value)](#setUseAntiAliasing-boolean) | Sets a value determining whether or not to use anti-aliasing for rendering. |
| [setUseHighQualityRendering(boolean value)](#setUseHighQualityRendering-boolean) | Sets a value determining whether or not to use high quality (i.e. |
### HtmlSaveOptions() {#HtmlSaveOptions}
```
public HtmlSaveOptions()
```


Initializes a new instance of this class that can be used to save a document in the [SaveFormat.HTML](../../com.aspose.words/saveformat/\#HTML) format.

 **Examples:** 

Shows how to use a specific encoding when saving a document to .epub.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 // Use a SaveOptions object to specify the encoding for a document that we will save.
 HtmlSaveOptions saveOptions = new HtmlSaveOptions();
 saveOptions.setSaveFormat(SaveFormat.EPUB);
 saveOptions.setEncoding(StandardCharsets.UTF_8);

 // By default, an output .epub document will have all of its contents in one HTML part.
 // A split criterion allows us to segment the document into several HTML parts.
 // We will set the criteria to split the document into heading paragraphs.
 // This is useful for readers who cannot read HTML files more significant than a specific size.
 saveOptions.setDocumentSplitCriteria(DocumentSplitCriteria.HEADING_PARAGRAPH);

 // Specify that we want to export document properties.
 saveOptions.setExportDocumentProperties(true);

 doc.save(getArtifactsDir() + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
 
```

### HtmlSaveOptions(int saveFormat) {#HtmlSaveOptions-int}
```
public HtmlSaveOptions(int saveFormat)
```


Initializes a new instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| saveFormat | int |  |

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
### getAllowNegativeIndent() {#getAllowNegativeIndent}
```
public boolean getAllowNegativeIndent()
```


Specifies whether negative left and right indents of paragraphs are normalized when saving to HTML, MHTML or EPUB. Default value is  false .

 **Remarks:** 

When negative indent is not allowed, it is exported as zero margin to HTML. When negative indent is allowed, a paragraph might appear partially outside of the browser window.

 **Examples:** 

Shows how to preserve negative indents in the output .html.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a table with a negative indent, which will push it to the left past the left page boundary.
 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, Cell 1");
 builder.insertCell();
 builder.write("Row 1, Cell 2");
 builder.endTable();
 table.setLeftIndent(-36);
 table.setPreferredWidth(PreferredWidth.fromPoints(144.0));

 builder.insertBreak(BreakType.PARAGRAPH_BREAK);

 // Insert a table with a positive indent, which will push the table to the right.
 table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, Cell 1");
 builder.insertCell();
 builder.write("Row 1, Cell 2");
 builder.endTable();
 table.setLeftIndent(36.0);
 table.setPreferredWidth(PreferredWidth.fromPoints(144.0));

 // When we save a document to HTML, Aspose.Words will only preserve negative indents
 // such as the one we have applied to the first table if we set the "AllowNegativeIndent" flag
 // in a SaveOptions object that we will pass to "true".
 HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.HTML);
 {
     options.setAllowNegativeIndent(allowNegativeIndent);
     options.setTableWidthOutputMode(HtmlElementSizeOutputMode.RELATIVE_ONLY);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.NegativeIndent.html", options);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlSaveOptions.NegativeIndent.html"), StandardCharsets.UTF_8);

 if (allowNegativeIndent) {
     Assert.assertTrue(outDocContents.contains(
             " "));
     Assert.assertTrue(outDocContents.contains(
             " "));
 } else {
     Assert.assertTrue(outDocContents.contains(
             " "));
     Assert.assertTrue(outDocContents.contains(
             " "));
 }
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getCssClassNamePrefix() {#getCssClassNamePrefix}
```
public String getCssClassNamePrefix()
```


Specifies a prefix which is added to all CSS class names. Default value is an empty string and generated CSS class names have no common prefix.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getCssSavingCallback() {#getCssSavingCallback}
```
public ICssSavingCallback getCssSavingCallback()
```


Allows to control how CSS styles are saved when a document is saved to HTML, MHTML or EPUB.

 **Examples:** 

Shows how to work with CSS stylesheets that an HTML conversion creates.

```

 public void externalCssFilenames() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     // Create an "HtmlFixedSaveOptions" object, which we can pass to the document's "Save" method
     // to modify how we convert the document to HTML.
     HtmlSaveOptions options = new HtmlSaveOptions();

     // Set the "CssStylesheetType" property to "CssStyleSheetType.External" to
     // accompany a saved HTML document with an external CSS stylesheet file.
     options.setCssStyleSheetType(CssStyleSheetType.EXTERNAL);

     // Below are two ways of specifying directories and filenames for output CSS stylesheets.
     // 1 -  Use the "CssStyleSheetFileName" property to assign a filename to our stylesheet:
     options.setCssStyleSheetFileName(getArtifactsDir() + "SavingCallback.ExternalCssFilenames.css");

     // 2 -  Use a custom callback to name our stylesheet:
     options.setCssSavingCallback(new CustomCssSavingCallback(getArtifactsDir() + "SavingCallback.ExternalCssFilenames.css", true, false));

     doc.save(getArtifactsDir() + "SavingCallback.ExternalCssFilenames.html", options);
 }

 /// 
 /// Sets a custom filename, along with other parameters for an external CSS stylesheet.
 /// 
 private static class CustomCssSavingCallback implements ICssSavingCallback {
     public CustomCssSavingCallback(String cssDocFilename, boolean isExportNeeded, boolean keepCssStreamOpen) {
         mCssTextFileName = cssDocFilename;
         mIsExportNeeded = isExportNeeded;
         mKeepCssStreamOpen = keepCssStreamOpen;
     }

     public void cssSaving(CssSavingArgs args) throws Exception {
         // We can access the entire source document via the "Document" property.
         Assert.assertTrue(args.getDocument().getOriginalFileName().endsWith("Rendering.docx"));

         args.setCssStream(new FileOutputStream(mCssTextFileName));
         args.isExportNeeded(mIsExportNeeded);
         args.setKeepCssStreamOpen(mKeepCssStreamOpen);
     }

     private final String mCssTextFileName;
     private final boolean mIsExportNeeded;
     private final boolean mKeepCssStreamOpen;
 }
 
```

**Returns:**
[ICssSavingCallback](../../com.aspose.words/icsssavingcallback/) - The corresponding [ICssSavingCallback](../../com.aspose.words/icsssavingcallback/) value.
### getCssStyleSheetFileName() {#getCssStyleSheetFileName}
```
public String getCssStyleSheetFileName()
```


Specifies the path and the name of the Cascading Style Sheet (CSS) file written when a document is exported to HTML. Default is an empty string.

 **Remarks:** 

This property has effect only when saving a document to HTML format and external CSS style sheet is requested using [getCssStyleSheetType()](../../com.aspose.words/htmlsaveoptions/\#getCssStyleSheetType) / [setCssStyleSheetType(int)](../../com.aspose.words/htmlsaveoptions/\#setCssStyleSheetType-int).

If this property is empty, the CSS file will be saved into the same folder and with the same name as the HTML document but with the ".css" extension.

If only path but no file name is specified in this property, the CSS file will be saved into the specified folder and will have the same name as the HTML document but with the ".css" extension.

If the folder specified by this property doesn't exist, it will be created automatically before the CSS file is saved.

Another way to specify a folder where external CSS file is saved is to use [getResourceFolder()](../../com.aspose.words/htmlsaveoptions/\#getResourceFolder) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setResourceFolder-java.lang.String).

 **Examples:** 

Shows how to work with CSS stylesheets that an HTML conversion creates.

```

 public void externalCssFilenames() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     // Create an "HtmlFixedSaveOptions" object, which we can pass to the document's "Save" method
     // to modify how we convert the document to HTML.
     HtmlSaveOptions options = new HtmlSaveOptions();

     // Set the "CssStylesheetType" property to "CssStyleSheetType.External" to
     // accompany a saved HTML document with an external CSS stylesheet file.
     options.setCssStyleSheetType(CssStyleSheetType.EXTERNAL);

     // Below are two ways of specifying directories and filenames for output CSS stylesheets.
     // 1 -  Use the "CssStyleSheetFileName" property to assign a filename to our stylesheet:
     options.setCssStyleSheetFileName(getArtifactsDir() + "SavingCallback.ExternalCssFilenames.css");

     // 2 -  Use a custom callback to name our stylesheet:
     options.setCssSavingCallback(new CustomCssSavingCallback(getArtifactsDir() + "SavingCallback.ExternalCssFilenames.css", true, false));

     doc.save(getArtifactsDir() + "SavingCallback.ExternalCssFilenames.html", options);
 }

 /// 
 /// Sets a custom filename, along with other parameters for an external CSS stylesheet.
 /// 
 private static class CustomCssSavingCallback implements ICssSavingCallback {
     public CustomCssSavingCallback(String cssDocFilename, boolean isExportNeeded, boolean keepCssStreamOpen) {
         mCssTextFileName = cssDocFilename;
         mIsExportNeeded = isExportNeeded;
         mKeepCssStreamOpen = keepCssStreamOpen;
     }

     public void cssSaving(CssSavingArgs args) throws Exception {
         // We can access the entire source document via the "Document" property.
         Assert.assertTrue(args.getDocument().getOriginalFileName().endsWith("Rendering.docx"));

         args.setCssStream(new FileOutputStream(mCssTextFileName));
         args.isExportNeeded(mIsExportNeeded);
         args.setKeepCssStreamOpen(mKeepCssStreamOpen);
     }

     private final String mCssTextFileName;
     private final boolean mIsExportNeeded;
     private final boolean mKeepCssStreamOpen;
 }
 
```

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getCssStyleSheetType() {#getCssStyleSheetType}
```
public int getCssStyleSheetType()
```


Specifies how CSS (Cascading Style Sheet) styles are exported to HTML, MHTML or EPUB. Default value is [CssStyleSheetType.INLINE](../../com.aspose.words/cssstylesheettype/\#INLINE) for HTML/MHTML and [CssStyleSheetType.EXTERNAL](../../com.aspose.words/cssstylesheettype/\#EXTERNAL) for EPUB.

 **Remarks:** 

Saving CSS style sheet into an external file is only supported when saving to HTML. When you are exporting to one of the container formats (EPUB or MHTML) and specifying [CssStyleSheetType.EXTERNAL](../../com.aspose.words/cssstylesheettype/\#EXTERNAL), CSS file will be encapsulated into the output package.

 **Examples:** 

Shows how to work with CSS stylesheets that an HTML conversion creates.

```

 public void externalCssFilenames() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     // Create an "HtmlFixedSaveOptions" object, which we can pass to the document's "Save" method
     // to modify how we convert the document to HTML.
     HtmlSaveOptions options = new HtmlSaveOptions();

     // Set the "CssStylesheetType" property to "CssStyleSheetType.External" to
     // accompany a saved HTML document with an external CSS stylesheet file.
     options.setCssStyleSheetType(CssStyleSheetType.EXTERNAL);

     // Below are two ways of specifying directories and filenames for output CSS stylesheets.
     // 1 -  Use the "CssStyleSheetFileName" property to assign a filename to our stylesheet:
     options.setCssStyleSheetFileName(getArtifactsDir() + "SavingCallback.ExternalCssFilenames.css");

     // 2 -  Use a custom callback to name our stylesheet:
     options.setCssSavingCallback(new CustomCssSavingCallback(getArtifactsDir() + "SavingCallback.ExternalCssFilenames.css", true, false));

     doc.save(getArtifactsDir() + "SavingCallback.ExternalCssFilenames.html", options);
 }

 /// 
 /// Sets a custom filename, along with other parameters for an external CSS stylesheet.
 /// 
 private static class CustomCssSavingCallback implements ICssSavingCallback {
     public CustomCssSavingCallback(String cssDocFilename, boolean isExportNeeded, boolean keepCssStreamOpen) {
         mCssTextFileName = cssDocFilename;
         mIsExportNeeded = isExportNeeded;
         mKeepCssStreamOpen = keepCssStreamOpen;
     }

     public void cssSaving(CssSavingArgs args) throws Exception {
         // We can access the entire source document via the "Document" property.
         Assert.assertTrue(args.getDocument().getOriginalFileName().endsWith("Rendering.docx"));

         args.setCssStream(new FileOutputStream(mCssTextFileName));
         args.isExportNeeded(mIsExportNeeded);
         args.setKeepCssStreamOpen(mKeepCssStreamOpen);
     }

     private final String mCssTextFileName;
     private final boolean mIsExportNeeded;
     private final boolean mKeepCssStreamOpen;
 }
 
```

**Returns:**
int - The corresponding  int  value. The returned value is one of [CssStyleSheetType](../../com.aspose.words/cssstylesheettype/) constants.
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
### getDocumentPartSavingCallback() {#getDocumentPartSavingCallback}
```
public IDocumentPartSavingCallback getDocumentPartSavingCallback()
```


Allows to control how document parts are saved when a document is saved to HTML or EPUB.

 **Examples:** 

Shows how to split a document into parts and save them.

```

 public void documentPartsFileNames() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");
     String outFileName = "SavingCallback.DocumentPartsFileNames.html";

     // Create an "HtmlFixedSaveOptions" object, which we can pass to the document's "Save" method
     // to modify how we convert the document to HTML.
     HtmlSaveOptions options = new HtmlSaveOptions();

     // If we save the document normally, there will be one output HTML
     // document with all the source document's contents.
     // Set the "DocumentSplitCriteria" property to "DocumentSplitCriteria.SectionBreak" to
     // save our document to multiple HTML files: one for each section.
     options.setDocumentSplitCriteria(DocumentSplitCriteria.SECTION_BREAK);

     // Assign a custom callback to the "DocumentPartSavingCallback" property to alter the document part saving logic.
     options.setDocumentPartSavingCallback(new SavedDocumentPartRename(outFileName, options.getDocumentSplitCriteria()));

     // If we convert a document that contains images into html, we will end up with one html file which links to several images.
     // Each image will be in the form of a file in the local file system.
     // There is also a callback that can customize the name and file system location of each image.
     options.setImageSavingCallback(new SavedImageRename(outFileName));

     doc.save(getArtifactsDir() + outFileName, options);
 }

 /// 
 /// Sets custom filenames for output documents that the saving operation splits a document into.
 /// 
 private static class SavedDocumentPartRename implements IDocumentPartSavingCallback {
     public SavedDocumentPartRename(String outFileName, int documentSplitCriteria) {
         mOutFileName = outFileName;
         mDocumentSplitCriteria = documentSplitCriteria;
     }

     public void documentPartSaving(DocumentPartSavingArgs args) throws Exception {
         // We can access the entire source document via the "Document" property.
         Assert.assertTrue(args.getDocument().getOriginalFileName().endsWith("Rendering.docx"));

         String partType = "";

         switch (mDocumentSplitCriteria) {
             case DocumentSplitCriteria.PAGE_BREAK:
                 partType = "Page";
                 break;
             case DocumentSplitCriteria.COLUMN_BREAK:
                 partType = "Column";
                 break;
             case DocumentSplitCriteria.SECTION_BREAK:
                 partType = "Section";
                 break;
             case DocumentSplitCriteria.HEADING_PARAGRAPH:
                 partType = "Paragraph from heading";
                 break;
         }

         String partFileName = MessageFormat.format("{0} part {1}, of type {2}.{3}", mOutFileName, ++mCount, partType, FilenameUtils.getExtension(args.getDocumentPartFileName()));

         // Below are two ways of specifying where Aspose.Words will save each part of the document.
         // 1 -  Set a filename for the output part file:
         args.setDocumentPartFileName(partFileName);

         // 2 -  Create a custom stream for the output part file:
         try (FileOutputStream outputStream = new FileOutputStream(getArtifactsDir() + partFileName)) {
             args.setDocumentPartStream(outputStream);
         }

         Assert.assertNotNull(args.getDocumentPartStream());
         Assert.assertFalse(args.getKeepDocumentPartStreamOpen());
     }

     private int mCount;
     private final String mOutFileName;
     private final int mDocumentSplitCriteria;
 }

 /// 
 /// Sets custom filenames for image files that an HTML conversion creates.
 /// 
 public static class SavedImageRename implements IImageSavingCallback {
     public SavedImageRename(String outFileName) {
         mOutFileName = outFileName;
     }

     public void imageSaving(ImageSavingArgs args) throws Exception {
         String imageFileName = MessageFormat.format("{0} shape {1}, of type {2}.{3}", mOutFileName, ++mCount, args.getCurrentShape().getShapeType(), FilenameUtils.getExtension(args.getImageFileName()));

         // Below are two ways of specifying where Aspose.Words will save each part of the document.
         // 1 -  Set a filename for the output image file:
         args.setImageFileName(imageFileName);

         // 2 -  Create a custom stream for the output image file:
         args.setImageStream(new FileOutputStream(getArtifactsDir() + imageFileName));

         Assert.assertNotNull(args.getImageStream());
         Assert.assertTrue(args.isImageAvailable());
         Assert.assertFalse(args.getKeepImageStreamOpen());
     }

     private int mCount;
     private final String mOutFileName;
 }
 
```

**Returns:**
[IDocumentPartSavingCallback](../../com.aspose.words/idocumentpartsavingcallback/) - The corresponding [IDocumentPartSavingCallback](../../com.aspose.words/idocumentpartsavingcallback/) value.
### getDocumentSplitCriteria() {#getDocumentSplitCriteria}
```
public int getDocumentSplitCriteria()
```


Specifies how the document should be split when saving to [SaveFormat.HTML](../../com.aspose.words/saveformat/\#HTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat/\#EPUB) or [SaveFormat.AZW\_3](../../com.aspose.words/saveformat/\#AZW-3) format. Default is [DocumentSplitCriteria.NONE](../../com.aspose.words/documentsplitcriteria/\#NONE) for HTML and [DocumentSplitCriteria.HEADING\_PARAGRAPH](../../com.aspose.words/documentsplitcriteria/\#HEADING-PARAGRAPH) for EPUB and AZW3.

 **Remarks:** 

Normally you would want a document saved to HTML as a single file. But in some cases it is preferable to split the output into several smaller HTML pages. When saving to HTML format these pages will be output to individual files or streams. When saving to EPUB format they will be incorporated into corresponding packages.

A document cannot be split when saving in the MHTML format.

 **Examples:** 

Shows how to use a specific encoding when saving a document to .epub.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 // Use a SaveOptions object to specify the encoding for a document that we will save.
 HtmlSaveOptions saveOptions = new HtmlSaveOptions();
 saveOptions.setSaveFormat(SaveFormat.EPUB);
 saveOptions.setEncoding(StandardCharsets.UTF_8);

 // By default, an output .epub document will have all of its contents in one HTML part.
 // A split criterion allows us to segment the document into several HTML parts.
 // We will set the criteria to split the document into heading paragraphs.
 // This is useful for readers who cannot read HTML files more significant than a specific size.
 saveOptions.setDocumentSplitCriteria(DocumentSplitCriteria.HEADING_PARAGRAPH);

 // Specify that we want to export document properties.
 saveOptions.setExportDocumentProperties(true);

 doc.save(getArtifactsDir() + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
 
```

**Returns:**
int - The corresponding  int  value. The returned value is a bitwise combination of [DocumentSplitCriteria](../../com.aspose.words/documentsplitcriteria/) constants.
### getDocumentSplitHeadingLevel() {#getDocumentSplitHeadingLevel}
```
public int getDocumentSplitHeadingLevel()
```


Specifies the maximum level of headings at which to split the document. Default value is  2 .

 **Remarks:** 

When [getDocumentSplitCriteria()](../../com.aspose.words/htmlsaveoptions/\#getDocumentSplitCriteria) / [setDocumentSplitCriteria(int)](../../com.aspose.words/htmlsaveoptions/\#setDocumentSplitCriteria-int) includes [DocumentSplitCriteria.HEADING\_PARAGRAPH](../../com.aspose.words/documentsplitcriteria/\#HEADING-PARAGRAPH) and this property is set to a value from 1 to 9, the document will be split at paragraphs formatted using **Heading 1**, **Heading 2** , **Heading 3** etc. styles up to the specified heading level.

By default, only **Heading 1** and **Heading 2** paragraphs cause the document to be split. Setting this property to zero will cause the document not to be split at heading paragraphs at all.

 **Examples:** 

Shows how to split an output HTML document by headings into several parts.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Every paragraph that we format using a "Heading" style can serve as a heading.
 // Each heading may also have a heading level, determined by the number of its heading style.
 // The headings below are of levels 1-3.
 builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get("Heading 1"));
 builder.writeln("Heading #1");
 builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get("Heading 2"));
 builder.writeln("Heading #2");
 builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get("Heading 3"));
 builder.writeln("Heading #3");
 builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get("Heading 1"));
 builder.writeln("Heading #4");
 builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get("Heading 2"));
 builder.writeln("Heading #5");
 builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get("Heading 3"));
 builder.writeln("Heading #6");

 // Create a HtmlSaveOptions object and set the split criteria to "HeadingParagraph".
 // These criteria will split the document at paragraphs with "Heading" styles into several smaller documents,
 // and save each document in a separate HTML file in the local file system.
 // We will also set the maximum heading level, which splits the document to 2.
 // Saving the document will split it at headings of levels 1 and 2, but not at 3 to 9.
 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setDocumentSplitCriteria(DocumentSplitCriteria.HEADING_PARAGRAPH);
     options.setDocumentSplitHeadingLevel(2);
 }

 // Our document has four headings of levels 1 - 2. One of those headings will not be
 // a split point since it is at the beginning of the document.
 // The saving operation will split our document at three places, into four smaller documents.
 doc.save(getArtifactsDir() + "HtmlSaveOptions.HeadingLevels.html", options);

 doc = new Document(getArtifactsDir() + "HtmlSaveOptions.HeadingLevels.html");

 Assert.assertEquals("Heading #1", doc.getText().trim());

 doc = new Document(getArtifactsDir() + "HtmlSaveOptions.HeadingLevels-01.html");

 Assert.assertEquals("Heading #2\r" +
         "Heading #3", doc.getText().trim());

 doc = new Document(getArtifactsDir() + "HtmlSaveOptions.HeadingLevels-02.html");

 Assert.assertEquals("Heading #4", doc.getText().trim());

 doc = new Document(getArtifactsDir() + "HtmlSaveOptions.HeadingLevels-03.html");

 Assert.assertEquals("Heading #5\rHeading #6", doc.getText().trim());
 
```

**Returns:**
int - The corresponding  int  value.
### getEncoding() {#getEncoding}
```
public Charset getEncoding()
```




**Returns:**
java.nio.charset.Charset
### getExportCidUrlsForMhtmlResources() {#getExportCidUrlsForMhtmlResources}
```
public boolean getExportCidUrlsForMhtmlResources()
```


Specifies whether to use CID (Content-ID) URLs to reference resources (images, fonts, CSS) included in MHTML documents. Default value is  false .

 **Remarks:** 

This option affects only documents being saved to MHTML.

By default, resources in MHTML documents are referenced by file name (for example, "image.png"), which are matched against "Content-Location" headers of MIME parts.

This option enables an alternative method, where references to resource files are written as CID (Content-ID) URLs (for example, "cid:image.png") and are matched against "Content-ID" headers.

In theory, there should be no difference between the two referencing methods and either of them should work fine in any browser or mail agent. In practice, however, some agents fail to fetch resources by file name. If your browser or mail agent refuses to load resources included in an MTHML document (doesn't show images or doesn't load CSS styles), try exporting the document with CID URLs.

 **Examples:** 

Shows how to enable content IDs for output MHTML documents.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 // Setting this flag will replace "Content-Location" tags
 // with "Content-ID" tags for each resource from the input document.
 HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.MHTML);
 {
     options.setExportCidUrlsForMhtmlResources(exportCidUrlsForMhtmlResources);
     options.setCssStyleSheetType(CssStyleSheetType.EXTERNAL);
     options.setExportFontResources(true);
     options.setPrettyFormat(true);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.ContentIdUrls.mht", options);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlSaveOptions.ContentIdUrls.mht"), StandardCharsets.UTF_8);

 if (exportCidUrlsForMhtmlResources) {
     Assert.assertTrue(outDocContents.contains("Content-ID: "));
     Assert.assertTrue(outDocContents.contains(""));
     Assert.assertTrue(outDocContents.contains("@font-face { font-family:'Arial Black'; font-weight:bold; src:url('cid:arib=\r\nlk.ttf') }"));
     Assert.assertTrue(outDocContents.contains(""));
 } else {
     Assert.assertTrue(outDocContents.contains("Content-Location: document.html"));
     Assert.assertTrue(outDocContents.contains(""));
     Assert.assertTrue(outDocContents.contains("@font-face { font-family:'Arial Black'; font-weight:bold; src:url('ariblk.t=\r\ntf') }"));
     Assert.assertTrue(outDocContents.contains(""));
 }
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getExportDocumentProperties() {#getExportDocumentProperties}
```
public boolean getExportDocumentProperties()
```


Specifies whether to export built-in and custom document properties to HTML, MHTML or EPUB. Default value is  false .

 **Examples:** 

Shows how to use a specific encoding when saving a document to .epub.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 // Use a SaveOptions object to specify the encoding for a document that we will save.
 HtmlSaveOptions saveOptions = new HtmlSaveOptions();
 saveOptions.setSaveFormat(SaveFormat.EPUB);
 saveOptions.setEncoding(StandardCharsets.UTF_8);

 // By default, an output .epub document will have all of its contents in one HTML part.
 // A split criterion allows us to segment the document into several HTML parts.
 // We will set the criteria to split the document into heading paragraphs.
 // This is useful for readers who cannot read HTML files more significant than a specific size.
 saveOptions.setDocumentSplitCriteria(DocumentSplitCriteria.HEADING_PARAGRAPH);

 // Specify that we want to export document properties.
 saveOptions.setExportDocumentProperties(true);

 doc.save(getArtifactsDir() + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getExportDropDownFormFieldAsText() {#getExportDropDownFormFieldAsText}
```
public boolean getExportDropDownFormFieldAsText()
```


Controls how drop-down form fields are saved to HTML or MHTML. Default value is  false .

 **Remarks:** 

When set to  true , exports drop-down form fields as normal text. When  false , exports drop-down form fields as SELECT element in HTML.

When exporting to EPUB, text drop-down form fields are always saved as text due to requirements of this format.

 **Examples:** 

Shows how to get drop-down combo box form fields to blend in with paragraph text when saving to html.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Use a document builder to insert a combo box with the value "Two" selected.
 builder.insertComboBox("MyComboBox", new String[]{"One", "Two", "Three"}, 1);

 // The "ExportDropDownFormFieldAsText" flag of this SaveOptions object allows us to
 // control how saving the document to HTML treats drop-down combo boxes.
 // Setting it to "true" will convert each combo box into simple text
 // that displays the combo box's currently selected value, effectively freezing it.
 // Setting it to "false" will preserve the functionality of the combo box using  and  tags.
 HtmlSaveOptions options = new HtmlSaveOptions();
 options.setExportDropDownFormFieldAsText(exportDropDownFormFieldAsText);

 doc.save(getArtifactsDir() + "HtmlSaveOptions.DropDownFormField.html", options);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlSaveOptions.DropDownFormField.html"), StandardCharsets.UTF_8);

 if (exportDropDownFormFieldAsText)
     Assert.assertTrue(outDocContents.contains(
             "Two"));
 else
     Assert.assertTrue(outDocContents.contains(
             "" +
                     "One" +
                     "Two" +
                     "Three" +
                     ""));
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getExportFontResources() {#getExportFontResources}
```
public boolean getExportFontResources()
```


Specifies whether font resources should be exported to HTML, MHTML or EPUB. Default is  false .

 **Remarks:** 

Exporting font resources allows for consistent document rendering independent of the fonts available in a given user's environment.

If [getExportFontResources()](../../com.aspose.words/htmlsaveoptions/\#getExportFontResources) / [setExportFontResources(boolean)](../../com.aspose.words/htmlsaveoptions/\#setExportFontResources-boolean) is set to  true , main HTML document will refer to every font via the CSS 3 **@font-face** at-rule and fonts will be output as separate files. When exporting to IDPF EPUB or MHTML formats, fonts will be embedded into the corresponding package along with other subsidiary files.

If [getExportFontsAsBase64()](../../com.aspose.words/htmlsaveoptions/\#getExportFontsAsBase64) / [setExportFontsAsBase64(boolean)](../../com.aspose.words/htmlsaveoptions/\#setExportFontsAsBase64-boolean) is set to  true , fonts will not be saved to separate files. Instead, they will be embedded into **@font-face** at-rules in Base64 encoding.

**Important!** When exporting font resources, font licensing issues should be considered. Authors who want to use specific fonts via a downloadable font mechanism must always carefully verify that their intended use is within the scope of the font license. Many commercial fonts presently do not allow web downloading of their fonts in any form. License agreements that cover some fonts specifically note that usage via **@font-face** rules in CSS style sheets is not allowed. Font subsetting can also violate license terms.

 **Examples:** 

Shows how to define custom logic for exporting fonts when saving to HTML.

```

 public void saveExportedFonts() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     // Configure a SaveOptions object to export fonts to separate files.
     // Set a callback that will handle font saving in a custom manner.
     HtmlSaveOptions options = new HtmlSaveOptions();
     {
         options.setExportFontResources(true);
         options.setFontSavingCallback(new HandleFontSaving());
     }

     // The callback will export .ttf files and save them alongside the output document.
     doc.save(getArtifactsDir() + "HtmlSaveOptions.SaveExportedFonts.html", options);

     File[] fontFileNames = new File(getArtifactsDir()).listFiles((d, name) -> name.endsWith(".ttf"));

     for (File fontFilename : fontFileNames) {
         System.out.println(fontFilename.getName());
     }

 }

 /// 
 /// Prints information about exported fonts and saves them in the same local system folder as their output .html.
 /// 
 public static class HandleFontSaving implements IFontSavingCallback {
     public void fontSaving(FontSavingArgs args) throws Exception {
         System.out.println(MessageFormat.format("Font:\t{0}", args.getFontFamilyName()));
         if (args.getBold()) System.out.print(", bold");
         if (args.getItalic()) System.out.print(", italic");
         System.out.println(MessageFormat.format("\nSource:\t{0}, {1} bytes\n", args.getOriginalFileName(), args.getOriginalFileSize()));

         // We can also access the source document from here.
         Assert.assertTrue(args.getDocument().getOriginalFileName().endsWith("Rendering.docx"));

         Assert.assertTrue(args.isExportNeeded());
         Assert.assertTrue(args.isSubsettingNeeded());

         String[] splittedFileName = args.getOriginalFileName().split("\\\\");
         String fileName = splittedFileName[splittedFileName.length - 1];

         // There are two ways of saving an exported font.
         // 1 -  Save it to a local file system location:
         args.setFontFileName(fileName);

         // 2 -  Save it to a stream:
         args.setFontStream(new FileOutputStream(fileName));
         Assert.assertFalse(args.getKeepFontStreamOpen());
     }
 }
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getExportFontsAsBase64() {#getExportFontsAsBase64}
```
public boolean getExportFontsAsBase64()
```


Specifies whether fonts resources should be embedded to HTML in Base64 encoding. Default is  false .

 **Remarks:** 

By default, fonts are written to separate files. If this option is set to  true , fonts will be embedded into the document's CSS in Base64 encoding.

 **Examples:** 

Shows how to embed fonts inside a saved HTML document.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setExportFontsAsBase64(true);
     options.setCssStyleSheetType(CssStyleSheetType.EMBEDDED);
     options.setPrettyFormat(true);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.ExportFontsAsBase64.html", options);
 
```

Shows how to save a .html document with images embedded inside it.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setExportImagesAsBase64(exportImagesAsBase64);
     options.setPrettyFormat(true);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.ExportImagesAsBase64.html", options);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlSaveOptions.ExportImagesAsBase64.html"), StandardCharsets.UTF_8);

 Assert.assertTrue(exportImagesAsBase64
         ? outDocContents.contains("
```

**Returns:**
boolean - The corresponding  boolean  value.
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


Specifies how headers and footers are output to HTML, MHTML or EPUB. Default value is [ExportHeadersFootersMode.PER\_SECTION](../../com.aspose.words/exportheadersfootersmode/\#PER-SECTION) for HTML/MHTML and [ExportHeadersFootersMode.NONE](../../com.aspose.words/exportheadersfootersmode/\#NONE) for EPUB.

 **Remarks:** 

It is hard to meaningfully output headers and footers to HTML because HTML is not paginated.

When this property is [ExportHeadersFootersMode.PER\_SECTION](../../com.aspose.words/exportheadersfootersmode/\#PER-SECTION), Aspose.Words exports only primary headers and footers at the beginning and the end of each section.

When it is [ExportHeadersFootersMode.FIRST\_SECTION\_HEADER\_LAST\_SECTION\_FOOTER](../../com.aspose.words/exportheadersfootersmode/\#FIRST-SECTION-HEADER-LAST-SECTION-FOOTER) only first primary header and the last primary footer (including linked to previous) are exported.

You can disable export of headers and footers altogether by setting this property to [ExportHeadersFootersMode.NONE](../../com.aspose.words/exportheadersfootersmode/\#NONE).

 **Examples:** 

Shows how to omit headers/footers when saving a document to HTML.

```

 Document doc = new Document(getMyDir() + "Header and footer types.docx");

 // This document contains headers and footers. We can access them via the "HeadersFooters" collection.
 Assert.assertEquals("First header", doc.getFirstSection().getHeadersFooters().getByHeaderFooterType(HeaderFooterType.HEADER_FIRST).getText().trim());

 // Formats such as .html do not split the document into pages, so headers/footers will not function the same way
 // they would when we open the document as a .docx using Microsoft Word.
 // If we convert a document with headers/footers to html, the conversion will assimilate the headers/footers into body text.
 // We can use a SaveOptions object to omit headers/footers while converting to html.
 HtmlSaveOptions saveOptions =
         new HtmlSaveOptions(SaveFormat.HTML);
 {
     saveOptions.setExportHeadersFootersMode(ExportHeadersFootersMode.NONE);
 }

 doc.save(getArtifactsDir() + "HeaderFooter.ExportMode.html", saveOptions);

 // Open our saved document and verify that it does not contain the header's text.
 doc = new Document(getArtifactsDir() + "HeaderFooter.ExportMode.html");

 Assert.assertFalse(doc.getRange().getText().contains("First header"));
 
```

**Returns:**
int - The corresponding  int  value. The returned value is one of [ExportHeadersFootersMode](../../com.aspose.words/exportheadersfootersmode/) constants.
### getExportImagesAsBase64() {#getExportImagesAsBase64}
```
public boolean getExportImagesAsBase64()
```


Specifies whether images are saved in Base64 format to the output HTML, MHTML or EPUB. Default is  false .

 **Remarks:** 

When this property is set to  true  images data are exported directly into the **img** elements and separate files are not created.

 **Examples:** 

Shows how to embed fonts inside a saved HTML document.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setExportFontsAsBase64(true);
     options.setCssStyleSheetType(CssStyleSheetType.EMBEDDED);
     options.setPrettyFormat(true);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.ExportFontsAsBase64.html", options);
 
```

Shows how to save a .html document with images embedded inside it.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setExportImagesAsBase64(exportImagesAsBase64);
     options.setPrettyFormat(true);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.ExportImagesAsBase64.html", options);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlSaveOptions.ExportImagesAsBase64.html"), StandardCharsets.UTF_8);

 Assert.assertTrue(exportImagesAsBase64
         ? outDocContents.contains("
```

**Returns:**
boolean - The corresponding  boolean  value.
### getExportLanguageInformation() {#getExportLanguageInformation}
```
public boolean getExportLanguageInformation()
```


Specifies whether language information is exported to HTML, MHTML or EPUB. Default is  false .

 **Remarks:** 

When this property is set to  true  Aspose.Words outputs **lang** HTML attribute on the document elements that specify language. This can be needed to preserve language related semantics.

 **Examples:** 

Shows how to preserve language information when saving to .html.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Use the builder to write text while formatting it in different locales.
 builder.getFont().setLocaleId(1033);
 builder.writeln("Hello world!");

 builder.getFont().setLocaleId(2057);
 builder.writeln("Hello again!");

 builder.getFont().setLocaleId(1049);
 builder.write("\u041f\u0440\u0438\u0432\u0435\u0442, \u043c\u0438\u0440!");

 // When saving the document to HTML, we can pass a SaveOptions object
 // to either preserve or discard each formatted text's locale.
 // If we set the "ExportLanguageInformation" flag to "true",
 // the output HTML document will contain the locales in "lang" attributes of  tags.
 // If we set the "ExportLanguageInformation" flag to "false',
 // the text in the output HTML document will not contain any locale information.
 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setExportLanguageInformation(exportLanguageInformation);
     options.setPrettyFormat(true);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.ExportLanguageInformation.html", options);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlSaveOptions.ExportLanguageInformation.html"), StandardCharsets.UTF_8);

 if (exportLanguageInformation) {
     Assert.assertTrue(outDocContents.contains("Hello world!"));
     Assert.assertTrue(outDocContents.contains("Hello again!"));
     Assert.assertTrue(outDocContents.contains("\u041f\u0440\u0438\u0432\u0435\u0442, \u043c\u0438\u0440!"));
 } else {
     Assert.assertTrue(outDocContents.contains("Hello world!"));
     Assert.assertTrue(outDocContents.contains("Hello again!"));
     Assert.assertTrue(outDocContents.contains("\u041f\u0440\u0438\u0432\u0435\u0442, \u043c\u0438\u0440!"));
 }
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getExportListLabels() {#getExportListLabels}
```
public int getExportListLabels()
```


Controls how list labels are output to HTML, MHTML or EPUB. Default value is [ExportListLabels.AUTO](../../com.aspose.words/exportlistlabels/\#AUTO).

 **Examples:** 

Shows how to configure list exporting to HTML.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 List list = doc.getLists().add(ListTemplate.NUMBER_DEFAULT);
 builder.getListFormat().setList(list);

 builder.writeln("Default numbered list item 1.");
 builder.writeln("Default numbered list item 2.");
 builder.getListFormat().listIndent();
 builder.writeln("Default numbered list item 3.");
 builder.getListFormat().removeNumbers();

 list = doc.getLists().add(ListTemplate.OUTLINE_HEADINGS_LEGAL);
 builder.getListFormat().setList(list);

 builder.writeln("Outline legal heading list item 1.");
 builder.writeln("Outline legal heading list item 2.");
 builder.getListFormat().listIndent();
 builder.writeln("Outline legal heading list item 3.");
 builder.getListFormat().listIndent();
 builder.writeln("Outline legal heading list item 4.");
 builder.getListFormat().listIndent();
 builder.writeln("Outline legal heading list item 5.");
 builder.getListFormat().removeNumbers();

 // When saving the document to HTML, we can pass a SaveOptions object
 // to decide which HTML elements the document will use to represent lists.
 // Setting the "ExportListLabels" property to "ExportListLabels.AsInlineText"
 // will create lists by formatting spans.
 // Setting the "ExportListLabels" property to "ExportListLabels.Auto" will use the  tag
 // to build lists in cases when using the  and  tags may cause loss of formatting.
 // Setting the "ExportListLabels" property to "ExportListLabels.ByHtmlTags"
 // will use  and  tags to build all lists.
 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setExportListLabels(exportListLabels);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.List.html", options);
 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlSaveOptions.List.html"), StandardCharsets.UTF_8);

 switch (exportListLabels) {
     case ExportListLabels.AS_INLINE_TEXT:
         Assert.assertTrue(outDocContents.contains(
                 " " +
                         "" +
                         "a." +
                         "       " +
                         "" +
                         "Default numbered list item 3." +
                         ""));

         Assert.assertTrue(outDocContents.contains(
                 " " +
                         "" +
                         "2.1.1.1" +
                         "       " +
                         "" +
                         "Outline legal heading list item 5." +
                         ""));
         break;
     case ExportListLabels.AUTO:
         Assert.assertTrue(outDocContents.contains(
                 " " +
                         " " +
                         "Default numbered list item 3." +
                         "" +
                         ""));

         break;
     case ExportListLabels.BY_HTML_TAGS:
         Assert.assertTrue(outDocContents.contains(
                 " " +
                         " " +
                         "Default numbered list item 3." +
                         "" +
                         ""));

         break;
 }
 
```

**Returns:**
int - The corresponding  int  value. The returned value is one of [ExportListLabels](../../com.aspose.words/exportlistlabels/) constants.
### getExportOriginalUrlForLinkedImages() {#getExportOriginalUrlForLinkedImages}
```
public boolean getExportOriginalUrlForLinkedImages()
```


Specifies whether original URL should be used as the URL of the linked images. Default value is  false .

 **Remarks:** 

If value is set to  true  [ImageData.getSourceFullName()](../../com.aspose.words/imagedata/\#getSourceFullName) / [ImageData.setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata/\#setSourceFullName-java.lang.String) value is used as the URL of linked images and linked images are not loaded into document's folder or [getImagesFolder()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolder) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolder-java.lang.String).

If value is set to  false  linked images are loaded into document's folder or [getImagesFolder()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolder) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolder-java.lang.String) and URL of each linked image is constructed depending on document's folder, [getImagesFolder()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolder) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolder-java.lang.String) and [getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolderAlias) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolderAlias-java.lang.String) properties.

 **Examples:** 

Shows how to set folders and folder aliases for externally saved resources that Aspose.Words will create when saving a document to HTML.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setCssStyleSheetType(CssStyleSheetType.EXTERNAL);
     options.setExportFontResources(true);
     options.setImageResolution(72);
     options.setFontResourcesSubsettingSizeThreshold(0);
     options.setFontsFolder(getArtifactsDir() + "Fonts");
     options.setImagesFolder(getArtifactsDir() + "Images");
     options.setResourceFolder(getArtifactsDir() + "Resources");
     options.setFontsFolderAlias("http://example.com/fonts");
     options.setImagesFolderAlias("http://example.com/images");
     options.setResourceFolderAlias("http://example.com/resources");
     options.setExportOriginalUrlForLinkedImages(true);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.FolderAlias.html", options);
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getExportPageMargins() {#getExportPageMargins}
```
public boolean getExportPageMargins()
```


Specifies whether page margins is exported to HTML, MHTML or EPUB. Default is  false .

 **Remarks:** 

Aspose.Words does not show area of page margins by default. If any elements are completely or partially clipped by the document edge the displayed area can be extended with this option.

 **Examples:** 

Shows how to show out-of-bounds objects in output HTML documents.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Use a builder to insert a shape with no wrapping.
 Shape shape = builder.insertShape(ShapeType.CUBE, 200.0, 200.0);

 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setWrapType(WrapType.NONE);

 // Negative shape position values may place the shape outside of page boundaries.
 // If we export this to HTML, the shape will appear truncated.
 shape.setLeft(-150);

 // When saving the document to HTML, we can pass a SaveOptions object
 // to decide whether to adjust the page to display out-of-bounds objects fully.
 // If we set the "ExportPageMargins" flag to "true", the shape will be fully visible in the output HTML.
 // If we set the "ExportPageMargins" flag to "false",
 // our document will display the shape truncated as we would see it in Microsoft Word.
 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setExportPageMargins(exportPageMargins);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.ExportPageMargins.html", options);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlSaveOptions.ExportPageMargins.html"), StandardCharsets.UTF_8);

 if (exportPageMargins)
 {
     Assert.assertTrue(outDocContents.contains(""));
     Assert.assertTrue(outDocContents.contains(" "));
 }
 else
 {
     Assert.assertFalse(outDocContents.contains("style type=\"text/css\">"));
     Assert.assertTrue(outDocContents.contains(" "));
 }
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getExportPageSetup() {#getExportPageSetup}
```
public boolean getExportPageSetup()
```


Specifies whether page setup is exported to HTML, MHTML or EPUB. Default is  false .

 **Remarks:** 

Each [Section](../../com.aspose.words/section/) in Aspose.Words document model provides page setup information via [PageSetup](../../com.aspose.words/pagesetup/) class. When you export a document to HTML format you might need to keep this information for further usage. In particular, page setup might be important for rendering to paged media (printing) or subsequent conversion to the native Microsoft Word file formats (DOCX, DOC, RTF, WML).

In most cases HTML is intended for viewing in browsers where pagination is not performed. So this feature is inactive by default.

 **Examples:** 

Shows how decide whether to preserve section structure/page setup information when saving to HTML.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Section 1");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.write("Section 2");

 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setTopMargin(36.0);
 pageSetup.setBottomMargin(36.0);
 pageSetup.setPaperSize(PaperSize.A5);

 // When saving the document to HTML, we can pass a SaveOptions object
 // to decide whether to preserve or discard page setup settings.
 // If we set the "ExportPageSetup" flag to "true", the output HTML document will contain our page setup configuration.
 // If we set the "ExportPageSetup" flag to "false", the save operation will discard our page setup settings
 // for the first section, and both sections will look identical.
 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setExportPageSetup(exportPageSetup);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.ExportPageSetup.html", options);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlSaveOptions.ExportPageSetup.html"), StandardCharsets.UTF_8);

 if (exportPageSetup) {
     Assert.assertTrue(outDocContents.contains(
             ""));

     Assert.assertTrue(outDocContents.contains(
             " " +
                     " " +
                     "Section 1" +
                     "" +
                     ""));
 } else {
     Assert.assertFalse(outDocContents.contains("style type=\"text/css\">"));

     Assert.assertTrue(outDocContents.contains(
             " " +
                     " " +
                     "Section 1" +
                     "" +
                     ""));
 }
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getExportRelativeFontSize() {#getExportRelativeFontSize}
```
public boolean getExportRelativeFontSize()
```


Specifies whether font sizes should be output in relative units when saving to HTML, MHTML or EPUB. Default is  false .

 **Remarks:** 

In many existing documents (HTML, IDPF EPUB) font sizes are specified in relative units. This allows applications to adjust text size when viewing/processing documents. For instance, Microsoft Internet Explorer has "View->Text Size" submenu, Adobe Digital Editions has two buttons: Increase/Decrease Text Size. If you expect this functionality to work then set [getExportRelativeFontSize()](../../com.aspose.words/htmlsaveoptions/\#getExportRelativeFontSize) / [setExportRelativeFontSize(boolean)](../../com.aspose.words/htmlsaveoptions/\#setExportRelativeFontSize-boolean) property to  true .

Aspose Words document model contains and operates only with absolute font size units. Relative units need additional logic to be recalculated from some initial (standard) size. Font size of **Normal** document style is taken as standard. For instance, if **Normal** has 12pt font and some text is 18pt then it will be output as **1.5em.** to the HTML.

When this option is enabled, document elements other than text will still have absolute sizes. Also some text-related attributes might be expressed absolutely. In particular, line spacing specified with "exactly" rule might produce unwanted results when scaling text. So the source documents should be properly designed and tested when exporting with [getExportRelativeFontSize()](../../com.aspose.words/htmlsaveoptions/\#getExportRelativeFontSize) / [setExportRelativeFontSize(boolean)](../../com.aspose.words/htmlsaveoptions/\#setExportRelativeFontSize-boolean) set to  true .

 **Examples:** 

Shows how to use relative font sizes when saving to .html.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Default font size, ");
 builder.getFont().setSize(24.0);
 builder.writeln("2x default font size,");
 builder.getFont().setSize(96.0);
 builder.write("8x default font size");

 // When we save the document to HTML, we can pass a SaveOptions object
 // to determine whether to use relative or absolute font sizes.
 // Set the "ExportRelativeFontSize" flag to "true" to declare font sizes
 // using the "em" measurement unit, which is a factor that multiplies the current font size.
 // Set the "ExportRelativeFontSize" flag to "false" to declare font sizes
 // using the "pt" measurement unit, which is the font's absolute size in points.
 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setExportRelativeFontSize(exportRelativeFontSize);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.RelativeFontSize.html", options);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlSaveOptions.RelativeFontSize.html"), StandardCharsets.UTF_8);

 if (exportRelativeFontSize) {
     Assert.assertTrue(outDocContents.contains(
             "" +
                     " " +
                     " " +
                     "Default font size, " +
                     "" +
                     " " +
                     "2x default font size," +
                     "" +
                     " " +
                     "8x default font size" +
                     "" +
                     "" +
                     ""));
 } else {
     Assert.assertTrue(outDocContents.contains(
             "" +
                     " " +
                     " " +
                     "Default font size, " +
                     "" +
                     " " +
                     "2x default font size," +
                     "" +
                     " " +
                     "8x default font size" +
                     "" +
                     "" +
                     ""));
 }
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getExportRoundtripInformation() {#getExportRoundtripInformation}
```
public boolean getExportRoundtripInformation()
```


Specifies whether to write the roundtrip information when saving to HTML, MHTML or EPUB. Default value is  true  for HTML and  false  for MHTML and EPUB.

 **Remarks:** 

Saving of the roundtrip information allows to restore document properties such as tab stops, comments, headers and footers during the HTML documents loading back into a [Document](../../com.aspose.words/document/) object.

When  true , the roundtrip information is exported as -aw-\* CSS properties of the corresponding HTML elements.

When  false , causes no roundtrip information to be output into produced files.

 **Examples:** 

Shows how to preserve hidden elements when converting to .html.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 // When converting a document to .html, some elements such as hidden bookmarks, original shape positions,
 // or footnotes will be either removed or converted to plain text and effectively be lost.
 // Saving with a HtmlSaveOptions object with ExportRoundtripInformation set to true will preserve these elements.

 // When we save the document to HTML, we can pass a SaveOptions object to determine
 // how the saving operation will export document elements that HTML does not support or use,
 // such as hidden bookmarks and original shape positions.
 // If we set the "ExportRoundtripInformation" flag to "true", the save operation will preserve these elements.
 // If we set the "ExportRoundTripInformation" flag to "false", the save operation will discard these elements.
 // We will want to preserve such elements if we intend to load the saved HTML using Aspose.Words,
 // as they could be of use once again.
 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setExportRoundtripInformation(exportRoundtripInformation);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.RoundTripInformation.html", options);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlSaveOptions.RoundTripInformation.html"), StandardCharsets.UTF_8);
 doc = new Document(getArtifactsDir() + "HtmlSaveOptions.RoundTripInformation.html");

 if (exportRoundtripInformation) {
     Assert.assertTrue(outDocContents.contains(" "));
     Assert.assertTrue(outDocContents.contains(" "));

     Assert.assertTrue(outDocContents.contains(
             "td colspan=\"2\" style=\"width:210.6pt; border-style:solid; border-width:0.75pt 6pt 0.75pt 0.75pt; " +
                     "padding-right:2.4pt; padding-left:5.03pt; vertical-align:top; " +
                     "-aw-border-bottom:0.5pt single; -aw-border-left:0.5pt single; -aw-border-top:0.5pt single\">"));

     Assert.assertTrue(outDocContents.contains(
             " "));

     Assert.assertTrue(outDocContents.contains(
             ""));

     Assert.assertTrue(outDocContents.contains(
             "Page number " +
                     "" +
                     "" +
                     "" +
                     "1" +
                     ""));

     Assert.assertEquals(1, IterableUtils.countMatches(doc.getRange().getFields(), f -> f.getType() == FieldType.FIELD_PAGE));
 } else {
     Assert.assertTrue(outDocContents.contains(" "));
     Assert.assertTrue(outDocContents.contains(" "));

     Assert.assertTrue(outDocContents.contains(
             ""));

     Assert.assertTrue(outDocContents.contains(
             " "));

     Assert.assertTrue(outDocContents.contains(
             ""));

     Assert.assertTrue(outDocContents.contains(
             "Page number 1"));

     Assert.assertEquals(0, IterableUtils.countMatches(doc.getRange().getFields(), f -> f.getType() == FieldType.FIELD_PAGE));
 }
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getExportShapesAsSvg() {#getExportShapesAsSvg}
```
public boolean getExportShapesAsSvg()
```


Controls whether [Shape](../../com.aspose.words/shape/) nodes are converted to SVG images when saving to HTML, MHTML, EPUB or AZW3. Default value is  false .

 **Remarks:** 

If this option is set to  true , [Shape](../../com.aspose.words/shape/) nodes are exported as  elements. Otherwise, they are rendered to bitmaps and are exported as ![Image 1][] elements.

 **Examples:** 

Shows how to export shape as scalable vector graphics.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape textBox = builder.insertShape(ShapeType.TEXT_BOX, 100.0, 60.0);
 builder.moveTo(textBox.getFirstParagraph());
 builder.write("My text box");

 // When we save the document to HTML, we can pass a SaveOptions object
 // to determine how the saving operation will export text box shapes.
 // If we set the "ExportTextBoxAsSvg" flag to "true",
 // the save operation will convert shapes with text into SVG objects.
 // If we set the "ExportTextBoxAsSvg" flag to "false",
 // the save operation will convert shapes with text into images.
 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setExportShapesAsSvg(exportShapesAsSvg);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.ExportTextBox.html", options);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlSaveOptions.ExportTextBox.html"), StandardCharsets.UTF_8);

 if (exportShapesAsSvg) {
     Assert.assertTrue(outDocContents.contains(
             "" +
                     ""));
 } else {
     Assert.assertTrue(outDocContents.contains(
             " " +
                     "" +
                     ""));
 }
 
```


[Image 1]: 

**Returns:**
boolean - The corresponding  boolean  value.
### getExportTextInputFormFieldAsText() {#getExportTextInputFormFieldAsText}
```
public boolean getExportTextInputFormFieldAsText()
```


Controls how text input form fields are saved to HTML or MHTML. Default value is  false .

 **Remarks:** 

When set to  true , exports text input form fields as normal text. When  false , exports Word text input form fields as INPUT elements in HTML.

When exporting to EPUB, text input form fields are always saved as text due to requirements of this format.

 **Examples:** 

Shows how to specify the folder for storing linked images after saving to .html.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 File imagesDir = new File(getArtifactsDir() + "SaveHtmlWithOptions");

 if (imagesDir.exists())
     imagesDir.delete();

 imagesDir.mkdir();

 // Set an option to export form fields as plain text instead of HTML input elements.
 HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.HTML);
 options.setExportTextInputFormFieldAsText(true);
 options.setImagesFolder(imagesDir.getPath());

 doc.save(getArtifactsDir() + "HtmlSaveOptions.SaveHtmlWithOptions.html", options);
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getExportTocPageNumbers() {#getExportTocPageNumbers}
```
public boolean getExportTocPageNumbers()
```


Specifies whether to write page numbers to table of contents when saving HTML, MHTML and EPUB. Default value is  false .

 **Examples:** 

Shows how to display page numbers when saving a document with a table of contents to .html.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a table of contents, and then populate the document with paragraphs formatted using a "Heading"
 // style that the table of contents will pick up as entries. Each entry will display the heading paragraph on the left,
 // and the page number that contains the heading on the right.
 FieldToc fieldToc = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

 builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get("Heading 1"));
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Entry 1");
 builder.writeln("Entry 2");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Entry 3");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Entry 4");
 fieldToc.updatePageNumbers();
 doc.updateFields();

 // HTML documents do not have pages. If we save this document to HTML,
 // the page numbers that our TOC displays will have no meaning.
 // When we save the document to HTML, we can pass a SaveOptions object to omit these page numbers from the TOC.
 // If we set the "ExportTocPageNumbers" flag to "true",
 // each TOC entry will display the heading, separator, and page number, preserving its appearance in Microsoft Word.
 // If we set the "ExportTocPageNumbers" flag to "false",
 // the save operation will omit both the separator and page number and leave the heading for each entry intact.
 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setExportTocPageNumbers(exportTocPageNumbers);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.ExportTocPageNumbers.html", options);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlSaveOptions.ExportTocPageNumbers.html"), StandardCharsets.UTF_8);

 if (exportTocPageNumbers) {
     Assert.assertTrue(outDocContents.contains(
             "Entry 1" +
                     "......................................................................" +
                     "2" +
                     " "));
 } else {
     Assert.assertTrue(outDocContents.contains(
             " " +
                     "Entry 2" +
                     ""));
 }
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getExportXhtmlTransitional() {#getExportXhtmlTransitional}
```
public boolean getExportXhtmlTransitional()
```


Specifies whether to write the DOCTYPE declaration when saving to HTML or MHTML. When  true , writes a DOCTYPE declaration in the document prior to the root element. Default value is  false . When saving to EPUB or HTML5 ( [HtmlVersion.HTML\_5](../../com.aspose.words/htmlversion/\#HTML-5)) the DOCTYPE declaration is always written.

 **Remarks:** 

Aspose.Words always writes well formed HTML regardless of this setting.

When  true , the beginning of the HTML output document will look like this:

```

 
 
 
 
```

Aspose.Words aims to output XHTML according to the XHTML 1.0 Transitional specification, but the output will not always validate against the DTD. Some structures inside a Microsoft Word document are hard or impossible to map to a document that will validate against the XHTML schema. For example, XHTML does not allow nested lists (UL cannot be nested inside another UL element), but in Microsoft Word document multilevel lists occur quite often.

 **Examples:** 

Shows how to display a DOCTYPE heading when converting documents to the Xhtml 1.0 transitional standard.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");

 HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.HTML);
 {
     options.setHtmlVersion(HtmlVersion.XHTML);
     options.setExportXhtmlTransitional(showDoctypeDeclaration);
     options.setPrettyFormat(true);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.ExportXhtmlTransitional.html", options);

 // Our document will only contain a DOCTYPE declaration heading if we have set the "ExportXhtmlTransitional" flag to "true".
 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlSaveOptions.ExportXhtmlTransitional.html"), StandardCharsets.UTF_8);

 if (showDoctypeDeclaration)
     Assert.assertTrue(outDocContents.contains(
             "\r\n" +
                     "\r\n" +
                     ""));
 else
     Assert.assertTrue(outDocContents.contains(""));
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getFontResourcesSubsettingSizeThreshold() {#getFontResourcesSubsettingSizeThreshold}
```
public int getFontResourcesSubsettingSizeThreshold()
```


Controls which font resources need subsetting when saving to HTML, MHTML or EPUB. Default is  0 .

 **Remarks:** 

[getExportFontResources()](../../com.aspose.words/htmlsaveoptions/\#getExportFontResources) / [setExportFontResources(boolean)](../../com.aspose.words/htmlsaveoptions/\#setExportFontResources-boolean) allows exporting fonts as subsidiary files or as parts of the output package. If the document uses many fonts, especially with large number of glyphs, then output size can grow significantly. Font subsetting reduces the size of the exported font resource by filtering out glyphs that are not used by the current document.

Font subsetting works as follows:

 *  By default, all exported fonts are subsetted.
 *  Setting [getFontResourcesSubsettingSizeThreshold()](../../com.aspose.words/htmlsaveoptions/\#getFontResourcesSubsettingSizeThreshold) / [setFontResourcesSubsettingSizeThreshold(int)](../../com.aspose.words/htmlsaveoptions/\#setFontResourcesSubsettingSizeThreshold-int) to a positive value instructs Aspose.Words to subset fonts which file size is larger than the specified value.
 *  Setting the property to **Integer.MAX\_VALUE** suppresses font subsetting.

**Important!** When exporting font resources, font licensing issues should be considered. Authors who want to use specific fonts via a downloadable font mechanism must always carefully verify that their intended use is within the scope of the font license. Many commercial fonts presently do not allow web downloading of their fonts in any form. License agreements that cover some fonts specifically note that usage via **@font-face** rules in CSS style sheets is not allowed. Font subsetting can also violate license terms.

 **Examples:** 

Shows how to work with font subsetting.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setName("Arial");
 builder.writeln("Hello world!");
 builder.getFont().setName("Times New Roman");
 builder.writeln("Hello world!");
 builder.getFont().setName("Courier New");
 builder.writeln("Hello world!");

 // When we save the document to HTML, we can pass a SaveOptions object configure font subsetting.
 // Suppose we set the "ExportFontResources" flag to "true" and also name a folder in the "FontsFolder" property.
 // In that case, the saving operation will create that folder and place a .ttf file inside
 // that folder for each font that our document uses.
 // Each .ttf file will contain that font's entire glyph set,
 // which may potentially result in a very large file that accompanies the document.
 // When we apply subsetting to a font, its exported raw data will only contain the glyphs that the document is
 // using instead of the entire glyph set. If the text in our document only uses a small fraction of a font's
 // glyph set, then subsetting will significantly reduce our output documents' size.
 // We can use the "FontResourcesSubsettingSizeThreshold" property to define a .ttf file size, in bytes.
 // If an exported font creates a size bigger file than that, then the save operation will apply subsetting to that font.
 // Setting a threshold of 0 applies subsetting to all fonts,
 // and setting it to "int.MaxValue" effectively disables subsetting.
 String fontsFolder = getArtifactsDir() + "HtmlSaveOptions.FontSubsetting.Fonts";

 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setExportFontResources(true);
     options.setFontsFolder(fontsFolder);
     options.setFontResourcesSubsettingSizeThreshold(fontResourcesSubsettingSizeThreshold);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.FontSubsetting.html", options);

 File[] fontFileNames = new File(fontsFolder).listFiles((d, name) -> name.endsWith(".ttf"));

 Assert.assertEquals(3, fontFileNames.length);
 
```

**Returns:**
int - The corresponding  int  value.
### getFontSavingCallback() {#getFontSavingCallback}
```
public IFontSavingCallback getFontSavingCallback()
```


Allows to control how fonts are saved when a document is saved to HTML, MHTML or EPUB.

 **Examples:** 

Shows how to define custom logic for exporting fonts when saving to HTML.

```

 public void saveExportedFonts() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     // Configure a SaveOptions object to export fonts to separate files.
     // Set a callback that will handle font saving in a custom manner.
     HtmlSaveOptions options = new HtmlSaveOptions();
     {
         options.setExportFontResources(true);
         options.setFontSavingCallback(new HandleFontSaving());
     }

     // The callback will export .ttf files and save them alongside the output document.
     doc.save(getArtifactsDir() + "HtmlSaveOptions.SaveExportedFonts.html", options);

     File[] fontFileNames = new File(getArtifactsDir()).listFiles((d, name) -> name.endsWith(".ttf"));

     for (File fontFilename : fontFileNames) {
         System.out.println(fontFilename.getName());
     }

 }

 /// 
 /// Prints information about exported fonts and saves them in the same local system folder as their output .html.
 /// 
 public static class HandleFontSaving implements IFontSavingCallback {
     public void fontSaving(FontSavingArgs args) throws Exception {
         System.out.println(MessageFormat.format("Font:\t{0}", args.getFontFamilyName()));
         if (args.getBold()) System.out.print(", bold");
         if (args.getItalic()) System.out.print(", italic");
         System.out.println(MessageFormat.format("\nSource:\t{0}, {1} bytes\n", args.getOriginalFileName(), args.getOriginalFileSize()));

         // We can also access the source document from here.
         Assert.assertTrue(args.getDocument().getOriginalFileName().endsWith("Rendering.docx"));

         Assert.assertTrue(args.isExportNeeded());
         Assert.assertTrue(args.isSubsettingNeeded());

         String[] splittedFileName = args.getOriginalFileName().split("\\\\");
         String fileName = splittedFileName[splittedFileName.length - 1];

         // There are two ways of saving an exported font.
         // 1 -  Save it to a local file system location:
         args.setFontFileName(fileName);

         // 2 -  Save it to a stream:
         args.setFontStream(new FileOutputStream(fileName));
         Assert.assertFalse(args.getKeepFontStreamOpen());
     }
 }
 
```

**Returns:**
[IFontSavingCallback](../../com.aspose.words/ifontsavingcallback/) - The corresponding [IFontSavingCallback](../../com.aspose.words/ifontsavingcallback/) value.
### getFontsFolder() {#getFontsFolder}
```
public String getFontsFolder()
```


Specifies the physical folder where fonts are saved when exporting a document to HTML. Default is an empty string.

 **Remarks:** 

When you save a [Document](../../com.aspose.words/document/) in HTML format and [getExportFontResources()](../../com.aspose.words/htmlsaveoptions/\#getExportFontResources) / [setExportFontResources(boolean)](../../com.aspose.words/htmlsaveoptions/\#setExportFontResources-boolean) is set to  true , Aspose.Words needs to save fonts used in the document as standalone files. [getFontsFolder()](../../com.aspose.words/htmlsaveoptions/\#getFontsFolder) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setFontsFolder-java.lang.String) allows you to specify where the fonts will be saved and [getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getFontsFolderAlias) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setFontsFolderAlias-java.lang.String) allows to specify how the font URIs will be constructed.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the fonts in the same folder where the document file is saved. Use [getFontsFolder()](../../com.aspose.words/htmlsaveoptions/\#getFontsFolder) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setFontsFolder-java.lang.String) to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the fonts, but still needs to save the fonts somewhere. In this case, you need to specify an accessible folder in the [getFontsFolder()](../../com.aspose.words/htmlsaveoptions/\#getFontsFolder) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setFontsFolder-java.lang.String) property or provide custom streams via the [getFontSavingCallback()](../../com.aspose.words/htmlsaveoptions/\#getFontSavingCallback) / [setFontSavingCallback(com.aspose.words.IFontSavingCallback)](../../com.aspose.words/htmlsaveoptions/\#setFontSavingCallback-com.aspose.words.IFontSavingCallback) event handler.

If the folder specified by [getFontsFolder()](../../com.aspose.words/htmlsaveoptions/\#getFontsFolder) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setFontsFolder-java.lang.String) doesn't exist, it will be created automatically.

[getResourceFolder()](../../com.aspose.words/htmlsaveoptions/\#getResourceFolder) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setResourceFolder-java.lang.String) is another way to specify a folder where fonts should be saved.

 **Examples:** 

Shows how to set folders and folder aliases for externally saved resources that Aspose.Words will create when saving a document to HTML.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setCssStyleSheetType(CssStyleSheetType.EXTERNAL);
     options.setExportFontResources(true);
     options.setImageResolution(72);
     options.setFontResourcesSubsettingSizeThreshold(0);
     options.setFontsFolder(getArtifactsDir() + "Fonts");
     options.setImagesFolder(getArtifactsDir() + "Images");
     options.setResourceFolder(getArtifactsDir() + "Resources");
     options.setFontsFolderAlias("http://example.com/fonts");
     options.setImagesFolderAlias("http://example.com/images");
     options.setResourceFolderAlias("http://example.com/resources");
     options.setExportOriginalUrlForLinkedImages(true);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.FolderAlias.html", options);
 
```

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getFontsFolderAlias() {#getFontsFolderAlias}
```
public String getFontsFolderAlias()
```


Specifies the name of the folder used to construct font URIs written into an HTML document. Default is an empty string.

 **Remarks:** 

When you save a [Document](../../com.aspose.words/document/) in HTML format and [getExportFontResources()](../../com.aspose.words/htmlsaveoptions/\#getExportFontResources) / [setExportFontResources(boolean)](../../com.aspose.words/htmlsaveoptions/\#setExportFontResources-boolean) is set to  true , Aspose.Words needs to save fonts used in the document as standalone files. [getFontsFolder()](../../com.aspose.words/htmlsaveoptions/\#getFontsFolder) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setFontsFolder-java.lang.String) allows you to specify where the fonts will be saved and [getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getFontsFolderAlias) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setFontsFolderAlias-java.lang.String) allows to specify how the font URIs will be constructed.

If [getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getFontsFolderAlias) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setFontsFolderAlias-java.lang.String) is not an empty string, then the font URI written to HTML will be *FontsFolderAlias +* . 

If [getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getFontsFolderAlias) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setFontsFolderAlias-java.lang.String) is an empty string, then the font URI written to HTML will be *FontsFolder +* . 

If [getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getFontsFolderAlias) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setFontsFolderAlias-java.lang.String) is set to '.' (dot), then the font file name will be written to HTML without path regardless of other options.

Alternative way to specify the name of the folder to construct font URIs is to use [getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getResourceFolderAlias) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setResourceFolderAlias-java.lang.String).

 **Examples:** 

Shows how to set folders and folder aliases for externally saved resources that Aspose.Words will create when saving a document to HTML.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setCssStyleSheetType(CssStyleSheetType.EXTERNAL);
     options.setExportFontResources(true);
     options.setImageResolution(72);
     options.setFontResourcesSubsettingSizeThreshold(0);
     options.setFontsFolder(getArtifactsDir() + "Fonts");
     options.setImagesFolder(getArtifactsDir() + "Images");
     options.setResourceFolder(getArtifactsDir() + "Resources");
     options.setFontsFolderAlias("http://example.com/fonts");
     options.setImagesFolderAlias("http://example.com/images");
     options.setResourceFolderAlias("http://example.com/resources");
     options.setExportOriginalUrlForLinkedImages(true);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.FolderAlias.html", options);
 
```

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getHtmlVersion() {#getHtmlVersion}
```
public int getHtmlVersion()
```


Specifies version of HTML standard that should be used when saving the document to HTML or MHTML. Default value is [HtmlVersion.XHTML](../../com.aspose.words/htmlversion/\#XHTML).

 **Examples:** 

Shows how to display a DOCTYPE heading when converting documents to the Xhtml 1.0 transitional standard.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");

 HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.HTML);
 {
     options.setHtmlVersion(HtmlVersion.XHTML);
     options.setExportXhtmlTransitional(showDoctypeDeclaration);
     options.setPrettyFormat(true);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.ExportXhtmlTransitional.html", options);

 // Our document will only contain a DOCTYPE declaration heading if we have set the "ExportXhtmlTransitional" flag to "true".
 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlSaveOptions.ExportXhtmlTransitional.html"), StandardCharsets.UTF_8);

 if (showDoctypeDeclaration)
     Assert.assertTrue(outDocContents.contains(
             "\r\n" +
                     "\r\n" +
                     ""));
 else
     Assert.assertTrue(outDocContents.contains(""));
 
```

Shows how to save a document to a specific version of HTML.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.HTML);
 {
     options.setHtmlVersion(htmlVersion);
     options.setPrettyFormat(true);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.HtmlVersions.html", options);

 // Our HTML documents will have minor differences to be compatible with different HTML versions.
 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlSaveOptions.HtmlVersions.html"), StandardCharsets.UTF_8);

 switch (htmlVersion) {
     case HtmlVersion.HTML_5:
         Assert.assertTrue(outDocContents.contains(""));
         Assert.assertTrue(outDocContents.contains(""));
         Assert.assertTrue(outDocContents.contains(" "));
         Assert.assertTrue(outDocContents.contains(" "));
         break;
     case HtmlVersion.XHTML:
         Assert.assertTrue(outDocContents.contains(""));
         Assert.assertTrue(outDocContents.contains(" "));
         break;
 }
 
```

**Returns:**
int - The corresponding  int  value. The returned value is one of [HtmlVersion](../../com.aspose.words/htmlversion/) constants.
### getImageResolution() {#getImageResolution}
```
public int getImageResolution()
```


Specifies the output resolution for images when exporting to HTML, MHTML or EPUB. Default is  96 dpi .

 **Remarks:** 

This property effects raster images when [getScaleImageToShapeSize()](../../com.aspose.words/htmlsaveoptions/\#getScaleImageToShapeSize) / [setScaleImageToShapeSize(boolean)](../../com.aspose.words/htmlsaveoptions/\#setScaleImageToShapeSize-boolean) is  true  and effects metafiles exported as raster images. Some image properties such as cropping or rotation require saving transformed images and in this case transformed images are created in the given resolution.

 **Examples:** 

Shows how to set folders and folder aliases for externally saved resources that Aspose.Words will create when saving a document to HTML.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setCssStyleSheetType(CssStyleSheetType.EXTERNAL);
     options.setExportFontResources(true);
     options.setImageResolution(72);
     options.setFontResourcesSubsettingSizeThreshold(0);
     options.setFontsFolder(getArtifactsDir() + "Fonts");
     options.setImagesFolder(getArtifactsDir() + "Images");
     options.setResourceFolder(getArtifactsDir() + "Resources");
     options.setFontsFolderAlias("http://example.com/fonts");
     options.setImagesFolderAlias("http://example.com/images");
     options.setResourceFolderAlias("http://example.com/resources");
     options.setExportOriginalUrlForLinkedImages(true);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.FolderAlias.html", options);
 
```

**Returns:**
int - The corresponding  int  value.
### getImageSavingCallback() {#getImageSavingCallback}
```
public IImageSavingCallback getImageSavingCallback()
```


Allows to control how images are saved when a document is saved to HTML, MHTML or EPUB.

 **Examples:** 

Shows how to split a document into parts and save them.

```

 public void documentPartsFileNames() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");
     String outFileName = "SavingCallback.DocumentPartsFileNames.html";

     // Create an "HtmlFixedSaveOptions" object, which we can pass to the document's "Save" method
     // to modify how we convert the document to HTML.
     HtmlSaveOptions options = new HtmlSaveOptions();

     // If we save the document normally, there will be one output HTML
     // document with all the source document's contents.
     // Set the "DocumentSplitCriteria" property to "DocumentSplitCriteria.SectionBreak" to
     // save our document to multiple HTML files: one for each section.
     options.setDocumentSplitCriteria(DocumentSplitCriteria.SECTION_BREAK);

     // Assign a custom callback to the "DocumentPartSavingCallback" property to alter the document part saving logic.
     options.setDocumentPartSavingCallback(new SavedDocumentPartRename(outFileName, options.getDocumentSplitCriteria()));

     // If we convert a document that contains images into html, we will end up with one html file which links to several images.
     // Each image will be in the form of a file in the local file system.
     // There is also a callback that can customize the name and file system location of each image.
     options.setImageSavingCallback(new SavedImageRename(outFileName));

     doc.save(getArtifactsDir() + outFileName, options);
 }

 /// 
 /// Sets custom filenames for output documents that the saving operation splits a document into.
 /// 
 private static class SavedDocumentPartRename implements IDocumentPartSavingCallback {
     public SavedDocumentPartRename(String outFileName, int documentSplitCriteria) {
         mOutFileName = outFileName;
         mDocumentSplitCriteria = documentSplitCriteria;
     }

     public void documentPartSaving(DocumentPartSavingArgs args) throws Exception {
         // We can access the entire source document via the "Document" property.
         Assert.assertTrue(args.getDocument().getOriginalFileName().endsWith("Rendering.docx"));

         String partType = "";

         switch (mDocumentSplitCriteria) {
             case DocumentSplitCriteria.PAGE_BREAK:
                 partType = "Page";
                 break;
             case DocumentSplitCriteria.COLUMN_BREAK:
                 partType = "Column";
                 break;
             case DocumentSplitCriteria.SECTION_BREAK:
                 partType = "Section";
                 break;
             case DocumentSplitCriteria.HEADING_PARAGRAPH:
                 partType = "Paragraph from heading";
                 break;
         }

         String partFileName = MessageFormat.format("{0} part {1}, of type {2}.{3}", mOutFileName, ++mCount, partType, FilenameUtils.getExtension(args.getDocumentPartFileName()));

         // Below are two ways of specifying where Aspose.Words will save each part of the document.
         // 1 -  Set a filename for the output part file:
         args.setDocumentPartFileName(partFileName);

         // 2 -  Create a custom stream for the output part file:
         try (FileOutputStream outputStream = new FileOutputStream(getArtifactsDir() + partFileName)) {
             args.setDocumentPartStream(outputStream);
         }

         Assert.assertNotNull(args.getDocumentPartStream());
         Assert.assertFalse(args.getKeepDocumentPartStreamOpen());
     }

     private int mCount;
     private final String mOutFileName;
     private final int mDocumentSplitCriteria;
 }

 /// 
 /// Sets custom filenames for image files that an HTML conversion creates.
 /// 
 public static class SavedImageRename implements IImageSavingCallback {
     public SavedImageRename(String outFileName) {
         mOutFileName = outFileName;
     }

     public void imageSaving(ImageSavingArgs args) throws Exception {
         String imageFileName = MessageFormat.format("{0} shape {1}, of type {2}.{3}", mOutFileName, ++mCount, args.getCurrentShape().getShapeType(), FilenameUtils.getExtension(args.getImageFileName()));

         // Below are two ways of specifying where Aspose.Words will save each part of the document.
         // 1 -  Set a filename for the output image file:
         args.setImageFileName(imageFileName);

         // 2 -  Create a custom stream for the output image file:
         args.setImageStream(new FileOutputStream(getArtifactsDir() + imageFileName));

         Assert.assertNotNull(args.getImageStream());
         Assert.assertTrue(args.isImageAvailable());
         Assert.assertFalse(args.getKeepImageStreamOpen());
     }

     private int mCount;
     private final String mOutFileName;
 }
 
```

**Returns:**
[IImageSavingCallback](../../com.aspose.words/iimagesavingcallback/) - The corresponding [IImageSavingCallback](../../com.aspose.words/iimagesavingcallback/) value.
### getImagesFolder() {#getImagesFolder}
```
public String getImagesFolder()
```


Specifies the physical folder where images are saved when exporting a document to HTML format. Default is an empty string.

 **Remarks:** 

When you save a [Document](../../com.aspose.words/document/) in HTML format, Aspose.Words needs to save all images embedded in the document as standalone files. [getImagesFolder()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolder) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolder-java.lang.String) allows you to specify where the images will be saved and [getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolderAlias) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolderAlias-java.lang.String) allows to specify how the image URIs will be constructed.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the images in the same folder where the document file is saved. Use [getImagesFolder()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolder) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolder-java.lang.String) to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the images, but still needs to save the images somewhere. In this case, you need to specify an accessible folder in the [getImagesFolder()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolder) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolder-java.lang.String) property or provide custom streams via the [getImageSavingCallback()](../../com.aspose.words/htmlsaveoptions/\#getImageSavingCallback) / [setImageSavingCallback(com.aspose.words.IImageSavingCallback)](../../com.aspose.words/htmlsaveoptions/\#setImageSavingCallback-com.aspose.words.IImageSavingCallback) event handler.

If the folder specified by [getImagesFolder()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolder) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolder-java.lang.String) doesn't exist, it will be created automatically.

[getResourceFolder()](../../com.aspose.words/htmlsaveoptions/\#getResourceFolder) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setResourceFolder-java.lang.String) is another way to specify a folder where images should be saved.

 **Examples:** 

Shows how to specify the folder for storing linked images after saving to .html.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 File imagesDir = new File(getArtifactsDir() + "SaveHtmlWithOptions");

 if (imagesDir.exists())
     imagesDir.delete();

 imagesDir.mkdir();

 // Set an option to export form fields as plain text instead of HTML input elements.
 HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.HTML);
 options.setExportTextInputFormFieldAsText(true);
 options.setImagesFolder(imagesDir.getPath());

 doc.save(getArtifactsDir() + "HtmlSaveOptions.SaveHtmlWithOptions.html", options);
 
```

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getImagesFolderAlias() {#getImagesFolderAlias}
```
public String getImagesFolderAlias()
```


Specifies the name of the folder used to construct image URIs written into an HTML document. Default is an empty string.

 **Remarks:** 

When you save a [Document](../../com.aspose.words/document/) in HTML format, Aspose.Words needs to save all images embedded in the document as standalone files. [getImagesFolder()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolder) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolder-java.lang.String) allows you to specify where the images will be saved and [getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolderAlias) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolderAlias-java.lang.String) allows to specify how the image URIs will be constructed.

If [getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolderAlias) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolderAlias-java.lang.String) is not an empty string, then the image URI written to HTML will be *ImagesFolderAlias + ![Image 1][]*.

If [getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolderAlias) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolderAlias-java.lang.String) is an empty string, then the image URI written to HTML will be *ImagesFolder + ![Image 1][]*.

If [getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolderAlias) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolderAlias-java.lang.String) is set to '.' (dot), then the image file name will be written to HTML without path regardless of other options.

Alternative way to specify the name of the folder to construct image URIs is to use [getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getResourceFolderAlias) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setResourceFolderAlias-java.lang.String).

 **Examples:** 

Shows how to set folders and folder aliases for externally saved resources that Aspose.Words will create when saving a document to HTML.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setCssStyleSheetType(CssStyleSheetType.EXTERNAL);
     options.setExportFontResources(true);
     options.setImageResolution(72);
     options.setFontResourcesSubsettingSizeThreshold(0);
     options.setFontsFolder(getArtifactsDir() + "Fonts");
     options.setImagesFolder(getArtifactsDir() + "Images");
     options.setResourceFolder(getArtifactsDir() + "Resources");
     options.setFontsFolderAlias("http://example.com/fonts");
     options.setImagesFolderAlias("http://example.com/images");
     options.setResourceFolderAlias("http://example.com/resources");
     options.setExportOriginalUrlForLinkedImages(true);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.FolderAlias.html", options);
 
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
### getMetafileFormat() {#getMetafileFormat}
```
public int getMetafileFormat()
```


Specifies in what format metafiles are saved when exporting to HTML, MHTML, or EPUB. Default value is [HtmlMetafileFormat.PNG](../../com.aspose.words/htmlmetafileformat/\#PNG), meaning that metafiles are rendered to raster PNG images.

 **Remarks:** 

Metafiles are not natively displayed by HTML browsers. By default, Aspose.Words converts WMF and EMF images into PNG files when exporting to HTML. Other options are to convert metafiles to SVG images or to export them as is without conversion.

Some image transforms, in particular image cropping, will not be applied to metafile images if they are exported to HTML without conversion.

 **Examples:** 

Shows how to convert SVG objects to a different format when saving HTML documents.

```

 String html =
     "\n                    \n                        Hello world!\n                    \n                ";

 // Use 'ConvertSvgToEmf' to turn back the legacy behavior
 // where all SVG images loaded from an HTML document were converted to EMF.
 // Now SVG images are loaded without conversion
 // if the MS Word version specified in load options supports SVG images natively.
 HtmlLoadOptions loadOptions = new HtmlLoadOptions(); { loadOptions.setConvertSvgToEmf(true); }

 Document doc = new Document(new ByteArrayInputStream(html.getBytes()));

 // This document contains a  element in the form of text.
 // When we save the document to HTML, we can pass a SaveOptions object
 // to determine how the saving operation handles this object.
 // Setting the "MetafileFormat" property to "HtmlMetafileFormat.Png" to convert it to a PNG image.
 // Setting the "MetafileFormat" property to "HtmlMetafileFormat.Svg" preserve it as a SVG object.
 // Setting the "MetafileFormat" property to "HtmlMetafileFormat.EmfOrWmf" to convert it to a metafile.
 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setMetafileFormat(htmlMetafileFormat);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.MetafileFormat.html", options);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlSaveOptions.MetafileFormat.html"), StandardCharsets.UTF_8);

 switch (htmlMetafileFormat) {
     case HtmlMetafileFormat.PNG:
         Assert.assertTrue(outDocContents.contains(
                 " " +
                         "" +
                         ""));
         break;
     case HtmlMetafileFormat.SVG:
         Assert.assertTrue(outDocContents.contains(
                 "" +
                         ""));
         break;
     case HtmlMetafileFormat.EMF_OR_WMF:
         Assert.assertTrue(outDocContents.contains(
                 " " +
                         "" +
                         ""));
         break;
 }
 
```

**Returns:**
int - The corresponding  int  value. The returned value is one of [HtmlMetafileFormat](../../com.aspose.words/htmlmetafileformat/) constants.
### getNavigationMapLevel() {#getNavigationMapLevel}
```
public int getNavigationMapLevel()
```


Specifies the maximum level of headings populated to the navigation map when exporting to EPUB, MOBI, or AZW3 formats. Default value is  3 .

 **Remarks:** 

The navigation map allows user agents to provide an easy way of navigation through the document structure. Usually navigation points correspond to headings in the document. In order to populate headings up to level **N** assign this value to [getNavigationMapLevel()](../../com.aspose.words/htmlsaveoptions/\#getNavigationMapLevel) / [setNavigationMapLevel(int)](../../com.aspose.words/htmlsaveoptions/\#setNavigationMapLevel-int).

By default, three levels of headings are populated: paragraphs of styles **Heading 1**, **Heading 2** and **Heading 3**. You can set this property to a value from 1 to 9 in order to request the corresponding maximum level. Setting it to zero will reduce the navigation map to only the document root or roots of document parts.

 **Examples:** 

Shows how to generate table of contents for Mobi documents.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.MOBI);
 options.setNavigationMapLevel(5);

 doc.save(getArtifactsDir() + "HtmlSaveOptions.CreateMobiToc.mobi", options);
 
```

Shows how to generate table of contents for Azw3 documents.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.AZW_3);
 options.setNavigationMapLevel(2);

 doc.save(getArtifactsDir() + "HtmlSaveOptions.CreateAZW3Toc.azw3", options);
 
```

Shows how to filter headings that appear in the navigation panel of a saved Epub document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Every paragraph that we format using a "Heading" style can serve as a heading.
 // Each heading may also have a heading level, determined by the number of its heading style.
 // The headings below are of levels 1-3.
 builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get("Heading 1"));
 builder.writeln("Heading #1");
 builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get("Heading 2"));
 builder.writeln("Heading #2");
 builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get("Heading 3"));
 builder.writeln("Heading #3");
 builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get("Heading 1"));
 builder.writeln("Heading #4");
 builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get("Heading 2"));
 builder.writeln("Heading #5");
 builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get("Heading 3"));
 builder.writeln("Heading #6");

 // Epub readers typically create a table of contents for their documents.
 // Each paragraph with a "Heading" style in the document will create an entry in this table of contents.
 // We can use the "NavigationMapLevel" property to set a maximum heading level.
 // The Epub reader will not add headings with a level above the one we specify to the contents table.
 HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.EPUB);
 options.setNavigationMapLevel(2);

 // Our document has six headings, two of which are above level 2.
 // The table of contents for this document will have four entries.
 doc.save(getArtifactsDir() + "HtmlSaveOptions.EpubHeadings.epub", options);
 
```

**Returns:**
int - The corresponding  int  value.
### getOfficeMathOutputMode() {#getOfficeMathOutputMode}
```
public int getOfficeMathOutputMode()
```


Controls how OfficeMath objects are exported to HTML, MHTML or EPUB. Default value is [HtmlOfficeMathOutputMode.IMAGE](../../com.aspose.words/htmlofficemathoutputmode/\#IMAGE).

 **Examples:** 

Shows how to specify how to export Microsoft OfficeMath objects to HTML.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 // When we save the document to HTML, we can pass a SaveOptions object
 // to determine how the saving operation handles OfficeMath objects.
 // Setting the "OfficeMathOutputMode" property to "HtmlOfficeMathOutputMode.Image"
 // will render each OfficeMath object into an image.
 // Setting the "OfficeMathOutputMode" property to "HtmlOfficeMathOutputMode.MathML"
 // will convert each OfficeMath object into MathML.
 // Setting the "OfficeMathOutputMode" property to "HtmlOfficeMathOutputMode.Text"
 // will represent each OfficeMath formula using plain HTML text.
 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setOfficeMathOutputMode(htmlOfficeMathOutputMode);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.OfficeMathOutputMode.html", options);
 
```

**Returns:**
int - The corresponding  int  value. The returned value is one of [HtmlOfficeMathOutputMode](../../com.aspose.words/htmlofficemathoutputmode/) constants.
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
### getRemoveJavaScriptFromLinks() {#getRemoveJavaScriptFromLinks}
```
public boolean getRemoveJavaScriptFromLinks()
```


Specifies whether JavaScript will be removed from links. Default is  false .

 **Remarks:** 

If this option is enabled, all links containing JavaScript (e.g., links with "javascript:" in the href attribute) will be replaced with "javascript:void(0)". This can help prevent potential security risks, such as XSS attacks.

**Returns:**
boolean - The corresponding  boolean  value.
### getReplaceBackslashWithYenSign() {#getReplaceBackslashWithYenSign}
```
public boolean getReplaceBackslashWithYenSign()
```


Specifies whether backslash characters should be replaced with yen signs. Default value is  false .

 **Remarks:** 

By default, Aspose.Words mimics MS Word's behavior and doesn't replace backslash characters with yen signs in generated HTML documents. However, previous versions of Aspose.Words performed such replacements in certain scenarios. This flag enables backward compatibility with previous versions of Aspose.Words.

 **Examples:** 

Shows how to replace backslash characters with yen signs (Html).

```

 Document doc = new Document(getMyDir() + "Korean backslash symbol.docx");

 // By default, Aspose.Words mimics MS Word's behavior and doesn't replace backslash characters with yen signs in
 // generated HTML documents. However, previous versions of Aspose.Words performed such replacements in certain
 // scenarios. This flag enables backward compatibility with previous versions of Aspose.Words.
 HtmlSaveOptions saveOptions = new HtmlSaveOptions();
 saveOptions.setReplaceBackslashWithYenSign(true);

 doc.save(getArtifactsDir() + "HtmlSaveOptions.ReplaceBackslashWithYenSign.html", saveOptions);
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getResolveFontNames() {#getResolveFontNames}
```
public boolean getResolveFontNames()
```


Specifies whether font family names used in the document are resolved and substituted according to [Document.getFontSettings()](../../com.aspose.words/document/\#getFontSettings) / [Document.setFontSettings(com.aspose.words.FontSettings)](../../com.aspose.words/document/\#setFontSettings-com.aspose.words.FontSettings) when being written into HTML-based formats.

 **Remarks:** 

By default, this option is set to  false  and font family names are written to HTML as specified in source documents. That is, [Document.getFontSettings()](../../com.aspose.words/document/\#getFontSettings) / [Document.setFontSettings(com.aspose.words.FontSettings)](../../com.aspose.words/document/\#setFontSettings-com.aspose.words.FontSettings) are ignored and no resolution or substitution of font family names is performed.

If this option is set to  true , Aspose.Words uses [Document.getFontSettings()](../../com.aspose.words/document/\#getFontSettings) / [Document.setFontSettings(com.aspose.words.FontSettings)](../../com.aspose.words/document/\#setFontSettings-com.aspose.words.FontSettings) to resolve each font family name specified in a source document into the name of an available font family, performing font substitution as required.

 **Examples:** 

Shows how to resolve all font names before writing them to HTML.

```

 Document doc = new Document(getMyDir() + "Missing font.docx");

 // This document contains text that names a font that we do not have.
 Assert.assertNotNull(doc.getFontInfos().get("28 Days Later"));

 // If we have no way of getting this font, and we want to be able to display all the text
 // in this document in an output HTML, we can substitute it with another font.
 FontSettings fontSettings = new FontSettings();
 {
     fontSettings.getSubstitutionSettings().getDefaultFontSubstitution().setDefaultFontName("Arial");
     fontSettings.getSubstitutionSettings().getDefaultFontSubstitution().setEnabled(true);
 }

 doc.setFontSettings(fontSettings);

 HtmlSaveOptions saveOptions = new HtmlSaveOptions(SaveFormat.HTML);
 {
     // By default, this option is set to 'False' and Aspose.Words writes font names as specified in the source document.
     saveOptions.setResolveFontNames(resolveFontNames);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.ResolveFontNames.html", saveOptions);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlSaveOptions.ResolveFontNames.html"), "utf-8");

 Assert.assertTrue(outDocContents.matches(""));
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getResourceFolder() {#getResourceFolder}
```
public String getResourceFolder()
```


Specifies a physical folder where all resources like images, fonts, and external CSS are saved when a document is exported to HTML. Default is an empty string.

 **Remarks:** 

[getResourceFolder()](../../com.aspose.words/htmlsaveoptions/\#getResourceFolder) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setResourceFolder-java.lang.String) is the simplest way to specify a folder where all resources should be written. Another way is to use individual properties [getFontsFolder()](../../com.aspose.words/htmlsaveoptions/\#getFontsFolder) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setFontsFolder-java.lang.String), [getImagesFolder()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolder) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolder-java.lang.String), and [getCssStyleSheetFileName()](../../com.aspose.words/htmlsaveoptions/\#getCssStyleSheetFileName) / [setCssStyleSheetFileName(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setCssStyleSheetFileName-java.lang.String).

[getResourceFolder()](../../com.aspose.words/htmlsaveoptions/\#getResourceFolder) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setResourceFolder-java.lang.String) has a lower priority than folders specified via [getFontsFolder()](../../com.aspose.words/htmlsaveoptions/\#getFontsFolder) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setFontsFolder-java.lang.String), [getImagesFolder()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolder) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolder-java.lang.String), and [getCssStyleSheetFileName()](../../com.aspose.words/htmlsaveoptions/\#getCssStyleSheetFileName) / [setCssStyleSheetFileName(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setCssStyleSheetFileName-java.lang.String). For example, if both [getResourceFolder()](../../com.aspose.words/htmlsaveoptions/\#getResourceFolder) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setResourceFolder-java.lang.String) and [getFontsFolder()](../../com.aspose.words/htmlsaveoptions/\#getFontsFolder) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setFontsFolder-java.lang.String) are specified, fonts will be saved to [getFontsFolder()](../../com.aspose.words/htmlsaveoptions/\#getFontsFolder) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setFontsFolder-java.lang.String), while images and CSS will be saved to [getResourceFolder()](../../com.aspose.words/htmlsaveoptions/\#getResourceFolder) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setResourceFolder-java.lang.String).

If the folder specified by [getResourceFolder()](../../com.aspose.words/htmlsaveoptions/\#getResourceFolder) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setResourceFolder-java.lang.String) doesn't exist, it will be created automatically.

 **Examples:** 

Shows how to set folders and folder aliases for externally saved resources that Aspose.Words will create when saving a document to HTML.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setCssStyleSheetType(CssStyleSheetType.EXTERNAL);
     options.setExportFontResources(true);
     options.setImageResolution(72);
     options.setFontResourcesSubsettingSizeThreshold(0);
     options.setFontsFolder(getArtifactsDir() + "Fonts");
     options.setImagesFolder(getArtifactsDir() + "Images");
     options.setResourceFolder(getArtifactsDir() + "Resources");
     options.setFontsFolderAlias("http://example.com/fonts");
     options.setImagesFolderAlias("http://example.com/images");
     options.setResourceFolderAlias("http://example.com/resources");
     options.setExportOriginalUrlForLinkedImages(true);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.FolderAlias.html", options);
 
```

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getResourceFolderAlias() {#getResourceFolderAlias}
```
public String getResourceFolderAlias()
```


Specifies the name of the folder used to construct URIs of all resources written into an HTML document. Default is an empty string.

 **Remarks:** 

[getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getResourceFolderAlias) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setResourceFolderAlias-java.lang.String) is the simplest way to specify how URIs for all resource files should be constructed. Same information can be specified for images and fonts separately via [getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolderAlias) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolderAlias-java.lang.String) and [getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getFontsFolderAlias) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setFontsFolderAlias-java.lang.String) properties, respectively. However, there is no individual property for CSS.

[getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getResourceFolderAlias) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setResourceFolderAlias-java.lang.String) has lower priority than [getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getFontsFolderAlias) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setFontsFolderAlias-java.lang.String) and [getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolderAlias) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolderAlias-java.lang.String). For example, if both [getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getResourceFolderAlias) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setResourceFolderAlias-java.lang.String) and [getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getFontsFolderAlias) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setFontsFolderAlias-java.lang.String) are specified, fonts' URIs will be constructed using [getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getFontsFolderAlias) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setFontsFolderAlias-java.lang.String), while URIs of images and CSS will be constructed using [getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getResourceFolderAlias) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setResourceFolderAlias-java.lang.String).

If [getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getResourceFolderAlias) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setResourceFolderAlias-java.lang.String) is empty, the [getResourceFolder()](../../com.aspose.words/htmlsaveoptions/\#getResourceFolder) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setResourceFolder-java.lang.String) property value will be used to construct resource URIs.

If [getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getResourceFolderAlias) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setResourceFolderAlias-java.lang.String) is set to '.' (dot), resource URIs will contain file names only, without any path.

 **Examples:** 

Shows how to set folders and folder aliases for externally saved resources that Aspose.Words will create when saving a document to HTML.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setCssStyleSheetType(CssStyleSheetType.EXTERNAL);
     options.setExportFontResources(true);
     options.setImageResolution(72);
     options.setFontResourcesSubsettingSizeThreshold(0);
     options.setFontsFolder(getArtifactsDir() + "Fonts");
     options.setImagesFolder(getArtifactsDir() + "Images");
     options.setResourceFolder(getArtifactsDir() + "Resources");
     options.setFontsFolderAlias("http://example.com/fonts");
     options.setImagesFolderAlias("http://example.com/images");
     options.setResourceFolderAlias("http://example.com/resources");
     options.setExportOriginalUrlForLinkedImages(true);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.FolderAlias.html", options);
 
```

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getSaveFormat() {#getSaveFormat}
```
public int getSaveFormat()
```


Specifies the format in which the document will be saved if this save options object is used. Can be [SaveFormat.HTML](../../com.aspose.words/saveformat/\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat/\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat/\#EPUB), [SaveFormat.AZW\_3](../../com.aspose.words/saveformat/\#AZW-3) or [SaveFormat.MOBI](../../com.aspose.words/saveformat/\#MOBI).

 **Examples:** 

Shows how to use a specific encoding when saving a document to .epub.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 // Use a SaveOptions object to specify the encoding for a document that we will save.
 HtmlSaveOptions saveOptions = new HtmlSaveOptions();
 saveOptions.setSaveFormat(SaveFormat.EPUB);
 saveOptions.setEncoding(StandardCharsets.UTF_8);

 // By default, an output .epub document will have all of its contents in one HTML part.
 // A split criterion allows us to segment the document into several HTML parts.
 // We will set the criteria to split the document into heading paragraphs.
 // This is useful for readers who cannot read HTML files more significant than a specific size.
 saveOptions.setDocumentSplitCriteria(DocumentSplitCriteria.HEADING_PARAGRAPH);

 // Specify that we want to export document properties.
 saveOptions.setExportDocumentProperties(true);

 doc.save(getArtifactsDir() + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
 
```

**Returns:**
int - The corresponding  int  value. The returned value is one of [SaveFormat](../../com.aspose.words/saveformat/) constants.
### getScaleImageToShapeSize() {#getScaleImageToShapeSize}
```
public boolean getScaleImageToShapeSize()
```


Specifies whether images are scaled by Aspose.Words to the bounding shape size when exporting to HTML, MHTML or EPUB. Default value is  true .

 **Remarks:** 

An image in a Microsoft Word document is a shape. The shape has a size and the image has its own size. The sizes are not directly linked. For example, the image can be 1024x786 pixels, but shape that displays this image can be 400x300 points.

In order to display an image in the browser, it must be scaled to the shape size. The [getScaleImageToShapeSize()](../../com.aspose.words/htmlsaveoptions/\#getScaleImageToShapeSize) / [setScaleImageToShapeSize(boolean)](../../com.aspose.words/htmlsaveoptions/\#setScaleImageToShapeSize-boolean) property controls where the scaling of the image takes place: in Aspose.Words during export to HTML or in the browser when displaying the document.

When [getScaleImageToShapeSize()](../../com.aspose.words/htmlsaveoptions/\#getScaleImageToShapeSize) / [setScaleImageToShapeSize(boolean)](../../com.aspose.words/htmlsaveoptions/\#setScaleImageToShapeSize-boolean) is  true , the image is scaled by Aspose.Words using high quality scaling during export to HTML. When [getScaleImageToShapeSize()](../../com.aspose.words/htmlsaveoptions/\#getScaleImageToShapeSize) / [setScaleImageToShapeSize(boolean)](../../com.aspose.words/htmlsaveoptions/\#setScaleImageToShapeSize-boolean) is  false , the image is output with its original size and the browser has to scale it.

In general, browsers do quick and poor quality scaling. As a result, you will normally get better display quality in the browser and smaller file size when [getScaleImageToShapeSize()](../../com.aspose.words/htmlsaveoptions/\#getScaleImageToShapeSize) / [setScaleImageToShapeSize(boolean)](../../com.aspose.words/htmlsaveoptions/\#setScaleImageToShapeSize-boolean) is  true , but better printing quality and faster conversion when [getScaleImageToShapeSize()](../../com.aspose.words/htmlsaveoptions/\#getScaleImageToShapeSize) / [setScaleImageToShapeSize(boolean)](../../com.aspose.words/htmlsaveoptions/\#setScaleImageToShapeSize-boolean) is  false .

In addition to shapes containing individual raster images, this option also affects group shapes consisting of raster images. If [getScaleImageToShapeSize()](../../com.aspose.words/htmlsaveoptions/\#getScaleImageToShapeSize) / [setScaleImageToShapeSize(boolean)](../../com.aspose.words/htmlsaveoptions/\#setScaleImageToShapeSize-boolean) is  false  and a group shape contains raster images whose intrinsic resolution is higher than the value specified in [getImageResolution()](../../com.aspose.words/htmlsaveoptions/\#getImageResolution) / [setImageResolution(int)](../../com.aspose.words/htmlsaveoptions/\#setImageResolution-int), Aspose.Words will increase rendering resolution for that group. This allows to better preserve quality of grouped high resolution images when saving to HTML.

 **Examples:** 

Shows how to disable the scaling of images to their parent shape dimensions when saving to .html.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a shape which contains an image, and then make that shape considerably smaller than the image.
 Shape imageShape = builder.insertImage(getImageDir() + "Transparent background logo.png");
 imageShape.setWidth(50.0);
 imageShape.setHeight(50.0);

 // Saving a document that contains shapes with images to HTML will create an image file in the local file system
 // for each such shape. The output HTML document will use  tags to link to and display these images.
 // When we save the document to HTML, we can pass a SaveOptions object to determine
 // whether to scale all images that are inside shapes to the sizes of their shapes.
 // Setting the "ScaleImageToShapeSize" flag to "true" will shrink every image
 // to the size of the shape that contains it, so that no saved images will be larger than the document requires them to be.
 // Setting the "ScaleImageToShapeSize" flag to "false" will preserve these images' original sizes,
 // which will take up more space in exchange for preserving image quality.
 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setScaleImageToShapeSize(scaleImageToShapeSize);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.ScaleImageToShapeSize.html", options);
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getTableWidthOutputMode() {#getTableWidthOutputMode}
```
public int getTableWidthOutputMode()
```


Controls how table, row and cell widths are exported to HTML, MHTML or EPUB. Default value is [HtmlElementSizeOutputMode.ALL](../../com.aspose.words/htmlelementsizeoutputmode/\#ALL).

 **Remarks:** 

In the HTML format, table, row and cell elements ( 

    | -- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
    | ,  | ) can have their widths specified either in relative (percentage) or in absolute units. In a document in Aspose.Words, tables, rows and cells can have their widths specified using either relative or absolute units too.  When you convert a document to HTML using Aspose.Words, you might want to control how table, row and cell widths are exported to affect how the resulting document is displayed in the visual agent (e.g. a browser or viewer).  Use this property as a filter to specify what table widths values are exported into the destination document. For example, if you are converting a document to EPUB and intend to view the document on a mobile reading device, then you probably want to avoid exporting absolute width values. To do this you need to specify the output mode [HtmlElementSizeOutputMode.RELATIVE\_ONLY](../../com.aspose.words/htmlelementsizeoutputmode/\#RELATIVE-ONLY) or [HtmlElementSizeOutputMode.NONE](../../com.aspose.words/htmlelementsizeoutputmode/\#NONE) so the viewer on the mobile device can layout the table to fit the width of the screen as best as it can.   **Examples:**   Shows how to preserve negative indents in the output .html.   Document doc = new Document(); DocumentBuilder builder = new DocumentBuilder(doc); // Insert a table with a negative indent, which will push it to the left past the left page boundary. Table table = builder.startTable(); builder.insertCell(); builder.write("Row 1, Cell 1"); builder.insertCell(); builder.write("Row 1, Cell 2"); builder.endTable(); table.setLeftIndent(-36); table.setPreferredWidth(PreferredWidth.fromPoints(144.0)); builder.insertBreak(BreakType.PARAGRAPH\_BREAK); // Insert a table with a positive indent, which will push the table to the right. table = builder.startTable(); builder.insertCell(); builder.write("Row 1, Cell 1"); builder.insertCell(); builder.write("Row 1, Cell 2"); builder.endTable(); table.setLeftIndent(36.0); table.setPreferredWidth(PreferredWidth.fromPoints(144.0)); // When we save a document to HTML, Aspose.Words will only preserve negative indents // such as the one we have applied to the first table if we set the "AllowNegativeIndent" flag // in a SaveOptions object that we will pass to "true". HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.HTML); \{ options.setAllowNegativeIndent(allowNegativeIndent); options.setTableWidthOutputMode(HtmlElementSizeOutputMode.RELATIVE\_ONLY); \} doc.save(getArtifactsDir() + "HtmlSaveOptions.NegativeIndent.html", options); String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlSaveOptions.NegativeIndent.html"), StandardCharsets.UTF\_8); if (allowNegativeIndent) \{ Assert.assertTrue(outDocContents.contains( "  ")); Assert.assertTrue(outDocContents.contains( "  ")); \} else \{ Assert.assertTrue(outDocContents.contains( "  ")); Assert.assertTrue(outDocContents.contains( "  ")); \}  |

**Returns:**
int - The corresponding  int  value. The returned value is one of [HtmlElementSizeOutputMode](../../com.aspose.words/htmlelementsizeoutputmode/) constants.
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

### setAllowNegativeIndent(boolean value) {#setAllowNegativeIndent-boolean}
```
public void setAllowNegativeIndent(boolean value)
```


Specifies whether negative left and right indents of paragraphs are normalized when saving to HTML, MHTML or EPUB. Default value is  false .

 **Remarks:** 

When negative indent is not allowed, it is exported as zero margin to HTML. When negative indent is allowed, a paragraph might appear partially outside of the browser window.

 **Examples:** 

Shows how to preserve negative indents in the output .html.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a table with a negative indent, which will push it to the left past the left page boundary.
 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, Cell 1");
 builder.insertCell();
 builder.write("Row 1, Cell 2");
 builder.endTable();
 table.setLeftIndent(-36);
 table.setPreferredWidth(PreferredWidth.fromPoints(144.0));

 builder.insertBreak(BreakType.PARAGRAPH_BREAK);

 // Insert a table with a positive indent, which will push the table to the right.
 table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, Cell 1");
 builder.insertCell();
 builder.write("Row 1, Cell 2");
 builder.endTable();
 table.setLeftIndent(36.0);
 table.setPreferredWidth(PreferredWidth.fromPoints(144.0));

 // When we save a document to HTML, Aspose.Words will only preserve negative indents
 // such as the one we have applied to the first table if we set the "AllowNegativeIndent" flag
 // in a SaveOptions object that we will pass to "true".
 HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.HTML);
 {
     options.setAllowNegativeIndent(allowNegativeIndent);
     options.setTableWidthOutputMode(HtmlElementSizeOutputMode.RELATIVE_ONLY);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.NegativeIndent.html", options);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlSaveOptions.NegativeIndent.html"), StandardCharsets.UTF_8);

 if (allowNegativeIndent) {
     Assert.assertTrue(outDocContents.contains(
             " "));
     Assert.assertTrue(outDocContents.contains(
             " "));
 } else {
     Assert.assertTrue(outDocContents.contains(
             " "));
     Assert.assertTrue(outDocContents.contains(
             " "));
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setCssClassNamePrefix(String value) {#setCssClassNamePrefix-java.lang.String}
```
public void setCssClassNamePrefix(String value)
```


Specifies a prefix which is added to all CSS class names. Default value is an empty string and generated CSS class names have no common prefix.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setCssSavingCallback(ICssSavingCallback value) {#setCssSavingCallback-com.aspose.words.ICssSavingCallback}
```
public void setCssSavingCallback(ICssSavingCallback value)
```


Allows to control how CSS styles are saved when a document is saved to HTML, MHTML or EPUB.

 **Examples:** 

Shows how to work with CSS stylesheets that an HTML conversion creates.

```

 public void externalCssFilenames() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     // Create an "HtmlFixedSaveOptions" object, which we can pass to the document's "Save" method
     // to modify how we convert the document to HTML.
     HtmlSaveOptions options = new HtmlSaveOptions();

     // Set the "CssStylesheetType" property to "CssStyleSheetType.External" to
     // accompany a saved HTML document with an external CSS stylesheet file.
     options.setCssStyleSheetType(CssStyleSheetType.EXTERNAL);

     // Below are two ways of specifying directories and filenames for output CSS stylesheets.
     // 1 -  Use the "CssStyleSheetFileName" property to assign a filename to our stylesheet:
     options.setCssStyleSheetFileName(getArtifactsDir() + "SavingCallback.ExternalCssFilenames.css");

     // 2 -  Use a custom callback to name our stylesheet:
     options.setCssSavingCallback(new CustomCssSavingCallback(getArtifactsDir() + "SavingCallback.ExternalCssFilenames.css", true, false));

     doc.save(getArtifactsDir() + "SavingCallback.ExternalCssFilenames.html", options);
 }

 /// 
 /// Sets a custom filename, along with other parameters for an external CSS stylesheet.
 /// 
 private static class CustomCssSavingCallback implements ICssSavingCallback {
     public CustomCssSavingCallback(String cssDocFilename, boolean isExportNeeded, boolean keepCssStreamOpen) {
         mCssTextFileName = cssDocFilename;
         mIsExportNeeded = isExportNeeded;
         mKeepCssStreamOpen = keepCssStreamOpen;
     }

     public void cssSaving(CssSavingArgs args) throws Exception {
         // We can access the entire source document via the "Document" property.
         Assert.assertTrue(args.getDocument().getOriginalFileName().endsWith("Rendering.docx"));

         args.setCssStream(new FileOutputStream(mCssTextFileName));
         args.isExportNeeded(mIsExportNeeded);
         args.setKeepCssStreamOpen(mKeepCssStreamOpen);
     }

     private final String mCssTextFileName;
     private final boolean mIsExportNeeded;
     private final boolean mKeepCssStreamOpen;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [ICssSavingCallback](../../com.aspose.words/icsssavingcallback/) | The corresponding [ICssSavingCallback](../../com.aspose.words/icsssavingcallback/) value. |

### setCssStyleSheetFileName(String value) {#setCssStyleSheetFileName-java.lang.String}
```
public void setCssStyleSheetFileName(String value)
```


Specifies the path and the name of the Cascading Style Sheet (CSS) file written when a document is exported to HTML. Default is an empty string.

 **Remarks:** 

This property has effect only when saving a document to HTML format and external CSS style sheet is requested using [getCssStyleSheetType()](../../com.aspose.words/htmlsaveoptions/\#getCssStyleSheetType) / [setCssStyleSheetType(int)](../../com.aspose.words/htmlsaveoptions/\#setCssStyleSheetType-int).

If this property is empty, the CSS file will be saved into the same folder and with the same name as the HTML document but with the ".css" extension.

If only path but no file name is specified in this property, the CSS file will be saved into the specified folder and will have the same name as the HTML document but with the ".css" extension.

If the folder specified by this property doesn't exist, it will be created automatically before the CSS file is saved.

Another way to specify a folder where external CSS file is saved is to use [getResourceFolder()](../../com.aspose.words/htmlsaveoptions/\#getResourceFolder) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setResourceFolder-java.lang.String).

 **Examples:** 

Shows how to work with CSS stylesheets that an HTML conversion creates.

```

 public void externalCssFilenames() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     // Create an "HtmlFixedSaveOptions" object, which we can pass to the document's "Save" method
     // to modify how we convert the document to HTML.
     HtmlSaveOptions options = new HtmlSaveOptions();

     // Set the "CssStylesheetType" property to "CssStyleSheetType.External" to
     // accompany a saved HTML document with an external CSS stylesheet file.
     options.setCssStyleSheetType(CssStyleSheetType.EXTERNAL);

     // Below are two ways of specifying directories and filenames for output CSS stylesheets.
     // 1 -  Use the "CssStyleSheetFileName" property to assign a filename to our stylesheet:
     options.setCssStyleSheetFileName(getArtifactsDir() + "SavingCallback.ExternalCssFilenames.css");

     // 2 -  Use a custom callback to name our stylesheet:
     options.setCssSavingCallback(new CustomCssSavingCallback(getArtifactsDir() + "SavingCallback.ExternalCssFilenames.css", true, false));

     doc.save(getArtifactsDir() + "SavingCallback.ExternalCssFilenames.html", options);
 }

 /// 
 /// Sets a custom filename, along with other parameters for an external CSS stylesheet.
 /// 
 private static class CustomCssSavingCallback implements ICssSavingCallback {
     public CustomCssSavingCallback(String cssDocFilename, boolean isExportNeeded, boolean keepCssStreamOpen) {
         mCssTextFileName = cssDocFilename;
         mIsExportNeeded = isExportNeeded;
         mKeepCssStreamOpen = keepCssStreamOpen;
     }

     public void cssSaving(CssSavingArgs args) throws Exception {
         // We can access the entire source document via the "Document" property.
         Assert.assertTrue(args.getDocument().getOriginalFileName().endsWith("Rendering.docx"));

         args.setCssStream(new FileOutputStream(mCssTextFileName));
         args.isExportNeeded(mIsExportNeeded);
         args.setKeepCssStreamOpen(mKeepCssStreamOpen);
     }

     private final String mCssTextFileName;
     private final boolean mIsExportNeeded;
     private final boolean mKeepCssStreamOpen;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setCssStyleSheetType(int value) {#setCssStyleSheetType-int}
```
public void setCssStyleSheetType(int value)
```


Specifies how CSS (Cascading Style Sheet) styles are exported to HTML, MHTML or EPUB. Default value is [CssStyleSheetType.INLINE](../../com.aspose.words/cssstylesheettype/\#INLINE) for HTML/MHTML and [CssStyleSheetType.EXTERNAL](../../com.aspose.words/cssstylesheettype/\#EXTERNAL) for EPUB.

 **Remarks:** 

Saving CSS style sheet into an external file is only supported when saving to HTML. When you are exporting to one of the container formats (EPUB or MHTML) and specifying [CssStyleSheetType.EXTERNAL](../../com.aspose.words/cssstylesheettype/\#EXTERNAL), CSS file will be encapsulated into the output package.

 **Examples:** 

Shows how to work with CSS stylesheets that an HTML conversion creates.

```

 public void externalCssFilenames() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     // Create an "HtmlFixedSaveOptions" object, which we can pass to the document's "Save" method
     // to modify how we convert the document to HTML.
     HtmlSaveOptions options = new HtmlSaveOptions();

     // Set the "CssStylesheetType" property to "CssStyleSheetType.External" to
     // accompany a saved HTML document with an external CSS stylesheet file.
     options.setCssStyleSheetType(CssStyleSheetType.EXTERNAL);

     // Below are two ways of specifying directories and filenames for output CSS stylesheets.
     // 1 -  Use the "CssStyleSheetFileName" property to assign a filename to our stylesheet:
     options.setCssStyleSheetFileName(getArtifactsDir() + "SavingCallback.ExternalCssFilenames.css");

     // 2 -  Use a custom callback to name our stylesheet:
     options.setCssSavingCallback(new CustomCssSavingCallback(getArtifactsDir() + "SavingCallback.ExternalCssFilenames.css", true, false));

     doc.save(getArtifactsDir() + "SavingCallback.ExternalCssFilenames.html", options);
 }

 /// 
 /// Sets a custom filename, along with other parameters for an external CSS stylesheet.
 /// 
 private static class CustomCssSavingCallback implements ICssSavingCallback {
     public CustomCssSavingCallback(String cssDocFilename, boolean isExportNeeded, boolean keepCssStreamOpen) {
         mCssTextFileName = cssDocFilename;
         mIsExportNeeded = isExportNeeded;
         mKeepCssStreamOpen = keepCssStreamOpen;
     }

     public void cssSaving(CssSavingArgs args) throws Exception {
         // We can access the entire source document via the "Document" property.
         Assert.assertTrue(args.getDocument().getOriginalFileName().endsWith("Rendering.docx"));

         args.setCssStream(new FileOutputStream(mCssTextFileName));
         args.isExportNeeded(mIsExportNeeded);
         args.setKeepCssStreamOpen(mKeepCssStreamOpen);
     }

     private final String mCssTextFileName;
     private final boolean mIsExportNeeded;
     private final boolean mKeepCssStreamOpen;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [CssStyleSheetType](../../com.aspose.words/cssstylesheettype/) constants. |

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

### setDocumentPartSavingCallback(IDocumentPartSavingCallback value) {#setDocumentPartSavingCallback-com.aspose.words.IDocumentPartSavingCallback}
```
public void setDocumentPartSavingCallback(IDocumentPartSavingCallback value)
```


Allows to control how document parts are saved when a document is saved to HTML or EPUB.

 **Examples:** 

Shows how to split a document into parts and save them.

```

 public void documentPartsFileNames() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");
     String outFileName = "SavingCallback.DocumentPartsFileNames.html";

     // Create an "HtmlFixedSaveOptions" object, which we can pass to the document's "Save" method
     // to modify how we convert the document to HTML.
     HtmlSaveOptions options = new HtmlSaveOptions();

     // If we save the document normally, there will be one output HTML
     // document with all the source document's contents.
     // Set the "DocumentSplitCriteria" property to "DocumentSplitCriteria.SectionBreak" to
     // save our document to multiple HTML files: one for each section.
     options.setDocumentSplitCriteria(DocumentSplitCriteria.SECTION_BREAK);

     // Assign a custom callback to the "DocumentPartSavingCallback" property to alter the document part saving logic.
     options.setDocumentPartSavingCallback(new SavedDocumentPartRename(outFileName, options.getDocumentSplitCriteria()));

     // If we convert a document that contains images into html, we will end up with one html file which links to several images.
     // Each image will be in the form of a file in the local file system.
     // There is also a callback that can customize the name and file system location of each image.
     options.setImageSavingCallback(new SavedImageRename(outFileName));

     doc.save(getArtifactsDir() + outFileName, options);
 }

 /// 
 /// Sets custom filenames for output documents that the saving operation splits a document into.
 /// 
 private static class SavedDocumentPartRename implements IDocumentPartSavingCallback {
     public SavedDocumentPartRename(String outFileName, int documentSplitCriteria) {
         mOutFileName = outFileName;
         mDocumentSplitCriteria = documentSplitCriteria;
     }

     public void documentPartSaving(DocumentPartSavingArgs args) throws Exception {
         // We can access the entire source document via the "Document" property.
         Assert.assertTrue(args.getDocument().getOriginalFileName().endsWith("Rendering.docx"));

         String partType = "";

         switch (mDocumentSplitCriteria) {
             case DocumentSplitCriteria.PAGE_BREAK:
                 partType = "Page";
                 break;
             case DocumentSplitCriteria.COLUMN_BREAK:
                 partType = "Column";
                 break;
             case DocumentSplitCriteria.SECTION_BREAK:
                 partType = "Section";
                 break;
             case DocumentSplitCriteria.HEADING_PARAGRAPH:
                 partType = "Paragraph from heading";
                 break;
         }

         String partFileName = MessageFormat.format("{0} part {1}, of type {2}.{3}", mOutFileName, ++mCount, partType, FilenameUtils.getExtension(args.getDocumentPartFileName()));

         // Below are two ways of specifying where Aspose.Words will save each part of the document.
         // 1 -  Set a filename for the output part file:
         args.setDocumentPartFileName(partFileName);

         // 2 -  Create a custom stream for the output part file:
         try (FileOutputStream outputStream = new FileOutputStream(getArtifactsDir() + partFileName)) {
             args.setDocumentPartStream(outputStream);
         }

         Assert.assertNotNull(args.getDocumentPartStream());
         Assert.assertFalse(args.getKeepDocumentPartStreamOpen());
     }

     private int mCount;
     private final String mOutFileName;
     private final int mDocumentSplitCriteria;
 }

 /// 
 /// Sets custom filenames for image files that an HTML conversion creates.
 /// 
 public static class SavedImageRename implements IImageSavingCallback {
     public SavedImageRename(String outFileName) {
         mOutFileName = outFileName;
     }

     public void imageSaving(ImageSavingArgs args) throws Exception {
         String imageFileName = MessageFormat.format("{0} shape {1}, of type {2}.{3}", mOutFileName, ++mCount, args.getCurrentShape().getShapeType(), FilenameUtils.getExtension(args.getImageFileName()));

         // Below are two ways of specifying where Aspose.Words will save each part of the document.
         // 1 -  Set a filename for the output image file:
         args.setImageFileName(imageFileName);

         // 2 -  Create a custom stream for the output image file:
         args.setImageStream(new FileOutputStream(getArtifactsDir() + imageFileName));

         Assert.assertNotNull(args.getImageStream());
         Assert.assertTrue(args.isImageAvailable());
         Assert.assertFalse(args.getKeepImageStreamOpen());
     }

     private int mCount;
     private final String mOutFileName;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IDocumentPartSavingCallback](../../com.aspose.words/idocumentpartsavingcallback/) | The corresponding [IDocumentPartSavingCallback](../../com.aspose.words/idocumentpartsavingcallback/) value. |

### setDocumentSplitCriteria(int value) {#setDocumentSplitCriteria-int}
```
public void setDocumentSplitCriteria(int value)
```


Specifies how the document should be split when saving to [SaveFormat.HTML](../../com.aspose.words/saveformat/\#HTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat/\#EPUB) or [SaveFormat.AZW\_3](../../com.aspose.words/saveformat/\#AZW-3) format. Default is [DocumentSplitCriteria.NONE](../../com.aspose.words/documentsplitcriteria/\#NONE) for HTML and [DocumentSplitCriteria.HEADING\_PARAGRAPH](../../com.aspose.words/documentsplitcriteria/\#HEADING-PARAGRAPH) for EPUB and AZW3.

 **Remarks:** 

Normally you would want a document saved to HTML as a single file. But in some cases it is preferable to split the output into several smaller HTML pages. When saving to HTML format these pages will be output to individual files or streams. When saving to EPUB format they will be incorporated into corresponding packages.

A document cannot be split when saving in the MHTML format.

 **Examples:** 

Shows how to use a specific encoding when saving a document to .epub.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 // Use a SaveOptions object to specify the encoding for a document that we will save.
 HtmlSaveOptions saveOptions = new HtmlSaveOptions();
 saveOptions.setSaveFormat(SaveFormat.EPUB);
 saveOptions.setEncoding(StandardCharsets.UTF_8);

 // By default, an output .epub document will have all of its contents in one HTML part.
 // A split criterion allows us to segment the document into several HTML parts.
 // We will set the criteria to split the document into heading paragraphs.
 // This is useful for readers who cannot read HTML files more significant than a specific size.
 saveOptions.setDocumentSplitCriteria(DocumentSplitCriteria.HEADING_PARAGRAPH);

 // Specify that we want to export document properties.
 saveOptions.setExportDocumentProperties(true);

 doc.save(getArtifactsDir() + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be a bitwise combination of [DocumentSplitCriteria](../../com.aspose.words/documentsplitcriteria/) constants. |

### setDocumentSplitHeadingLevel(int value) {#setDocumentSplitHeadingLevel-int}
```
public void setDocumentSplitHeadingLevel(int value)
```


Specifies the maximum level of headings at which to split the document. Default value is  2 .

 **Remarks:** 

When [getDocumentSplitCriteria()](../../com.aspose.words/htmlsaveoptions/\#getDocumentSplitCriteria) / [setDocumentSplitCriteria(int)](../../com.aspose.words/htmlsaveoptions/\#setDocumentSplitCriteria-int) includes [DocumentSplitCriteria.HEADING\_PARAGRAPH](../../com.aspose.words/documentsplitcriteria/\#HEADING-PARAGRAPH) and this property is set to a value from 1 to 9, the document will be split at paragraphs formatted using **Heading 1**, **Heading 2** , **Heading 3** etc. styles up to the specified heading level.

By default, only **Heading 1** and **Heading 2** paragraphs cause the document to be split. Setting this property to zero will cause the document not to be split at heading paragraphs at all.

 **Examples:** 

Shows how to split an output HTML document by headings into several parts.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Every paragraph that we format using a "Heading" style can serve as a heading.
 // Each heading may also have a heading level, determined by the number of its heading style.
 // The headings below are of levels 1-3.
 builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get("Heading 1"));
 builder.writeln("Heading #1");
 builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get("Heading 2"));
 builder.writeln("Heading #2");
 builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get("Heading 3"));
 builder.writeln("Heading #3");
 builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get("Heading 1"));
 builder.writeln("Heading #4");
 builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get("Heading 2"));
 builder.writeln("Heading #5");
 builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get("Heading 3"));
 builder.writeln("Heading #6");

 // Create a HtmlSaveOptions object and set the split criteria to "HeadingParagraph".
 // These criteria will split the document at paragraphs with "Heading" styles into several smaller documents,
 // and save each document in a separate HTML file in the local file system.
 // We will also set the maximum heading level, which splits the document to 2.
 // Saving the document will split it at headings of levels 1 and 2, but not at 3 to 9.
 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setDocumentSplitCriteria(DocumentSplitCriteria.HEADING_PARAGRAPH);
     options.setDocumentSplitHeadingLevel(2);
 }

 // Our document has four headings of levels 1 - 2. One of those headings will not be
 // a split point since it is at the beginning of the document.
 // The saving operation will split our document at three places, into four smaller documents.
 doc.save(getArtifactsDir() + "HtmlSaveOptions.HeadingLevels.html", options);

 doc = new Document(getArtifactsDir() + "HtmlSaveOptions.HeadingLevels.html");

 Assert.assertEquals("Heading #1", doc.getText().trim());

 doc = new Document(getArtifactsDir() + "HtmlSaveOptions.HeadingLevels-01.html");

 Assert.assertEquals("Heading #2\r" +
         "Heading #3", doc.getText().trim());

 doc = new Document(getArtifactsDir() + "HtmlSaveOptions.HeadingLevels-02.html");

 Assert.assertEquals("Heading #4", doc.getText().trim());

 doc = new Document(getArtifactsDir() + "HtmlSaveOptions.HeadingLevels-03.html");

 Assert.assertEquals("Heading #5\rHeading #6", doc.getText().trim());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### setEncoding(Charset value) {#setEncoding-java.nio.charset.Charset}
```
public void setEncoding(Charset value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.nio.charset.Charset |  |

### setExportCidUrlsForMhtmlResources(boolean value) {#setExportCidUrlsForMhtmlResources-boolean}
```
public void setExportCidUrlsForMhtmlResources(boolean value)
```


Specifies whether to use CID (Content-ID) URLs to reference resources (images, fonts, CSS) included in MHTML documents. Default value is  false .

 **Remarks:** 

This option affects only documents being saved to MHTML.

By default, resources in MHTML documents are referenced by file name (for example, "image.png"), which are matched against "Content-Location" headers of MIME parts.

This option enables an alternative method, where references to resource files are written as CID (Content-ID) URLs (for example, "cid:image.png") and are matched against "Content-ID" headers.

In theory, there should be no difference between the two referencing methods and either of them should work fine in any browser or mail agent. In practice, however, some agents fail to fetch resources by file name. If your browser or mail agent refuses to load resources included in an MTHML document (doesn't show images or doesn't load CSS styles), try exporting the document with CID URLs.

 **Examples:** 

Shows how to enable content IDs for output MHTML documents.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 // Setting this flag will replace "Content-Location" tags
 // with "Content-ID" tags for each resource from the input document.
 HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.MHTML);
 {
     options.setExportCidUrlsForMhtmlResources(exportCidUrlsForMhtmlResources);
     options.setCssStyleSheetType(CssStyleSheetType.EXTERNAL);
     options.setExportFontResources(true);
     options.setPrettyFormat(true);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.ContentIdUrls.mht", options);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlSaveOptions.ContentIdUrls.mht"), StandardCharsets.UTF_8);

 if (exportCidUrlsForMhtmlResources) {
     Assert.assertTrue(outDocContents.contains("Content-ID: "));
     Assert.assertTrue(outDocContents.contains(""));
     Assert.assertTrue(outDocContents.contains("@font-face { font-family:'Arial Black'; font-weight:bold; src:url('cid:arib=\r\nlk.ttf') }"));
     Assert.assertTrue(outDocContents.contains(""));
 } else {
     Assert.assertTrue(outDocContents.contains("Content-Location: document.html"));
     Assert.assertTrue(outDocContents.contains(""));
     Assert.assertTrue(outDocContents.contains("@font-face { font-family:'Arial Black'; font-weight:bold; src:url('ariblk.t=\r\ntf') }"));
     Assert.assertTrue(outDocContents.contains(""));
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setExportDocumentProperties(boolean value) {#setExportDocumentProperties-boolean}
```
public void setExportDocumentProperties(boolean value)
```


Specifies whether to export built-in and custom document properties to HTML, MHTML or EPUB. Default value is  false .

 **Examples:** 

Shows how to use a specific encoding when saving a document to .epub.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 // Use a SaveOptions object to specify the encoding for a document that we will save.
 HtmlSaveOptions saveOptions = new HtmlSaveOptions();
 saveOptions.setSaveFormat(SaveFormat.EPUB);
 saveOptions.setEncoding(StandardCharsets.UTF_8);

 // By default, an output .epub document will have all of its contents in one HTML part.
 // A split criterion allows us to segment the document into several HTML parts.
 // We will set the criteria to split the document into heading paragraphs.
 // This is useful for readers who cannot read HTML files more significant than a specific size.
 saveOptions.setDocumentSplitCriteria(DocumentSplitCriteria.HEADING_PARAGRAPH);

 // Specify that we want to export document properties.
 saveOptions.setExportDocumentProperties(true);

 doc.save(getArtifactsDir() + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setExportDropDownFormFieldAsText(boolean value) {#setExportDropDownFormFieldAsText-boolean}
```
public void setExportDropDownFormFieldAsText(boolean value)
```


Controls how drop-down form fields are saved to HTML or MHTML. Default value is  false .

 **Remarks:** 

When set to  true , exports drop-down form fields as normal text. When  false , exports drop-down form fields as SELECT element in HTML.

When exporting to EPUB, text drop-down form fields are always saved as text due to requirements of this format.

 **Examples:** 

Shows how to get drop-down combo box form fields to blend in with paragraph text when saving to html.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Use a document builder to insert a combo box with the value "Two" selected.
 builder.insertComboBox("MyComboBox", new String[]{"One", "Two", "Three"}, 1);

 // The "ExportDropDownFormFieldAsText" flag of this SaveOptions object allows us to
 // control how saving the document to HTML treats drop-down combo boxes.
 // Setting it to "true" will convert each combo box into simple text
 // that displays the combo box's currently selected value, effectively freezing it.
 // Setting it to "false" will preserve the functionality of the combo box using  and  tags.
 HtmlSaveOptions options = new HtmlSaveOptions();
 options.setExportDropDownFormFieldAsText(exportDropDownFormFieldAsText);

 doc.save(getArtifactsDir() + "HtmlSaveOptions.DropDownFormField.html", options);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlSaveOptions.DropDownFormField.html"), StandardCharsets.UTF_8);

 if (exportDropDownFormFieldAsText)
     Assert.assertTrue(outDocContents.contains(
             "Two"));
 else
     Assert.assertTrue(outDocContents.contains(
             "" +
                     "One" +
                     "Two" +
                     "Three" +
                     ""));
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setExportFontResources(boolean value) {#setExportFontResources-boolean}
```
public void setExportFontResources(boolean value)
```


Specifies whether font resources should be exported to HTML, MHTML or EPUB. Default is  false .

 **Remarks:** 

Exporting font resources allows for consistent document rendering independent of the fonts available in a given user's environment.

If [getExportFontResources()](../../com.aspose.words/htmlsaveoptions/\#getExportFontResources) / [setExportFontResources(boolean)](../../com.aspose.words/htmlsaveoptions/\#setExportFontResources-boolean) is set to  true , main HTML document will refer to every font via the CSS 3 **@font-face** at-rule and fonts will be output as separate files. When exporting to IDPF EPUB or MHTML formats, fonts will be embedded into the corresponding package along with other subsidiary files.

If [getExportFontsAsBase64()](../../com.aspose.words/htmlsaveoptions/\#getExportFontsAsBase64) / [setExportFontsAsBase64(boolean)](../../com.aspose.words/htmlsaveoptions/\#setExportFontsAsBase64-boolean) is set to  true , fonts will not be saved to separate files. Instead, they will be embedded into **@font-face** at-rules in Base64 encoding.

**Important!** When exporting font resources, font licensing issues should be considered. Authors who want to use specific fonts via a downloadable font mechanism must always carefully verify that their intended use is within the scope of the font license. Many commercial fonts presently do not allow web downloading of their fonts in any form. License agreements that cover some fonts specifically note that usage via **@font-face** rules in CSS style sheets is not allowed. Font subsetting can also violate license terms.

 **Examples:** 

Shows how to define custom logic for exporting fonts when saving to HTML.

```

 public void saveExportedFonts() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     // Configure a SaveOptions object to export fonts to separate files.
     // Set a callback that will handle font saving in a custom manner.
     HtmlSaveOptions options = new HtmlSaveOptions();
     {
         options.setExportFontResources(true);
         options.setFontSavingCallback(new HandleFontSaving());
     }

     // The callback will export .ttf files and save them alongside the output document.
     doc.save(getArtifactsDir() + "HtmlSaveOptions.SaveExportedFonts.html", options);

     File[] fontFileNames = new File(getArtifactsDir()).listFiles((d, name) -> name.endsWith(".ttf"));

     for (File fontFilename : fontFileNames) {
         System.out.println(fontFilename.getName());
     }

 }

 /// 
 /// Prints information about exported fonts and saves them in the same local system folder as their output .html.
 /// 
 public static class HandleFontSaving implements IFontSavingCallback {
     public void fontSaving(FontSavingArgs args) throws Exception {
         System.out.println(MessageFormat.format("Font:\t{0}", args.getFontFamilyName()));
         if (args.getBold()) System.out.print(", bold");
         if (args.getItalic()) System.out.print(", italic");
         System.out.println(MessageFormat.format("\nSource:\t{0}, {1} bytes\n", args.getOriginalFileName(), args.getOriginalFileSize()));

         // We can also access the source document from here.
         Assert.assertTrue(args.getDocument().getOriginalFileName().endsWith("Rendering.docx"));

         Assert.assertTrue(args.isExportNeeded());
         Assert.assertTrue(args.isSubsettingNeeded());

         String[] splittedFileName = args.getOriginalFileName().split("\\\\");
         String fileName = splittedFileName[splittedFileName.length - 1];

         // There are two ways of saving an exported font.
         // 1 -  Save it to a local file system location:
         args.setFontFileName(fileName);

         // 2 -  Save it to a stream:
         args.setFontStream(new FileOutputStream(fileName));
         Assert.assertFalse(args.getKeepFontStreamOpen());
     }
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setExportFontsAsBase64(boolean value) {#setExportFontsAsBase64-boolean}
```
public void setExportFontsAsBase64(boolean value)
```


Specifies whether fonts resources should be embedded to HTML in Base64 encoding. Default is  false .

 **Remarks:** 

By default, fonts are written to separate files. If this option is set to  true , fonts will be embedded into the document's CSS in Base64 encoding.

 **Examples:** 

Shows how to embed fonts inside a saved HTML document.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setExportFontsAsBase64(true);
     options.setCssStyleSheetType(CssStyleSheetType.EMBEDDED);
     options.setPrettyFormat(true);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.ExportFontsAsBase64.html", options);
 
```

Shows how to save a .html document with images embedded inside it.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setExportImagesAsBase64(exportImagesAsBase64);
     options.setPrettyFormat(true);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.ExportImagesAsBase64.html", options);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlSaveOptions.ExportImagesAsBase64.html"), StandardCharsets.UTF_8);

 Assert.assertTrue(exportImagesAsBase64
         ? outDocContents.contains("
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

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


Specifies how headers and footers are output to HTML, MHTML or EPUB. Default value is [ExportHeadersFootersMode.PER\_SECTION](../../com.aspose.words/exportheadersfootersmode/\#PER-SECTION) for HTML/MHTML and [ExportHeadersFootersMode.NONE](../../com.aspose.words/exportheadersfootersmode/\#NONE) for EPUB.

 **Remarks:** 

It is hard to meaningfully output headers and footers to HTML because HTML is not paginated.

When this property is [ExportHeadersFootersMode.PER\_SECTION](../../com.aspose.words/exportheadersfootersmode/\#PER-SECTION), Aspose.Words exports only primary headers and footers at the beginning and the end of each section.

When it is [ExportHeadersFootersMode.FIRST\_SECTION\_HEADER\_LAST\_SECTION\_FOOTER](../../com.aspose.words/exportheadersfootersmode/\#FIRST-SECTION-HEADER-LAST-SECTION-FOOTER) only first primary header and the last primary footer (including linked to previous) are exported.

You can disable export of headers and footers altogether by setting this property to [ExportHeadersFootersMode.NONE](../../com.aspose.words/exportheadersfootersmode/\#NONE).

 **Examples:** 

Shows how to omit headers/footers when saving a document to HTML.

```

 Document doc = new Document(getMyDir() + "Header and footer types.docx");

 // This document contains headers and footers. We can access them via the "HeadersFooters" collection.
 Assert.assertEquals("First header", doc.getFirstSection().getHeadersFooters().getByHeaderFooterType(HeaderFooterType.HEADER_FIRST).getText().trim());

 // Formats such as .html do not split the document into pages, so headers/footers will not function the same way
 // they would when we open the document as a .docx using Microsoft Word.
 // If we convert a document with headers/footers to html, the conversion will assimilate the headers/footers into body text.
 // We can use a SaveOptions object to omit headers/footers while converting to html.
 HtmlSaveOptions saveOptions =
         new HtmlSaveOptions(SaveFormat.HTML);
 {
     saveOptions.setExportHeadersFootersMode(ExportHeadersFootersMode.NONE);
 }

 doc.save(getArtifactsDir() + "HeaderFooter.ExportMode.html", saveOptions);

 // Open our saved document and verify that it does not contain the header's text.
 doc = new Document(getArtifactsDir() + "HeaderFooter.ExportMode.html");

 Assert.assertFalse(doc.getRange().getText().contains("First header"));
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [ExportHeadersFootersMode](../../com.aspose.words/exportheadersfootersmode/) constants. |

### setExportImagesAsBase64(boolean value) {#setExportImagesAsBase64-boolean}
```
public void setExportImagesAsBase64(boolean value)
```


Specifies whether images are saved in Base64 format to the output HTML, MHTML or EPUB. Default is  false .

 **Remarks:** 

When this property is set to  true  images data are exported directly into the **img** elements and separate files are not created.

 **Examples:** 

Shows how to embed fonts inside a saved HTML document.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setExportFontsAsBase64(true);
     options.setCssStyleSheetType(CssStyleSheetType.EMBEDDED);
     options.setPrettyFormat(true);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.ExportFontsAsBase64.html", options);
 
```

Shows how to save a .html document with images embedded inside it.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setExportImagesAsBase64(exportImagesAsBase64);
     options.setPrettyFormat(true);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.ExportImagesAsBase64.html", options);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlSaveOptions.ExportImagesAsBase64.html"), StandardCharsets.UTF_8);

 Assert.assertTrue(exportImagesAsBase64
         ? outDocContents.contains("
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setExportLanguageInformation(boolean value) {#setExportLanguageInformation-boolean}
```
public void setExportLanguageInformation(boolean value)
```


Specifies whether language information is exported to HTML, MHTML or EPUB. Default is  false .

 **Remarks:** 

When this property is set to  true  Aspose.Words outputs **lang** HTML attribute on the document elements that specify language. This can be needed to preserve language related semantics.

 **Examples:** 

Shows how to preserve language information when saving to .html.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Use the builder to write text while formatting it in different locales.
 builder.getFont().setLocaleId(1033);
 builder.writeln("Hello world!");

 builder.getFont().setLocaleId(2057);
 builder.writeln("Hello again!");

 builder.getFont().setLocaleId(1049);
 builder.write("\u041f\u0440\u0438\u0432\u0435\u0442, \u043c\u0438\u0440!");

 // When saving the document to HTML, we can pass a SaveOptions object
 // to either preserve or discard each formatted text's locale.
 // If we set the "ExportLanguageInformation" flag to "true",
 // the output HTML document will contain the locales in "lang" attributes of  tags.
 // If we set the "ExportLanguageInformation" flag to "false',
 // the text in the output HTML document will not contain any locale information.
 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setExportLanguageInformation(exportLanguageInformation);
     options.setPrettyFormat(true);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.ExportLanguageInformation.html", options);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlSaveOptions.ExportLanguageInformation.html"), StandardCharsets.UTF_8);

 if (exportLanguageInformation) {
     Assert.assertTrue(outDocContents.contains("Hello world!"));
     Assert.assertTrue(outDocContents.contains("Hello again!"));
     Assert.assertTrue(outDocContents.contains("\u041f\u0440\u0438\u0432\u0435\u0442, \u043c\u0438\u0440!"));
 } else {
     Assert.assertTrue(outDocContents.contains("Hello world!"));
     Assert.assertTrue(outDocContents.contains("Hello again!"));
     Assert.assertTrue(outDocContents.contains("\u041f\u0440\u0438\u0432\u0435\u0442, \u043c\u0438\u0440!"));
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setExportListLabels(int value) {#setExportListLabels-int}
```
public void setExportListLabels(int value)
```


Controls how list labels are output to HTML, MHTML or EPUB. Default value is [ExportListLabels.AUTO](../../com.aspose.words/exportlistlabels/\#AUTO).

 **Examples:** 

Shows how to configure list exporting to HTML.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 List list = doc.getLists().add(ListTemplate.NUMBER_DEFAULT);
 builder.getListFormat().setList(list);

 builder.writeln("Default numbered list item 1.");
 builder.writeln("Default numbered list item 2.");
 builder.getListFormat().listIndent();
 builder.writeln("Default numbered list item 3.");
 builder.getListFormat().removeNumbers();

 list = doc.getLists().add(ListTemplate.OUTLINE_HEADINGS_LEGAL);
 builder.getListFormat().setList(list);

 builder.writeln("Outline legal heading list item 1.");
 builder.writeln("Outline legal heading list item 2.");
 builder.getListFormat().listIndent();
 builder.writeln("Outline legal heading list item 3.");
 builder.getListFormat().listIndent();
 builder.writeln("Outline legal heading list item 4.");
 builder.getListFormat().listIndent();
 builder.writeln("Outline legal heading list item 5.");
 builder.getListFormat().removeNumbers();

 // When saving the document to HTML, we can pass a SaveOptions object
 // to decide which HTML elements the document will use to represent lists.
 // Setting the "ExportListLabels" property to "ExportListLabels.AsInlineText"
 // will create lists by formatting spans.
 // Setting the "ExportListLabels" property to "ExportListLabels.Auto" will use the  tag
 // to build lists in cases when using the  and  tags may cause loss of formatting.
 // Setting the "ExportListLabels" property to "ExportListLabels.ByHtmlTags"
 // will use  and  tags to build all lists.
 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setExportListLabels(exportListLabels);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.List.html", options);
 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlSaveOptions.List.html"), StandardCharsets.UTF_8);

 switch (exportListLabels) {
     case ExportListLabels.AS_INLINE_TEXT:
         Assert.assertTrue(outDocContents.contains(
                 " " +
                         "" +
                         "a." +
                         "       " +
                         "" +
                         "Default numbered list item 3." +
                         ""));

         Assert.assertTrue(outDocContents.contains(
                 " " +
                         "" +
                         "2.1.1.1" +
                         "       " +
                         "" +
                         "Outline legal heading list item 5." +
                         ""));
         break;
     case ExportListLabels.AUTO:
         Assert.assertTrue(outDocContents.contains(
                 " " +
                         " " +
                         "Default numbered list item 3." +
                         "" +
                         ""));

         break;
     case ExportListLabels.BY_HTML_TAGS:
         Assert.assertTrue(outDocContents.contains(
                 " " +
                         " " +
                         "Default numbered list item 3." +
                         "" +
                         ""));

         break;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [ExportListLabels](../../com.aspose.words/exportlistlabels/) constants. |

### setExportOriginalUrlForLinkedImages(boolean value) {#setExportOriginalUrlForLinkedImages-boolean}
```
public void setExportOriginalUrlForLinkedImages(boolean value)
```


Specifies whether original URL should be used as the URL of the linked images. Default value is  false .

 **Remarks:** 

If value is set to  true  [ImageData.getSourceFullName()](../../com.aspose.words/imagedata/\#getSourceFullName) / [ImageData.setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata/\#setSourceFullName-java.lang.String) value is used as the URL of linked images and linked images are not loaded into document's folder or [getImagesFolder()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolder) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolder-java.lang.String).

If value is set to  false  linked images are loaded into document's folder or [getImagesFolder()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolder) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolder-java.lang.String) and URL of each linked image is constructed depending on document's folder, [getImagesFolder()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolder) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolder-java.lang.String) and [getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolderAlias) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolderAlias-java.lang.String) properties.

 **Examples:** 

Shows how to set folders and folder aliases for externally saved resources that Aspose.Words will create when saving a document to HTML.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setCssStyleSheetType(CssStyleSheetType.EXTERNAL);
     options.setExportFontResources(true);
     options.setImageResolution(72);
     options.setFontResourcesSubsettingSizeThreshold(0);
     options.setFontsFolder(getArtifactsDir() + "Fonts");
     options.setImagesFolder(getArtifactsDir() + "Images");
     options.setResourceFolder(getArtifactsDir() + "Resources");
     options.setFontsFolderAlias("http://example.com/fonts");
     options.setImagesFolderAlias("http://example.com/images");
     options.setResourceFolderAlias("http://example.com/resources");
     options.setExportOriginalUrlForLinkedImages(true);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.FolderAlias.html", options);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setExportPageMargins(boolean value) {#setExportPageMargins-boolean}
```
public void setExportPageMargins(boolean value)
```


Specifies whether page margins is exported to HTML, MHTML or EPUB. Default is  false .

 **Remarks:** 

Aspose.Words does not show area of page margins by default. If any elements are completely or partially clipped by the document edge the displayed area can be extended with this option.

 **Examples:** 

Shows how to show out-of-bounds objects in output HTML documents.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Use a builder to insert a shape with no wrapping.
 Shape shape = builder.insertShape(ShapeType.CUBE, 200.0, 200.0);

 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setWrapType(WrapType.NONE);

 // Negative shape position values may place the shape outside of page boundaries.
 // If we export this to HTML, the shape will appear truncated.
 shape.setLeft(-150);

 // When saving the document to HTML, we can pass a SaveOptions object
 // to decide whether to adjust the page to display out-of-bounds objects fully.
 // If we set the "ExportPageMargins" flag to "true", the shape will be fully visible in the output HTML.
 // If we set the "ExportPageMargins" flag to "false",
 // our document will display the shape truncated as we would see it in Microsoft Word.
 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setExportPageMargins(exportPageMargins);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.ExportPageMargins.html", options);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlSaveOptions.ExportPageMargins.html"), StandardCharsets.UTF_8);

 if (exportPageMargins)
 {
     Assert.assertTrue(outDocContents.contains(""));
     Assert.assertTrue(outDocContents.contains(" "));
 }
 else
 {
     Assert.assertFalse(outDocContents.contains("style type=\"text/css\">"));
     Assert.assertTrue(outDocContents.contains(" "));
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setExportPageSetup(boolean value) {#setExportPageSetup-boolean}
```
public void setExportPageSetup(boolean value)
```


Specifies whether page setup is exported to HTML, MHTML or EPUB. Default is  false .

 **Remarks:** 

Each [Section](../../com.aspose.words/section/) in Aspose.Words document model provides page setup information via [PageSetup](../../com.aspose.words/pagesetup/) class. When you export a document to HTML format you might need to keep this information for further usage. In particular, page setup might be important for rendering to paged media (printing) or subsequent conversion to the native Microsoft Word file formats (DOCX, DOC, RTF, WML).

In most cases HTML is intended for viewing in browsers where pagination is not performed. So this feature is inactive by default.

 **Examples:** 

Shows how decide whether to preserve section structure/page setup information when saving to HTML.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Section 1");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.write("Section 2");

 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setTopMargin(36.0);
 pageSetup.setBottomMargin(36.0);
 pageSetup.setPaperSize(PaperSize.A5);

 // When saving the document to HTML, we can pass a SaveOptions object
 // to decide whether to preserve or discard page setup settings.
 // If we set the "ExportPageSetup" flag to "true", the output HTML document will contain our page setup configuration.
 // If we set the "ExportPageSetup" flag to "false", the save operation will discard our page setup settings
 // for the first section, and both sections will look identical.
 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setExportPageSetup(exportPageSetup);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.ExportPageSetup.html", options);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlSaveOptions.ExportPageSetup.html"), StandardCharsets.UTF_8);

 if (exportPageSetup) {
     Assert.assertTrue(outDocContents.contains(
             ""));

     Assert.assertTrue(outDocContents.contains(
             " " +
                     " " +
                     "Section 1" +
                     "" +
                     ""));
 } else {
     Assert.assertFalse(outDocContents.contains("style type=\"text/css\">"));

     Assert.assertTrue(outDocContents.contains(
             " " +
                     " " +
                     "Section 1" +
                     "" +
                     ""));
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setExportRelativeFontSize(boolean value) {#setExportRelativeFontSize-boolean}
```
public void setExportRelativeFontSize(boolean value)
```


Specifies whether font sizes should be output in relative units when saving to HTML, MHTML or EPUB. Default is  false .

 **Remarks:** 

In many existing documents (HTML, IDPF EPUB) font sizes are specified in relative units. This allows applications to adjust text size when viewing/processing documents. For instance, Microsoft Internet Explorer has "View->Text Size" submenu, Adobe Digital Editions has two buttons: Increase/Decrease Text Size. If you expect this functionality to work then set [getExportRelativeFontSize()](../../com.aspose.words/htmlsaveoptions/\#getExportRelativeFontSize) / [setExportRelativeFontSize(boolean)](../../com.aspose.words/htmlsaveoptions/\#setExportRelativeFontSize-boolean) property to  true .

Aspose Words document model contains and operates only with absolute font size units. Relative units need additional logic to be recalculated from some initial (standard) size. Font size of **Normal** document style is taken as standard. For instance, if **Normal** has 12pt font and some text is 18pt then it will be output as **1.5em.** to the HTML.

When this option is enabled, document elements other than text will still have absolute sizes. Also some text-related attributes might be expressed absolutely. In particular, line spacing specified with "exactly" rule might produce unwanted results when scaling text. So the source documents should be properly designed and tested when exporting with [getExportRelativeFontSize()](../../com.aspose.words/htmlsaveoptions/\#getExportRelativeFontSize) / [setExportRelativeFontSize(boolean)](../../com.aspose.words/htmlsaveoptions/\#setExportRelativeFontSize-boolean) set to  true .

 **Examples:** 

Shows how to use relative font sizes when saving to .html.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Default font size, ");
 builder.getFont().setSize(24.0);
 builder.writeln("2x default font size,");
 builder.getFont().setSize(96.0);
 builder.write("8x default font size");

 // When we save the document to HTML, we can pass a SaveOptions object
 // to determine whether to use relative or absolute font sizes.
 // Set the "ExportRelativeFontSize" flag to "true" to declare font sizes
 // using the "em" measurement unit, which is a factor that multiplies the current font size.
 // Set the "ExportRelativeFontSize" flag to "false" to declare font sizes
 // using the "pt" measurement unit, which is the font's absolute size in points.
 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setExportRelativeFontSize(exportRelativeFontSize);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.RelativeFontSize.html", options);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlSaveOptions.RelativeFontSize.html"), StandardCharsets.UTF_8);

 if (exportRelativeFontSize) {
     Assert.assertTrue(outDocContents.contains(
             "" +
                     " " +
                     " " +
                     "Default font size, " +
                     "" +
                     " " +
                     "2x default font size," +
                     "" +
                     " " +
                     "8x default font size" +
                     "" +
                     "" +
                     ""));
 } else {
     Assert.assertTrue(outDocContents.contains(
             "" +
                     " " +
                     " " +
                     "Default font size, " +
                     "" +
                     " " +
                     "2x default font size," +
                     "" +
                     " " +
                     "8x default font size" +
                     "" +
                     "" +
                     ""));
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setExportRoundtripInformation(boolean value) {#setExportRoundtripInformation-boolean}
```
public void setExportRoundtripInformation(boolean value)
```


Specifies whether to write the roundtrip information when saving to HTML, MHTML or EPUB. Default value is  true  for HTML and  false  for MHTML and EPUB.

 **Remarks:** 

Saving of the roundtrip information allows to restore document properties such as tab stops, comments, headers and footers during the HTML documents loading back into a [Document](../../com.aspose.words/document/) object.

When  true , the roundtrip information is exported as -aw-\* CSS properties of the corresponding HTML elements.

When  false , causes no roundtrip information to be output into produced files.

 **Examples:** 

Shows how to preserve hidden elements when converting to .html.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 // When converting a document to .html, some elements such as hidden bookmarks, original shape positions,
 // or footnotes will be either removed or converted to plain text and effectively be lost.
 // Saving with a HtmlSaveOptions object with ExportRoundtripInformation set to true will preserve these elements.

 // When we save the document to HTML, we can pass a SaveOptions object to determine
 // how the saving operation will export document elements that HTML does not support or use,
 // such as hidden bookmarks and original shape positions.
 // If we set the "ExportRoundtripInformation" flag to "true", the save operation will preserve these elements.
 // If we set the "ExportRoundTripInformation" flag to "false", the save operation will discard these elements.
 // We will want to preserve such elements if we intend to load the saved HTML using Aspose.Words,
 // as they could be of use once again.
 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setExportRoundtripInformation(exportRoundtripInformation);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.RoundTripInformation.html", options);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlSaveOptions.RoundTripInformation.html"), StandardCharsets.UTF_8);
 doc = new Document(getArtifactsDir() + "HtmlSaveOptions.RoundTripInformation.html");

 if (exportRoundtripInformation) {
     Assert.assertTrue(outDocContents.contains(" "));
     Assert.assertTrue(outDocContents.contains(" "));

     Assert.assertTrue(outDocContents.contains(
             "td colspan=\"2\" style=\"width:210.6pt; border-style:solid; border-width:0.75pt 6pt 0.75pt 0.75pt; " +
                     "padding-right:2.4pt; padding-left:5.03pt; vertical-align:top; " +
                     "-aw-border-bottom:0.5pt single; -aw-border-left:0.5pt single; -aw-border-top:0.5pt single\">"));

     Assert.assertTrue(outDocContents.contains(
             " "));

     Assert.assertTrue(outDocContents.contains(
             ""));

     Assert.assertTrue(outDocContents.contains(
             "Page number " +
                     "" +
                     "" +
                     "" +
                     "1" +
                     ""));

     Assert.assertEquals(1, IterableUtils.countMatches(doc.getRange().getFields(), f -> f.getType() == FieldType.FIELD_PAGE));
 } else {
     Assert.assertTrue(outDocContents.contains(" "));
     Assert.assertTrue(outDocContents.contains(" "));

     Assert.assertTrue(outDocContents.contains(
             ""));

     Assert.assertTrue(outDocContents.contains(
             " "));

     Assert.assertTrue(outDocContents.contains(
             ""));

     Assert.assertTrue(outDocContents.contains(
             "Page number 1"));

     Assert.assertEquals(0, IterableUtils.countMatches(doc.getRange().getFields(), f -> f.getType() == FieldType.FIELD_PAGE));
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setExportShapesAsSvg(boolean value) {#setExportShapesAsSvg-boolean}
```
public void setExportShapesAsSvg(boolean value)
```


Controls whether [Shape](../../com.aspose.words/shape/) nodes are converted to SVG images when saving to HTML, MHTML, EPUB or AZW3. Default value is  false .

 **Remarks:** 

If this option is set to  true , [Shape](../../com.aspose.words/shape/) nodes are exported as  elements. Otherwise, they are rendered to bitmaps and are exported as ![Image 1][] elements.

 **Examples:** 

Shows how to export shape as scalable vector graphics.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape textBox = builder.insertShape(ShapeType.TEXT_BOX, 100.0, 60.0);
 builder.moveTo(textBox.getFirstParagraph());
 builder.write("My text box");

 // When we save the document to HTML, we can pass a SaveOptions object
 // to determine how the saving operation will export text box shapes.
 // If we set the "ExportTextBoxAsSvg" flag to "true",
 // the save operation will convert shapes with text into SVG objects.
 // If we set the "ExportTextBoxAsSvg" flag to "false",
 // the save operation will convert shapes with text into images.
 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setExportShapesAsSvg(exportShapesAsSvg);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.ExportTextBox.html", options);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlSaveOptions.ExportTextBox.html"), StandardCharsets.UTF_8);

 if (exportShapesAsSvg) {
     Assert.assertTrue(outDocContents.contains(
             "" +
                     ""));
 } else {
     Assert.assertTrue(outDocContents.contains(
             " " +
                     "" +
                     ""));
 }
 
```


[Image 1]: 

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setExportTextInputFormFieldAsText(boolean value) {#setExportTextInputFormFieldAsText-boolean}
```
public void setExportTextInputFormFieldAsText(boolean value)
```


Controls how text input form fields are saved to HTML or MHTML. Default value is  false .

 **Remarks:** 

When set to  true , exports text input form fields as normal text. When  false , exports Word text input form fields as INPUT elements in HTML.

When exporting to EPUB, text input form fields are always saved as text due to requirements of this format.

 **Examples:** 

Shows how to specify the folder for storing linked images after saving to .html.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 File imagesDir = new File(getArtifactsDir() + "SaveHtmlWithOptions");

 if (imagesDir.exists())
     imagesDir.delete();

 imagesDir.mkdir();

 // Set an option to export form fields as plain text instead of HTML input elements.
 HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.HTML);
 options.setExportTextInputFormFieldAsText(true);
 options.setImagesFolder(imagesDir.getPath());

 doc.save(getArtifactsDir() + "HtmlSaveOptions.SaveHtmlWithOptions.html", options);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setExportTocPageNumbers(boolean value) {#setExportTocPageNumbers-boolean}
```
public void setExportTocPageNumbers(boolean value)
```


Specifies whether to write page numbers to table of contents when saving HTML, MHTML and EPUB. Default value is  false .

 **Examples:** 

Shows how to display page numbers when saving a document with a table of contents to .html.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a table of contents, and then populate the document with paragraphs formatted using a "Heading"
 // style that the table of contents will pick up as entries. Each entry will display the heading paragraph on the left,
 // and the page number that contains the heading on the right.
 FieldToc fieldToc = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

 builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get("Heading 1"));
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Entry 1");
 builder.writeln("Entry 2");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Entry 3");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Entry 4");
 fieldToc.updatePageNumbers();
 doc.updateFields();

 // HTML documents do not have pages. If we save this document to HTML,
 // the page numbers that our TOC displays will have no meaning.
 // When we save the document to HTML, we can pass a SaveOptions object to omit these page numbers from the TOC.
 // If we set the "ExportTocPageNumbers" flag to "true",
 // each TOC entry will display the heading, separator, and page number, preserving its appearance in Microsoft Word.
 // If we set the "ExportTocPageNumbers" flag to "false",
 // the save operation will omit both the separator and page number and leave the heading for each entry intact.
 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setExportTocPageNumbers(exportTocPageNumbers);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.ExportTocPageNumbers.html", options);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlSaveOptions.ExportTocPageNumbers.html"), StandardCharsets.UTF_8);

 if (exportTocPageNumbers) {
     Assert.assertTrue(outDocContents.contains(
             "Entry 1" +
                     "......................................................................" +
                     "2" +
                     " "));
 } else {
     Assert.assertTrue(outDocContents.contains(
             " " +
                     "Entry 2" +
                     ""));
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setExportXhtmlTransitional(boolean value) {#setExportXhtmlTransitional-boolean}
```
public void setExportXhtmlTransitional(boolean value)
```


Specifies whether to write the DOCTYPE declaration when saving to HTML or MHTML. When  true , writes a DOCTYPE declaration in the document prior to the root element. Default value is  false . When saving to EPUB or HTML5 ( [HtmlVersion.HTML\_5](../../com.aspose.words/htmlversion/\#HTML-5)) the DOCTYPE declaration is always written.

 **Remarks:** 

Aspose.Words always writes well formed HTML regardless of this setting.

When  true , the beginning of the HTML output document will look like this:

```

 
 
 
 
```

Aspose.Words aims to output XHTML according to the XHTML 1.0 Transitional specification, but the output will not always validate against the DTD. Some structures inside a Microsoft Word document are hard or impossible to map to a document that will validate against the XHTML schema. For example, XHTML does not allow nested lists (UL cannot be nested inside another UL element), but in Microsoft Word document multilevel lists occur quite often.

 **Examples:** 

Shows how to display a DOCTYPE heading when converting documents to the Xhtml 1.0 transitional standard.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");

 HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.HTML);
 {
     options.setHtmlVersion(HtmlVersion.XHTML);
     options.setExportXhtmlTransitional(showDoctypeDeclaration);
     options.setPrettyFormat(true);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.ExportXhtmlTransitional.html", options);

 // Our document will only contain a DOCTYPE declaration heading if we have set the "ExportXhtmlTransitional" flag to "true".
 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlSaveOptions.ExportXhtmlTransitional.html"), StandardCharsets.UTF_8);

 if (showDoctypeDeclaration)
     Assert.assertTrue(outDocContents.contains(
             "\r\n" +
                     "\r\n" +
                     ""));
 else
     Assert.assertTrue(outDocContents.contains(""));
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setFontResourcesSubsettingSizeThreshold(int value) {#setFontResourcesSubsettingSizeThreshold-int}
```
public void setFontResourcesSubsettingSizeThreshold(int value)
```


Controls which font resources need subsetting when saving to HTML, MHTML or EPUB. Default is  0 .

 **Remarks:** 

[getExportFontResources()](../../com.aspose.words/htmlsaveoptions/\#getExportFontResources) / [setExportFontResources(boolean)](../../com.aspose.words/htmlsaveoptions/\#setExportFontResources-boolean) allows exporting fonts as subsidiary files or as parts of the output package. If the document uses many fonts, especially with large number of glyphs, then output size can grow significantly. Font subsetting reduces the size of the exported font resource by filtering out glyphs that are not used by the current document.

Font subsetting works as follows:

 *  By default, all exported fonts are subsetted.
 *  Setting [getFontResourcesSubsettingSizeThreshold()](../../com.aspose.words/htmlsaveoptions/\#getFontResourcesSubsettingSizeThreshold) / [setFontResourcesSubsettingSizeThreshold(int)](../../com.aspose.words/htmlsaveoptions/\#setFontResourcesSubsettingSizeThreshold-int) to a positive value instructs Aspose.Words to subset fonts which file size is larger than the specified value.
 *  Setting the property to **Integer.MAX\_VALUE** suppresses font subsetting.

**Important!** When exporting font resources, font licensing issues should be considered. Authors who want to use specific fonts via a downloadable font mechanism must always carefully verify that their intended use is within the scope of the font license. Many commercial fonts presently do not allow web downloading of their fonts in any form. License agreements that cover some fonts specifically note that usage via **@font-face** rules in CSS style sheets is not allowed. Font subsetting can also violate license terms.

 **Examples:** 

Shows how to work with font subsetting.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setName("Arial");
 builder.writeln("Hello world!");
 builder.getFont().setName("Times New Roman");
 builder.writeln("Hello world!");
 builder.getFont().setName("Courier New");
 builder.writeln("Hello world!");

 // When we save the document to HTML, we can pass a SaveOptions object configure font subsetting.
 // Suppose we set the "ExportFontResources" flag to "true" and also name a folder in the "FontsFolder" property.
 // In that case, the saving operation will create that folder and place a .ttf file inside
 // that folder for each font that our document uses.
 // Each .ttf file will contain that font's entire glyph set,
 // which may potentially result in a very large file that accompanies the document.
 // When we apply subsetting to a font, its exported raw data will only contain the glyphs that the document is
 // using instead of the entire glyph set. If the text in our document only uses a small fraction of a font's
 // glyph set, then subsetting will significantly reduce our output documents' size.
 // We can use the "FontResourcesSubsettingSizeThreshold" property to define a .ttf file size, in bytes.
 // If an exported font creates a size bigger file than that, then the save operation will apply subsetting to that font.
 // Setting a threshold of 0 applies subsetting to all fonts,
 // and setting it to "int.MaxValue" effectively disables subsetting.
 String fontsFolder = getArtifactsDir() + "HtmlSaveOptions.FontSubsetting.Fonts";

 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setExportFontResources(true);
     options.setFontsFolder(fontsFolder);
     options.setFontResourcesSubsettingSizeThreshold(fontResourcesSubsettingSizeThreshold);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.FontSubsetting.html", options);

 File[] fontFileNames = new File(fontsFolder).listFiles((d, name) -> name.endsWith(".ttf"));

 Assert.assertEquals(3, fontFileNames.length);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### setFontSavingCallback(IFontSavingCallback value) {#setFontSavingCallback-com.aspose.words.IFontSavingCallback}
```
public void setFontSavingCallback(IFontSavingCallback value)
```


Allows to control how fonts are saved when a document is saved to HTML, MHTML or EPUB.

 **Examples:** 

Shows how to define custom logic for exporting fonts when saving to HTML.

```

 public void saveExportedFonts() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     // Configure a SaveOptions object to export fonts to separate files.
     // Set a callback that will handle font saving in a custom manner.
     HtmlSaveOptions options = new HtmlSaveOptions();
     {
         options.setExportFontResources(true);
         options.setFontSavingCallback(new HandleFontSaving());
     }

     // The callback will export .ttf files and save them alongside the output document.
     doc.save(getArtifactsDir() + "HtmlSaveOptions.SaveExportedFonts.html", options);

     File[] fontFileNames = new File(getArtifactsDir()).listFiles((d, name) -> name.endsWith(".ttf"));

     for (File fontFilename : fontFileNames) {
         System.out.println(fontFilename.getName());
     }

 }

 /// 
 /// Prints information about exported fonts and saves them in the same local system folder as their output .html.
 /// 
 public static class HandleFontSaving implements IFontSavingCallback {
     public void fontSaving(FontSavingArgs args) throws Exception {
         System.out.println(MessageFormat.format("Font:\t{0}", args.getFontFamilyName()));
         if (args.getBold()) System.out.print(", bold");
         if (args.getItalic()) System.out.print(", italic");
         System.out.println(MessageFormat.format("\nSource:\t{0}, {1} bytes\n", args.getOriginalFileName(), args.getOriginalFileSize()));

         // We can also access the source document from here.
         Assert.assertTrue(args.getDocument().getOriginalFileName().endsWith("Rendering.docx"));

         Assert.assertTrue(args.isExportNeeded());
         Assert.assertTrue(args.isSubsettingNeeded());

         String[] splittedFileName = args.getOriginalFileName().split("\\\\");
         String fileName = splittedFileName[splittedFileName.length - 1];

         // There are two ways of saving an exported font.
         // 1 -  Save it to a local file system location:
         args.setFontFileName(fileName);

         // 2 -  Save it to a stream:
         args.setFontStream(new FileOutputStream(fileName));
         Assert.assertFalse(args.getKeepFontStreamOpen());
     }
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IFontSavingCallback](../../com.aspose.words/ifontsavingcallback/) | The corresponding [IFontSavingCallback](../../com.aspose.words/ifontsavingcallback/) value. |

### setFontsFolder(String value) {#setFontsFolder-java.lang.String}
```
public void setFontsFolder(String value)
```


Specifies the physical folder where fonts are saved when exporting a document to HTML. Default is an empty string.

 **Remarks:** 

When you save a [Document](../../com.aspose.words/document/) in HTML format and [getExportFontResources()](../../com.aspose.words/htmlsaveoptions/\#getExportFontResources) / [setExportFontResources(boolean)](../../com.aspose.words/htmlsaveoptions/\#setExportFontResources-boolean) is set to  true , Aspose.Words needs to save fonts used in the document as standalone files. [getFontsFolder()](../../com.aspose.words/htmlsaveoptions/\#getFontsFolder) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setFontsFolder-java.lang.String) allows you to specify where the fonts will be saved and [getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getFontsFolderAlias) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setFontsFolderAlias-java.lang.String) allows to specify how the font URIs will be constructed.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the fonts in the same folder where the document file is saved. Use [getFontsFolder()](../../com.aspose.words/htmlsaveoptions/\#getFontsFolder) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setFontsFolder-java.lang.String) to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the fonts, but still needs to save the fonts somewhere. In this case, you need to specify an accessible folder in the [getFontsFolder()](../../com.aspose.words/htmlsaveoptions/\#getFontsFolder) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setFontsFolder-java.lang.String) property or provide custom streams via the [getFontSavingCallback()](../../com.aspose.words/htmlsaveoptions/\#getFontSavingCallback) / [setFontSavingCallback(com.aspose.words.IFontSavingCallback)](../../com.aspose.words/htmlsaveoptions/\#setFontSavingCallback-com.aspose.words.IFontSavingCallback) event handler.

If the folder specified by [getFontsFolder()](../../com.aspose.words/htmlsaveoptions/\#getFontsFolder) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setFontsFolder-java.lang.String) doesn't exist, it will be created automatically.

[getResourceFolder()](../../com.aspose.words/htmlsaveoptions/\#getResourceFolder) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setResourceFolder-java.lang.String) is another way to specify a folder where fonts should be saved.

 **Examples:** 

Shows how to set folders and folder aliases for externally saved resources that Aspose.Words will create when saving a document to HTML.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setCssStyleSheetType(CssStyleSheetType.EXTERNAL);
     options.setExportFontResources(true);
     options.setImageResolution(72);
     options.setFontResourcesSubsettingSizeThreshold(0);
     options.setFontsFolder(getArtifactsDir() + "Fonts");
     options.setImagesFolder(getArtifactsDir() + "Images");
     options.setResourceFolder(getArtifactsDir() + "Resources");
     options.setFontsFolderAlias("http://example.com/fonts");
     options.setImagesFolderAlias("http://example.com/images");
     options.setResourceFolderAlias("http://example.com/resources");
     options.setExportOriginalUrlForLinkedImages(true);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.FolderAlias.html", options);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setFontsFolderAlias(String value) {#setFontsFolderAlias-java.lang.String}
```
public void setFontsFolderAlias(String value)
```


Specifies the name of the folder used to construct font URIs written into an HTML document. Default is an empty string.

 **Remarks:** 

When you save a [Document](../../com.aspose.words/document/) in HTML format and [getExportFontResources()](../../com.aspose.words/htmlsaveoptions/\#getExportFontResources) / [setExportFontResources(boolean)](../../com.aspose.words/htmlsaveoptions/\#setExportFontResources-boolean) is set to  true , Aspose.Words needs to save fonts used in the document as standalone files. [getFontsFolder()](../../com.aspose.words/htmlsaveoptions/\#getFontsFolder) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setFontsFolder-java.lang.String) allows you to specify where the fonts will be saved and [getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getFontsFolderAlias) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setFontsFolderAlias-java.lang.String) allows to specify how the font URIs will be constructed.

If [getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getFontsFolderAlias) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setFontsFolderAlias-java.lang.String) is not an empty string, then the font URI written to HTML will be *FontsFolderAlias +* . 

If [getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getFontsFolderAlias) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setFontsFolderAlias-java.lang.String) is an empty string, then the font URI written to HTML will be *FontsFolder +* . 

If [getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getFontsFolderAlias) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setFontsFolderAlias-java.lang.String) is set to '.' (dot), then the font file name will be written to HTML without path regardless of other options.

Alternative way to specify the name of the folder to construct font URIs is to use [getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getResourceFolderAlias) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setResourceFolderAlias-java.lang.String).

 **Examples:** 

Shows how to set folders and folder aliases for externally saved resources that Aspose.Words will create when saving a document to HTML.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setCssStyleSheetType(CssStyleSheetType.EXTERNAL);
     options.setExportFontResources(true);
     options.setImageResolution(72);
     options.setFontResourcesSubsettingSizeThreshold(0);
     options.setFontsFolder(getArtifactsDir() + "Fonts");
     options.setImagesFolder(getArtifactsDir() + "Images");
     options.setResourceFolder(getArtifactsDir() + "Resources");
     options.setFontsFolderAlias("http://example.com/fonts");
     options.setImagesFolderAlias("http://example.com/images");
     options.setResourceFolderAlias("http://example.com/resources");
     options.setExportOriginalUrlForLinkedImages(true);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.FolderAlias.html", options);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setHtmlVersion(int value) {#setHtmlVersion-int}
```
public void setHtmlVersion(int value)
```


Specifies version of HTML standard that should be used when saving the document to HTML or MHTML. Default value is [HtmlVersion.XHTML](../../com.aspose.words/htmlversion/\#XHTML).

 **Examples:** 

Shows how to display a DOCTYPE heading when converting documents to the Xhtml 1.0 transitional standard.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");

 HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.HTML);
 {
     options.setHtmlVersion(HtmlVersion.XHTML);
     options.setExportXhtmlTransitional(showDoctypeDeclaration);
     options.setPrettyFormat(true);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.ExportXhtmlTransitional.html", options);

 // Our document will only contain a DOCTYPE declaration heading if we have set the "ExportXhtmlTransitional" flag to "true".
 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlSaveOptions.ExportXhtmlTransitional.html"), StandardCharsets.UTF_8);

 if (showDoctypeDeclaration)
     Assert.assertTrue(outDocContents.contains(
             "\r\n" +
                     "\r\n" +
                     ""));
 else
     Assert.assertTrue(outDocContents.contains(""));
 
```

Shows how to save a document to a specific version of HTML.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.HTML);
 {
     options.setHtmlVersion(htmlVersion);
     options.setPrettyFormat(true);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.HtmlVersions.html", options);

 // Our HTML documents will have minor differences to be compatible with different HTML versions.
 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlSaveOptions.HtmlVersions.html"), StandardCharsets.UTF_8);

 switch (htmlVersion) {
     case HtmlVersion.HTML_5:
         Assert.assertTrue(outDocContents.contains(""));
         Assert.assertTrue(outDocContents.contains(""));
         Assert.assertTrue(outDocContents.contains(" "));
         Assert.assertTrue(outDocContents.contains(" "));
         break;
     case HtmlVersion.XHTML:
         Assert.assertTrue(outDocContents.contains(""));
         Assert.assertTrue(outDocContents.contains(" "));
         break;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [HtmlVersion](../../com.aspose.words/htmlversion/) constants. |

### setImageResolution(int value) {#setImageResolution-int}
```
public void setImageResolution(int value)
```


Specifies the output resolution for images when exporting to HTML, MHTML or EPUB. Default is  96 dpi .

 **Remarks:** 

This property effects raster images when [getScaleImageToShapeSize()](../../com.aspose.words/htmlsaveoptions/\#getScaleImageToShapeSize) / [setScaleImageToShapeSize(boolean)](../../com.aspose.words/htmlsaveoptions/\#setScaleImageToShapeSize-boolean) is  true  and effects metafiles exported as raster images. Some image properties such as cropping or rotation require saving transformed images and in this case transformed images are created in the given resolution.

 **Examples:** 

Shows how to set folders and folder aliases for externally saved resources that Aspose.Words will create when saving a document to HTML.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setCssStyleSheetType(CssStyleSheetType.EXTERNAL);
     options.setExportFontResources(true);
     options.setImageResolution(72);
     options.setFontResourcesSubsettingSizeThreshold(0);
     options.setFontsFolder(getArtifactsDir() + "Fonts");
     options.setImagesFolder(getArtifactsDir() + "Images");
     options.setResourceFolder(getArtifactsDir() + "Resources");
     options.setFontsFolderAlias("http://example.com/fonts");
     options.setImagesFolderAlias("http://example.com/images");
     options.setResourceFolderAlias("http://example.com/resources");
     options.setExportOriginalUrlForLinkedImages(true);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.FolderAlias.html", options);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### setImageSavingCallback(IImageSavingCallback value) {#setImageSavingCallback-com.aspose.words.IImageSavingCallback}
```
public void setImageSavingCallback(IImageSavingCallback value)
```


Allows to control how images are saved when a document is saved to HTML, MHTML or EPUB.

 **Examples:** 

Shows how to split a document into parts and save them.

```

 public void documentPartsFileNames() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");
     String outFileName = "SavingCallback.DocumentPartsFileNames.html";

     // Create an "HtmlFixedSaveOptions" object, which we can pass to the document's "Save" method
     // to modify how we convert the document to HTML.
     HtmlSaveOptions options = new HtmlSaveOptions();

     // If we save the document normally, there will be one output HTML
     // document with all the source document's contents.
     // Set the "DocumentSplitCriteria" property to "DocumentSplitCriteria.SectionBreak" to
     // save our document to multiple HTML files: one for each section.
     options.setDocumentSplitCriteria(DocumentSplitCriteria.SECTION_BREAK);

     // Assign a custom callback to the "DocumentPartSavingCallback" property to alter the document part saving logic.
     options.setDocumentPartSavingCallback(new SavedDocumentPartRename(outFileName, options.getDocumentSplitCriteria()));

     // If we convert a document that contains images into html, we will end up with one html file which links to several images.
     // Each image will be in the form of a file in the local file system.
     // There is also a callback that can customize the name and file system location of each image.
     options.setImageSavingCallback(new SavedImageRename(outFileName));

     doc.save(getArtifactsDir() + outFileName, options);
 }

 /// 
 /// Sets custom filenames for output documents that the saving operation splits a document into.
 /// 
 private static class SavedDocumentPartRename implements IDocumentPartSavingCallback {
     public SavedDocumentPartRename(String outFileName, int documentSplitCriteria) {
         mOutFileName = outFileName;
         mDocumentSplitCriteria = documentSplitCriteria;
     }

     public void documentPartSaving(DocumentPartSavingArgs args) throws Exception {
         // We can access the entire source document via the "Document" property.
         Assert.assertTrue(args.getDocument().getOriginalFileName().endsWith("Rendering.docx"));

         String partType = "";

         switch (mDocumentSplitCriteria) {
             case DocumentSplitCriteria.PAGE_BREAK:
                 partType = "Page";
                 break;
             case DocumentSplitCriteria.COLUMN_BREAK:
                 partType = "Column";
                 break;
             case DocumentSplitCriteria.SECTION_BREAK:
                 partType = "Section";
                 break;
             case DocumentSplitCriteria.HEADING_PARAGRAPH:
                 partType = "Paragraph from heading";
                 break;
         }

         String partFileName = MessageFormat.format("{0} part {1}, of type {2}.{3}", mOutFileName, ++mCount, partType, FilenameUtils.getExtension(args.getDocumentPartFileName()));

         // Below are two ways of specifying where Aspose.Words will save each part of the document.
         // 1 -  Set a filename for the output part file:
         args.setDocumentPartFileName(partFileName);

         // 2 -  Create a custom stream for the output part file:
         try (FileOutputStream outputStream = new FileOutputStream(getArtifactsDir() + partFileName)) {
             args.setDocumentPartStream(outputStream);
         }

         Assert.assertNotNull(args.getDocumentPartStream());
         Assert.assertFalse(args.getKeepDocumentPartStreamOpen());
     }

     private int mCount;
     private final String mOutFileName;
     private final int mDocumentSplitCriteria;
 }

 /// 
 /// Sets custom filenames for image files that an HTML conversion creates.
 /// 
 public static class SavedImageRename implements IImageSavingCallback {
     public SavedImageRename(String outFileName) {
         mOutFileName = outFileName;
     }

     public void imageSaving(ImageSavingArgs args) throws Exception {
         String imageFileName = MessageFormat.format("{0} shape {1}, of type {2}.{3}", mOutFileName, ++mCount, args.getCurrentShape().getShapeType(), FilenameUtils.getExtension(args.getImageFileName()));

         // Below are two ways of specifying where Aspose.Words will save each part of the document.
         // 1 -  Set a filename for the output image file:
         args.setImageFileName(imageFileName);

         // 2 -  Create a custom stream for the output image file:
         args.setImageStream(new FileOutputStream(getArtifactsDir() + imageFileName));

         Assert.assertNotNull(args.getImageStream());
         Assert.assertTrue(args.isImageAvailable());
         Assert.assertFalse(args.getKeepImageStreamOpen());
     }

     private int mCount;
     private final String mOutFileName;
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


Specifies the physical folder where images are saved when exporting a document to HTML format. Default is an empty string.

 **Remarks:** 

When you save a [Document](../../com.aspose.words/document/) in HTML format, Aspose.Words needs to save all images embedded in the document as standalone files. [getImagesFolder()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolder) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolder-java.lang.String) allows you to specify where the images will be saved and [getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolderAlias) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolderAlias-java.lang.String) allows to specify how the image URIs will be constructed.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the images in the same folder where the document file is saved. Use [getImagesFolder()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolder) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolder-java.lang.String) to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the images, but still needs to save the images somewhere. In this case, you need to specify an accessible folder in the [getImagesFolder()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolder) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolder-java.lang.String) property or provide custom streams via the [getImageSavingCallback()](../../com.aspose.words/htmlsaveoptions/\#getImageSavingCallback) / [setImageSavingCallback(com.aspose.words.IImageSavingCallback)](../../com.aspose.words/htmlsaveoptions/\#setImageSavingCallback-com.aspose.words.IImageSavingCallback) event handler.

If the folder specified by [getImagesFolder()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolder) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolder-java.lang.String) doesn't exist, it will be created automatically.

[getResourceFolder()](../../com.aspose.words/htmlsaveoptions/\#getResourceFolder) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setResourceFolder-java.lang.String) is another way to specify a folder where images should be saved.

 **Examples:** 

Shows how to specify the folder for storing linked images after saving to .html.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 File imagesDir = new File(getArtifactsDir() + "SaveHtmlWithOptions");

 if (imagesDir.exists())
     imagesDir.delete();

 imagesDir.mkdir();

 // Set an option to export form fields as plain text instead of HTML input elements.
 HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.HTML);
 options.setExportTextInputFormFieldAsText(true);
 options.setImagesFolder(imagesDir.getPath());

 doc.save(getArtifactsDir() + "HtmlSaveOptions.SaveHtmlWithOptions.html", options);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setImagesFolderAlias(String value) {#setImagesFolderAlias-java.lang.String}
```
public void setImagesFolderAlias(String value)
```


Specifies the name of the folder used to construct image URIs written into an HTML document. Default is an empty string.

 **Remarks:** 

When you save a [Document](../../com.aspose.words/document/) in HTML format, Aspose.Words needs to save all images embedded in the document as standalone files. [getImagesFolder()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolder) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolder-java.lang.String) allows you to specify where the images will be saved and [getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolderAlias) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolderAlias-java.lang.String) allows to specify how the image URIs will be constructed.

If [getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolderAlias) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolderAlias-java.lang.String) is not an empty string, then the image URI written to HTML will be *ImagesFolderAlias + ![Image 1][]*.

If [getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolderAlias) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolderAlias-java.lang.String) is an empty string, then the image URI written to HTML will be *ImagesFolder + ![Image 1][]*.

If [getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolderAlias) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolderAlias-java.lang.String) is set to '.' (dot), then the image file name will be written to HTML without path regardless of other options.

Alternative way to specify the name of the folder to construct image URIs is to use [getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getResourceFolderAlias) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setResourceFolderAlias-java.lang.String).

 **Examples:** 

Shows how to set folders and folder aliases for externally saved resources that Aspose.Words will create when saving a document to HTML.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setCssStyleSheetType(CssStyleSheetType.EXTERNAL);
     options.setExportFontResources(true);
     options.setImageResolution(72);
     options.setFontResourcesSubsettingSizeThreshold(0);
     options.setFontsFolder(getArtifactsDir() + "Fonts");
     options.setImagesFolder(getArtifactsDir() + "Images");
     options.setResourceFolder(getArtifactsDir() + "Resources");
     options.setFontsFolderAlias("http://example.com/fonts");
     options.setImagesFolderAlias("http://example.com/images");
     options.setResourceFolderAlias("http://example.com/resources");
     options.setExportOriginalUrlForLinkedImages(true);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.FolderAlias.html", options);
 
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

### setMetafileFormat(int value) {#setMetafileFormat-int}
```
public void setMetafileFormat(int value)
```


Specifies in what format metafiles are saved when exporting to HTML, MHTML, or EPUB. Default value is [HtmlMetafileFormat.PNG](../../com.aspose.words/htmlmetafileformat/\#PNG), meaning that metafiles are rendered to raster PNG images.

 **Remarks:** 

Metafiles are not natively displayed by HTML browsers. By default, Aspose.Words converts WMF and EMF images into PNG files when exporting to HTML. Other options are to convert metafiles to SVG images or to export them as is without conversion.

Some image transforms, in particular image cropping, will not be applied to metafile images if they are exported to HTML without conversion.

 **Examples:** 

Shows how to convert SVG objects to a different format when saving HTML documents.

```

 String html =
     "\n                    \n                        Hello world!\n                    \n                ";

 // Use 'ConvertSvgToEmf' to turn back the legacy behavior
 // where all SVG images loaded from an HTML document were converted to EMF.
 // Now SVG images are loaded without conversion
 // if the MS Word version specified in load options supports SVG images natively.
 HtmlLoadOptions loadOptions = new HtmlLoadOptions(); { loadOptions.setConvertSvgToEmf(true); }

 Document doc = new Document(new ByteArrayInputStream(html.getBytes()));

 // This document contains a  element in the form of text.
 // When we save the document to HTML, we can pass a SaveOptions object
 // to determine how the saving operation handles this object.
 // Setting the "MetafileFormat" property to "HtmlMetafileFormat.Png" to convert it to a PNG image.
 // Setting the "MetafileFormat" property to "HtmlMetafileFormat.Svg" preserve it as a SVG object.
 // Setting the "MetafileFormat" property to "HtmlMetafileFormat.EmfOrWmf" to convert it to a metafile.
 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setMetafileFormat(htmlMetafileFormat);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.MetafileFormat.html", options);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlSaveOptions.MetafileFormat.html"), StandardCharsets.UTF_8);

 switch (htmlMetafileFormat) {
     case HtmlMetafileFormat.PNG:
         Assert.assertTrue(outDocContents.contains(
                 " " +
                         "" +
                         ""));
         break;
     case HtmlMetafileFormat.SVG:
         Assert.assertTrue(outDocContents.contains(
                 "" +
                         ""));
         break;
     case HtmlMetafileFormat.EMF_OR_WMF:
         Assert.assertTrue(outDocContents.contains(
                 " " +
                         "" +
                         ""));
         break;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [HtmlMetafileFormat](../../com.aspose.words/htmlmetafileformat/) constants. |

### setNavigationMapLevel(int value) {#setNavigationMapLevel-int}
```
public void setNavigationMapLevel(int value)
```


Specifies the maximum level of headings populated to the navigation map when exporting to EPUB, MOBI, or AZW3 formats. Default value is  3 .

 **Remarks:** 

The navigation map allows user agents to provide an easy way of navigation through the document structure. Usually navigation points correspond to headings in the document. In order to populate headings up to level **N** assign this value to [getNavigationMapLevel()](../../com.aspose.words/htmlsaveoptions/\#getNavigationMapLevel) / [setNavigationMapLevel(int)](../../com.aspose.words/htmlsaveoptions/\#setNavigationMapLevel-int).

By default, three levels of headings are populated: paragraphs of styles **Heading 1**, **Heading 2** and **Heading 3**. You can set this property to a value from 1 to 9 in order to request the corresponding maximum level. Setting it to zero will reduce the navigation map to only the document root or roots of document parts.

 **Examples:** 

Shows how to generate table of contents for Mobi documents.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.MOBI);
 options.setNavigationMapLevel(5);

 doc.save(getArtifactsDir() + "HtmlSaveOptions.CreateMobiToc.mobi", options);
 
```

Shows how to generate table of contents for Azw3 documents.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.AZW_3);
 options.setNavigationMapLevel(2);

 doc.save(getArtifactsDir() + "HtmlSaveOptions.CreateAZW3Toc.azw3", options);
 
```

Shows how to filter headings that appear in the navigation panel of a saved Epub document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Every paragraph that we format using a "Heading" style can serve as a heading.
 // Each heading may also have a heading level, determined by the number of its heading style.
 // The headings below are of levels 1-3.
 builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get("Heading 1"));
 builder.writeln("Heading #1");
 builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get("Heading 2"));
 builder.writeln("Heading #2");
 builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get("Heading 3"));
 builder.writeln("Heading #3");
 builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get("Heading 1"));
 builder.writeln("Heading #4");
 builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get("Heading 2"));
 builder.writeln("Heading #5");
 builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get("Heading 3"));
 builder.writeln("Heading #6");

 // Epub readers typically create a table of contents for their documents.
 // Each paragraph with a "Heading" style in the document will create an entry in this table of contents.
 // We can use the "NavigationMapLevel" property to set a maximum heading level.
 // The Epub reader will not add headings with a level above the one we specify to the contents table.
 HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.EPUB);
 options.setNavigationMapLevel(2);

 // Our document has six headings, two of which are above level 2.
 // The table of contents for this document will have four entries.
 doc.save(getArtifactsDir() + "HtmlSaveOptions.EpubHeadings.epub", options);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### setOfficeMathOutputMode(int value) {#setOfficeMathOutputMode-int}
```
public void setOfficeMathOutputMode(int value)
```


Controls how OfficeMath objects are exported to HTML, MHTML or EPUB. Default value is [HtmlOfficeMathOutputMode.IMAGE](../../com.aspose.words/htmlofficemathoutputmode/\#IMAGE).

 **Examples:** 

Shows how to specify how to export Microsoft OfficeMath objects to HTML.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 // When we save the document to HTML, we can pass a SaveOptions object
 // to determine how the saving operation handles OfficeMath objects.
 // Setting the "OfficeMathOutputMode" property to "HtmlOfficeMathOutputMode.Image"
 // will render each OfficeMath object into an image.
 // Setting the "OfficeMathOutputMode" property to "HtmlOfficeMathOutputMode.MathML"
 // will convert each OfficeMath object into MathML.
 // Setting the "OfficeMathOutputMode" property to "HtmlOfficeMathOutputMode.Text"
 // will represent each OfficeMath formula using plain HTML text.
 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setOfficeMathOutputMode(htmlOfficeMathOutputMode);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.OfficeMathOutputMode.html", options);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [HtmlOfficeMathOutputMode](../../com.aspose.words/htmlofficemathoutputmode/) constants. |

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

### setRemoveJavaScriptFromLinks(boolean value) {#setRemoveJavaScriptFromLinks-boolean}
```
public void setRemoveJavaScriptFromLinks(boolean value)
```


Specifies whether JavaScript will be removed from links. Default is  false .

 **Remarks:** 

If this option is enabled, all links containing JavaScript (e.g., links with "javascript:" in the href attribute) will be replaced with "javascript:void(0)". This can help prevent potential security risks, such as XSS attacks.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setReplaceBackslashWithYenSign(boolean value) {#setReplaceBackslashWithYenSign-boolean}
```
public void setReplaceBackslashWithYenSign(boolean value)
```


Specifies whether backslash characters should be replaced with yen signs. Default value is  false .

 **Remarks:** 

By default, Aspose.Words mimics MS Word's behavior and doesn't replace backslash characters with yen signs in generated HTML documents. However, previous versions of Aspose.Words performed such replacements in certain scenarios. This flag enables backward compatibility with previous versions of Aspose.Words.

 **Examples:** 

Shows how to replace backslash characters with yen signs (Html).

```

 Document doc = new Document(getMyDir() + "Korean backslash symbol.docx");

 // By default, Aspose.Words mimics MS Word's behavior and doesn't replace backslash characters with yen signs in
 // generated HTML documents. However, previous versions of Aspose.Words performed such replacements in certain
 // scenarios. This flag enables backward compatibility with previous versions of Aspose.Words.
 HtmlSaveOptions saveOptions = new HtmlSaveOptions();
 saveOptions.setReplaceBackslashWithYenSign(true);

 doc.save(getArtifactsDir() + "HtmlSaveOptions.ReplaceBackslashWithYenSign.html", saveOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setResolveFontNames(boolean value) {#setResolveFontNames-boolean}
```
public void setResolveFontNames(boolean value)
```


Specifies whether font family names used in the document are resolved and substituted according to [Document.getFontSettings()](../../com.aspose.words/document/\#getFontSettings) / [Document.setFontSettings(com.aspose.words.FontSettings)](../../com.aspose.words/document/\#setFontSettings-com.aspose.words.FontSettings) when being written into HTML-based formats.

 **Remarks:** 

By default, this option is set to  false  and font family names are written to HTML as specified in source documents. That is, [Document.getFontSettings()](../../com.aspose.words/document/\#getFontSettings) / [Document.setFontSettings(com.aspose.words.FontSettings)](../../com.aspose.words/document/\#setFontSettings-com.aspose.words.FontSettings) are ignored and no resolution or substitution of font family names is performed.

If this option is set to  true , Aspose.Words uses [Document.getFontSettings()](../../com.aspose.words/document/\#getFontSettings) / [Document.setFontSettings(com.aspose.words.FontSettings)](../../com.aspose.words/document/\#setFontSettings-com.aspose.words.FontSettings) to resolve each font family name specified in a source document into the name of an available font family, performing font substitution as required.

 **Examples:** 

Shows how to resolve all font names before writing them to HTML.

```

 Document doc = new Document(getMyDir() + "Missing font.docx");

 // This document contains text that names a font that we do not have.
 Assert.assertNotNull(doc.getFontInfos().get("28 Days Later"));

 // If we have no way of getting this font, and we want to be able to display all the text
 // in this document in an output HTML, we can substitute it with another font.
 FontSettings fontSettings = new FontSettings();
 {
     fontSettings.getSubstitutionSettings().getDefaultFontSubstitution().setDefaultFontName("Arial");
     fontSettings.getSubstitutionSettings().getDefaultFontSubstitution().setEnabled(true);
 }

 doc.setFontSettings(fontSettings);

 HtmlSaveOptions saveOptions = new HtmlSaveOptions(SaveFormat.HTML);
 {
     // By default, this option is set to 'False' and Aspose.Words writes font names as specified in the source document.
     saveOptions.setResolveFontNames(resolveFontNames);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.ResolveFontNames.html", saveOptions);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlSaveOptions.ResolveFontNames.html"), "utf-8");

 Assert.assertTrue(outDocContents.matches(""));
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setResourceFolder(String value) {#setResourceFolder-java.lang.String}
```
public void setResourceFolder(String value)
```


Specifies a physical folder where all resources like images, fonts, and external CSS are saved when a document is exported to HTML. Default is an empty string.

 **Remarks:** 

[getResourceFolder()](../../com.aspose.words/htmlsaveoptions/\#getResourceFolder) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setResourceFolder-java.lang.String) is the simplest way to specify a folder where all resources should be written. Another way is to use individual properties [getFontsFolder()](../../com.aspose.words/htmlsaveoptions/\#getFontsFolder) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setFontsFolder-java.lang.String), [getImagesFolder()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolder) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolder-java.lang.String), and [getCssStyleSheetFileName()](../../com.aspose.words/htmlsaveoptions/\#getCssStyleSheetFileName) / [setCssStyleSheetFileName(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setCssStyleSheetFileName-java.lang.String).

[getResourceFolder()](../../com.aspose.words/htmlsaveoptions/\#getResourceFolder) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setResourceFolder-java.lang.String) has a lower priority than folders specified via [getFontsFolder()](../../com.aspose.words/htmlsaveoptions/\#getFontsFolder) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setFontsFolder-java.lang.String), [getImagesFolder()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolder) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolder-java.lang.String), and [getCssStyleSheetFileName()](../../com.aspose.words/htmlsaveoptions/\#getCssStyleSheetFileName) / [setCssStyleSheetFileName(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setCssStyleSheetFileName-java.lang.String). For example, if both [getResourceFolder()](../../com.aspose.words/htmlsaveoptions/\#getResourceFolder) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setResourceFolder-java.lang.String) and [getFontsFolder()](../../com.aspose.words/htmlsaveoptions/\#getFontsFolder) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setFontsFolder-java.lang.String) are specified, fonts will be saved to [getFontsFolder()](../../com.aspose.words/htmlsaveoptions/\#getFontsFolder) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setFontsFolder-java.lang.String), while images and CSS will be saved to [getResourceFolder()](../../com.aspose.words/htmlsaveoptions/\#getResourceFolder) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setResourceFolder-java.lang.String).

If the folder specified by [getResourceFolder()](../../com.aspose.words/htmlsaveoptions/\#getResourceFolder) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setResourceFolder-java.lang.String) doesn't exist, it will be created automatically.

 **Examples:** 

Shows how to set folders and folder aliases for externally saved resources that Aspose.Words will create when saving a document to HTML.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setCssStyleSheetType(CssStyleSheetType.EXTERNAL);
     options.setExportFontResources(true);
     options.setImageResolution(72);
     options.setFontResourcesSubsettingSizeThreshold(0);
     options.setFontsFolder(getArtifactsDir() + "Fonts");
     options.setImagesFolder(getArtifactsDir() + "Images");
     options.setResourceFolder(getArtifactsDir() + "Resources");
     options.setFontsFolderAlias("http://example.com/fonts");
     options.setImagesFolderAlias("http://example.com/images");
     options.setResourceFolderAlias("http://example.com/resources");
     options.setExportOriginalUrlForLinkedImages(true);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.FolderAlias.html", options);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setResourceFolderAlias(String value) {#setResourceFolderAlias-java.lang.String}
```
public void setResourceFolderAlias(String value)
```


Specifies the name of the folder used to construct URIs of all resources written into an HTML document. Default is an empty string.

 **Remarks:** 

[getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getResourceFolderAlias) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setResourceFolderAlias-java.lang.String) is the simplest way to specify how URIs for all resource files should be constructed. Same information can be specified for images and fonts separately via [getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolderAlias) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolderAlias-java.lang.String) and [getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getFontsFolderAlias) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setFontsFolderAlias-java.lang.String) properties, respectively. However, there is no individual property for CSS.

[getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getResourceFolderAlias) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setResourceFolderAlias-java.lang.String) has lower priority than [getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getFontsFolderAlias) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setFontsFolderAlias-java.lang.String) and [getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolderAlias) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolderAlias-java.lang.String). For example, if both [getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getResourceFolderAlias) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setResourceFolderAlias-java.lang.String) and [getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getFontsFolderAlias) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setFontsFolderAlias-java.lang.String) are specified, fonts' URIs will be constructed using [getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getFontsFolderAlias) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setFontsFolderAlias-java.lang.String), while URIs of images and CSS will be constructed using [getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getResourceFolderAlias) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setResourceFolderAlias-java.lang.String).

If [getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getResourceFolderAlias) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setResourceFolderAlias-java.lang.String) is empty, the [getResourceFolder()](../../com.aspose.words/htmlsaveoptions/\#getResourceFolder) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setResourceFolder-java.lang.String) property value will be used to construct resource URIs.

If [getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getResourceFolderAlias) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setResourceFolderAlias-java.lang.String) is set to '.' (dot), resource URIs will contain file names only, without any path.

 **Examples:** 

Shows how to set folders and folder aliases for externally saved resources that Aspose.Words will create when saving a document to HTML.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setCssStyleSheetType(CssStyleSheetType.EXTERNAL);
     options.setExportFontResources(true);
     options.setImageResolution(72);
     options.setFontResourcesSubsettingSizeThreshold(0);
     options.setFontsFolder(getArtifactsDir() + "Fonts");
     options.setImagesFolder(getArtifactsDir() + "Images");
     options.setResourceFolder(getArtifactsDir() + "Resources");
     options.setFontsFolderAlias("http://example.com/fonts");
     options.setImagesFolderAlias("http://example.com/images");
     options.setResourceFolderAlias("http://example.com/resources");
     options.setExportOriginalUrlForLinkedImages(true);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.FolderAlias.html", options);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setSaveFormat(int value) {#setSaveFormat-int}
```
public void setSaveFormat(int value)
```


Specifies the format in which the document will be saved if this save options object is used. Can be [SaveFormat.HTML](../../com.aspose.words/saveformat/\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat/\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat/\#EPUB), [SaveFormat.AZW\_3](../../com.aspose.words/saveformat/\#AZW-3) or [SaveFormat.MOBI](../../com.aspose.words/saveformat/\#MOBI).

 **Examples:** 

Shows how to use a specific encoding when saving a document to .epub.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 // Use a SaveOptions object to specify the encoding for a document that we will save.
 HtmlSaveOptions saveOptions = new HtmlSaveOptions();
 saveOptions.setSaveFormat(SaveFormat.EPUB);
 saveOptions.setEncoding(StandardCharsets.UTF_8);

 // By default, an output .epub document will have all of its contents in one HTML part.
 // A split criterion allows us to segment the document into several HTML parts.
 // We will set the criteria to split the document into heading paragraphs.
 // This is useful for readers who cannot read HTML files more significant than a specific size.
 saveOptions.setDocumentSplitCriteria(DocumentSplitCriteria.HEADING_PARAGRAPH);

 // Specify that we want to export document properties.
 saveOptions.setExportDocumentProperties(true);

 doc.save(getArtifactsDir() + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [SaveFormat](../../com.aspose.words/saveformat/) constants. |

### setScaleImageToShapeSize(boolean value) {#setScaleImageToShapeSize-boolean}
```
public void setScaleImageToShapeSize(boolean value)
```


Specifies whether images are scaled by Aspose.Words to the bounding shape size when exporting to HTML, MHTML or EPUB. Default value is  true .

 **Remarks:** 

An image in a Microsoft Word document is a shape. The shape has a size and the image has its own size. The sizes are not directly linked. For example, the image can be 1024x786 pixels, but shape that displays this image can be 400x300 points.

In order to display an image in the browser, it must be scaled to the shape size. The [getScaleImageToShapeSize()](../../com.aspose.words/htmlsaveoptions/\#getScaleImageToShapeSize) / [setScaleImageToShapeSize(boolean)](../../com.aspose.words/htmlsaveoptions/\#setScaleImageToShapeSize-boolean) property controls where the scaling of the image takes place: in Aspose.Words during export to HTML or in the browser when displaying the document.

When [getScaleImageToShapeSize()](../../com.aspose.words/htmlsaveoptions/\#getScaleImageToShapeSize) / [setScaleImageToShapeSize(boolean)](../../com.aspose.words/htmlsaveoptions/\#setScaleImageToShapeSize-boolean) is  true , the image is scaled by Aspose.Words using high quality scaling during export to HTML. When [getScaleImageToShapeSize()](../../com.aspose.words/htmlsaveoptions/\#getScaleImageToShapeSize) / [setScaleImageToShapeSize(boolean)](../../com.aspose.words/htmlsaveoptions/\#setScaleImageToShapeSize-boolean) is  false , the image is output with its original size and the browser has to scale it.

In general, browsers do quick and poor quality scaling. As a result, you will normally get better display quality in the browser and smaller file size when [getScaleImageToShapeSize()](../../com.aspose.words/htmlsaveoptions/\#getScaleImageToShapeSize) / [setScaleImageToShapeSize(boolean)](../../com.aspose.words/htmlsaveoptions/\#setScaleImageToShapeSize-boolean) is  true , but better printing quality and faster conversion when [getScaleImageToShapeSize()](../../com.aspose.words/htmlsaveoptions/\#getScaleImageToShapeSize) / [setScaleImageToShapeSize(boolean)](../../com.aspose.words/htmlsaveoptions/\#setScaleImageToShapeSize-boolean) is  false .

In addition to shapes containing individual raster images, this option also affects group shapes consisting of raster images. If [getScaleImageToShapeSize()](../../com.aspose.words/htmlsaveoptions/\#getScaleImageToShapeSize) / [setScaleImageToShapeSize(boolean)](../../com.aspose.words/htmlsaveoptions/\#setScaleImageToShapeSize-boolean) is  false  and a group shape contains raster images whose intrinsic resolution is higher than the value specified in [getImageResolution()](../../com.aspose.words/htmlsaveoptions/\#getImageResolution) / [setImageResolution(int)](../../com.aspose.words/htmlsaveoptions/\#setImageResolution-int), Aspose.Words will increase rendering resolution for that group. This allows to better preserve quality of grouped high resolution images when saving to HTML.

 **Examples:** 

Shows how to disable the scaling of images to their parent shape dimensions when saving to .html.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a shape which contains an image, and then make that shape considerably smaller than the image.
 Shape imageShape = builder.insertImage(getImageDir() + "Transparent background logo.png");
 imageShape.setWidth(50.0);
 imageShape.setHeight(50.0);

 // Saving a document that contains shapes with images to HTML will create an image file in the local file system
 // for each such shape. The output HTML document will use  tags to link to and display these images.
 // When we save the document to HTML, we can pass a SaveOptions object to determine
 // whether to scale all images that are inside shapes to the sizes of their shapes.
 // Setting the "ScaleImageToShapeSize" flag to "true" will shrink every image
 // to the size of the shape that contains it, so that no saved images will be larger than the document requires them to be.
 // Setting the "ScaleImageToShapeSize" flag to "false" will preserve these images' original sizes,
 // which will take up more space in exchange for preserving image quality.
 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setScaleImageToShapeSize(scaleImageToShapeSize);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.ScaleImageToShapeSize.html", options);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setTableWidthOutputMode(int value) {#setTableWidthOutputMode-int}
```
public void setTableWidthOutputMode(int value)
```


Controls how table, row and cell widths are exported to HTML, MHTML or EPUB. Default value is [HtmlElementSizeOutputMode.ALL](../../com.aspose.words/htmlelementsizeoutputmode/\#ALL).

 **Remarks:** 

In the HTML format, table, row and cell elements ( 

    | -- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
    | ,  | ) can have their widths specified either in relative (percentage) or in absolute units. In a document in Aspose.Words, tables, rows and cells can have their widths specified using either relative or absolute units too.  When you convert a document to HTML using Aspose.Words, you might want to control how table, row and cell widths are exported to affect how the resulting document is displayed in the visual agent (e.g. a browser or viewer).  Use this property as a filter to specify what table widths values are exported into the destination document. For example, if you are converting a document to EPUB and intend to view the document on a mobile reading device, then you probably want to avoid exporting absolute width values. To do this you need to specify the output mode [HtmlElementSizeOutputMode.RELATIVE\_ONLY](../../com.aspose.words/htmlelementsizeoutputmode/\#RELATIVE-ONLY) or [HtmlElementSizeOutputMode.NONE](../../com.aspose.words/htmlelementsizeoutputmode/\#NONE) so the viewer on the mobile device can layout the table to fit the width of the screen as best as it can.   **Examples:**   Shows how to preserve negative indents in the output .html.   Document doc = new Document(); DocumentBuilder builder = new DocumentBuilder(doc); // Insert a table with a negative indent, which will push it to the left past the left page boundary. Table table = builder.startTable(); builder.insertCell(); builder.write("Row 1, Cell 1"); builder.insertCell(); builder.write("Row 1, Cell 2"); builder.endTable(); table.setLeftIndent(-36); table.setPreferredWidth(PreferredWidth.fromPoints(144.0)); builder.insertBreak(BreakType.PARAGRAPH\_BREAK); // Insert a table with a positive indent, which will push the table to the right. table = builder.startTable(); builder.insertCell(); builder.write("Row 1, Cell 1"); builder.insertCell(); builder.write("Row 1, Cell 2"); builder.endTable(); table.setLeftIndent(36.0); table.setPreferredWidth(PreferredWidth.fromPoints(144.0)); // When we save a document to HTML, Aspose.Words will only preserve negative indents // such as the one we have applied to the first table if we set the "AllowNegativeIndent" flag // in a SaveOptions object that we will pass to "true". HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.HTML); \{ options.setAllowNegativeIndent(allowNegativeIndent); options.setTableWidthOutputMode(HtmlElementSizeOutputMode.RELATIVE\_ONLY); \} doc.save(getArtifactsDir() + "HtmlSaveOptions.NegativeIndent.html", options); String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlSaveOptions.NegativeIndent.html"), StandardCharsets.UTF\_8); if (allowNegativeIndent) \{ Assert.assertTrue(outDocContents.contains( "  ")); Assert.assertTrue(outDocContents.contains( "  ")); \} else \{ Assert.assertTrue(outDocContents.contains( "  ")); Assert.assertTrue(outDocContents.contains( "  ")); \}  |

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [HtmlElementSizeOutputMode](../../com.aspose.words/htmlelementsizeoutputmode/) constants. |

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

