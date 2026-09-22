---
title: "ResourceSavingArgs"
linktitle: "ResourceSavingArgs"
second_title: "Aspose.Words لـ Java"
description: "يوفر البيانات لحدث IResourceSavingCallback.resourceSavingcom.aspose.words.ResourceSavingArgs في Java."
type: docs
weight: 577
url: /ar/java/com.aspose.words/resourcesavingargs/
---

**Inheritance:**
java.lang.Object
```
public class ResourceSavingArgs
```

يوفر البيانات لحدث [IResourceSavingCallback.resourceSaving(com.aspose.words.ResourceSavingArgs)](../../com.aspose.words/iresourcesavingcallback/\#resourceSaving-com.aspose.words.ResourceSavingArgs).

للتعرف على المزيد، زر [ Save a Document ][Save a Document] مقالة الوثائق.

 **Remarks:** 

بشكل افتراضي، عندما تقوم Aspose.Words بحفظ مستند إلى HTML ثابت الصفحة أو SVG أو Markdown، فإنها تحفظ كل مورد في ملف منفصل. تستخدم Aspose.Words اسم ملف المستند ورقمًا فريدًا لإنشاء اسم ملف فريد لكل مورد موجود في المستند.

[ResourceSavingArgs](../../com.aspose.words/resourcesavingargs/) allows to redefine how resource file names are generated or to completely circumvent saving of resources into files by providing your own stream objects.

لتطبيق المنطق الخاص بك لتوليد أسماء ملفات الموارد، استخدم الخاصية [getResourceFileName()](../../com.aspose.words/resourcesavingargs/\#getResourceFileName) / [setResourceFileName(java.lang.String)](../../com.aspose.words/resourcesavingargs/\#setResourceFileName-java.lang.String).

لحفظ الموارد في تدفقات بدلاً من ملفات، استخدم الخاصية **P:Aspose.Words.Saving.ResourceSavingArgs.ResourceStream**.

 **Examples:** 

يعرض كيفية استخدام رد نداء لتتبع الموارد الخارجية التي تم إنشاؤها أثناء تحويل مستند إلى HTML.

```

 public void resourceSavingCallback() throws Exception {
     Document doc = new Document(getMyDir() + "Bullet points with alternative font.docx");

     FontSavingCallback callback = new FontSavingCallback();

     HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions();
     {
         saveOptions.setResourceSavingCallback(callback);
     }

     doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.UsingMachineFonts.html", saveOptions);

     System.out.println(callback.getText());
 }

 private static class FontSavingCallback implements IResourceSavingCallback {
     /// 
     /// Called when Aspose.Words saves an external resource to fixed page HTML or SVG.
     /// 
     public void resourceSaving(ResourceSavingArgs args) {
         mText.append(MessageFormat.format("Original document URI:\t{0}", args.getDocument().getOriginalFileName()));
         mText.append(MessageFormat.format("Resource being saved:\t{0}", args.getResourceFileName()));
         mText.append(MessageFormat.format("Full uri after saving:\t{0}\n", args.getResourceFileUri()));
     }

     public String getText() {
         return mText.toString();
     }

     private final StringBuilder mText = new StringBuilder();
 }
 
```


[Save a Document]: https://docs.aspose.com/words/java/save-a-document/
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getDocument()](#getDocument) | يحصل على كائن المستند الذي يتم حفظه حالياً. |
| [getKeepResourceStreamOpen()](#getKeepResourceStreamOpen) | يحدد ما إذا كان يجب على Aspose.Words إبقاء التدفق مفتوحًا أو إغلاقه بعد حفظ المورد. |
| [getResourceFileName()](#getResourceFileName) | يحصل على اسم الملف (بدون مسار) حيث سيتم حفظ المورد. |
| [getResourceFileUri()](#getResourceFileUri) | يحصل على معرف الموارد الموحد (URI) المستخدم للإشارة إلى ملف المورد من المستند. |
| [getResourceStream()](#getResourceStream) |  |
| [setKeepResourceStreamOpen(boolean value)](#setKeepResourceStreamOpen-boolean) | يحدد ما إذا كان يجب على Aspose.Words إبقاء التدفق مفتوحًا أو إغلاقه بعد حفظ المورد. |
| [setResourceFileName(String value)](#setResourceFileName-java.lang.String) | يضبط اسم الملف (بدون مسار) حيث سيتم حفظ المورد. |
| [setResourceFileUri(String value)](#setResourceFileUri-java.lang.String) | يضبط معرف الموارد الموحد (URI) المستخدم للإشارة إلى ملف المورد من المستند. |
| [setResourceStream(OutputStream value)](#setResourceStream-java.io.OutputStream) |  |
### getDocument() {#getDocument}
```
public Document getDocument()
```


يحصل على كائن المستند الذي يتم حفظه حالياً.

 **Examples:** 

يعرض كيفية استخدام رد نداء لتتبع الموارد الخارجية التي تم إنشاؤها أثناء تحويل مستند إلى HTML.

```

 public void resourceSavingCallback() throws Exception {
     Document doc = new Document(getMyDir() + "Bullet points with alternative font.docx");

     FontSavingCallback callback = new FontSavingCallback();

     HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions();
     {
         saveOptions.setResourceSavingCallback(callback);
     }

     doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.UsingMachineFonts.html", saveOptions);

     System.out.println(callback.getText());
 }

 private static class FontSavingCallback implements IResourceSavingCallback {
     /// 
     /// Called when Aspose.Words saves an external resource to fixed page HTML or SVG.
     /// 
     public void resourceSaving(ResourceSavingArgs args) {
         mText.append(MessageFormat.format("Original document URI:\t{0}", args.getDocument().getOriginalFileName()));
         mText.append(MessageFormat.format("Resource being saved:\t{0}", args.getResourceFileName()));
         mText.append(MessageFormat.format("Full uri after saving:\t{0}\n", args.getResourceFileUri()));
     }

     public String getText() {
         return mText.toString();
     }

     private final StringBuilder mText = new StringBuilder();
 }
 
```

**Returns:**
[Document](../../com.aspose.words/document/) - The document object that is currently being saved.
### getKeepResourceStreamOpen() {#getKeepResourceStreamOpen}
```
public boolean getKeepResourceStreamOpen()
```


يحدد ما إذا كان يجب على Aspose.Words إبقاء التدفق مفتوحًا أو إغلاقه بعد حفظ المورد.

 **Remarks:** 

القيمة الافتراضية هي  false  وستقوم Aspose.Words بإغلاق التدفق الذي قدمته في الخاصية **P:Aspose.Words.Saving.ResourceSavingArgs.ResourceStream** بعد كتابة مورد فيه. حدد  true  لإبقاء التدفق مفتوحًا.

 **Examples:** 

يعرض كيفية استخدام رد نداء لطباعة عناوين URI للموارد الخارجية التي تم إنشاؤها أثناء تحويل مستند إلى HTML.

```

 public void htmlFixedResourceFolder() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     ResourceUriPrinter callback = new ResourceUriPrinter();

     HtmlFixedSaveOptions options = new HtmlFixedSaveOptions();
     {
         options.setSaveFormat(SaveFormat.HTML_FIXED);
         options.setExportEmbeddedImages(false);
         options.setResourcesFolder(getArtifactsDir() + "HtmlFixedResourceFolder");
         options.setResourcesFolderAlias(getArtifactsDir() + "HtmlFixedResourceFolderAlias");
         options.setShowPageBorder(false);
         options.setResourceSavingCallback(callback);
     }

     // A folder specified by ResourcesFolderAlias will contain the resources instead of ResourcesFolder.
     // We must ensure the folder exists before the streams can put their resources into it.
     new File(options.getResourcesFolderAlias()).mkdir();

     doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.HtmlFixedResourceFolder.html", options);

     System.out.println(callback.getText());

     String[] resourceFiles = new File(getArtifactsDir() + "HtmlFixedResourceFolderAlias").list();

     Assert.assertFalse(new File(getArtifactsDir() + "HtmlFixedResourceFolder").exists());
     Assert.assertEquals(6, IterableUtils.countMatches(Arrays.asList(resourceFiles),
             f -> f.endsWith(".jpeg") || f.endsWith(".png") || f.endsWith(".css")));
 }

 /// 
 /// Counts and prints URIs of resources contained by as they are converted to fixed HTML.
 /// 
 private static class ResourceUriPrinter implements IResourceSavingCallback {
     public void resourceSaving(ResourceSavingArgs args) throws Exception {
         // If we set a folder alias in the SaveOptions object, we will be able to print it from here.
         mText.append(MessageFormat.format("Resource #{0} \"{1}\"", ++mSavedResourceCount, args.getResourceFileName()));

         String extension = FilenameUtils.getExtension(args.getResourceFileName());
         switch (extension) {
             case "ttf":
             case "woff": {
                 // By default, 'ResourceFileUri' uses system folder for fonts.
                 // To avoid problems in other platforms you must explicitly specify the path for the fonts.
                 args.setResourceFileUri(getArtifactsDir() + File.separatorChar + args.getResourceFileName());
                 break;
             }
         }

         mText.append("\t" + args.getResourceFileUri());

         // If we have specified a folder in the "ResourcesFolderAlias" property,
         // we will also need to redirect each stream to put its resource in that folder.
         args.setResourceStream(new FileOutputStream(args.getResourceFileUri()));
         args.setKeepResourceStreamOpen(false);
     }

     public String getText() {
         return mText.toString();
     }

     private int mSavedResourceCount;
     private final  StringBuilder mText = new StringBuilder();
 }
 
```

**P:Aspose.Words.Saving.ResourceSavingArgs.ResourceStream**

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getResourceFileName() {#getResourceFileName}
```
public String getResourceFileName()
```


يحصل على اسم الملف (بدون مسار) حيث سيتم حفظ المورد.

 **Remarks:** 

تتيح لك هذه الخاصية إعادة تعريف كيفية توليد أسماء ملفات الموارد أثناء التصدير إلى HTML ثابت الصفحة أو SVG أو Markdown.

عند حدوث الحدث، تحتوي هذه الخاصية على اسم الملف الذي تم توليده بواسطة Aspose.Words. يمكنك تغيير قيمة هذه الخاصية لحفظ المورد في ملف مختلف. لاحظ أن أسماء الملفات يجب أن تكون فريدة.

تقوم Aspose.Words تلقائيًا بإنشاء اسم ملف فريد لكل مورد عند التصدير إلى تنسيق HTML ثابت الصفحة أو SVG أو Markdown. يعتمد طريقة توليد اسم ملف المورد على ما إذا كنت تحفظ المستند في ملف أو في تدفق.

عند حفظ المستند في ملف، يبدو اسم ملف المورد المُولد مثل *.![Image 1][].*.

عند حفظ المستند في تدفق، يبدو اسم ملف المورد المُولد مثل *Aspose.Words..![Image 1][].*.

[getResourceFileName()](../../com.aspose.words/resourcesavingargs/\#getResourceFileName) / [setResourceFileName(java.lang.String)](../../com.aspose.words/resourcesavingargs/\#setResourceFileName-java.lang.String) must contain only the file name without the path. Aspose.Words determines the path for saving and the value of the  src  attribute for writing to fixed page HTML, SVG or Markdown using the document file name, the [HtmlFixedSaveOptions.getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolder) / [HtmlFixedSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolder-java.lang.String) or [SvgSaveOptions.getResourcesFolder()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolder) / [SvgSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolder-java.lang.String) and [HtmlFixedSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolderAlias) / [HtmlFixedSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolderAlias-java.lang.String) or [SvgSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolderAlias) / [SvgSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolderAlias-java.lang.String) or [MarkdownSaveOptions.getImagesFolder()](../../com.aspose.words/markdownsaveoptions/\#getImagesFolder) / [MarkdownSaveOptions.setImagesFolder(java.lang.String)](../../com.aspose.words/markdownsaveoptions/\#setImagesFolder-java.lang.String) or [MarkdownSaveOptions.getImagesFolderAlias()](../../com.aspose.words/markdownsaveoptions/\#getImagesFolderAlias) / [MarkdownSaveOptions.setImagesFolderAlias(java.lang.String)](../../com.aspose.words/markdownsaveoptions/\#setImagesFolderAlias-java.lang.String) properties.

[HtmlFixedSaveOptions.getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolder) / [HtmlFixedSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolder-java.lang.String) [SvgSaveOptions.getResourcesFolder()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolder) / [SvgSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolder-java.lang.String) [HtmlFixedSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolderAlias) / [HtmlFixedSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolderAlias-java.lang.String) [SvgSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolderAlias) / [SvgSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolderAlias-java.lang.String)

 **Examples:** 

يعرض كيفية استخدام رد نداء لتتبع الموارد الخارجية التي تم إنشاؤها أثناء تحويل مستند إلى HTML.

```

 public void resourceSavingCallback() throws Exception {
     Document doc = new Document(getMyDir() + "Bullet points with alternative font.docx");

     FontSavingCallback callback = new FontSavingCallback();

     HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions();
     {
         saveOptions.setResourceSavingCallback(callback);
     }

     doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.UsingMachineFonts.html", saveOptions);

     System.out.println(callback.getText());
 }

 private static class FontSavingCallback implements IResourceSavingCallback {
     /// 
     /// Called when Aspose.Words saves an external resource to fixed page HTML or SVG.
     /// 
     public void resourceSaving(ResourceSavingArgs args) {
         mText.append(MessageFormat.format("Original document URI:\t{0}", args.getDocument().getOriginalFileName()));
         mText.append(MessageFormat.format("Resource being saved:\t{0}", args.getResourceFileName()));
         mText.append(MessageFormat.format("Full uri after saving:\t{0}\n", args.getResourceFileUri()));
     }

     public String getText() {
         return mText.toString();
     }

     private final StringBuilder mText = new StringBuilder();
 }
 
```

**P:Aspose.Words.Saving.ResourceSavingArgs.ResourceStream**


[Image 1]: 

**Returns:**
java.lang.String - اسم الملف (بدون مسار) حيث سيتم حفظ المورد.
### getResourceFileUri() {#getResourceFileUri}
```
public String getResourceFileUri()
```


يحصل على معرف الموارد الموحد (URI) المستخدم للإشارة إلى ملف المورد من المستند.

 **Remarks:** 

تتيح لك هذه الخاصية تغيير عناوين URI لملفات الموارد المصدرة إلى مستندات HTML ثابت الصفحة أو SVG أو Markdown.

تقوم Aspose.Words تلقائيًا بإنشاء URI لكل ملف مورد أثناء التصدير إلى تنسيق HTML ثابت الصفحة أو SVG أو Markdown. تشير عناوين URI المُولدة إلى ملفات الموارد التي حفظتها Aspose.Words. ومع ذلك، قد تكون عناوين URI غير صحيحة إذا تم نقل ملفات الموارد إلى موقع آخر أو إذا تم حفظ ملفات الموارد في تدفقات. تتيح هذه الخاصية تصحيح عناوين URI في هذه الحالات.

عند حدوث الحدث، تحتوي هذه الخاصية على URI الذي تم توليده بواسطة Aspose.Words. يمكنك تغيير قيمة هذه الخاصية لتوفير URI مخصص لملف المورد.

[HtmlFixedSaveOptions.getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolder) / [HtmlFixedSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolder-java.lang.String) [SvgSaveOptions.getResourcesFolder()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolder) / [SvgSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolder-java.lang.String) [MarkdownSaveOptions.getImagesFolder()](../../com.aspose.words/markdownsaveoptions/\#getImagesFolder) / [MarkdownSaveOptions.setImagesFolder(java.lang.String)](../../com.aspose.words/markdownsaveoptions/\#setImagesFolder-java.lang.String) [HtmlFixedSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolderAlias) / [HtmlFixedSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolderAlias-java.lang.String) [SvgSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolderAlias) / [SvgSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolderAlias-java.lang.String) [MarkdownSaveOptions.getImagesFolderAlias()](../../com.aspose.words/markdownsaveoptions/\#getImagesFolderAlias) / [MarkdownSaveOptions.setImagesFolderAlias(java.lang.String)](../../com.aspose.words/markdownsaveoptions/\#setImagesFolderAlias-java.lang.String)

 **Examples:** 

يعرض كيفية استخدام رد نداء لتتبع الموارد الخارجية التي تم إنشاؤها أثناء تحويل مستند إلى HTML.

```

 public void resourceSavingCallback() throws Exception {
     Document doc = new Document(getMyDir() + "Bullet points with alternative font.docx");

     FontSavingCallback callback = new FontSavingCallback();

     HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions();
     {
         saveOptions.setResourceSavingCallback(callback);
     }

     doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.UsingMachineFonts.html", saveOptions);

     System.out.println(callback.getText());
 }

 private static class FontSavingCallback implements IResourceSavingCallback {
     /// 
     /// Called when Aspose.Words saves an external resource to fixed page HTML or SVG.
     /// 
     public void resourceSaving(ResourceSavingArgs args) {
         mText.append(MessageFormat.format("Original document URI:\t{0}", args.getDocument().getOriginalFileName()));
         mText.append(MessageFormat.format("Resource being saved:\t{0}", args.getResourceFileName()));
         mText.append(MessageFormat.format("Full uri after saving:\t{0}\n", args.getResourceFileUri()));
     }

     public String getText() {
         return mText.toString();
     }

     private final StringBuilder mText = new StringBuilder();
 }
 
```

**Returns:**
java.lang.String - معرف الموارد الموحد (URI) المستخدم للإشارة إلى ملف المورد من المستند.
### getResourceStream() {#getResourceStream}
```
public OutputStream getResourceStream()
```




**Returns:**
java.io.OutputStream
### setKeepResourceStreamOpen(boolean value) {#setKeepResourceStreamOpen-boolean}
```
public void setKeepResourceStreamOpen(boolean value)
```


يحدد ما إذا كان يجب على Aspose.Words إبقاء التدفق مفتوحًا أو إغلاقه بعد حفظ المورد.

 **Remarks:** 

القيمة الافتراضية هي  false  وستقوم Aspose.Words بإغلاق التدفق الذي قدمته في الخاصية **P:Aspose.Words.Saving.ResourceSavingArgs.ResourceStream** بعد كتابة مورد فيه. حدد  true  لإبقاء التدفق مفتوحًا.

 **Examples:** 

يعرض كيفية استخدام رد نداء لطباعة عناوين URI للموارد الخارجية التي تم إنشاؤها أثناء تحويل مستند إلى HTML.

```

 public void htmlFixedResourceFolder() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     ResourceUriPrinter callback = new ResourceUriPrinter();

     HtmlFixedSaveOptions options = new HtmlFixedSaveOptions();
     {
         options.setSaveFormat(SaveFormat.HTML_FIXED);
         options.setExportEmbeddedImages(false);
         options.setResourcesFolder(getArtifactsDir() + "HtmlFixedResourceFolder");
         options.setResourcesFolderAlias(getArtifactsDir() + "HtmlFixedResourceFolderAlias");
         options.setShowPageBorder(false);
         options.setResourceSavingCallback(callback);
     }

     // A folder specified by ResourcesFolderAlias will contain the resources instead of ResourcesFolder.
     // We must ensure the folder exists before the streams can put their resources into it.
     new File(options.getResourcesFolderAlias()).mkdir();

     doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.HtmlFixedResourceFolder.html", options);

     System.out.println(callback.getText());

     String[] resourceFiles = new File(getArtifactsDir() + "HtmlFixedResourceFolderAlias").list();

     Assert.assertFalse(new File(getArtifactsDir() + "HtmlFixedResourceFolder").exists());
     Assert.assertEquals(6, IterableUtils.countMatches(Arrays.asList(resourceFiles),
             f -> f.endsWith(".jpeg") || f.endsWith(".png") || f.endsWith(".css")));
 }

 /// 
 /// Counts and prints URIs of resources contained by as they are converted to fixed HTML.
 /// 
 private static class ResourceUriPrinter implements IResourceSavingCallback {
     public void resourceSaving(ResourceSavingArgs args) throws Exception {
         // If we set a folder alias in the SaveOptions object, we will be able to print it from here.
         mText.append(MessageFormat.format("Resource #{0} \"{1}\"", ++mSavedResourceCount, args.getResourceFileName()));

         String extension = FilenameUtils.getExtension(args.getResourceFileName());
         switch (extension) {
             case "ttf":
             case "woff": {
                 // By default, 'ResourceFileUri' uses system folder for fonts.
                 // To avoid problems in other platforms you must explicitly specify the path for the fonts.
                 args.setResourceFileUri(getArtifactsDir() + File.separatorChar + args.getResourceFileName());
                 break;
             }
         }

         mText.append("\t" + args.getResourceFileUri());

         // If we have specified a folder in the "ResourcesFolderAlias" property,
         // we will also need to redirect each stream to put its resource in that folder.
         args.setResourceStream(new FileOutputStream(args.getResourceFileUri()));
         args.setKeepResourceStreamOpen(false);
     }

     public String getText() {
         return mText.toString();
     }

     private int mSavedResourceCount;
     private final  StringBuilder mText = new StringBuilder();
 }
 
```

**P:Aspose.Words.Saving.ResourceSavingArgs.ResourceStream**

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setResourceFileName(String value) {#setResourceFileName-java.lang.String}
```
public void setResourceFileName(String value)
```


يضبط اسم الملف (بدون مسار) حيث سيتم حفظ المورد.

 **Remarks:** 

تتيح لك هذه الخاصية إعادة تعريف كيفية توليد أسماء ملفات الموارد أثناء التصدير إلى HTML ثابت الصفحة أو SVG أو Markdown.

عند حدوث الحدث، تحتوي هذه الخاصية على اسم الملف الذي تم توليده بواسطة Aspose.Words. يمكنك تغيير قيمة هذه الخاصية لحفظ المورد في ملف مختلف. لاحظ أن أسماء الملفات يجب أن تكون فريدة.

تقوم Aspose.Words تلقائيًا بإنشاء اسم ملف فريد لكل مورد عند التصدير إلى تنسيق HTML ثابت الصفحة أو SVG أو Markdown. يعتمد طريقة توليد اسم ملف المورد على ما إذا كنت تحفظ المستند في ملف أو في تدفق.

عند حفظ المستند في ملف، يبدو اسم ملف المورد المُولد مثل *.![Image 1][].*.

عند حفظ المستند في تدفق، يبدو اسم ملف المورد المُولد مثل *Aspose.Words..![Image 1][].*.

[getResourceFileName()](../../com.aspose.words/resourcesavingargs/\#getResourceFileName) / [setResourceFileName(java.lang.String)](../../com.aspose.words/resourcesavingargs/\#setResourceFileName-java.lang.String) must contain only the file name without the path. Aspose.Words determines the path for saving and the value of the  src  attribute for writing to fixed page HTML, SVG or Markdown using the document file name, the [HtmlFixedSaveOptions.getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolder) / [HtmlFixedSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolder-java.lang.String) or [SvgSaveOptions.getResourcesFolder()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolder) / [SvgSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolder-java.lang.String) and [HtmlFixedSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolderAlias) / [HtmlFixedSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolderAlias-java.lang.String) or [SvgSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolderAlias) / [SvgSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolderAlias-java.lang.String) or [MarkdownSaveOptions.getImagesFolder()](../../com.aspose.words/markdownsaveoptions/\#getImagesFolder) / [MarkdownSaveOptions.setImagesFolder(java.lang.String)](../../com.aspose.words/markdownsaveoptions/\#setImagesFolder-java.lang.String) or [MarkdownSaveOptions.getImagesFolderAlias()](../../com.aspose.words/markdownsaveoptions/\#getImagesFolderAlias) / [MarkdownSaveOptions.setImagesFolderAlias(java.lang.String)](../../com.aspose.words/markdownsaveoptions/\#setImagesFolderAlias-java.lang.String) properties.

[HtmlFixedSaveOptions.getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolder) / [HtmlFixedSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolder-java.lang.String) [SvgSaveOptions.getResourcesFolder()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolder) / [SvgSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolder-java.lang.String) [HtmlFixedSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolderAlias) / [HtmlFixedSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolderAlias-java.lang.String) [SvgSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolderAlias) / [SvgSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolderAlias-java.lang.String)

 **Examples:** 

يعرض كيفية استخدام رد نداء لتتبع الموارد الخارجية التي تم إنشاؤها أثناء تحويل مستند إلى HTML.

```

 public void resourceSavingCallback() throws Exception {
     Document doc = new Document(getMyDir() + "Bullet points with alternative font.docx");

     FontSavingCallback callback = new FontSavingCallback();

     HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions();
     {
         saveOptions.setResourceSavingCallback(callback);
     }

     doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.UsingMachineFonts.html", saveOptions);

     System.out.println(callback.getText());
 }

 private static class FontSavingCallback implements IResourceSavingCallback {
     /// 
     /// Called when Aspose.Words saves an external resource to fixed page HTML or SVG.
     /// 
     public void resourceSaving(ResourceSavingArgs args) {
         mText.append(MessageFormat.format("Original document URI:\t{0}", args.getDocument().getOriginalFileName()));
         mText.append(MessageFormat.format("Resource being saved:\t{0}", args.getResourceFileName()));
         mText.append(MessageFormat.format("Full uri after saving:\t{0}\n", args.getResourceFileUri()));
     }

     public String getText() {
         return mText.toString();
     }

     private final StringBuilder mText = new StringBuilder();
 }
 
```

**P:Aspose.Words.Saving.ResourceSavingArgs.ResourceStream**


[Image 1]: 

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | اسم الملف (بدون مسار) حيث سيتم حفظ المورد. |

### setResourceFileUri(String value) {#setResourceFileUri-java.lang.String}
```
public void setResourceFileUri(String value)
```


يضبط معرف الموارد الموحد (URI) المستخدم للإشارة إلى ملف المورد من المستند.

 **Remarks:** 

تتيح لك هذه الخاصية تغيير عناوين URI لملفات الموارد المصدرة إلى مستندات HTML ثابت الصفحة أو SVG أو Markdown.

تقوم Aspose.Words تلقائيًا بإنشاء URI لكل ملف مورد أثناء التصدير إلى تنسيق HTML ثابت الصفحة أو SVG أو Markdown. تشير عناوين URI المُولدة إلى ملفات الموارد التي حفظتها Aspose.Words. ومع ذلك، قد تكون عناوين URI غير صحيحة إذا تم نقل ملفات الموارد إلى موقع آخر أو إذا تم حفظ ملفات الموارد في تدفقات. تتيح هذه الخاصية تصحيح عناوين URI في هذه الحالات.

عند حدوث الحدث، تحتوي هذه الخاصية على URI الذي تم توليده بواسطة Aspose.Words. يمكنك تغيير قيمة هذه الخاصية لتوفير URI مخصص لملف المورد.

[HtmlFixedSaveOptions.getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolder) / [HtmlFixedSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolder-java.lang.String) [SvgSaveOptions.getResourcesFolder()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolder) / [SvgSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolder-java.lang.String) [MarkdownSaveOptions.getImagesFolder()](../../com.aspose.words/markdownsaveoptions/\#getImagesFolder) / [MarkdownSaveOptions.setImagesFolder(java.lang.String)](../../com.aspose.words/markdownsaveoptions/\#setImagesFolder-java.lang.String) [HtmlFixedSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolderAlias) / [HtmlFixedSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolderAlias-java.lang.String) [SvgSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolderAlias) / [SvgSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolderAlias-java.lang.String) [MarkdownSaveOptions.getImagesFolderAlias()](../../com.aspose.words/markdownsaveoptions/\#getImagesFolderAlias) / [MarkdownSaveOptions.setImagesFolderAlias(java.lang.String)](../../com.aspose.words/markdownsaveoptions/\#setImagesFolderAlias-java.lang.String)

 **Examples:** 

يعرض كيفية استخدام رد نداء لتتبع الموارد الخارجية التي تم إنشاؤها أثناء تحويل مستند إلى HTML.

```

 public void resourceSavingCallback() throws Exception {
     Document doc = new Document(getMyDir() + "Bullet points with alternative font.docx");

     FontSavingCallback callback = new FontSavingCallback();

     HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions();
     {
         saveOptions.setResourceSavingCallback(callback);
     }

     doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.UsingMachineFonts.html", saveOptions);

     System.out.println(callback.getText());
 }

 private static class FontSavingCallback implements IResourceSavingCallback {
     /// 
     /// Called when Aspose.Words saves an external resource to fixed page HTML or SVG.
     /// 
     public void resourceSaving(ResourceSavingArgs args) {
         mText.append(MessageFormat.format("Original document URI:\t{0}", args.getDocument().getOriginalFileName()));
         mText.append(MessageFormat.format("Resource being saved:\t{0}", args.getResourceFileName()));
         mText.append(MessageFormat.format("Full uri after saving:\t{0}\n", args.getResourceFileUri()));
     }

     public String getText() {
         return mText.toString();
     }

     private final StringBuilder mText = new StringBuilder();
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | معرف الموارد الموحد (URI) المستخدم للإشارة إلى ملف المورد من المستند. |

### setResourceStream(OutputStream value) {#setResourceStream-java.io.OutputStream}
```
public void setResourceStream(OutputStream value)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.io.OutputStream |  |

