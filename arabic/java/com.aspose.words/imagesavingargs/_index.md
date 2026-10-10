---
title: "ImageSavingArgs"
linktitle: "ImageSavingArgs"
second_title: "Aspose.Words لـ Java"
description: "يوفر البيانات لحدث IImageSavingCallback.imageSavingcom.aspose.words.ImageSavingArgs في Java."
type: docs
weight: 395
url: /ar/java/com.aspose.words/imagesavingargs/
---

**Inheritance:**
java.lang.Object
```
public class ImageSavingArgs
```

يوفر البيانات لحدث [IImageSavingCallback.imageSaving(com.aspose.words.ImageSavingArgs)](../../com.aspose.words/iimagesavingcallback/\#imageSaving-com.aspose.words.ImageSavingArgs).

للتعرف على المزيد، زر [ Save a Document ][Save a Document] مقالة الوثائق.

 **Remarks:** 

بشكل افتراضي، عندما يقوم Aspose.Words بحفظ مستند إلى HTML، يحفظ كل صورة في ملف منفصل. يستخدم Aspose.Words اسم ملف المستند ورقمًا فريدًا لإنشاء اسم ملف فريد لكل صورة موجودة في المستند.

[ImageSavingArgs](../../com.aspose.words/imagesavingargs/) allows to redefine how image file names are generated or to completely circumvent saving of images into files by providing your own stream objects.

لتطبيق المنطق الخاص بك لتوليد أسماء ملفات الصور استخدم [getImageFileName()](../../com.aspose.words/imagesavingargs/#getImageFileName) / [setImageFileName(java.lang.String)](../../com.aspose.words/imagesavingargs/#setImageFileName-java.lang.String)، [getCurrentShape()](../../com.aspose.words/imagesavingargs/#getCurrentShape) و [isImageAvailable()](../../com.aspose.words/imagesavingargs/#isImageAvailable) الخصائص.

لحفظ الصور في تدفقات بدلاً من الملفات، استخدم الخاصية **P:Aspose.Words.Saving.ImageSavingArgs.ImageStream**.

 **Examples:** 

يوضح كيفية تقسيم المستند إلى أجزاء وحفظها.

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
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getCurrentShape()](#getCurrentShape) | يحصل على كائن [ShapeBase](../../com.aspose.words/shapebase/) المقابل للشكل أو مجموعة الأشكال التي ستُحفظ. |
| [getDocument()](#getDocument) | يحصل على كائن المستند الذي يتم حفظه حالياً. |
| [getImageFileName()](#getImageFileName) | يحصل على اسم الملف (بدون مسار) حيث سيتم حفظ الصورة. |
| [getImageStream()](#getImageStream) |  |
| [getKeepImageStreamOpen()](#getKeepImageStreamOpen) | يحدد ما إذا كان Aspose.Words يجب أن يبقي التدفق مفتوحًا أو يغلقه بعد حفظ الصورة. |
| [isImageAvailable()](#isImageAvailable) | يرجع  true  إذا كانت الصورة الحالية متاحة للتصدير. |
| [setImageFileName(String value)](#setImageFileName-java.lang.String) | يضبط اسم الملف (بدون مسار) حيث سيتم حفظ الصورة. |
| [setImageStream(OutputStream value)](#setImageStream-java.io.OutputStream) |  |
| [setKeepImageStreamOpen(boolean value)](#setKeepImageStreamOpen-boolean) | يحدد ما إذا كان Aspose.Words يجب أن يبقي التدفق مفتوحًا أو يغلقه بعد حفظ الصورة. |
### getCurrentShape() {#getCurrentShape}
```
public ShapeBase getCurrentShape()
```


يحصل على كائن [ShapeBase](../../com.aspose.words/shapebase/) المقابل للشكل أو مجموعة الأشكال التي ستُحفظ.

 **Remarks:** 

[IImageSavingCallback](../../com.aspose.words/iimagesavingcallback/) can be fired while saving either a shape or a group shape. That's why the property has [ShapeBase](../../com.aspose.words/shapebase/) type. You can check whether it's a group shape comparing [ShapeBase.getShapeType()](../../com.aspose.words/shapebase/\#getShapeType) with [ShapeType.GROUP](../../com.aspose.words/shapetype/\#GROUP) or by casting it to one of derived classes: [Shape](../../com.aspose.words/shape/) or [GroupShape](../../com.aspose.words/groupshape/).

يستخدم Aspose.Words اسم ملف المستند ورقمًا فريدًا لتوليد اسم ملف فريد لكل صورة موجودة في المستند. يمكنك استخدام الخاصية [getCurrentShape()](../../com.aspose.words/imagesavingargs/#getCurrentShape) لتوليد اسم ملف "أفضل" من خلال فحص خصائص الشكل مثل [ImageData.getTitle()](../../com.aspose.words/imagedata/#getTitle) / [ImageData.setTitle(java.lang.String)](../../com.aspose.words/imagedata/#setTitle-java.lang.String) (للشكل فقط)، [ImageData.getSourceFullName()](../../com.aspose.words/imagedata/#getSourceFullName) / [ImageData.setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata/#setSourceFullName-java.lang.String) (للشكل فقط) و [ShapeBase.getName()](../../com.aspose.words/shapebase/#getName) / [ShapeBase.setName(java.lang.String)](../../com.aspose.words/shapebase/#setName-java.lang.String). بالطبع يمكنك بناء أسماء الملفات باستخدام أي خصائص أو معايير أخرى لكن لاحظ أن أسماء الملفات الفرعية يجب أن تكون فريدة داخل عملية التصدير.

بعض الصور في المستند قد تكون غير متاحة. للتحقق من توفر الصورة استخدم الخاصية [isImageAvailable()](../../com.aspose.words/imagesavingargs/#isImageAvailable).

 **Examples:** 

يوضح كيفية تضمين رد نداء حفظ الصورة في عملية تحويل HTML.

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


يحصل على كائن المستند الذي يتم حفظه حالياً.

 **Examples:** 

يوضح كيفية تضمين رد نداء حفظ الصورة في عملية تحويل HTML.

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


يحصل على اسم الملف (بدون مسار) حيث سيتم حفظ الصورة.

 **Remarks:** 

تتيح لك هذه الخاصية إعادة تعريف كيفية توليد أسماء ملفات الصور أثناء التصدير إلى HTML.

عند إطلاق الحدث، تحتوي هذه الخاصية على اسم الملف الذي تم توليده بواسطة Aspose.Words. يمكنك تغيير قيمة هذه الخاصية لحفظ الصورة في ملف مختلف. لاحظ أن أسماء الملفات يجب أن تكون فريدة.

يقوم Aspose.Words تلقائيًا بتوليد اسم ملف فريد لكل صورة مدمجة عند التصدير إلى تنسيق HTML. يعتمد كيفية توليد اسم ملف الصورة على ما إذا كنت تحفظ المستند إلى ملف أو إلى تدفق.

عند حفظ المستند إلى ملف، يبدو اسم ملف الصورة المُولد مثل *.![Image 1][].*.

عند حفظ المستند إلى تدفق، يبدو اسم ملف الصورة المُولد مثل *Aspose.Words..![Image 1][].*.

[getImageFileName()](../../com.aspose.words/imagesavingargs/\#getImageFileName) / [setImageFileName(java.lang.String)](../../com.aspose.words/imagesavingargs/\#setImageFileName-java.lang.String) must contain only the file name without the path. Aspose.Words determines the path for saving and the value of the  src  attribute for writing to HTML using the document file name, the [HtmlSaveOptions.getImagesFolder()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolder) / [HtmlSaveOptions.setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolder-java.lang.String) and [HtmlSaveOptions.getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolderAlias) / [HtmlSaveOptions.setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolderAlias-java.lang.String) properties.

 **Examples:** 

يوضح كيفية تقسيم المستند إلى أجزاء وحفظها.

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
java.lang.String - اسم الملف (بدون مسار) حيث سيتم حفظ الصورة.
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


يحدد ما إذا كان Aspose.Words يجب أن يبقي التدفق مفتوحًا أو يغلقه بعد حفظ الصورة.

 **Remarks:** 

القيمة الافتراضية هي  false  وستغلق Aspose.Words التدفق الذي قدمته في الخاصية **P:Aspose.Words.Saving.ImageSavingArgs.ImageStream** بعد كتابة صورة فيه. حدد  true  لإبقاء التدفق مفتوحًا.

 **Examples:** 

يوضح كيفية تضمين رد نداء حفظ الصورة في عملية تحويل HTML.

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
boolean - القيمة المنطقية المقابلة.
### isImageAvailable() {#isImageAvailable}
```
public boolean isImageAvailable()
```


يرجع  true  إذا كانت الصورة الحالية متاحة للتصدير.

 **Remarks:** 

بعض الصور في المستند قد تكون غير متاحة، على سبيل المثال، لأن الصورة مرتبطة والرابط غير قابل للوصول أو لا يشير إلى صورة صالحة. في هذه الحالة يصدر Aspose.Words أيقونة بعلامة X حمراء. تُرجع هذه الخاصية  true  إذا كانت الصورة الأصلية متاحة؛ وتُرجع  false  إذا لم تكن الصورة الأصلية متاحة وسيتم تقديم أيقونة "لا صورة" للحفظ.

عند حفظ مجموعة أشكال أو شكل لا يتطلب أي صورة تكون هذه الخاصية دائمًا  true .

 **Examples:** 

يوضح كيفية تضمين رد نداء حفظ الصورة في عملية تحويل HTML.

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
boolean -  true  إذا كانت الصورة الحالية متاحة للتصدير.
### setImageFileName(String value) {#setImageFileName-java.lang.String}
```
public void setImageFileName(String value)
```


يضبط اسم الملف (بدون مسار) حيث سيتم حفظ الصورة.

 **Remarks:** 

تتيح لك هذه الخاصية إعادة تعريف كيفية توليد أسماء ملفات الصور أثناء التصدير إلى HTML.

عند إطلاق الحدث، تحتوي هذه الخاصية على اسم الملف الذي تم توليده بواسطة Aspose.Words. يمكنك تغيير قيمة هذه الخاصية لحفظ الصورة في ملف مختلف. لاحظ أن أسماء الملفات يجب أن تكون فريدة.

يقوم Aspose.Words تلقائيًا بتوليد اسم ملف فريد لكل صورة مدمجة عند التصدير إلى تنسيق HTML. يعتمد كيفية توليد اسم ملف الصورة على ما إذا كنت تحفظ المستند إلى ملف أو إلى تدفق.

عند حفظ المستند إلى ملف، يبدو اسم ملف الصورة المُولد مثل *.![Image 1][].*.

عند حفظ المستند إلى تدفق، يبدو اسم ملف الصورة المُولد مثل *Aspose.Words..![Image 1][].*.

[getImageFileName()](../../com.aspose.words/imagesavingargs/\#getImageFileName) / [setImageFileName(java.lang.String)](../../com.aspose.words/imagesavingargs/\#setImageFileName-java.lang.String) must contain only the file name without the path. Aspose.Words determines the path for saving and the value of the  src  attribute for writing to HTML using the document file name, the [HtmlSaveOptions.getImagesFolder()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolder) / [HtmlSaveOptions.setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolder-java.lang.String) and [HtmlSaveOptions.getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getImagesFolderAlias) / [HtmlSaveOptions.setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setImagesFolderAlias-java.lang.String) properties.

 **Examples:** 

يوضح كيفية تقسيم المستند إلى أجزاء وحفظها.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | اسم الملف (بدون مسار) حيث سيتم حفظ الصورة. |

### setImageStream(OutputStream value) {#setImageStream-java.io.OutputStream}
```
public void setImageStream(OutputStream value)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.io.OutputStream |  |

### setKeepImageStreamOpen(boolean value) {#setKeepImageStreamOpen-boolean}
```
public void setKeepImageStreamOpen(boolean value)
```


يحدد ما إذا كان Aspose.Words يجب أن يبقي التدفق مفتوحًا أو يغلقه بعد حفظ الصورة.

 **Remarks:** 

القيمة الافتراضية هي  false  وستغلق Aspose.Words التدفق الذي قدمته في الخاصية **P:Aspose.Words.Saving.ImageSavingArgs.ImageStream** بعد كتابة صورة فيه. حدد  true  لإبقاء التدفق مفتوحًا.

 **Examples:** 

يوضح كيفية تضمين رد نداء حفظ الصورة في عملية تحويل HTML.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

