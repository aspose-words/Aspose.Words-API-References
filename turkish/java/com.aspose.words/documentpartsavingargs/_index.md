---
title: "DocumentPartSavingArgs"
linktitle: "DocumentPartSavingArgs"
second_title: "Aspose.Words Java için"
description: "Java'da IDocumentPartSavingCallback.documentPartSavingcom.aspose.words.DocumentPartSavingArgs geri çağrısı için veri sağlar."
type: docs
weight: 167
url: /tr/java/com.aspose.words/documentpartsavingargs/
---

**Inheritance:**
java.lang.Object
```
public class DocumentPartSavingArgs
```

Bu [IDocumentPartSavingCallback.documentPartSaving(com.aspose.words.DocumentPartSavingArgs)](../../com.aspose.words/idocumentpartsavingcallback/\#documentPartSaving-com.aspose.words.DocumentPartSavingArgs) geri çağrısı için veri sağlar.

Daha fazla bilgi edinmek için [ Save a Document ][Save a Document] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

Aspose.Words bir belgeyi HTML veya ilgili formatlara kaydederken ve [HtmlSaveOptions.getDocumentSplitCriteria()](../../com.aspose.words/htmlsaveoptions/\#getDocumentSplitCriteria) / [HtmlSaveOptions.setDocumentSplitCriteria(int)](../../com.aspose.words/htmlsaveoptions/\#setDocumentSplitCriteria-int) belirtilmişse, belge parçalara bölünür ve varsayılan olarak, her belge parçası ayrı bir dosyaya kaydedilir.

Sınıf [DocumentPartSavingArgs](../../com.aspose.words/documentpartsavingargs/) size her belge parçasının nasıl kaydedileceğini kontrol etme imkanı sağlar. Dosya adlarının nasıl oluşturulacağını yeniden tanımlamanıza veya kendi akış nesnelerinizi sağlayarak belge parçalarının dosyalara kaydedilmesini tamamen atlamanıza olanak tanır.

Belge parçalarını dosyalar yerine akışlara kaydetmek için **P:Aspose.Words.Saving.DocumentPartSavingArgs.DocumentPartStream** özelliğini kullanın.

 **Examples:** 

Bir belgeyi parçalara bölüp kaydetmenin nasıl yapılacağını gösterir.

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
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getDocument()](#getDocument) | Kaydedilen belge nesnesini alır. |
| [getDocumentPartFileName()](#getDocumentPartFileName) | Belge parçasının kaydedileceği dosya adını (yol olmadan) alır. |
| [getDocumentPartStream()](#getDocumentPartStream) |  |
| [getKeepDocumentPartStreamOpen()](#getKeepDocumentPartStreamOpen) | Aspose.Words'un belge parçasını kaydettikten sonra akışı açık tutup tutmayacağını belirtir. |
| [setDocumentPartFileName(String value)](#setDocumentPartFileName-java.lang.String) | Belge parçasının kaydedileceği dosya adını (yol olmadan) ayarlar. |
| [setDocumentPartStream(OutputStream value)](#setDocumentPartStream-java.io.OutputStream) |  |
| [setKeepDocumentPartStreamOpen(boolean value)](#setKeepDocumentPartStreamOpen-boolean) | Aspose.Words'un belge parçasını kaydettikten sonra akışı açık tutup tutmayacağını belirtir. |
### getDocument() {#getDocument}
```
public Document getDocument()
```


Kaydedilen belge nesnesini alır.

 **Examples:** 

Bir belgeyi parçalara bölüp kaydetmenin nasıl yapılacağını gösterir.

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


Belge parçasının kaydedileceği dosya adını (yol olmadan) alır.

 **Remarks:** 

Bu özellik, belge parçası dosya adlarının HTML veya EPUB dışa aktarımı sırasında nasıl oluşturulacağını yeniden tanımlamanıza olanak tanır.

Geri arama tetiklendiğinde, bu özellik Aspose.Words tarafından oluşturulan dosya adını içerir. Bu özelliğin değerini değiştirerek belge parçasını farklı bir dosyaya kaydedebilirsiniz. Her parçanın dosya adının benzersiz olması gerektiğini unutmayın.

[getDocumentPartFileName()](../../com.aspose.words/documentpartsavingargs/\#getDocumentPartFileName) / [setDocumentPartFileName(java.lang.String)](../../com.aspose.words/documentpartsavingargs/\#setDocumentPartFileName-java.lang.String) must contain only the file name without the path. Aspose.Words determines the path for saving using the document file name. If output document file name was not specified, for instance when saving to a stream, this file name is used only for referencing document parts. The same is true when saving to EPUB format.

 **Examples:** 

Bir belgeyi parçalara bölüp kaydetmenin nasıl yapılacağını gösterir.

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
java.lang.String - Belge parçasının kaydedileceği dosya adı (yol olmadan).
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


Aspose.Words'un belge parçasını kaydettikten sonra akışı açık tutup tutmayacağını belirtir.

 **Remarks:** 

Varsayılan değer **false** olup, Aspose.Words **P:Aspose.Words.Saving.DocumentPartSavingArgs.DocumentPartStream** özelliğinde sağladığınız akışı, içine bir belge parçası yazdıktan sonra kapatır. Akışı açık tutmak için **true** belirtin. Lütfen **M:Aspose.Words.Document.Save(System.IO.Stream,Aspose.Words.SaveFormat)** veya **M:Aspose.Words.Document.Save(System.IO.Stream,Aspose.Words.Saving.SaveOptions)** çağrısında sağlanan ana çıktı akışının, [getKeepDocumentPartStreamOpen()](../../com.aspose.words/documentpartsavingargs/\#getKeepDocumentPartStreamOpen) / [setKeepDocumentPartStreamOpen(boolean)](../../com.aspose.words/documentpartsavingargs/\#setKeepDocumentPartStreamOpen-boolean) **false** olarak ayarlı olsa bile Aspose.Words tarafından asla kapatılmayacağını unutmayın.

 **Examples:** 

Bir belgeyi parçalara bölüp kaydetmenin nasıl yapılacağını gösterir.

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
boolean - İlgili  boolean  değeri.
### setDocumentPartFileName(String value) {#setDocumentPartFileName-java.lang.String}
```
public void setDocumentPartFileName(String value)
```


Belge parçasının kaydedileceği dosya adını (yol olmadan) ayarlar.

 **Remarks:** 

Bu özellik, belge parçası dosya adlarının HTML veya EPUB dışa aktarımı sırasında nasıl oluşturulacağını yeniden tanımlamanıza olanak tanır.

Geri arama tetiklendiğinde, bu özellik Aspose.Words tarafından oluşturulan dosya adını içerir. Bu özelliğin değerini değiştirerek belge parçasını farklı bir dosyaya kaydedebilirsiniz. Her parçanın dosya adının benzersiz olması gerektiğini unutmayın.

[getDocumentPartFileName()](../../com.aspose.words/documentpartsavingargs/\#getDocumentPartFileName) / [setDocumentPartFileName(java.lang.String)](../../com.aspose.words/documentpartsavingargs/\#setDocumentPartFileName-java.lang.String) must contain only the file name without the path. Aspose.Words determines the path for saving using the document file name. If output document file name was not specified, for instance when saving to a stream, this file name is used only for referencing document parts. The same is true when saving to EPUB format.

 **Examples:** 

Bir belgeyi parçalara bölüp kaydetmenin nasıl yapılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Belge parçasının kaydedileceği dosya adı (yol olmadan). |

### setDocumentPartStream(OutputStream value) {#setDocumentPartStream-java.io.OutputStream}
```
public void setDocumentPartStream(OutputStream value)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.io.OutputStream |  |

### setKeepDocumentPartStreamOpen(boolean value) {#setKeepDocumentPartStreamOpen-boolean}
```
public void setKeepDocumentPartStreamOpen(boolean value)
```


Aspose.Words'un belge parçasını kaydettikten sonra akışı açık tutup tutmayacağını belirtir.

 **Remarks:** 

Varsayılan değer **false** olup, Aspose.Words **P:Aspose.Words.Saving.DocumentPartSavingArgs.DocumentPartStream** özelliğinde sağladığınız akışı, içine bir belge parçası yazdıktan sonra kapatır. Akışı açık tutmak için **true** belirtin. Lütfen **M:Aspose.Words.Document.Save(System.IO.Stream,Aspose.Words.SaveFormat)** veya **M:Aspose.Words.Document.Save(System.IO.Stream,Aspose.Words.Saving.SaveOptions)** çağrısında sağlanan ana çıktı akışının, [getKeepDocumentPartStreamOpen()](../../com.aspose.words/documentpartsavingargs/\#getKeepDocumentPartStreamOpen) / [setKeepDocumentPartStreamOpen(boolean)](../../com.aspose.words/documentpartsavingargs/\#setKeepDocumentPartStreamOpen-boolean) **false** olarak ayarlı olsa bile Aspose.Words tarafından asla kapatılmayacağını unutmayın.

 **Examples:** 

Bir belgeyi parçalara bölüp kaydetmenin nasıl yapılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

