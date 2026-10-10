---
title: "DocumentPartSavingArgs"
linktitle: "DocumentPartSavingArgs"
second_title: "Aspose.Words para Java"
description: "Proporciona datos para la devolución de llamada IDocumentPartSavingCallback.documentPartSavingcom.aspose.words.DocumentPartSavingArgs en Java."
type: docs
weight: 167
url: /es/java/com.aspose.words/documentpartsavingargs/
---

**Inheritance:**
java.lang.Object
```
public class DocumentPartSavingArgs
```

Proporciona datos para la devolución de llamada [IDocumentPartSavingCallback.documentPartSaving(com.aspose.words.DocumentPartSavingArgs)](../../com.aspose.words/idocumentpartsavingcallback/\#documentPartSaving-com.aspose.words.DocumentPartSavingArgs).

Para obtener más información, visite el artículo de documentación [ Save a Document ][Save a Document].

 **Remarks:** 

Cuando Aspose.Words guarda un documento en HTML o formatos relacionados y se especifica [HtmlSaveOptions.getDocumentSplitCriteria()](../../com.aspose.words/htmlsaveoptions/\#getDocumentSplitCriteria) / [HtmlSaveOptions.setDocumentSplitCriteria(int)](../../com.aspose.words/htmlsaveoptions/\#setDocumentSplitCriteria-int), el documento se divide en partes y, por defecto, cada parte del documento se guarda en un archivo separado.

La clase [DocumentPartSavingArgs](../../com.aspose.words/documentpartsavingargs/) permite controlar cómo se guardará cada parte del documento. Permite redefinir cómo se generan los nombres de archivo o evitar completamente el guardado de partes del documento en archivos proporcionando tus propios objetos de flujo.

Para guardar partes del documento en flujos en lugar de archivos, usa la propiedad **P:Aspose.Words.Saving.DocumentPartSavingArgs.DocumentPartStream**.

 **Examples:** 

Muestra cómo dividir un documento en partes y guardarlas.

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
## Métodos

| Método | Descripción |
| --- | --- |
| [getDocument()](#getDocument) | Obtiene el objeto de documento que se está guardando. |
| [getDocumentPartFileName()](#getDocumentPartFileName) | Obtiene el nombre de archivo (sin ruta) donde se guardará la parte del documento. |
| [getDocumentPartStream()](#getDocumentPartStream) |  |
| [getKeepDocumentPartStreamOpen()](#getKeepDocumentPartStreamOpen) | Especifica si Aspose.Words debe mantener el flujo abierto o cerrarlo después de guardar una parte del documento. |
| [setDocumentPartFileName(String value)](#setDocumentPartFileName-java.lang.String) | Establece el nombre de archivo (sin ruta) donde se guardará la parte del documento. |
| [setDocumentPartStream(OutputStream value)](#setDocumentPartStream-java.io.OutputStream) |  |
| [setKeepDocumentPartStreamOpen(boolean value)](#setKeepDocumentPartStreamOpen-boolean) | Especifica si Aspose.Words debe mantener el flujo abierto o cerrarlo después de guardar una parte del documento. |
### getDocument() {#getDocument}
```
public Document getDocument()
```


Obtiene el objeto de documento que se está guardando.

 **Examples:** 

Muestra cómo dividir un documento en partes y guardarlas.

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


Obtiene el nombre de archivo (sin ruta) donde se guardará la parte del documento.

 **Remarks:** 

Esta propiedad permite redefinir cómo se generan los nombres de archivo de las partes del documento durante la exportación a HTML o EPUB.

Cuando se invoca la devolución de llamada, esta propiedad contiene el nombre de archivo generado por Aspose.Words. Puedes cambiar el valor de esta propiedad para guardar la parte del documento en un archivo diferente. Ten en cuenta que el nombre de archivo para cada parte debe ser único.

[getDocumentPartFileName()](../../com.aspose.words/documentpartsavingargs/\#getDocumentPartFileName) / [setDocumentPartFileName(java.lang.String)](../../com.aspose.words/documentpartsavingargs/\#setDocumentPartFileName-java.lang.String) must contain only the file name without the path. Aspose.Words determines the path for saving using the document file name. If output document file name was not specified, for instance when saving to a stream, this file name is used only for referencing document parts. The same is true when saving to EPUB format.

 **Examples:** 

Muestra cómo dividir un documento en partes y guardarlas.

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
java.lang.String - El nombre de archivo (sin ruta) donde se guardará la parte del documento.
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


Especifica si Aspose.Words debe mantener el flujo abierto o cerrarlo después de guardar una parte del documento.

 **Remarks:** 

El valor predeterminado es  false  y Aspose.Words cerrará el flujo que proporcionaste en la propiedad **P:Aspose.Words.Saving.DocumentPartSavingArgs.DocumentPartStream** después de escribir una parte del documento en él. Especifica  true  para mantener el flujo abierto. Ten en cuenta que el flujo de salida principal proporcionado en la llamada a **M:Aspose.Words.Document.Save(System.IO.Stream,Aspose.Words.SaveFormat)** o **M:Aspose.Words.Document.Save(System.IO.Stream,Aspose.Words.Saving.SaveOptions)** nunca será cerrado por Aspose.Words incluso si [getKeepDocumentPartStreamOpen()](../../com.aspose.words/documentpartsavingargs/\#getKeepDocumentPartStreamOpen) / [setKeepDocumentPartStreamOpen(boolean)](../../com.aspose.words/documentpartsavingargs/\#setKeepDocumentPartStreamOpen-boolean) está configurado en  false .

 **Examples:** 

Muestra cómo dividir un documento en partes y guardarlas.

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
boolean - El valor  boolean  correspondiente.
### setDocumentPartFileName(String value) {#setDocumentPartFileName-java.lang.String}
```
public void setDocumentPartFileName(String value)
```


Establece el nombre de archivo (sin ruta) donde se guardará la parte del documento.

 **Remarks:** 

Esta propiedad permite redefinir cómo se generan los nombres de archivo de las partes del documento durante la exportación a HTML o EPUB.

Cuando se invoca la devolución de llamada, esta propiedad contiene el nombre de archivo generado por Aspose.Words. Puedes cambiar el valor de esta propiedad para guardar la parte del documento en un archivo diferente. Ten en cuenta que el nombre de archivo para cada parte debe ser único.

[getDocumentPartFileName()](../../com.aspose.words/documentpartsavingargs/\#getDocumentPartFileName) / [setDocumentPartFileName(java.lang.String)](../../com.aspose.words/documentpartsavingargs/\#setDocumentPartFileName-java.lang.String) must contain only the file name without the path. Aspose.Words determines the path for saving using the document file name. If output document file name was not specified, for instance when saving to a stream, this file name is used only for referencing document parts. The same is true when saving to EPUB format.

 **Examples:** 

Muestra cómo dividir un documento en partes y guardarlas.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | El nombre de archivo (sin ruta) donde se guardará la parte del documento. |

### setDocumentPartStream(OutputStream value) {#setDocumentPartStream-java.io.OutputStream}
```
public void setDocumentPartStream(OutputStream value)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.io.OutputStream |  |

### setKeepDocumentPartStreamOpen(boolean value) {#setKeepDocumentPartStreamOpen-boolean}
```
public void setKeepDocumentPartStreamOpen(boolean value)
```


Especifica si Aspose.Words debe mantener el flujo abierto o cerrarlo después de guardar una parte del documento.

 **Remarks:** 

El valor predeterminado es  false  y Aspose.Words cerrará el flujo que proporcionaste en la propiedad **P:Aspose.Words.Saving.DocumentPartSavingArgs.DocumentPartStream** después de escribir una parte del documento en él. Especifica  true  para mantener el flujo abierto. Ten en cuenta que el flujo de salida principal proporcionado en la llamada a **M:Aspose.Words.Document.Save(System.IO.Stream,Aspose.Words.SaveFormat)** o **M:Aspose.Words.Document.Save(System.IO.Stream,Aspose.Words.Saving.SaveOptions)** nunca será cerrado por Aspose.Words incluso si [getKeepDocumentPartStreamOpen()](../../com.aspose.words/documentpartsavingargs/\#getKeepDocumentPartStreamOpen) / [setKeepDocumentPartStreamOpen(boolean)](../../com.aspose.words/documentpartsavingargs/\#setKeepDocumentPartStreamOpen-boolean) está configurado en  false .

 **Examples:** 

Muestra cómo dividir un documento en partes y guardarlas.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

