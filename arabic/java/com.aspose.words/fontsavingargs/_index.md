---
title: "FontSavingArgs"
linktitle: "FontSavingArgs"
second_title: "Aspose.Words لـ Java"
description: "يوفر البيانات لحدث IFontSavingCallback.fontSavingcom.aspose.words.FontSavingArgs في Java."
type: docs
weight: 331
url: /ar/java/com.aspose.words/fontsavingargs/
---

**Inheritance:**
java.lang.Object
```
public class FontSavingArgs
```

يوفر البيانات لحدث [IFontSavingCallback.fontSaving(com.aspose.words.FontSavingArgs)](../../com.aspose.words/ifontsavingcallback/\#fontSaving-com.aspose.words.FontSavingArgs).

للتعرف على المزيد، زر [ Save a Document ][Save a Document] مقالة الوثائق.

 **Remarks:** 

عند حفظ Aspose.Words مستندًا إلى HTML أو صيغ ذات صلة وتكون الخاصية [HtmlSaveOptions.getExportFontResources()](../../com.aspose.words/htmlsaveoptions/\#getExportFontResources) / [HtmlSaveOptions.setExportFontResources(boolean)](../../com.aspose.words/htmlsaveoptions/\#setExportFontResources-boolean) مضبوطة على true، فإنه يحفظ كل خط لتصديره في ملف منفصل.

[FontSavingArgs](../../com.aspose.words/fontsavingargs/) controls whether particular font resource should be exported and how.

[FontSavingArgs](../../com.aspose.words/fontsavingargs/) also allows to redefine how font file names are generated or to completely circumvent saving of fonts into files by providing your own stream objects.

لتحديد ما إذا كان يجب حفظ مورد خط معين، استخدم الخاصية [isExportNeeded()](../../com.aspose.words/fontsavingargs/\#isExportNeeded) / [isExportNeeded(boolean)](../../com.aspose.words/fontsavingargs/\#isExportNeeded-boolean).

لحفظ الخطوط في تدفقات بدلاً من ملفات، استخدم الخاصية **P:Aspose.Words.Saving.FontSavingArgs.FontStream**.

 **Examples:** 

يوضح كيفية تعريف منطق مخصص لتصدير الخطوط عند الحفظ إلى HTML.

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


[Save a Document]: https://docs.aspose.com/words/java/save-a-document/
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getBold()](#getBold) | يشير إلى ما إذا كان الخط الحالي عريضًا. |
| [getDocument()](#getDocument) | يحصل على كائن المستند الذي يتم حفظه. |
| [getFontFamilyName()](#getFontFamilyName) | يشير إلى اسم عائلة الخط الحالي. |
| [getFontFileName()](#getFontFileName) | يحصل على اسم الملف (بدون المسار) حيث سيتم حفظ الخط. |
| [getFontStream()](#getFontStream) |  |
| [getItalic()](#getItalic) | يشير إلى ما إذا كان الخط الحالي مائلًا. |
| [getKeepFontStreamOpen()](#getKeepFontStreamOpen) | يحدد ما إذا كان يجب على Aspose.Words إبقاء التدفق مفتوحًا أو إغلاقه بعد حفظ الخط. |
| [getOriginalFileName()](#getOriginalFileName) | يحصل على اسم ملف الخط الأصلي مع الامتداد. |
| [getOriginalFileSize()](#getOriginalFileSize) | يحصل على حجم ملف الخط الأصلي. |
| [isExportNeeded()](#isExportNeeded) | يسمح بتحديد ما إذا كان سيتم تصدير الخط الحالي كموارد خط. |
| [isExportNeeded(boolean value)](#isExportNeeded-boolean) | يسمح بتحديد ما إذا كان سيتم تصدير الخط الحالي كموارد خط. |
| [isSubsettingNeeded()](#isSubsettingNeeded) | يسمح بتحديد ما إذا كان سيتم تقليل الخط الحالي قبل تصديره كموارد خط. |
| [isSubsettingNeeded(boolean value)](#isSubsettingNeeded-boolean) | يسمح بتحديد ما إذا كان سيتم تقليل الخط الحالي قبل تصديره كموارد خط. |
| [setFontFileName(String value)](#setFontFileName-java.lang.String) | يضبط اسم الملف (بدون المسار) حيث سيتم حفظ الخط. |
| [setFontStream(OutputStream value)](#setFontStream-java.io.OutputStream) |  |
| [setKeepFontStreamOpen(boolean value)](#setKeepFontStreamOpen-boolean) | يحدد ما إذا كان يجب على Aspose.Words إبقاء التدفق مفتوحًا أو إغلاقه بعد حفظ الخط. |
### getBold() {#getBold}
```
public boolean getBold()
```


يشير إلى ما إذا كان الخط الحالي عريضًا.

 **Examples:** 

يوضح كيفية تعريف منطق مخصص لتصدير الخطوط عند الحفظ إلى HTML.

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
boolean - القيمة المنطقية المقابلة.
### getDocument() {#getDocument}
```
public Document getDocument()
```


يحصل على كائن المستند الذي يتم حفظه.

 **Examples:** 

يوضح كيفية تعريف منطق مخصص لتصدير الخطوط عند الحفظ إلى HTML.

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
[Document](../../com.aspose.words/document/) - The document object that is being saved.
### getFontFamilyName() {#getFontFamilyName}
```
public String getFontFamilyName()
```


يشير إلى اسم عائلة الخط الحالي.

 **Examples:** 

يوضح كيفية تعريف منطق مخصص لتصدير الخطوط عند الحفظ إلى HTML.

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
java.lang.String - القيمة المقابلة من نوع java.lang.String.
### getFontFileName() {#getFontFileName}
```
public String getFontFileName()
```


يحصل على اسم الملف (بدون المسار) حيث سيتم حفظ الخط.

 **Remarks:** 

تسمح لك هذه الخاصية بإعادة تعريف كيفية إنشاء أسماء ملفات الخط أثناء التصدير إلى HTML.

عند إطلاق الحدث، تحتوي هذه الخاصية على اسم الملف الذي تم إنشاؤه بواسطة Aspose.Words. يمكنك تغيير قيمة هذه الخاصية لحفظ الخط في ملف مختلف. لاحظ أن أسماء الملفات يجب أن تكون فريدة.

يقوم Aspose.Words تلقائيًا بإنشاء اسم ملف فريد لكل خط مضمّن عند التصدير إلى تنسيق HTML. طريقة إنشاء اسم ملف الخط تعتمد على ما إذا كنت تحفظ المستند إلى ملف أو إلى تدفق.

عند حفظ المستند إلى ملف، يبدو اسم ملف الخط الذي تم إنشاؤه مثل *..*.

عند حفظ المستند إلى تدفق، يبدو اسم ملف الخط الذي تم إنشاؤه مثل *Aspose.Words...*.

[getFontFileName()](../../com.aspose.words/fontsavingargs/\#getFontFileName) / [setFontFileName(java.lang.String)](../../com.aspose.words/fontsavingargs/\#setFontFileName-java.lang.String) must contain only the file name without the path. Aspose.Words determines the path for saving using the document file name, the [HtmlSaveOptions.getFontsFolder()](../../com.aspose.words/htmlsaveoptions/\#getFontsFolder) / [HtmlSaveOptions.setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setFontsFolder-java.lang.String) and [HtmlSaveOptions.getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getFontsFolderAlias) / [HtmlSaveOptions.setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setFontsFolderAlias-java.lang.String) properties.

 **Examples:** 

يوضح كيفية تعريف منطق مخصص لتصدير الخطوط عند الحفظ إلى HTML.

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

**P:Aspose.Words.Saving.FontSavingArgs.FontStream**

**Returns:**
java.lang.String - اسم الملف (بدون المسار) حيث سيتم حفظ الخط.
### getFontStream() {#getFontStream}
```
public OutputStream getFontStream()
```




**Returns:**
java.io.OutputStream
### getItalic() {#getItalic}
```
public boolean getItalic()
```


يشير إلى ما إذا كان الخط الحالي مائلًا.

 **Examples:** 

يوضح كيفية تعريف منطق مخصص لتصدير الخطوط عند الحفظ إلى HTML.

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
boolean - القيمة المنطقية المقابلة.
### getKeepFontStreamOpen() {#getKeepFontStreamOpen}
```
public boolean getKeepFontStreamOpen()
```


يحدد ما إذا كان يجب على Aspose.Words إبقاء التدفق مفتوحًا أو إغلاقه بعد حفظ الخط.

 **Remarks:** 

القيمة الافتراضية هي  false  وستقوم Aspose.Words بإغلاق التدفق الذي قدمته في الخاصية **P:Aspose.Words.Saving.FontSavingArgs.FontStream** بعد كتابة الخط فيه. حدد  true  لإبقاء التدفق مفتوحًا.

 **Examples:** 

يوضح كيفية تعريف منطق مخصص لتصدير الخطوط عند الحفظ إلى HTML.

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

**P:Aspose.Words.Saving.FontSavingArgs.FontStream**

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getOriginalFileName() {#getOriginalFileName}
```
public String getOriginalFileName()
```


يحصل على اسم ملف الخط الأصلي مع الامتداد.

 **Remarks:** 

تحتوي هذه الخاصية على اسم الملف الأصلي للخط الحالي إذا كان معروفًا. وإلا يمكن أن تكون سلسلة فارغة.

 **Examples:** 

يوضح كيفية تعريف منطق مخصص لتصدير الخطوط عند الحفظ إلى HTML.

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
java.lang.String - اسم ملف الخط الأصلي مع الامتداد.
### getOriginalFileSize() {#getOriginalFileSize}
```
public int getOriginalFileSize()
```


يحصل على حجم ملف الخط الأصلي.

 **Remarks:** 

تحتوي هذه الخاصية على حجم الملف الأصلي للخط الحالي إذا كان معروفًا. وإلا يمكن أن يكون صفرًا.

 **Examples:** 

يوضح كيفية تعريف منطق مخصص لتصدير الخطوط عند الحفظ إلى HTML.

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
int - حجم ملف الخط الأصلي.
### isExportNeeded() {#isExportNeeded}
```
public boolean isExportNeeded()
```


يسمح بتحديد ما إذا كان سيتم تصدير الخط الحالي كموارد خط. القيمة الافتراضية هي  true .

 **Examples:** 

يوضح كيفية تعريف منطق مخصص لتصدير الخطوط عند الحفظ إلى HTML.

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
boolean - القيمة المنطقية المقابلة.
### isExportNeeded(boolean value) {#isExportNeeded-boolean}
```
public void isExportNeeded(boolean value)
```


يسمح بتحديد ما إذا كان سيتم تصدير الخط الحالي كموارد خط. القيمة الافتراضية هي  true .

 **Examples:** 

يوضح كيفية تعريف منطق مخصص لتصدير الخطوط عند الحفظ إلى HTML.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### isSubsettingNeeded() {#isSubsettingNeeded}
```
public boolean isSubsettingNeeded()
```


يسمح بتحديد ما إذا كان سيتم تقليل الخط الحالي قبل تصديره كموارد خط.

 **Remarks:** 

يمكن تصدير الخطوط كملفات خطوط أصلية كاملة أو كنسخ جزئية تشمل فقط الأحرف المستخدمة في المستند. يسمح التقسيم الفرعي بتقليل حجم مورد الخط الناتج.

بشكل افتراضي، يقرر Aspose.Words ما إذا كان سيجري التقسيم الفرعي أم لا عن طريق مقارنة حجم ملف الخط الأصلي مع الحجم المحدد في [HtmlSaveOptions.getFontResourcesSubsettingSizeThreshold()](../../com.aspose.words/htmlsaveoptions/\#getFontResourcesSubsettingSizeThreshold) / [HtmlSaveOptions.setFontResourcesSubsettingSizeThreshold(int)](../../com.aspose.words/htmlsaveoptions/\#setFontResourcesSubsettingSizeThreshold-int). يمكنك تجاوز هذا السلوك للخطوط الفردية عن طريق ضبط الخاصية [isSubsettingNeeded()](../../com.aspose.words/fontsavingargs/\#isSubsettingNeeded) / [isSubsettingNeeded(boolean)](../../com.aspose.words/fontsavingargs/\#isSubsettingNeeded-boolean).

 **Examples:** 

يوضح كيفية تعريف منطق مخصص لتصدير الخطوط عند الحفظ إلى HTML.

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
boolean - القيمة المنطقية المقابلة.
### isSubsettingNeeded(boolean value) {#isSubsettingNeeded-boolean}
```
public void isSubsettingNeeded(boolean value)
```


يسمح بتحديد ما إذا كان سيتم تقليل الخط الحالي قبل تصديره كموارد خط.

 **Remarks:** 

يمكن تصدير الخطوط كملفات خطوط أصلية كاملة أو كنسخ جزئية تشمل فقط الأحرف المستخدمة في المستند. يسمح التقسيم الفرعي بتقليل حجم مورد الخط الناتج.

بشكل افتراضي، يقرر Aspose.Words ما إذا كان سيجري التقسيم الفرعي أم لا عن طريق مقارنة حجم ملف الخط الأصلي مع الحجم المحدد في [HtmlSaveOptions.getFontResourcesSubsettingSizeThreshold()](../../com.aspose.words/htmlsaveoptions/\#getFontResourcesSubsettingSizeThreshold) / [HtmlSaveOptions.setFontResourcesSubsettingSizeThreshold(int)](../../com.aspose.words/htmlsaveoptions/\#setFontResourcesSubsettingSizeThreshold-int). يمكنك تجاوز هذا السلوك للخطوط الفردية عن طريق ضبط الخاصية [isSubsettingNeeded()](../../com.aspose.words/fontsavingargs/\#isSubsettingNeeded) / [isSubsettingNeeded(boolean)](../../com.aspose.words/fontsavingargs/\#isSubsettingNeeded-boolean).

 **Examples:** 

يوضح كيفية تعريف منطق مخصص لتصدير الخطوط عند الحفظ إلى HTML.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setFontFileName(String value) {#setFontFileName-java.lang.String}
```
public void setFontFileName(String value)
```


يضبط اسم الملف (بدون المسار) حيث سيتم حفظ الخط.

 **Remarks:** 

تسمح لك هذه الخاصية بإعادة تعريف كيفية إنشاء أسماء ملفات الخط أثناء التصدير إلى HTML.

عند إطلاق الحدث، تحتوي هذه الخاصية على اسم الملف الذي تم إنشاؤه بواسطة Aspose.Words. يمكنك تغيير قيمة هذه الخاصية لحفظ الخط في ملف مختلف. لاحظ أن أسماء الملفات يجب أن تكون فريدة.

يقوم Aspose.Words تلقائيًا بإنشاء اسم ملف فريد لكل خط مضمّن عند التصدير إلى تنسيق HTML. طريقة إنشاء اسم ملف الخط تعتمد على ما إذا كنت تحفظ المستند إلى ملف أو إلى تدفق.

عند حفظ المستند إلى ملف، يبدو اسم ملف الخط الذي تم إنشاؤه مثل *..*.

عند حفظ المستند إلى تدفق، يبدو اسم ملف الخط الذي تم إنشاؤه مثل *Aspose.Words...*.

[getFontFileName()](../../com.aspose.words/fontsavingargs/\#getFontFileName) / [setFontFileName(java.lang.String)](../../com.aspose.words/fontsavingargs/\#setFontFileName-java.lang.String) must contain only the file name without the path. Aspose.Words determines the path for saving using the document file name, the [HtmlSaveOptions.getFontsFolder()](../../com.aspose.words/htmlsaveoptions/\#getFontsFolder) / [HtmlSaveOptions.setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setFontsFolder-java.lang.String) and [HtmlSaveOptions.getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getFontsFolderAlias) / [HtmlSaveOptions.setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setFontsFolderAlias-java.lang.String) properties.

 **Examples:** 

يوضح كيفية تعريف منطق مخصص لتصدير الخطوط عند الحفظ إلى HTML.

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

**P:Aspose.Words.Saving.FontSavingArgs.FontStream**

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | اسم الملف (بدون المسار) حيث سيتم حفظ الخط. |

### setFontStream(OutputStream value) {#setFontStream-java.io.OutputStream}
```
public void setFontStream(OutputStream value)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.io.OutputStream |  |

### setKeepFontStreamOpen(boolean value) {#setKeepFontStreamOpen-boolean}
```
public void setKeepFontStreamOpen(boolean value)
```


يحدد ما إذا كان يجب على Aspose.Words إبقاء التدفق مفتوحًا أو إغلاقه بعد حفظ الخط.

 **Remarks:** 

القيمة الافتراضية هي  false  وستقوم Aspose.Words بإغلاق التدفق الذي قدمته في الخاصية **P:Aspose.Words.Saving.FontSavingArgs.FontStream** بعد كتابة الخط فيه. حدد  true  لإبقاء التدفق مفتوحًا.

 **Examples:** 

يوضح كيفية تعريف منطق مخصص لتصدير الخطوط عند الحفظ إلى HTML.

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

**P:Aspose.Words.Saving.FontSavingArgs.FontStream**

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

