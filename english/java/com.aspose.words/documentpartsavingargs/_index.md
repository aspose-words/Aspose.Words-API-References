---
title: DocumentPartSavingArgs
linktitle: DocumentPartSavingArgs
second_title: Aspose.Words for Java
description: Provides data for the IDocumentPartSavingCallback.documentPartSavingcom.aspose.words.DocumentPartSavingArgs callback in Java.
type: docs
weight: 162
url: /java/com.aspose.words/documentpartsavingargs/
---

**Inheritance:**
java.lang.Object
```
public class DocumentPartSavingArgs
```

Provides data for the [IDocumentPartSavingCallback.documentPartSaving(com.aspose.words.DocumentPartSavingArgs)](../../com.aspose.words/idocumentpartsavingcallback/\#documentPartSaving-com.aspose.words.DocumentPartSavingArgs) callback.

To learn more, visit the [ Save a Document ][Save a Document] documentation article.

 **Remarks:** 

When Aspose.Words saves a document to HTML or related formats and [HtmlSaveOptions.getDocumentSplitCriteria()](../../com.aspose.words/htmlsaveoptions/\#getDocumentSplitCriteria) / [HtmlSaveOptions.setDocumentSplitCriteria(int)](../../com.aspose.words/htmlsaveoptions/\#setDocumentSplitCriteria-int) is specified, the document is split into parts and by default, each document part is saved into a separate file.

Class [DocumentPartSavingArgs](../../com.aspose.words/documentpartsavingargs/) allows you to control how each document part will be saved. It allows to redefine how file names are generated or to completely circumvent saving of document parts into files by providing your own stream objects.

To save document parts into streams instead of files, use the **P:Aspose.Words.Saving.DocumentPartSavingArgs.DocumentPartStream** property.

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
| [getDocument()](#getDocument) | Gets the document object that is being saved. |
| [getDocumentPartFileName()](#getDocumentPartFileName) | Gets the file name (without path) where the document part will be saved to. |
| [getDocumentPartStream()](#getDocumentPartStream) |  |
| [getKeepDocumentPartStreamOpen()](#getKeepDocumentPartStreamOpen) | Specifies whether Aspose.Words should keep the stream open or close it after saving a document part. |
| [setDocumentPartFileName(String value)](#setDocumentPartFileName-java.lang.String) | Sets the file name (without path) where the document part will be saved to. |
| [setDocumentPartStream(OutputStream value)](#setDocumentPartStream-java.io.OutputStream) |  |
| [setKeepDocumentPartStreamOpen(boolean value)](#setKeepDocumentPartStreamOpen-boolean) | Specifies whether Aspose.Words should keep the stream open or close it after saving a document part. |
### getDocument() {#getDocument}
```
public Document getDocument()
```


Gets the document object that is being saved.

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
[Document](../../com.aspose.words/document/) - The document object that is being saved.
### getDocumentPartFileName() {#getDocumentPartFileName}
```
public String getDocumentPartFileName()
```


Gets the file name (without path) where the document part will be saved to.

 **Remarks:** 

This property allows you to redefine how the document part file names are generated during export to HTML or EPUB.

When the callback is invoked, this property contains the file name that was generated by Aspose.Words. You can change the value of this property to save the document part into a different file. Note that the file name for each part must be unique.

[getDocumentPartFileName()](../../com.aspose.words/documentpartsavingargs/\#getDocumentPartFileName) / [setDocumentPartFileName(java.lang.String)](../../com.aspose.words/documentpartsavingargs/\#setDocumentPartFileName-java.lang.String) must contain only the file name without the path. Aspose.Words determines the path for saving using the document file name. If output document file name was not specified, for instance when saving to a stream, this file name is used only for referencing document parts. The same is true when saving to EPUB format.

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

**P:Aspose.Words.Saving.DocumentPartSavingArgs.DocumentPartStream**

**Returns:**
java.lang.String - The file name (without path) where the document part will be saved to.
### getDocumentPartStream() {#getDocumentPartStream}
```
public OutputStream getDocumentPartStream()
```




**Returns:**
java.io.OutputStream
### getKeepDocumentPartStreamOpen() {#getKeepDocumentPartStreamOpen}
```
public boolean getKeepDocumentPartStreamOpen()
```


Specifies whether Aspose.Words should keep the stream open or close it after saving a document part.

 **Remarks:** 

Default is  false  and Aspose.Words will close the stream you provided in the **P:Aspose.Words.Saving.DocumentPartSavingArgs.DocumentPartStream** property after writing a document part into it. Specify  true  to keep the stream open. Please note that the main output stream provided in the call to **M:Aspose.Words.Document.Save(System.IO.Stream,Aspose.Words.SaveFormat)** or **M:Aspose.Words.Document.Save(System.IO.Stream,Aspose.Words.Saving.SaveOptions)** will never be closed by Aspose.Words even if [getKeepDocumentPartStreamOpen()](../../com.aspose.words/documentpartsavingargs/\#getKeepDocumentPartStreamOpen) / [setKeepDocumentPartStreamOpen(boolean)](../../com.aspose.words/documentpartsavingargs/\#setKeepDocumentPartStreamOpen-boolean) is set to  false .

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

**P:Aspose.Words.Saving.DocumentPartSavingArgs.DocumentPartStream**

**Returns:**
boolean - The corresponding  boolean  value.
### setDocumentPartFileName(String value) {#setDocumentPartFileName-java.lang.String}
```
public void setDocumentPartFileName(String value)
```


Sets the file name (without path) where the document part will be saved to.

 **Remarks:** 

This property allows you to redefine how the document part file names are generated during export to HTML or EPUB.

When the callback is invoked, this property contains the file name that was generated by Aspose.Words. You can change the value of this property to save the document part into a different file. Note that the file name for each part must be unique.

[getDocumentPartFileName()](../../com.aspose.words/documentpartsavingargs/\#getDocumentPartFileName) / [setDocumentPartFileName(java.lang.String)](../../com.aspose.words/documentpartsavingargs/\#setDocumentPartFileName-java.lang.String) must contain only the file name without the path. Aspose.Words determines the path for saving using the document file name. If output document file name was not specified, for instance when saving to a stream, this file name is used only for referencing document parts. The same is true when saving to EPUB format.

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

**P:Aspose.Words.Saving.DocumentPartSavingArgs.DocumentPartStream**

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The file name (without path) where the document part will be saved to. |

### setDocumentPartStream(OutputStream value) {#setDocumentPartStream-java.io.OutputStream}
```
public void setDocumentPartStream(OutputStream value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.io.OutputStream |  |

### setKeepDocumentPartStreamOpen(boolean value) {#setKeepDocumentPartStreamOpen-boolean}
```
public void setKeepDocumentPartStreamOpen(boolean value)
```


Specifies whether Aspose.Words should keep the stream open or close it after saving a document part.

 **Remarks:** 

Default is  false  and Aspose.Words will close the stream you provided in the **P:Aspose.Words.Saving.DocumentPartSavingArgs.DocumentPartStream** property after writing a document part into it. Specify  true  to keep the stream open. Please note that the main output stream provided in the call to **M:Aspose.Words.Document.Save(System.IO.Stream,Aspose.Words.SaveFormat)** or **M:Aspose.Words.Document.Save(System.IO.Stream,Aspose.Words.Saving.SaveOptions)** will never be closed by Aspose.Words even if [getKeepDocumentPartStreamOpen()](../../com.aspose.words/documentpartsavingargs/\#getKeepDocumentPartStreamOpen) / [setKeepDocumentPartStreamOpen(boolean)](../../com.aspose.words/documentpartsavingargs/\#setKeepDocumentPartStreamOpen-boolean) is set to  false .

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

**P:Aspose.Words.Saving.DocumentPartSavingArgs.DocumentPartStream**

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

