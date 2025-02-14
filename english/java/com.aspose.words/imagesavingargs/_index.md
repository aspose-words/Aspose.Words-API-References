---
title: ImageSavingArgs
linktitle: ImageSavingArgs
second_title: Aspose.Words for Java
description: Provides data for the IImageSavingCallback.imageSavingcom.aspose.words.ImageSavingArgs event in Java.
type: docs
weight: 387
url: /java/com.aspose.words/imagesavingargs/
---

**Inheritance:**
java.lang.Object
```
public class ImageSavingArgs
```

Provides data for the [IImageSavingCallback.imageSaving(com.aspose.words.ImageSavingArgs)](../../com.aspose.words/iimagesavingcallback/\#imageSaving-com.aspose.words.ImageSavingArgs) event.

To learn more, visit the [ Save a Document ][Save a Document] documentation article.

 **Remarks:** 

By default, when Aspose.Words saves a document to HTML, it saves each image into a separate file. Aspose.Words uses the document file name and a unique number to generate unique file name for each image found in the document.

[ImageSavingArgs](../../com.aspose.words/imagesavingargs/) allows to redefine how image file names are generated or to completely circumvent saving of images into files by providing your own stream objects.

To apply your own logic for generating image file names use the [getImageFileName()](../../com.aspose.words/imagesavingargs/\#getImageFileName) / [setImageFileName(java.lang.String)](../../com.aspose.words/imagesavingargs/\#setImageFileName-java.lang.String), [getCurrentShape()](../../com.aspose.words/imagesavingargs/\#getCurrentShape) and [isImageAvailable()](../../com.aspose.words/imagesavingargs/\#isImageAvailable) properties.

To save images into streams instead of files, use the **P:Aspose.Words.Saving.ImageSavingArgs.ImageStream** property.

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


[Save a Document]: https://docs.aspose.com/words/java/save-a-document/
## Methods

| Method | Description |
| --- | --- |
| [getCurrentShape()](#getCurrentShape) | Gets the [ShapeBase](../../com.aspose.words/shapebase/) object corresponding to the shape or group shape that is about to be saved. |
| [getDocument()](#getDocument) | Gets the document object that is currently being saved. |
| [getImageFileName()](#getImageFileName) | Gets the file name (without path) where the image will be saved to. |
| [getImageStream()](#getImageStream) |  |
| [getKeepImageStreamOpen()](#getKeepImageStreamOpen) | Specifies whether Aspose.Words should keep the stream open or close it after saving an image. |
| [isImageAvailable()](#isImageAvailable) | Returns  true  if the current image is available for export. |
| [setImageFileName(String value)](#setImageFileName-java.lang.String) | Sets the file name (without path) where the image will be saved to. |
| [setImageStream(OutputStream value)](#setImageStream-java.io.OutputStream) |  |
| [setKeepImageStreamOpen(boolean value)](#setKeepImageStreamOpen-boolean) | Specifies whether Aspose.Words should keep the stream open or close it after saving an image. |
### getCurrentShape() {#getCurrentShape}
```
public ShapeBase getCurrentShape()
```


Gets the [ShapeBase](../../com.aspose.words/shapebase/) object corresponding to the shape or group shape that is about to be saved.

 **Remarks:** 

[IImageSavingCallback](../../com.aspose.words/iimagesavingcallback/) can be fired while saving either a shape or a group shape. That's why the property has [ShapeBase](../../com.aspose.words/shapebase/) type. You can check whether it's a group shape comparing [ShapeBase.getShapeType()](../../com.aspose.words/shapebase/\#getShapeType) with [ShapeType.GROUP](../../com.aspose.words/shapetype/\#GROUP) or by casting it to one of derived classes: [Shape](../../com.aspose.words/shape/) or [GroupShape](../../com.aspose.words/groupshape/).

Aspose.Words uses the document file name and a unique number to generate unique file name for each image found in the document. You can use the [getCurrentShape()](../../com.aspose.words/imagesavingargs/\#getCurrentShape) property to generate a "better" file name by examining shape properties such as [ImageData.getTitle()](../../com.aspose.words/imagedata/\#getTitle) / [ImageData.setTitle(java.lang.String)](../../com.aspose.words/imagedata/\#setTitle-java.lang.String)(Shape only), [ImageData.getSourceFullName()](../../com.aspose.words/imagedata/\#getSourceFullName) / [ImageData.setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata/\#setSourceFullName-java.lang.String) (Shape only) and [ShapeBase.getName()](../../com.aspose.words/shapebase/\#getName) / [ShapeBase.setName(java.lang.String)](../../com.aspose.words/shapebase/\#setName-java.lang.String). Of course you can build file names using any other properties or criteria but note that subsidiary file names must be unique within the export operation.

Some images in the document can be unavailable. To check image availability use the [isImageAvailable()](../../com.aspose.words/imagesavingargs/\#isImageAvailable) property.

 **Examples:** 

Shows how to involve an image saving callback in an HTML conversion process.

```

 public void imageSavingCallback() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     // When we save the document to HTML, we can pass a SaveOptions object to designate a callback
     // to customize the image saving process.
     HtmlSaveOptions options = new HtmlSaveOptions();
     options.setImageSavingCallback(new ImageShapePrinter());

     doc.save(getArtifactsDir() + "HtmlSaveOptions.ImageSavingCallback.html", options);
 }

 /// 
 /// Prints the properties of each image as the saving process saves it to an image file in the local file system
 /// during the exporting of a document to HTML.
 /// 
 private static class ImageShapePrinter implements IImageSavingCallback {
     public void imageSaving(ImageSavingArgs args) throws Exception {
         args.setKeepImageStreamOpen(false);
         Assert.assertTrue(args.isImageAvailable());

         String[] splitOriginalFileName = args.getDocument().getOriginalFileName().split("\\\\");
         System.out.println(MessageFormat.format("{0} Image #{1}", splitOriginalFileName[splitOriginalFileName.length - 1], ++mImageCount));

         LayoutCollector layoutCollector = new LayoutCollector(args.getDocument());

         System.out.println(MessageFormat.format("\tOn page:\t{0}", layoutCollector.getStartPageIndex(args.getCurrentShape())));
         System.out.println(MessageFormat.format("\tDimensions:\t{0}", args.getCurrentShape().getBounds().toString()));
         System.out.println(MessageFormat.format("\tAlignment:\t{0}", args.getCurrentShape().getVerticalAlignment()));
         System.out.println(MessageFormat.format("\tWrap type:\t{0}", args.getCurrentShape().getWrapType()));
         System.out.println(MessageFormat.format("Output filename:\t{0}\n", args.getImageFileName()));
     }

     private int mImageCount;
 }
 
```

**Returns:**
[ShapeBase](../../com.aspose.words/shapebase/) - The [ShapeBase](../../com.aspose.words/shapebase/) object corresponding to the shape or group shape that is about to be saved.
### getDocument() {#getDocument}
```
public Document getDocument()
```


Gets the document object that is currently being saved.

 **Examples:** 

Shows how to involve an image saving callback in an HTML conversion process.

```

 public void imageSavingCallback() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     // When we save the document to HTML, we can pass a SaveOptions object to designate a callback
     // to customize the image saving process.
     HtmlSaveOptions options = new HtmlSaveOptions();
     options.setImageSavingCallback(new ImageShapePrinter());

     doc.save(getArtifactsDir() + "HtmlSaveOptions.ImageSavingCallback.html", options);
 }

 /// 
 /// Prints the properties of each image as the saving process saves it to an image file in the local file system
 /// during the exporting of a document to HTML.
 /// 
 private static class ImageShapePrinter implements IImageSavingCallback {
     public void imageSaving(ImageSavingArgs args) throws Exception {
         args.setKeepImageStreamOpen(false);
         Assert.assertTrue(args.isImageAvailable());

         String[] splitOriginalFileName = args.getDocument().getOriginalFileName().split("\\\\");
         System.out.println(MessageFormat.format("{0} Image #{1}", splitOriginalFileName[splitOriginalFileName.length - 1], ++mImageCount));

         LayoutCollector layoutCollector = new LayoutCollector(args.getDocument());

         System.out.println(MessageFormat.format("\tOn page:\t{0}", layoutCollector.getStartPageIndex(args.getCurrentShape())));
         System.out.println(MessageFormat.format("\tDimensions:\t{0}", args.getCurrentShape().getBounds().toString()));
         System.out.println(MessageFormat.format("\tAlignment:\t{0}", args.getCurrentShape().getVerticalAlignment()));
         System.out.println(MessageFormat.format("\tWrap type:\t{0}", args.getCurrentShape().getWrapType()));
         System.out.println(MessageFormat.format("Output filename:\t{0}\n", args.getImageFileName()));
     }

     private int mImageCount;
 }
 
```

**Returns:**
[Document](../../com.aspose.words/document/) - The document object that is currently being saved.
### getImageFileName() {#getImageFileName}
```
public String getImageFileName()
```


Gets the file name (without path) where the image will be saved to.

 **Remarks:** 

This property allows you to redefine how the image file names are generated during export to HTML.

When the event is fired, this property contains the file name that was generated by Aspose.Words. You can change the value of this property to save the image into a different file. Note that file names must be unique.

Aspose.Words automatically generates a unique file name for every embedded image when exporting to HTML format. How the image file name is generated depends on whether you save the document to a file or to a stream.

When saving a document to a file, the generated image file name looks like *.![Image 1][].*.

When saving a document to a stream, the generated image file name looks like *Aspose.Words..![Image 1][].*.

[getImageFileName()](../../com.aspose.words/imagesavingargs/\#getImageFileName) / [setImageFileName(java.lang.String)](../../com.aspose.words/imagesavingargs/\#setImageFileName-java.lang.String) must contain only the file name without the path. Aspose.Words determines the path for saving and the value of the  src  attribute for writing to HTML using the document file name, the [HtmlSaveOptions.getImagesFolder()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolder) / [HtmlSaveOptions.setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolder-java.lang.String) and [HtmlSaveOptions.getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolderAlias) / [HtmlSaveOptions.setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolderAlias-java.lang.String) properties.

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


[Image 1]: 

**Returns:**
java.lang.String - The file name (without path) where the image will be saved to.
### getImageStream() {#getImageStream}
```
public OutputStream getImageStream()
```




**Returns:**
java.io.OutputStream
### getKeepImageStreamOpen() {#getKeepImageStreamOpen}
```
public boolean getKeepImageStreamOpen()
```


Specifies whether Aspose.Words should keep the stream open or close it after saving an image.

 **Remarks:** 

Default is  false  and Aspose.Words will close the stream you provided in the **P:Aspose.Words.Saving.ImageSavingArgs.ImageStream** property after writing an image into it. Specify  true  to keep the stream open.

 **Examples:** 

Shows how to involve an image saving callback in an HTML conversion process.

```

 public void imageSavingCallback() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     // When we save the document to HTML, we can pass a SaveOptions object to designate a callback
     // to customize the image saving process.
     HtmlSaveOptions options = new HtmlSaveOptions();
     options.setImageSavingCallback(new ImageShapePrinter());

     doc.save(getArtifactsDir() + "HtmlSaveOptions.ImageSavingCallback.html", options);
 }

 /// 
 /// Prints the properties of each image as the saving process saves it to an image file in the local file system
 /// during the exporting of a document to HTML.
 /// 
 private static class ImageShapePrinter implements IImageSavingCallback {
     public void imageSaving(ImageSavingArgs args) throws Exception {
         args.setKeepImageStreamOpen(false);
         Assert.assertTrue(args.isImageAvailable());

         String[] splitOriginalFileName = args.getDocument().getOriginalFileName().split("\\\\");
         System.out.println(MessageFormat.format("{0} Image #{1}", splitOriginalFileName[splitOriginalFileName.length - 1], ++mImageCount));

         LayoutCollector layoutCollector = new LayoutCollector(args.getDocument());

         System.out.println(MessageFormat.format("\tOn page:\t{0}", layoutCollector.getStartPageIndex(args.getCurrentShape())));
         System.out.println(MessageFormat.format("\tDimensions:\t{0}", args.getCurrentShape().getBounds().toString()));
         System.out.println(MessageFormat.format("\tAlignment:\t{0}", args.getCurrentShape().getVerticalAlignment()));
         System.out.println(MessageFormat.format("\tWrap type:\t{0}", args.getCurrentShape().getWrapType()));
         System.out.println(MessageFormat.format("Output filename:\t{0}\n", args.getImageFileName()));
     }

     private int mImageCount;
 }
 
```

**P:Aspose.Words.Saving.ImageSavingArgs.ImageStream**

**Returns:**
boolean - The corresponding  boolean  value.
### isImageAvailable() {#isImageAvailable}
```
public boolean isImageAvailable()
```


Returns  true  if the current image is available for export.

 **Remarks:** 

Some images in the document can be unavailable, for example, because the image is linked and the link is inaccessible or does not point to a valid image. In this case Aspose.Words exports an icon with a red cross. This property returns  true  if the original image is available; returns  false  if the original image is not available and a "no image" icon will be offered for save.

When saving a group shape or a shape that doesn't require any image this property is always  true .

 **Examples:** 

Shows how to involve an image saving callback in an HTML conversion process.

```

 public void imageSavingCallback() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     // When we save the document to HTML, we can pass a SaveOptions object to designate a callback
     // to customize the image saving process.
     HtmlSaveOptions options = new HtmlSaveOptions();
     options.setImageSavingCallback(new ImageShapePrinter());

     doc.save(getArtifactsDir() + "HtmlSaveOptions.ImageSavingCallback.html", options);
 }

 /// 
 /// Prints the properties of each image as the saving process saves it to an image file in the local file system
 /// during the exporting of a document to HTML.
 /// 
 private static class ImageShapePrinter implements IImageSavingCallback {
     public void imageSaving(ImageSavingArgs args) throws Exception {
         args.setKeepImageStreamOpen(false);
         Assert.assertTrue(args.isImageAvailable());

         String[] splitOriginalFileName = args.getDocument().getOriginalFileName().split("\\\\");
         System.out.println(MessageFormat.format("{0} Image #{1}", splitOriginalFileName[splitOriginalFileName.length - 1], ++mImageCount));

         LayoutCollector layoutCollector = new LayoutCollector(args.getDocument());

         System.out.println(MessageFormat.format("\tOn page:\t{0}", layoutCollector.getStartPageIndex(args.getCurrentShape())));
         System.out.println(MessageFormat.format("\tDimensions:\t{0}", args.getCurrentShape().getBounds().toString()));
         System.out.println(MessageFormat.format("\tAlignment:\t{0}", args.getCurrentShape().getVerticalAlignment()));
         System.out.println(MessageFormat.format("\tWrap type:\t{0}", args.getCurrentShape().getWrapType()));
         System.out.println(MessageFormat.format("Output filename:\t{0}\n", args.getImageFileName()));
     }

     private int mImageCount;
 }
 
```

**Returns:**
boolean -  true  if the current image is available for export.
### setImageFileName(String value) {#setImageFileName-java.lang.String}
```
public void setImageFileName(String value)
```


Sets the file name (without path) where the image will be saved to.

 **Remarks:** 

This property allows you to redefine how the image file names are generated during export to HTML.

When the event is fired, this property contains the file name that was generated by Aspose.Words. You can change the value of this property to save the image into a different file. Note that file names must be unique.

Aspose.Words automatically generates a unique file name for every embedded image when exporting to HTML format. How the image file name is generated depends on whether you save the document to a file or to a stream.

When saving a document to a file, the generated image file name looks like *.![Image 1][].*.

When saving a document to a stream, the generated image file name looks like *Aspose.Words..![Image 1][].*.

[getImageFileName()](../../com.aspose.words/imagesavingargs/\#getImageFileName) / [setImageFileName(java.lang.String)](../../com.aspose.words/imagesavingargs/\#setImageFileName-java.lang.String) must contain only the file name without the path. Aspose.Words determines the path for saving and the value of the  src  attribute for writing to HTML using the document file name, the [HtmlSaveOptions.getImagesFolder()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolder) / [HtmlSaveOptions.setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolder-java.lang.String) and [HtmlSaveOptions.getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolderAlias) / [HtmlSaveOptions.setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolderAlias-java.lang.String) properties.

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


[Image 1]: 

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The file name (without path) where the image will be saved to. |

### setImageStream(OutputStream value) {#setImageStream-java.io.OutputStream}
```
public void setImageStream(OutputStream value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.io.OutputStream |  |

### setKeepImageStreamOpen(boolean value) {#setKeepImageStreamOpen-boolean}
```
public void setKeepImageStreamOpen(boolean value)
```


Specifies whether Aspose.Words should keep the stream open or close it after saving an image.

 **Remarks:** 

Default is  false  and Aspose.Words will close the stream you provided in the **P:Aspose.Words.Saving.ImageSavingArgs.ImageStream** property after writing an image into it. Specify  true  to keep the stream open.

 **Examples:** 

Shows how to involve an image saving callback in an HTML conversion process.

```

 public void imageSavingCallback() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     // When we save the document to HTML, we can pass a SaveOptions object to designate a callback
     // to customize the image saving process.
     HtmlSaveOptions options = new HtmlSaveOptions();
     options.setImageSavingCallback(new ImageShapePrinter());

     doc.save(getArtifactsDir() + "HtmlSaveOptions.ImageSavingCallback.html", options);
 }

 /// 
 /// Prints the properties of each image as the saving process saves it to an image file in the local file system
 /// during the exporting of a document to HTML.
 /// 
 private static class ImageShapePrinter implements IImageSavingCallback {
     public void imageSaving(ImageSavingArgs args) throws Exception {
         args.setKeepImageStreamOpen(false);
         Assert.assertTrue(args.isImageAvailable());

         String[] splitOriginalFileName = args.getDocument().getOriginalFileName().split("\\\\");
         System.out.println(MessageFormat.format("{0} Image #{1}", splitOriginalFileName[splitOriginalFileName.length - 1], ++mImageCount));

         LayoutCollector layoutCollector = new LayoutCollector(args.getDocument());

         System.out.println(MessageFormat.format("\tOn page:\t{0}", layoutCollector.getStartPageIndex(args.getCurrentShape())));
         System.out.println(MessageFormat.format("\tDimensions:\t{0}", args.getCurrentShape().getBounds().toString()));
         System.out.println(MessageFormat.format("\tAlignment:\t{0}", args.getCurrentShape().getVerticalAlignment()));
         System.out.println(MessageFormat.format("\tWrap type:\t{0}", args.getCurrentShape().getWrapType()));
         System.out.println(MessageFormat.format("Output filename:\t{0}\n", args.getImageFileName()));
     }

     private int mImageCount;
 }
 
```

**P:Aspose.Words.Saving.ImageSavingArgs.ImageStream**

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

