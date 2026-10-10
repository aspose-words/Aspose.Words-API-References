---
title: "ImageSavingArgs"
linktitle: "ImageSavingArgs"
second_title: "Aspose.Words per Java"
description: "Fornisce i dati per l'evento IImageSavingCallback.imageSavingcom.aspose.words.ImageSavingArgs in Java."
type: docs
weight: 395
url: /it/java/com.aspose.words/imagesavingargs/
---

**Inheritance:**
java.lang.Object
```
public class ImageSavingArgs
```

Fornisce i dati per l'evento [IImageSavingCallback.imageSaving(com.aspose.words.ImageSavingArgs)](../../com.aspose.words/iimagesavingcallback/\#imageSaving-com.aspose.words.ImageSavingArgs).

Per saperne di più, visita l'articolo di documentazione [ Save a Document ][Save a Document].

 **Remarks:** 

Per impostazione predefinita, quando Aspose.Words salva un documento in HTML, salva ogni immagine in un file separato. Aspose.Words utilizza il nome del file del documento e un numero univoco per generare un nome file unico per ogni immagine trovata nel documento.

[ImageSavingArgs](../../com.aspose.words/imagesavingargs/) allows to redefine how image file names are generated or to completely circumvent saving of images into files by providing your own stream objects.

Per applicare la tua logica per generare i nomi dei file immagine usa le proprietà [getImageFileName()](../../com.aspose.words/imagesavingargs/\#getImageFileName) / [setImageFileName(java.lang.String)](../../com.aspose.words/imagesavingargs/\#setImageFileName-java.lang.String), [getCurrentShape()](../../com.aspose.words/imagesavingargs/\#getCurrentShape) e [isImageAvailable()](../../com.aspose.words/imagesavingargs/\#isImageAvailable).

Per salvare le immagini in stream invece che in file, usa la proprietà **P:Aspose.Words.Saving.ImageSavingArgs.ImageStream**.

 **Examples:** 

Mostra come suddividere un documento in parti e salvarle.

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
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getCurrentShape()](#getCurrentShape) | Ottiene l'oggetto [ShapeBase](../../com.aspose.words/shapebase/) corrispondente alla forma o al gruppo di forme che sta per essere salvato. |
| [getDocument()](#getDocument) | Ottiene l'oggetto documento che è attualmente in fase di salvataggio. |
| [getImageFileName()](#getImageFileName) | Ottiene il nome del file (senza percorso) in cui l'immagine verrà salvata. |
| [getImageStream()](#getImageStream) |  |
| [getKeepImageStreamOpen()](#getKeepImageStreamOpen) | Specifica se Aspose.Words deve mantenere lo stream aperto o chiuderlo dopo il salvataggio di un'immagine. |
| [isImageAvailable()](#isImageAvailable) | Restituisce  true  se l'immagine corrente è disponibile per l'esportazione. |
| [setImageFileName(String value)](#setImageFileName-java.lang.String) | Imposta il nome del file (senza percorso) in cui l'immagine verrà salvata. |
| [setImageStream(OutputStream value)](#setImageStream-java.io.OutputStream) |  |
| [setKeepImageStreamOpen(boolean value)](#setKeepImageStreamOpen-boolean) | Specifica se Aspose.Words deve mantenere lo stream aperto o chiuderlo dopo il salvataggio di un'immagine. |
### getCurrentShape() {#getCurrentShape}
```
public ShapeBase getCurrentShape()
```


Ottiene l'oggetto [ShapeBase](../../com.aspose.words/shapebase/) corrispondente alla forma o al gruppo di forme che sta per essere salvato.

 **Remarks:** 

[IImageSavingCallback](../../com.aspose.words/iimagesavingcallback/) can be fired while saving either a shape or a group shape. That's why the property has [ShapeBase](../../com.aspose.words/shapebase/) type. You can check whether it's a group shape comparing [ShapeBase.getShapeType()](../../com.aspose.words/shapebase/\#getShapeType) with [ShapeType.GROUP](../../com.aspose.words/shapetype/\#GROUP) or by casting it to one of derived classes: [Shape](../../com.aspose.words/shape/) or [GroupShape](../../com.aspose.words/groupshape/).

Aspose.Words utilizza il nome del file del documento e un numero univoco per generare un nome file unico per ogni immagine trovata nel documento. Puoi usare la proprietà [getCurrentShape()](../../com.aspose.words/imagesavingargs/\#getCurrentShape) per generare un nome file \"migliore\" esaminando le proprietà della forma come [ImageData.getTitle()](../../com.aspose.words/imagedata/\#getTitle) / [ImageData.setTitle(java.lang.String)](../../com.aspose.words/imagedata/\#setTitle-java.lang.String) (solo Shape), [ImageData.getSourceFullName()](../../com.aspose.words/imagedata/\#getSourceFullName) / [ImageData.setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata/\#setSourceFullName-java.lang.String) (solo Shape) e [ShapeBase.getName()](../../com.aspose.words/shapebase/\#getName) / [ShapeBase.setName(java.lang.String)](../../com.aspose.words/shapebase/\#setName-java.lang.String). Naturalmente puoi costruire i nomi dei file usando qualsiasi altra proprietà o criterio, ma nota che i nomi dei file secondari devono essere unici all'interno dell'operazione di esportazione.

Alcune immagini nel documento possono non essere disponibili. Per verificare la disponibilità dell'immagine usa la proprietà [isImageAvailable()](../../com.aspose.words/imagesavingargs/\#isImageAvailable).

 **Examples:** 

Mostra come coinvolgere un callback di salvataggio immagine in un processo di conversione HTML.

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


Ottiene l'oggetto documento che è attualmente in fase di salvataggio.

 **Examples:** 

Mostra come coinvolgere un callback di salvataggio immagine in un processo di conversione HTML.

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


Ottiene il nome del file (senza percorso) in cui l'immagine verrà salvata.

 **Remarks:** 

Questa proprietà ti consente di ridefinire come vengono generati i nomi dei file immagine durante l'esportazione in HTML.

Quando l'evento viene attivato, questa proprietà contiene il nome del file generato da Aspose.Words. Puoi modificare il valore di questa proprietà per salvare l'immagine in un file diverso. Nota che i nomi dei file devono essere unici.

Aspose.Words genera automaticamente un nome file unico per ogni immagine incorporata quando esporta in formato HTML. Il modo in cui il nome del file immagine viene generato dipende dal fatto che tu salvi il documento su un file o su uno stream.

Quando si salva un documento su un file, il nome del file immagine generato appare così *.![Image 1][].*.

Quando si salva un documento su uno stream, il nome del file immagine generato appare così *Aspose.Words..![Image 1][].*.

[getImageFileName()](../../com.aspose.words/imagesavingargs/\#getImageFileName) / [setImageFileName(java.lang.String)](../../com.aspose.words/imagesavingargs/\#setImageFileName-java.lang.String) must contain only the file name without the path. Aspose.Words determines the path for saving and the value of the  src  attribute for writing to HTML using the document file name, the [HtmlSaveOptions.getImagesFolder()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolder) / [HtmlSaveOptions.setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolder-java.lang.String) and [HtmlSaveOptions.getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolderAlias) / [HtmlSaveOptions.setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolderAlias-java.lang.String) properties.

 **Examples:** 

Mostra come suddividere un documento in parti e salvarle.

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
java.lang.String - Il nome del file (senza percorso) in cui l'immagine verrà salvata.
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


Specifica se Aspose.Words deve mantenere lo stream aperto o chiuderlo dopo il salvataggio di un'immagine.

 **Remarks:** 

Il valore predefinito è  false  e Aspose.Words chiuderà lo stream fornito nella proprietà **P:Aspose.Words.Saving.ImageSavingArgs.ImageStream** dopo aver scritto un'immagine. Specifica  true  per mantenere lo stream aperto.

 **Examples:** 

Mostra come coinvolgere un callback di salvataggio immagine in un processo di conversione HTML.

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
boolean - Il valore booleano corrispondente.
### isImageAvailable() {#isImageAvailable}
```
public boolean isImageAvailable()
```


Restituisce  true  se l'immagine corrente è disponibile per l'esportazione.

 **Remarks:** 

Alcune immagini nel documento possono non essere disponibili, ad esempio perché l'immagine è collegata e il collegamento è inaccessibile o non punta a un'immagine valida. In questo caso Aspose.Words esporta un'icona con una croce rossa. Questa proprietà restituisce  true  se l'immagine originale è disponibile; restituisce  false  se l'immagine originale non è disponibile e verrà offerta un'icona \"nessuna immagine\" per il salvataggio.

Quando si salva un gruppo di forme o una forma che non richiede alcuna immagine, questa proprietà è sempre  true .

 **Examples:** 

Mostra come coinvolgere un callback di salvataggio immagine in un processo di conversione HTML.

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
boolean -  true  se l'immagine corrente è disponibile per l'esportazione.
### setImageFileName(String value) {#setImageFileName-java.lang.String}
```
public void setImageFileName(String value)
```


Imposta il nome del file (senza percorso) in cui l'immagine verrà salvata.

 **Remarks:** 

Questa proprietà ti consente di ridefinire come vengono generati i nomi dei file immagine durante l'esportazione in HTML.

Quando l'evento viene attivato, questa proprietà contiene il nome del file generato da Aspose.Words. Puoi modificare il valore di questa proprietà per salvare l'immagine in un file diverso. Nota che i nomi dei file devono essere unici.

Aspose.Words genera automaticamente un nome file unico per ogni immagine incorporata quando esporta in formato HTML. Il modo in cui il nome del file immagine viene generato dipende dal fatto che tu salvi il documento su un file o su uno stream.

Quando si salva un documento su un file, il nome del file immagine generato appare così *.![Image 1][].*.

Quando si salva un documento su uno stream, il nome del file immagine generato appare così *Aspose.Words..![Image 1][].*.

[getImageFileName()](../../com.aspose.words/imagesavingargs/\#getImageFileName) / [setImageFileName(java.lang.String)](../../com.aspose.words/imagesavingargs/\#setImageFileName-java.lang.String) must contain only the file name without the path. Aspose.Words determines the path for saving and the value of the  src  attribute for writing to HTML using the document file name, the [HtmlSaveOptions.getImagesFolder()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolder) / [HtmlSaveOptions.setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolder-java.lang.String) and [HtmlSaveOptions.getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolderAlias) / [HtmlSaveOptions.setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolderAlias-java.lang.String) properties.

 **Examples:** 

Mostra come suddividere un documento in parti e salvarle.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Il nome del file (senza percorso) in cui l'immagine verrà salvata. |

### setImageStream(OutputStream value) {#setImageStream-java.io.OutputStream}
```
public void setImageStream(OutputStream value)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.io.OutputStream |  |

### setKeepImageStreamOpen(boolean value) {#setKeepImageStreamOpen-boolean}
```
public void setKeepImageStreamOpen(boolean value)
```


Specifica se Aspose.Words deve mantenere lo stream aperto o chiuderlo dopo il salvataggio di un'immagine.

 **Remarks:** 

Il valore predefinito è  false  e Aspose.Words chiuderà lo stream fornito nella proprietà **P:Aspose.Words.Saving.ImageSavingArgs.ImageStream** dopo aver scritto un'immagine. Specifica  true  per mantenere lo stream aperto.

 **Examples:** 

Mostra come coinvolgere un callback di salvataggio immagine in un processo di conversione HTML.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

