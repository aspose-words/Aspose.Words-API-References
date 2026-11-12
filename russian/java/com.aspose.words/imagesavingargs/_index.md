---
title: "ImageSavingArgs"
linktitle: "ImageSavingArgs"
second_title: "Aspose.Words для Java"
description: "Предоставляет данные для события IImageSavingCallback.imageSavingcom.aspose.words.ImageSavingArgs в Java."
type: docs
weight: 395
url: /ru/java/com.aspose.words/imagesavingargs/
---

**Inheritance:**
java.lang.Object
```
public class ImageSavingArgs
```

Предоставляет данные для события [IImageSavingCallback.imageSaving(com.aspose.words.ImageSavingArgs)](../../com.aspose.words/iimagesavingcallback/\#imageSaving-com.aspose.words.ImageSavingArgs).

Чтобы узнать больше, посетите статью документации [ Save a Document ][Save a Document].

 **Remarks:** 

По умолчанию, когда Aspose.Words сохраняет документ в HTML, он сохраняет каждое изображение в отдельный файл. Aspose.Words использует имя файла документа и уникальный номер для генерации уникального имени файла для каждого изображения, найденного в документе.

[ImageSavingArgs](../../com.aspose.words/imagesavingargs/) allows to redefine how image file names are generated or to completely circumvent saving of images into files by providing your own stream objects.

Чтобы применить собственную логику генерации имён файлов изображений, используйте свойства [getImageFileName()](../../com.aspose.words/imagesavingargs/\#getImageFileName) / [setImageFileName(java.lang.String)](../../com.aspose.words/imagesavingargs/\#setImageFileName-java.lang.String), [getCurrentShape()](../../com.aspose.words/imagesavingargs/\#getCurrentShape) и [isImageAvailable()](../../com.aspose.words/imagesavingargs/\#isImageAvailable).

Чтобы сохранять изображения в потоки вместо файлов, используйте свойство **P:Aspose.Words.Saving.ImageSavingArgs.ImageStream**.

 **Examples:** 

Показывает, как разбить документ на части и сохранить их.

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
## Методы

| Метод | Описание |
| --- | --- |
| [getCurrentShape()](#getCurrentShape) | Получает объект [ShapeBase](../../com.aspose.words/shapebase/), соответствующий фигуре или группе фигур, которые собираются быть сохранёнными. |
| [getDocument()](#getDocument) | Получает объект документа, который в данный момент сохраняется. |
| [getImageFileName()](#getImageFileName) | Получает имя файла (без пути), в который будет сохранено изображение. |
| [getImageStream()](#getImageStream) |  |
| [getKeepImageStreamOpen()](#getKeepImageStreamOpen) | Указывает, должен ли Aspose.Words оставлять поток открытым или закрывать его после сохранения изображения. |
| [isImageAvailable()](#isImageAvailable) | Возвращает  true  если текущее изображение доступно для экспорта. |
| [setImageFileName(String value)](#setImageFileName-java.lang.String) | Устанавливает имя файла (без пути), в который будет сохранено изображение. |
| [setImageStream(OutputStream value)](#setImageStream-java.io.OutputStream) |  |
| [setKeepImageStreamOpen(boolean value)](#setKeepImageStreamOpen-boolean) | Указывает, должен ли Aspose.Words оставлять поток открытым или закрывать его после сохранения изображения. |
### getCurrentShape() {#getCurrentShape}
```
public ShapeBase getCurrentShape()
```


Получает объект [ShapeBase](../../com.aspose.words/shapebase/), соответствующий фигуре или группе фигур, которые собираются быть сохранёнными.

 **Remarks:** 

[IImageSavingCallback](../../com.aspose.words/iimagesavingcallback/) can be fired while saving either a shape or a group shape. That's why the property has [ShapeBase](../../com.aspose.words/shapebase/) type. You can check whether it's a group shape comparing [ShapeBase.getShapeType()](../../com.aspose.words/shapebase/\#getShapeType) with [ShapeType.GROUP](../../com.aspose.words/shapetype/\#GROUP) or by casting it to one of derived classes: [Shape](../../com.aspose.words/shape/) or [GroupShape](../../com.aspose.words/groupshape/).

Aspose.Words использует имя файла документа и уникальный номер для генерации уникального имени файла для каждого изображения, найденного в документе. Вы можете использовать свойство [getCurrentShape()](../../com.aspose.words/imagesavingargs/\#getCurrentShape) для создания "better" имени файла, изучая свойства фигуры, такие как [ImageData.getTitle()](../../com.aspose.words/imagedata/\#getTitle) / [ImageData.setTitle(java.lang.String)](../../com.aspose.words/imagedata/\#setTitle-java.lang.String)(только для Shape), [ImageData.getSourceFullName()](../../com.aspose.words/imagedata/\#getSourceFullName) / [ImageData.setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata/\#setSourceFullName-java.lang.String)(только для Shape) и [ShapeBase.getName()](../../com.aspose.words/shapebase/\#getName) / [ShapeBase.setName(java.lang.String)](../../com.aspose.words/shapebase/\#setName-java.lang.String). Конечно, вы можете формировать имена файлов, используя любые другие свойства или критерии, но учитывайте, что дочерние имена файлов должны быть уникальными в рамках операции экспорта.

Некоторые изображения в документе могут быть недоступны. Чтобы проверить доступность изображения, используйте свойство [isImageAvailable()](../../com.aspose.words/imagesavingargs/\#isImageAvailable).

 **Examples:** 

Показывает, как задействовать обратный вызов сохранения изображения в процессе конвертации в HTML.

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


Получает объект документа, который в данный момент сохраняется.

 **Examples:** 

Показывает, как задействовать обратный вызов сохранения изображения в процессе конвертации в HTML.

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


Получает имя файла (без пути), в который будет сохранено изображение.

 **Remarks:** 

Это свойство позволяет переопределить способ генерации имён файлов изображений при экспорте в HTML.

Когда событие срабатывает, это свойство содержит имя файла, сгенерированное Aspose.Words. Вы можете изменить значение этого свойства, чтобы сохранить изображение в другой файл. Обратите внимание, что имена файлов должны быть уникальными.

Aspose.Words автоматически генерирует уникальное имя файла для каждого встроенного изображения при экспорте в формат HTML. Способ генерации имени файла изображения зависит от того, сохраняете ли вы документ в файл или в поток.

При сохранении документа в файл сгенерированное имя файла изображения выглядит как *.![Image 1][].*.

При сохранении документа в поток сгенерированное имя файла изображения выглядит как *Aspose.Words..![Image 1][].*.

[getImageFileName()](../../com.aspose.words/imagesavingargs/\#getImageFileName) / [setImageFileName(java.lang.String)](../../com.aspose.words/imagesavingargs/\#setImageFileName-java.lang.String) must contain only the file name without the path. Aspose.Words determines the path for saving and the value of the  src  attribute for writing to HTML using the document file name, the [HtmlSaveOptions.getImagesFolder()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolder) / [HtmlSaveOptions.setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolder-java.lang.String) and [HtmlSaveOptions.getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolderAlias) / [HtmlSaveOptions.setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolderAlias-java.lang.String) properties.

 **Examples:** 

Показывает, как разбить документ на части и сохранить их.

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
java.lang.String — имя файла (без пути), в который будет сохранено изображение.
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


Указывает, должен ли Aspose.Words оставлять поток открытым или закрывать его после сохранения изображения.

 **Remarks:** 

По умолчанию  false , и Aspose.Words закроет поток, указанный в свойстве **P:Aspose.Words.Saving.ImageSavingArgs.ImageStream**, после записи в него изображения. Укажите  true , чтобы оставить поток открытым.

 **Examples:** 

Показывает, как задействовать обратный вызов сохранения изображения в процессе конвертации в HTML.

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
boolean - Соответствующее  boolean  значение.
### isImageAvailable() {#isImageAvailable}
```
public boolean isImageAvailable()
```


Возвращает  true  если текущее изображение доступно для экспорта.

 **Remarks:** 

Некоторые изображения в документе могут быть недоступны, например, потому что изображение связано и ссылка недоступна или не указывает на действительное изображение. В этом случае Aspose.Words экспортирует значок с красным крестом. Это свойство возвращает  true , если оригинальное изображение доступно; возвращает  false , если оригинальное изображение недоступно и будет предложен значок "no image" для сохранения.

При сохранении групповой фигуры или фигуры, не требующей изображения, это свойство всегда равно  true .

 **Examples:** 

Показывает, как задействовать обратный вызов сохранения изображения в процессе конвертации в HTML.

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
boolean —  true , если текущее изображение доступно для экспорта.
### setImageFileName(String value) {#setImageFileName-java.lang.String}
```
public void setImageFileName(String value)
```


Устанавливает имя файла (без пути), в который будет сохранено изображение.

 **Remarks:** 

Это свойство позволяет переопределить способ генерации имён файлов изображений при экспорте в HTML.

Когда событие срабатывает, это свойство содержит имя файла, сгенерированное Aspose.Words. Вы можете изменить значение этого свойства, чтобы сохранить изображение в другой файл. Обратите внимание, что имена файлов должны быть уникальными.

Aspose.Words автоматически генерирует уникальное имя файла для каждого встроенного изображения при экспорте в формат HTML. Способ генерации имени файла изображения зависит от того, сохраняете ли вы документ в файл или в поток.

При сохранении документа в файл сгенерированное имя файла изображения выглядит как *.![Image 1][].*.

При сохранении документа в поток сгенерированное имя файла изображения выглядит как *Aspose.Words..![Image 1][].*.

[getImageFileName()](../../com.aspose.words/imagesavingargs/\#getImageFileName) / [setImageFileName(java.lang.String)](../../com.aspose.words/imagesavingargs/\#setImageFileName-java.lang.String) must contain only the file name without the path. Aspose.Words determines the path for saving and the value of the  src  attribute for writing to HTML using the document file name, the [HtmlSaveOptions.getImagesFolder()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolder) / [HtmlSaveOptions.setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolder-java.lang.String) and [HtmlSaveOptions.getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolderAlias) / [HtmlSaveOptions.setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolderAlias-java.lang.String) properties.

 **Examples:** 

Показывает, как разбить документ на части и сохранить их.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Имя файла (без пути), в который будет сохранено изображение. |

### setImageStream(OutputStream value) {#setImageStream-java.io.OutputStream}
```
public void setImageStream(OutputStream value)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.io.OutputStream |  |

### setKeepImageStreamOpen(boolean value) {#setKeepImageStreamOpen-boolean}
```
public void setKeepImageStreamOpen(boolean value)
```


Указывает, должен ли Aspose.Words оставлять поток открытым или закрывать его после сохранения изображения.

 **Remarks:** 

По умолчанию  false , и Aspose.Words закроет поток, указанный в свойстве **P:Aspose.Words.Saving.ImageSavingArgs.ImageStream**, после записи в него изображения. Укажите  true , чтобы оставить поток открытым.

 **Examples:** 

Показывает, как задействовать обратный вызов сохранения изображения в процессе конвертации в HTML.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

