---
title: "ImageSavingArgs"
linktitle: "ImageSavingArgs"
second_title: "Aspose.Words para Java"
description: "Proporciona datos para el evento IImageSavingCallback.imageSavingcom.aspose.words.ImageSavingArgs en Java."
type: docs
weight: 395
url: /es/java/com.aspose.words/imagesavingargs/
---

**Inheritance:**
java.lang.Object
```
public class ImageSavingArgs
```

Proporciona datos para el evento [IImageSavingCallback.imageSaving(com.aspose.words.ImageSavingArgs)](../../com.aspose.words/iimagesavingcallback/\#imageSaving-com.aspose.words.ImageSavingArgs).

Para obtener más información, visite el artículo de documentación [ Save a Document ][Save a Document].

 **Remarks:** 

Por defecto, cuando Aspose.Words guarda un documento en HTML, guarda cada imagen en un archivo separado. Aspose.Words utiliza el nombre del archivo del documento y un número único para generar un nombre de archivo único para cada imagen encontrada en el documento.

[ImageSavingArgs](../../com.aspose.words/imagesavingargs/) allows to redefine how image file names are generated or to completely circumvent saving of images into files by providing your own stream objects.

Para aplicar su propia lógica para generar nombres de archivo de imagen use las propiedades [getImageFileName()](../../com.aspose.words/imagesavingargs/\#getImageFileName) / [setImageFileName(java.lang.String)](../../com.aspose.words/imagesavingargs/\#setImageFileName-java.lang.String), [getCurrentShape()](../../com.aspose.words/imagesavingargs/\#getCurrentShape) y [isImageAvailable()](../../com.aspose.words/imagesavingargs/\#isImageAvailable).

Para guardar imágenes en flujos en lugar de archivos, use la propiedad **P:Aspose.Words.Saving.ImageSavingArgs.ImageStream**.

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
| [getCurrentShape()](#getCurrentShape) | Obtiene el objeto [ShapeBase](../../com.aspose.words/shapebase/) correspondiente a la forma o forma de grupo que está a punto de guardarse. |
| [getDocument()](#getDocument) | Obtiene el objeto documento que se está guardando actualmente. |
| [getImageFileName()](#getImageFileName) | Obtiene el nombre de archivo (sin ruta) donde se guardará la imagen. |
| [getImageStream()](#getImageStream) |  |
| [getKeepImageStreamOpen()](#getKeepImageStreamOpen) | Especifica si Aspose.Words debe mantener el flujo abierto o cerrarlo después de guardar una imagen. |
| [isImageAvailable()](#isImageAvailable) | Devuelve  true  si la imagen actual está disponible para exportar. |
| [setImageFileName(String value)](#setImageFileName-java.lang.String) | Establece el nombre de archivo (sin ruta) donde se guardará la imagen. |
| [setImageStream(OutputStream value)](#setImageStream-java.io.OutputStream) |  |
| [setKeepImageStreamOpen(boolean value)](#setKeepImageStreamOpen-boolean) | Especifica si Aspose.Words debe mantener el flujo abierto o cerrarlo después de guardar una imagen. |
### getCurrentShape() {#getCurrentShape}
```
public ShapeBase getCurrentShape()
```


Obtiene el objeto [ShapeBase](../../com.aspose.words/shapebase/) correspondiente a la forma o forma de grupo que está a punto de guardarse.

 **Remarks:** 

[IImageSavingCallback](../../com.aspose.words/iimagesavingcallback/) can be fired while saving either a shape or a group shape. That's why the property has [ShapeBase](../../com.aspose.words/shapebase/) type. You can check whether it's a group shape comparing [ShapeBase.getShapeType()](../../com.aspose.words/shapebase/\#getShapeType) with [ShapeType.GROUP](../../com.aspose.words/shapetype/\#GROUP) or by casting it to one of derived classes: [Shape](../../com.aspose.words/shape/) or [GroupShape](../../com.aspose.words/groupshape/).

Aspose.Words utiliza el nombre de archivo del documento y un número único para generar un nombre de archivo único para cada imagen encontrada en el documento. Puede usar la propiedad [getCurrentShape()](../../com.aspose.words/imagessavingargs/\#getCurrentShape) para generar un nombre de archivo "mejor" examinando propiedades de la forma como [ImageData.getTitle()](../../com.aspose.words/imagedata/\#getTitle) / [ImageData.setTitle(java.lang.String)](../../com.aspose.words/imagedata/\#setTitle-java.lang.String) (solo forma), [ImageData.getSourceFullName()](../../com.aspose.words/imagedata/\#getSourceFullName) / [ImageData.setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata/\#setSourceFullName-java.lang.String) (solo forma) y [ShapeBase.getName()](../../com.aspose.words/shapebase/\#getName) / [ShapeBase.setName(java.lang.String)](../../com.aspose.words/shapebase/\#setName-java.lang.String). Por supuesto, puede construir nombres de archivo usando cualquier otra propiedad o criterio, pero tenga en cuenta que los nombres de archivo subsidiarios deben ser únicos dentro de la operación de exportación.

Algunas imágenes en el documento pueden no estar disponibles. Para comprobar la disponibilidad de la imagen, use la propiedad [isImageAvailable()](../../com.aspose.words/imagesavingargs/\#isImageAvailable).

 **Examples:** 

Muestra cómo involucrar una devolución de llamada de guardado de imagen en un proceso de conversión a HTML.

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


Obtiene el objeto documento que se está guardando actualmente.

 **Examples:** 

Muestra cómo involucrar una devolución de llamada de guardado de imagen en un proceso de conversión a HTML.

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


Obtiene el nombre de archivo (sin ruta) donde se guardará la imagen.

 **Remarks:** 

Esta propiedad le permite redefinir cómo se generan los nombres de archivo de imagen durante la exportación a HTML.

Cuando se dispara el evento, esta propiedad contiene el nombre de archivo que fue generado por Aspose.Words. Puede cambiar el valor de esta propiedad para guardar la imagen en un archivo diferente. Tenga en cuenta que los nombres de archivo deben ser únicos.

Aspose.Words genera automáticamente un nombre de archivo único para cada imagen incrustada al exportar al formato HTML. Cómo se genera el nombre de archivo de la imagen depende de si guarda el documento en un archivo o en un flujo.

Al guardar un documento en un archivo, el nombre de archivo de imagen generado se ve como *.![Image 1][].*.

Al guardar un documento en un flujo, el nombre de archivo de imagen generado se ve como *Aspose.Words..![Image 1][].*.

[getImageFileName()](../../com.aspose.words/imagesavingargs/\#getImageFileName) / [setImageFileName(java.lang.String)](../../com.aspose.words/imagesavingargs/\#setImageFileName-java.lang.String) must contain only the file name without the path. Aspose.Words determines the path for saving and the value of the  src  attribute for writing to HTML using the document file name, the [HtmlSaveOptions.getImagesFolder()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolder) / [HtmlSaveOptions.setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolder-java.lang.String) and [HtmlSaveOptions.getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolderAlias) / [HtmlSaveOptions.setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolderAlias-java.lang.String) properties.

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


[Image 1]: 

**Returns:**
java.lang.String - El nombre de archivo (sin ruta) donde se guardará la imagen.
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


Especifica si Aspose.Words debe mantener el flujo abierto o cerrarlo después de guardar una imagen.

 **Remarks:** 

El valor predeterminado es  false  y Aspose.Words cerrará el flujo que proporcionó en la propiedad **P:Aspose.Words.Saving.ImageSavingArgs.ImageStream** después de escribir una imagen en él. Especifique  true  para mantener el flujo abierto.

 **Examples:** 

Muestra cómo involucrar una devolución de llamada de guardado de imagen en un proceso de conversión a HTML.

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
boolean - El valor  boolean  correspondiente.
### isImageAvailable() {#isImageAvailable}
```
public boolean isImageAvailable()
```


Devuelve  true  si la imagen actual está disponible para exportar.

 **Remarks:** 

Algunas imágenes en el documento pueden no estar disponibles, por ejemplo, porque la imagen está vinculada y el enlace es inaccesible o no apunta a una imagen válida. En este caso, Aspose.Words exporta un ícono con una cruz roja. Esta propiedad devuelve  true  si la imagen original está disponible; devuelve  false  si la imagen original no está disponible y se ofrecerá un ícono de "no image" para guardar.

Al guardar una forma de grupo o una forma que no requiere ninguna imagen, esta propiedad siempre es  true .

 **Examples:** 

Muestra cómo involucrar una devolución de llamada de guardado de imagen en un proceso de conversión a HTML.

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
boolean -  true  si la imagen actual está disponible para exportar.
### setImageFileName(String value) {#setImageFileName-java.lang.String}
```
public void setImageFileName(String value)
```


Establece el nombre de archivo (sin ruta) donde se guardará la imagen.

 **Remarks:** 

Esta propiedad le permite redefinir cómo se generan los nombres de archivo de imagen durante la exportación a HTML.

Cuando se dispara el evento, esta propiedad contiene el nombre de archivo que fue generado por Aspose.Words. Puede cambiar el valor de esta propiedad para guardar la imagen en un archivo diferente. Tenga en cuenta que los nombres de archivo deben ser únicos.

Aspose.Words genera automáticamente un nombre de archivo único para cada imagen incrustada al exportar al formato HTML. Cómo se genera el nombre de archivo de la imagen depende de si guarda el documento en un archivo o en un flujo.

Al guardar un documento en un archivo, el nombre de archivo de imagen generado se ve como *.![Image 1][].*.

Al guardar un documento en un flujo, el nombre de archivo de imagen generado se ve como *Aspose.Words..![Image 1][].*.

[getImageFileName()](../../com.aspose.words/imagesavingargs/\#getImageFileName) / [setImageFileName(java.lang.String)](../../com.aspose.words/imagesavingargs/\#setImageFileName-java.lang.String) must contain only the file name without the path. Aspose.Words determines the path for saving and the value of the  src  attribute for writing to HTML using the document file name, the [HtmlSaveOptions.getImagesFolder()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolder) / [HtmlSaveOptions.setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolder-java.lang.String) and [HtmlSaveOptions.getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolderAlias) / [HtmlSaveOptions.setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolderAlias-java.lang.String) properties.

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


[Image 1]: 

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | El nombre de archivo (sin ruta) donde se guardará la imagen. |

### setImageStream(OutputStream value) {#setImageStream-java.io.OutputStream}
```
public void setImageStream(OutputStream value)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.io.OutputStream |  |

### setKeepImageStreamOpen(boolean value) {#setKeepImageStreamOpen-boolean}
```
public void setKeepImageStreamOpen(boolean value)
```


Especifica si Aspose.Words debe mantener el flujo abierto o cerrarlo después de guardar una imagen.

 **Remarks:** 

El valor predeterminado es  false  y Aspose.Words cerrará el flujo que proporcionó en la propiedad **P:Aspose.Words.Saving.ImageSavingArgs.ImageStream** después de escribir una imagen en él. Especifique  true  para mantener el flujo abierto.

 **Examples:** 

Muestra cómo involucrar una devolución de llamada de guardado de imagen en un proceso de conversión a HTML.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

