---
title: "مستبدل"
linktitle: "مستبدل"
second_title: "Aspose.Words لـ Java"
description: "يوفر طرقًا تهدف إلى العثور على النص واستبداله في المستند باستخدام Java."
type: docs
weight: 567
url: /ar/java/com.aspose.words/replacer/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Processor](../../com.aspose.words/processor/)
```
public class Replacer extends Processor
```

يوفر طرقًا مخصصة للعثور على النص واستبداله في المستند.
## الطرق

| طريقة | الوصف |
| --- | --- |
| [create(ReplacerContext context)](#create-com.aspose.words.ReplacerContext) | ينشئ نسخة جديدة من معالج المستبدل. |
| [execute()](#execute) | نفّذ إجراء المعالج. |
| [from(InputStream input)](#from-java.io.InputStream) | يحدد المستند الإدخالي للمعالجة. |
| [from(InputStream input, LoadOptions loadOptions)](#from-java.io.InputStream-com.aspose.words.LoadOptions) | يحدد المستند الإدخالي للمعالجة. |
| [from(String input)](#from-java.lang.String) | يحدد المستند الإدخالي للمعالجة. |
| [from(String input, LoadOptions loadOptions)](#from-java.lang.String-com.aspose.words.LoadOptions) | يحدد المستند الإدخالي للمعالجة. |
| [replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String pattern, String replacement)](#replace-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String-java.lang.String) |  |
| [replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options)](#replace-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions) |  |
| [replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Pattern pattern, String replacement)](#replace-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.util.regex.Pattern-java.lang.String) |  |
| [replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options)](#replace-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions) |  |
| [replace(InputStream inputStream, OutputStream outputStream, int saveFormat, String pattern, String replacement)](#replace-java.io.InputStream-java.io.OutputStream-int-java.lang.String-java.lang.String) |  |
| [replace(InputStream inputStream, OutputStream outputStream, int saveFormat, String pattern, String replacement, FindReplaceOptions options)](#replace-java.io.InputStream-java.io.OutputStream-int-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions) |  |
| [replace(InputStream inputStream, OutputStream outputStream, int saveFormat, Pattern pattern, String replacement)](#replace-java.io.InputStream-java.io.OutputStream-int-java.util.regex.Pattern-java.lang.String) |  |
| [replace(InputStream inputStream, OutputStream outputStream, int saveFormat, Pattern pattern, String replacement, FindReplaceOptions options)](#replace-java.io.InputStream-java.io.OutputStream-int-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions) |  |
| [replace(String inputFileName, String outputFileName, SaveOptions saveOptions, String pattern, String replacement)](#replace-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-java.lang.String) | يستبدل جميع تكرارات نمط سلسلة الأحرف المحدد بسلسلة استبدال في ملف الإدخال، مع تنسيق الحفظ المحدد وخيارات إضافية. |
| [replace(String inputFileName, String outputFileName, SaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options)](#replace-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions) | يستبدل جميع تكرارات نمط سلسلة الأحرف المحدد بسلسلة استبدال في ملف الإدخال، مع تنسيق الحفظ المحدد وخيارات إضافية. |
| [replace(String inputFileName, String outputFileName, SaveOptions saveOptions, Pattern pattern, String replacement)](#replace-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.util.regex.Pattern-java.lang.String) | يستبدل جميع تكرارات نمط سلسلة الأحرف المحدد بسلسلة استبدال في ملف الإدخال باستخدام تعبير عادي، مع تنسيق الحفظ المحدد وخيارات إضافية. |
| [replace(String inputFileName, String outputFileName, SaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options)](#replace-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions) | يستبدل جميع تكرارات نمط سلسلة الأحرف المحدد بسلسلة استبدال في ملف الإدخال باستخدام تعبير عادي، مع تنسيق الحفظ المحدد وخيارات إضافية. |
| [replace(String inputFileName, String outputFileName, int saveFormat, String pattern, String replacement)](#replace-java.lang.String-java.lang.String-int-java.lang.String-java.lang.String) |  |
| [replace(String inputFileName, String outputFileName, int saveFormat, String pattern, String replacement, FindReplaceOptions options)](#replace-java.lang.String-java.lang.String-int-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions) |  |
| [replace(String inputFileName, String outputFileName, int saveFormat, Pattern pattern, String replacement)](#replace-java.lang.String-java.lang.String-int-java.util.regex.Pattern-java.lang.String) |  |
| [replace(String inputFileName, String outputFileName, int saveFormat, Pattern pattern, String replacement, FindReplaceOptions options)](#replace-java.lang.String-java.lang.String-int-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions) |  |
| [replace(String inputFileName, String outputFileName, String pattern, String replacement)](#replace-java.lang.String-java.lang.String-java.lang.String-java.lang.String) | يستبدل جميع تكرارات نمط سلسلة الأحرف المحدد بسلسلة استبدال في ملف الإدخال. |
| [replace(String inputFileName, String outputFileName, Pattern pattern, String replacement)](#replace-java.lang.String-java.lang.String-java.util.regex.Pattern-java.lang.String) | يستبدل جميع تكرارات نمط سلسلة الأحرف المحدد بسلسلة استبدال في ملف الإدخال باستخدام تعبير عادي. |
| [replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, String pattern, String replacement)](#replaceToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String-java.lang.String) | يستبدل جميع تكرارات نمط سلسلة الأحرف المحدد بسلسلة استبدال في ملف الإدخال. |
| [replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options)](#replaceToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions) | يستبدل جميع تكرارات نمط سلسلة الأحرف المحدد بسلسلة استبدال في ملف الإدخال. |
| [replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, Pattern pattern, String replacement)](#replaceToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.util.regex.Pattern-java.lang.String) | يستبدل جميع تكرارات نمط التعبير العادي المحدد بسلسلة استبدال في ملف الإدخال. |
| [replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options)](#replaceToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions) | يستبدل جميع تكرارات نمط التعبير العادي المحدد بسلسلة استبدال في ملف الإدخال. |
| [replaceToImages(String inputFileName, ImageSaveOptions saveOptions, String pattern, String replacement)](#replaceToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String-java.lang.String) | يستبدل جميع تكرارات نمط سلسلة الأحرف المحدد بسلسلة استبدال في ملف الإدخال. |
| [replaceToImages(String inputFileName, ImageSaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options)](#replaceToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions) | يستبدل جميع تكرارات نمط سلسلة الأحرف المحدد بسلسلة استبدال في ملف الإدخال. |
| [replaceToImages(String inputFileName, ImageSaveOptions saveOptions, Pattern pattern, String replacement)](#replaceToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.util.regex.Pattern-java.lang.String) | يستبدل جميع تكرارات نمط التعبير العادي المحدد بسلسلة استبدال في ملف الإدخال. |
| [replaceToImages(String inputFileName, ImageSaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options)](#replaceToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions) | يستبدل جميع تكرارات نمط التعبير العادي المحدد بسلسلة استبدال في ملف الإدخال. |
| [to(OutputStream output, SaveOptions saveOptions)](#to-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [to(OutputStream output, int saveFormat)](#to-java.io.OutputStream-int) |  |
| [to(String output)](#to-java.lang.String) | يحدد ملف الإخراج للمعالج. |
| [to(String output, SaveOptions saveOptions)](#to-java.lang.String-com.aspose.words.SaveOptions) | يحدد ملف الإخراج للمعالج. |
| [to(String output, int saveFormat)](#to-java.lang.String-int) |  |
| [to(ArrayList output, SaveOptions saveOptions)](#to-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [to(ArrayList output, int saveFormat)](#to-java.util.ArrayList-int) |  |
| [toOutput(ArrayList output, SaveOptions saveOptions)](#toOutput-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [toOutput(ArrayList output, int saveFormat)](#toOutput-java.util.ArrayList-int) |  |
### create(ReplacerContext context) {#create-com.aspose.words.ReplacerContext}
```
public static Replacer create(ReplacerContext context)
```


ينشئ نسخة جديدة من معالج المستبدل.

 **Examples:** 

يوضح كيفية استبدال السلسلة في المستند باستخدام السياق.

```

 // There is a several ways to replace string in the document:
 String doc = getMyDir() + "Footer.docx";
 String pattern = "(C)2006 Aspose Pty Ltd.";
 String replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

 ReplacerContext replacerContext = new ReplacerContext();
 replacerContext.setReplacement(pattern, replacement);
 replacerContext.getFindReplaceOptions().setFindWholeWordsOnly(false);

 Replacer.create(replacerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ReplaceContext.docx")
         .execute();
 
```

يوضح كيفية استبدال السلسلة في المستند باستخدام المستندات من الدفق باستخدام السياق.

```

 // There is a several ways to replace string in the document using documents from the stream:
 String pattern = "(C)2006 Aspose Pty Ltd.";
 String replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Footer.docx")) {
     ReplacerContext replacerContext = new ReplacerContext();
     replacerContext.setReplacement(pattern, replacement);
     replacerContext.getFindReplaceOptions().setFindWholeWordsOnly(false);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.ReplaceContextStream.docx")) {
         Replacer.create(replacerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

يوضح كيفية استبدال السلسلة باستخدام تعبير عادي في المستند باستخدام السياق.

```

 // There is a several ways to replace string with regex in the document:
 String doc = getMyDir() + "Footer.docx";
 Pattern pattern = Pattern.compile("gr(a|e)y");
 String replacement = "lavender";

 ReplacerContext replacerContext = new ReplacerContext();
 replacerContext.setReplacement(pattern, replacement);
 replacerContext.getFindReplaceOptions().setFindWholeWordsOnly(false);

 Replacer.create(replacerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ReplaceContextRegex.docx")
         .execute();
 
```

يوضح كيفية استبدال السلسلة باستخدام تعبير عادي في المستند باستخدام المستندات من الدفق باستخدام السياق.

```

 // There is a several ways to replace string with regex in the document using documents from the stream:
 Pattern pattern = Pattern.compile("gr(a|e)y");
 String replacement = "lavender";

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Replace regex.docx")) {
     ReplacerContext replacerContext = new ReplacerContext();
     replacerContext.setReplacement(pattern, replacement);
     replacerContext.getFindReplaceOptions().setFindWholeWordsOnly(false);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.ReplaceContextStreamRegex.docx")) {
         Replacer.create(replacerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| context | [ReplacerContext](../../com.aspose.words/replacercontext/) |  |

**Returns:**
[Replacer](../../com.aspose.words/replacer/)
### execute() {#execute}
```
public void execute()
```


نفّذ إجراء المعالج.

 **Examples:** 

يعرض كيفية دمج المستندات في مستند إخراج واحد باستخدام السياق.

```

 //There is a several ways to merge documents:
 String inputDoc1 = getMyDir() + "Big document.docx";
 String inputDoc2 = getMyDir() + "Tables.docx";

 MergerContext mergerContext = new MergerContext();
 mergerContext.setMergeFormatMode(MergeFormatMode.KEEP_SOURCE_FORMATTING);

 Merger.create(mergerContext)
         .from(inputDoc1)
         .from(inputDoc2)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.1.docx")
         .execute();

 LoadOptions firstLoadOptions = new LoadOptions();
 {
     firstLoadOptions.setIgnoreOleData(true);
 }
 LoadOptions secondLoadOptions = new LoadOptions();
 {
     secondLoadOptions.setIgnoreOleData(false);
 }
 Merger.create(mergerContext)
         .from(inputDoc1, firstLoadOptions)
         .from(inputDoc2, secondLoadOptions)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.2.docx", SaveFormat.DOCX)
         .execute();

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 Merger.create(mergerContext)
         .from(inputDoc1)
         .from(inputDoc2)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.3.docx", saveOptions)
         .execute();
 
```

يعرض كيفية دمج المستندات من الدفق في مستند إخراج واحد باستخدام السياق.

```

 //There is a several ways to merge documents:
 String inputDoc1 = getMyDir() + "Big document.docx";
 String inputDoc2 = getMyDir() + "Tables.docx";

 MergerContext mergerContext = new MergerContext();
 mergerContext.setMergeFormatMode(MergeFormatMode.KEEP_SOURCE_FORMATTING);

 try (FileInputStream firstStreamIn = new FileInputStream(inputDoc1)) {
     try (FileInputStream secondStreamIn = new FileInputStream(inputDoc2)) {
         OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
         {
             saveOptions.setPassword("Aspose.Words");
         }
         try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.MergeStreamContextDocuments.1.docx")) {
             Merger.create(mergerContext)
                     .from(firstStreamIn)
                     .from(secondStreamIn)
                     .to(streamOut, saveOptions)
                     .execute();
         }

         LoadOptions firstLoadOptions = new LoadOptions();
         {
             firstLoadOptions.setIgnoreOleData(true);
         }
         LoadOptions secondLoadOptions = new LoadOptions();
         {
             secondLoadOptions.setIgnoreOleData(false);
         }
         try (FileOutputStream streamOut1 = new FileOutputStream(getArtifactsDir() + "LowCode.MergeStreamContextDocuments.2.docx")) {
             Merger.create(mergerContext)
                     .from(firstStreamIn, firstLoadOptions)
                     .from(secondStreamIn, secondLoadOptions)
                     .to(streamOut1, SaveFormat.DOCX)
                     .execute();
         }
     }
 }
 
```

يعرض كيفية تحويل المستندات بسطر واحد من الشيفرة باستخدام السياق.

```

 String doc = getMyDir() + "Big document.docx";

 ConverterContext converterContext = new ConverterContext();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.1.pdf")
         .execute();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.2.pdf", SaveFormat.RTF)
         .execute();

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 LoadOptions loadOptions = new LoadOptions();
 {
     loadOptions.setIgnoreOleData(true);
 }
 Converter.create(converterContext)
         .from(doc, loadOptions)
         .to(getArtifactsDir() + "LowCode.ConvertContext.3.docx", saveOptions)
         .execute();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.4.png", new ImageSaveOptions(SaveFormat.PNG))
         .execute();
 
```

يعرض كيفية تحويل المستندات من الدفق بسطر واحد من الشيفرة باستخدام السياق.

```

 String doc = getMyDir() + "Document.docx";
 ConverterContext converterContext = new ConverterContext();

 try (FileInputStream streamIn = new FileInputStream(doc)) {
     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.ConvertContextStream.1.docx")) {
         Converter.create(converterContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.RTF)
                 .execute();
     }

     OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
     {
         saveOptions.setPassword("Aspose.Words");
     }
     LoadOptions loadOptions = new LoadOptions();
     {
         loadOptions.setIgnoreOleData(true);
     }
     try (FileOutputStream streamOut1 = new FileOutputStream(getArtifactsDir() + "LowCode.ConvertContextStream.2.docx")) {
         Converter.create(converterContext)
                 .from(streamIn, loadOptions)
                 .to(streamOut1, saveOptions)
                 .execute();
     }
 }
 
```

### from(InputStream input) {#from-java.io.InputStream}
```
public Processor from(InputStream input)
```


يحدد المستند الإدخالي للمعالجة.

 **Remarks:** 

إذا كان المعالج يقبل ملفًا واحدًا فقط كإدخال، فسيتم معالجة الملف الأخير المحدد فقط. معالج [Merger](../../com.aspose.words/merger/) يقبل ملفات متعددة كإدخال، وبالتالي سيتم دمج جميع المستندات المحددة. معالج [Converter](../../com.aspose.words/converter/) يقبل ملفًا واحدًا فقط كإدخال، لذا سيتم تحويل الملف الأخير المحدد فقط.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| إدخال | java.io.InputStream | دفق مستند الإدخال. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file stream.
### from(InputStream input, LoadOptions loadOptions) {#from-java.io.InputStream-com.aspose.words.LoadOptions}
```
public Processor from(InputStream input, LoadOptions loadOptions)
```


يحدد المستند الإدخالي للمعالجة.

 **Remarks:** 

إذا كان المعالج يقبل ملفًا واحدًا فقط كإدخال، فسيتم معالجة الملف الأخير المحدد فقط. معالج [Merger](../../com.aspose.words/merger/) يقبل ملفات متعددة كإدخال، وبالتالي سيتم دمج جميع المستندات المحددة. معالج [Converter](../../com.aspose.words/converter/) يقبل ملفًا واحدًا فقط كإدخال، لذا سيتم تحويل الملف الأخير المحدد فقط.

 **Examples:** 

يعرض كيفية دمج المستندات من الدفق في مستند إخراج واحد باستخدام السياق.

```

 //There is a several ways to merge documents:
 String inputDoc1 = getMyDir() + "Big document.docx";
 String inputDoc2 = getMyDir() + "Tables.docx";

 MergerContext mergerContext = new MergerContext();
 mergerContext.setMergeFormatMode(MergeFormatMode.KEEP_SOURCE_FORMATTING);

 try (FileInputStream firstStreamIn = new FileInputStream(inputDoc1)) {
     try (FileInputStream secondStreamIn = new FileInputStream(inputDoc2)) {
         OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
         {
             saveOptions.setPassword("Aspose.Words");
         }
         try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.MergeStreamContextDocuments.1.docx")) {
             Merger.create(mergerContext)
                     .from(firstStreamIn)
                     .from(secondStreamIn)
                     .to(streamOut, saveOptions)
                     .execute();
         }

         LoadOptions firstLoadOptions = new LoadOptions();
         {
             firstLoadOptions.setIgnoreOleData(true);
         }
         LoadOptions secondLoadOptions = new LoadOptions();
         {
             secondLoadOptions.setIgnoreOleData(false);
         }
         try (FileOutputStream streamOut1 = new FileOutputStream(getArtifactsDir() + "LowCode.MergeStreamContextDocuments.2.docx")) {
             Merger.create(mergerContext)
                     .from(firstStreamIn, firstLoadOptions)
                     .from(secondStreamIn, secondLoadOptions)
                     .to(streamOut1, SaveFormat.DOCX)
                     .execute();
         }
     }
 }
 
```

يعرض كيفية تحويل المستندات من الدفق بسطر واحد من الشيفرة باستخدام السياق.

```

 String doc = getMyDir() + "Document.docx";
 ConverterContext converterContext = new ConverterContext();

 try (FileInputStream streamIn = new FileInputStream(doc)) {
     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.ConvertContextStream.1.docx")) {
         Converter.create(converterContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.RTF)
                 .execute();
     }

     OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
     {
         saveOptions.setPassword("Aspose.Words");
     }
     LoadOptions loadOptions = new LoadOptions();
     {
         loadOptions.setIgnoreOleData(true);
     }
     try (FileOutputStream streamOut1 = new FileOutputStream(getArtifactsDir() + "LowCode.ConvertContextStream.2.docx")) {
         Converter.create(converterContext)
                 .from(streamIn, loadOptions)
                 .to(streamOut1, saveOptions)
                 .execute();
     }
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| إدخال | java.io.InputStream | دفق مستند الإدخال. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | خيارات التحميل الاختيارية المستخدمة لتحميل المستند. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file stream.
### from(String input) {#from-java.lang.String}
```
public Processor from(String input)
```


يحدد المستند الإدخالي للمعالجة.

 **Remarks:** 

إذا كان المعالج يقبل ملفًا واحدًا فقط كإدخال، فسيتم معالجة الملف الأخير المحدد فقط. معالج [Merger](../../com.aspose.words/merger/) يقبل ملفات متعددة كإدخال، وبالتالي سيتم دمج جميع المستندات المحددة. معالج [Converter](../../com.aspose.words/converter/) يقبل ملفًا واحدًا فقط كإدخال، لذا سيتم تحويل الملف الأخير المحدد فقط.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| إدخال | java.lang.String | اسم ملف مستند الإدخال. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file.
### from(String input, LoadOptions loadOptions) {#from-java.lang.String-com.aspose.words.LoadOptions}
```
public Processor from(String input, LoadOptions loadOptions)
```


يحدد المستند الإدخالي للمعالجة.

 **Remarks:** 

إذا كان المعالج يقبل ملفًا واحدًا فقط كإدخال، فسيتم معالجة الملف الأخير المحدد فقط. معالج [Merger](../../com.aspose.words/merger/) يقبل ملفات متعددة كإدخال، وبالتالي سيتم دمج جميع المستندات المحددة. معالج [Converter](../../com.aspose.words/converter/) يقبل ملفًا واحدًا فقط كإدخال، لذا سيتم تحويل الملف الأخير المحدد فقط.

 **Examples:** 

يعرض كيفية دمج المستندات في مستند إخراج واحد باستخدام السياق.

```

 //There is a several ways to merge documents:
 String inputDoc1 = getMyDir() + "Big document.docx";
 String inputDoc2 = getMyDir() + "Tables.docx";

 MergerContext mergerContext = new MergerContext();
 mergerContext.setMergeFormatMode(MergeFormatMode.KEEP_SOURCE_FORMATTING);

 Merger.create(mergerContext)
         .from(inputDoc1)
         .from(inputDoc2)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.1.docx")
         .execute();

 LoadOptions firstLoadOptions = new LoadOptions();
 {
     firstLoadOptions.setIgnoreOleData(true);
 }
 LoadOptions secondLoadOptions = new LoadOptions();
 {
     secondLoadOptions.setIgnoreOleData(false);
 }
 Merger.create(mergerContext)
         .from(inputDoc1, firstLoadOptions)
         .from(inputDoc2, secondLoadOptions)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.2.docx", SaveFormat.DOCX)
         .execute();

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 Merger.create(mergerContext)
         .from(inputDoc1)
         .from(inputDoc2)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.3.docx", saveOptions)
         .execute();
 
```

يعرض كيفية تحويل المستندات بسطر واحد من الشيفرة باستخدام السياق.

```

 String doc = getMyDir() + "Big document.docx";

 ConverterContext converterContext = new ConverterContext();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.1.pdf")
         .execute();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.2.pdf", SaveFormat.RTF)
         .execute();

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 LoadOptions loadOptions = new LoadOptions();
 {
     loadOptions.setIgnoreOleData(true);
 }
 Converter.create(converterContext)
         .from(doc, loadOptions)
         .to(getArtifactsDir() + "LowCode.ConvertContext.3.docx", saveOptions)
         .execute();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.4.png", new ImageSaveOptions(SaveFormat.PNG))
         .execute();
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| إدخال | java.lang.String | اسم ملف مستند الإدخال. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | خيارات التحميل الاختيارية المستخدمة لتحميل المستند. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file.
### replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String pattern, String replacement) {#replace-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String-java.lang.String}
```
public static int replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String pattern, String replacement)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| نمط | java.lang.String |  |
| استبدال | java.lang.String |  |

**Returns:**
int
### replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options) {#replace-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static int replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| نمط | java.lang.String |  |
| استبدال | java.lang.String |  |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) |  |

**Returns:**
int
### replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Pattern pattern, String replacement) {#replace-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.util.regex.Pattern-java.lang.String}
```
public static int replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Pattern pattern, String replacement)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| نمط | java.util.regex.Pattern |  |
| استبدال | java.lang.String |  |

**Returns:**
int
### replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options) {#replace-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static int replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| نمط | java.util.regex.Pattern |  |
| استبدال | java.lang.String |  |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) |  |

**Returns:**
int
### replace(InputStream inputStream, OutputStream outputStream, int saveFormat, String pattern, String replacement) {#replace-java.io.InputStream-java.io.OutputStream-int-java.lang.String-java.lang.String}
```
public static int replace(InputStream inputStream, OutputStream outputStream, int saveFormat, String pattern, String replacement)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| نمط | java.lang.String |  |
| استبدال | java.lang.String |  |

**Returns:**
int
### replace(InputStream inputStream, OutputStream outputStream, int saveFormat, String pattern, String replacement, FindReplaceOptions options) {#replace-java.io.InputStream-java.io.OutputStream-int-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static int replace(InputStream inputStream, OutputStream outputStream, int saveFormat, String pattern, String replacement, FindReplaceOptions options)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| نمط | java.lang.String |  |
| استبدال | java.lang.String |  |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) |  |

**Returns:**
int
### replace(InputStream inputStream, OutputStream outputStream, int saveFormat, Pattern pattern, String replacement) {#replace-java.io.InputStream-java.io.OutputStream-int-java.util.regex.Pattern-java.lang.String}
```
public static int replace(InputStream inputStream, OutputStream outputStream, int saveFormat, Pattern pattern, String replacement)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| نمط | java.util.regex.Pattern |  |
| استبدال | java.lang.String |  |

**Returns:**
int
### replace(InputStream inputStream, OutputStream outputStream, int saveFormat, Pattern pattern, String replacement, FindReplaceOptions options) {#replace-java.io.InputStream-java.io.OutputStream-int-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static int replace(InputStream inputStream, OutputStream outputStream, int saveFormat, Pattern pattern, String replacement, FindReplaceOptions options)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| نمط | java.util.regex.Pattern |  |
| استبدال | java.lang.String |  |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) |  |

**Returns:**
int
### replace(String inputFileName, String outputFileName, SaveOptions saveOptions, String pattern, String replacement) {#replace-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-java.lang.String}
```
public static int replace(String inputFileName, String outputFileName, SaveOptions saveOptions, String pattern, String replacement)
```


يستبدل جميع تكرارات نمط سلسلة الأحرف المحدد بسلسلة استبدال في ملف الإدخال، مع تنسيق الحفظ المحدد وخيارات إضافية.

 **Remarks:** 

إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile\_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String | اسم ملف الإدخال. |
| outputFileName | java.lang.String | اسم ملف الإخراج. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | خيارات الحفظ. |
| نمط | java.lang.String | سلسلة لتستبدل. |
| استبدال | java.lang.String | سلسلة لاستبدال جميع تكرارات النمط. |

**Returns:**
int - عدد الاستبدالات التي تم إجراؤها.
### replace(String inputFileName, String outputFileName, SaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options) {#replace-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static int replace(String inputFileName, String outputFileName, SaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options)
```


يستبدل جميع تكرارات نمط سلسلة الأحرف المحدد بسلسلة استبدال في ملف الإدخال، مع تنسيق الحفظ المحدد وخيارات إضافية.

 **Remarks:** 

إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile\_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String | اسم ملف الإدخال. |
| outputFileName | java.lang.String | اسم ملف الإخراج. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | خيارات الحفظ. |
| نمط | java.lang.String | سلسلة لتستبدل. |
| استبدال | java.lang.String | سلسلة لاستبدال جميع تكرارات النمط. |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) كائن لتحديد خيارات إضافية. |

**Returns:**
int - عدد الاستبدالات التي تم إجراؤها.
### replace(String inputFileName, String outputFileName, SaveOptions saveOptions, Pattern pattern, String replacement) {#replace-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.util.regex.Pattern-java.lang.String}
```
public static int replace(String inputFileName, String outputFileName, SaveOptions saveOptions, Pattern pattern, String replacement)
```


يستبدل جميع تكرارات نمط سلسلة الأحرف المحدد بسلسلة استبدال في ملف الإدخال باستخدام تعبير عادي، مع تنسيق الحفظ المحدد وخيارات إضافية.

 **Remarks:** 

إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile\_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String | اسم ملف الإدخال. |
| outputFileName | java.lang.String | اسم ملف الإخراج. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | خيارات الحفظ. |
| نمط | java.util.regex.Pattern | نمط تعبير عادي يُستخدم للعثور على التطابقات. |
| استبدال | java.lang.String | سلسلة لاستبدال جميع تكرارات النمط. |

**Returns:**
int - عدد الاستبدالات التي تم إجراؤها.
### replace(String inputFileName, String outputFileName, SaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options) {#replace-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static int replace(String inputFileName, String outputFileName, SaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options)
```


يستبدل جميع تكرارات نمط سلسلة الأحرف المحدد بسلسلة استبدال في ملف الإدخال باستخدام تعبير عادي، مع تنسيق الحفظ المحدد وخيارات إضافية.

 **Remarks:** 

إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile\_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String | اسم ملف الإدخال. |
| outputFileName | java.lang.String | اسم ملف الإخراج. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | خيارات الحفظ. |
| نمط | java.util.regex.Pattern | نمط تعبير عادي يُستخدم للعثور على التطابقات. |
| استبدال | java.lang.String | سلسلة لاستبدال جميع تكرارات النمط. |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) كائن لتحديد خيارات إضافية. |

**Returns:**
int - عدد الاستبدالات التي تم إجراؤها.
### replace(String inputFileName, String outputFileName, int saveFormat, String pattern, String replacement) {#replace-java.lang.String-java.lang.String-int-java.lang.String-java.lang.String}
```
public static int replace(String inputFileName, String outputFileName, int saveFormat, String pattern, String replacement)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| نمط | java.lang.String |  |
| استبدال | java.lang.String |  |

**Returns:**
int
### replace(String inputFileName, String outputFileName, int saveFormat, String pattern, String replacement, FindReplaceOptions options) {#replace-java.lang.String-java.lang.String-int-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static int replace(String inputFileName, String outputFileName, int saveFormat, String pattern, String replacement, FindReplaceOptions options)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| نمط | java.lang.String |  |
| استبدال | java.lang.String |  |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) |  |

**Returns:**
int
### replace(String inputFileName, String outputFileName, int saveFormat, Pattern pattern, String replacement) {#replace-java.lang.String-java.lang.String-int-java.util.regex.Pattern-java.lang.String}
```
public static int replace(String inputFileName, String outputFileName, int saveFormat, Pattern pattern, String replacement)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| نمط | java.util.regex.Pattern |  |
| استبدال | java.lang.String |  |

**Returns:**
int
### replace(String inputFileName, String outputFileName, int saveFormat, Pattern pattern, String replacement, FindReplaceOptions options) {#replace-java.lang.String-java.lang.String-int-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static int replace(String inputFileName, String outputFileName, int saveFormat, Pattern pattern, String replacement, FindReplaceOptions options)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| نمط | java.util.regex.Pattern |  |
| استبدال | java.lang.String |  |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) |  |

**Returns:**
int
### replace(String inputFileName, String outputFileName, String pattern, String replacement) {#replace-java.lang.String-java.lang.String-java.lang.String-java.lang.String}
```
public static int replace(String inputFileName, String outputFileName, String pattern, String replacement)
```


يستبدل جميع تكرارات نمط سلسلة الأحرف المحدد بسلسلة استبدال في ملف الإدخال.

 **Remarks:** 

إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile\_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

 **Examples:** 

يوضح كيفية استبدال السلسلة في المستند.

```

 // There is a several ways to replace string in the document:
 String doc = getMyDir() + "Footer.docx";
 String pattern = "(C)2006 Aspose Pty Ltd.";
 String replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

 FindReplaceOptions options = new FindReplaceOptions();
 options.setFindWholeWordsOnly(false);
 Replacer.replace(doc, getArtifactsDir() + "LowCode.Replace.1.docx", pattern, replacement);
 Replacer.replace(doc, getArtifactsDir() + "LowCode.Replace.2.docx", SaveFormat.DOCX, pattern, replacement);
 Replacer.replace(doc, getArtifactsDir() + "LowCode.Replace.3.docx", SaveFormat.DOCX, pattern, replacement, options);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String | اسم ملف الإدخال. |
| outputFileName | java.lang.String | اسم ملف الإخراج. |
| نمط | java.lang.String | سلسلة لتستبدل. |
| استبدال | java.lang.String | سلسلة لاستبدال جميع تكرارات النمط. |

**Returns:**
int - عدد الاستبدالات التي تم إجراؤها.
### replace(String inputFileName, String outputFileName, Pattern pattern, String replacement) {#replace-java.lang.String-java.lang.String-java.util.regex.Pattern-java.lang.String}
```
public static int replace(String inputFileName, String outputFileName, Pattern pattern, String replacement)
```


يستبدل جميع تكرارات نمط سلسلة الأحرف المحدد بسلسلة استبدال في ملف الإدخال باستخدام تعبير عادي.

 **Remarks:** 

إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile\_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

 **Examples:** 

يوضح كيفية استبدال السلسلة باستخدام تعبير عادي في المستند.

```

 // There is a several ways to replace string with regex in the document:
 String doc = getMyDir() + "Footer.docx";
 String pattern = "gr(a|e)y";
 String replacement = "lavender";

 Replacer.replace(doc, getArtifactsDir() + "LowCode.ReplaceRegex.1.docx", pattern, replacement);
 Replacer.replace(doc, getArtifactsDir() + "LowCode.ReplaceRegex.2.docx", SaveFormat.DOCX, pattern, replacement);
 FindReplaceOptions options = new FindReplaceOptions();
 options.setFindWholeWordsOnly(false);
 Replacer.replace(doc, getArtifactsDir() + "LowCode.ReplaceRegex.3.docx", SaveFormat.DOCX, pattern, replacement, options);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String | اسم ملف الإدخال. |
| outputFileName | java.lang.String | اسم ملف الإخراج. |
| نمط | java.util.regex.Pattern | نمط تعبير عادي يُستخدم للعثور على التطابقات. |
| استبدال | java.lang.String | سلسلة لاستبدال جميع تكرارات النمط. |

**Returns:**
int - عدد الاستبدالات التي تم إجراؤها.
### replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, String pattern, String replacement) {#replaceToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String-java.lang.String}
```
public static OutputStream[] replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, String pattern, String replacement)
```


يستبدل جميع تكرارات نمط سلسلة الأحرف المحدد بسلسلة استبدال في ملف الإدخال. يُظهر المخرجات كصور.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream | دفق ملف الإدخال. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | خيارات الحفظ. |
| نمط | java.lang.String | سلسلة لتستبدل. |
| استبدال | java.lang.String | سلسلة لاستبدال جميع تكرارات النمط. |

**Returns:**
java.io.OutputStream[]
### replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options) {#replaceToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static OutputStream[] replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options)
```


يستبدل جميع تكرارات نمط سلسلة الأحرف المحدد بسلسلة استبدال في ملف الإدخال. يُظهر المخرجات كصور.

 **Examples:** 

يوضح كيفية استبدال السلسلة في المستند باستخدام المستندات من الدفق وحفظ النتيجة كصور.

```

 // There is a several ways to replace string in the document using documents from the stream:
 String pattern = "(C)2006 Aspose Pty Ltd.";
 String replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Footer.docx")) {
     OutputStream[] images = Replacer.replaceToImages(streamIn, new ImageSaveOptions(SaveFormat.PNG), pattern, replacement);

     FindReplaceOptions options = new FindReplaceOptions();
     options.setFindWholeWordsOnly(false);
     images = Replacer.replaceToImages(streamIn, new ImageSaveOptions(SaveFormat.PNG), pattern, replacement, options);
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream | دفق ملف الإدخال. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | خيارات الحفظ. |
| نمط | java.lang.String | سلسلة لتستبدل. |
| استبدال | java.lang.String | سلسلة لاستبدال جميع تكرارات النمط. |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) كائن لتحديد خيارات إضافية. |

**Returns:**
java.io.OutputStream[]
### replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, Pattern pattern, String replacement) {#replaceToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.util.regex.Pattern-java.lang.String}
```
public static OutputStream[] replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, Pattern pattern, String replacement)
```


يستبدل جميع تكرارات نمط التعبير العادي المحدد بسلسلة استبدال في ملف الإدخال. يُظهر المخرجات كصور.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream | دفق ملف الإدخال. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | خيارات الحفظ. |
| نمط | java.util.regex.Pattern | نمط تعبير عادي يُستخدم للعثور على التطابقات. |
| استبدال | java.lang.String | سلسلة لاستبدال جميع تكرارات النمط. |

**Returns:**
java.io.OutputStream[]
### replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options) {#replaceToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static OutputStream[] replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options)
```


يستبدل جميع تكرارات نمط التعبير العادي المحدد بسلسلة استبدال في ملف الإدخال. يُظهر المخرجات كصور.

 **Examples:** 

يعرض كيفية استبدال النص باستخدام regex في المستند باستخدام المستندات من الدفق وحفظ النتيجة كصور.

```

 // There is a several ways to replace string with regex in the document using documents from the stream:
 Pattern pattern = Pattern.compile("gr(a|e)y");
 String replacement = "lavender";

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Replace regex.docx")) {
     OutputStream[] images = Replacer.replaceToImages(streamIn, new ImageSaveOptions(SaveFormat.PNG), pattern, replacement);
     FindReplaceOptions options = new FindReplaceOptions();
     options.setFindWholeWordsOnly(false);
     images = Replacer.replaceToImages(streamIn, new ImageSaveOptions(SaveFormat.PNG), pattern, replacement, options);
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream | دفق ملف الإدخال. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | خيارات الحفظ. |
| نمط | java.util.regex.Pattern | نمط تعبير عادي يُستخدم للعثور على التطابقات. |
| استبدال | java.lang.String | سلسلة لاستبدال جميع تكرارات النمط. |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) كائن لتحديد خيارات إضافية. |

**Returns:**
java.io.OutputStream[]
### replaceToImages(String inputFileName, ImageSaveOptions saveOptions, String pattern, String replacement) {#replaceToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String-java.lang.String}
```
public static OutputStream[] replaceToImages(String inputFileName, ImageSaveOptions saveOptions, String pattern, String replacement)
```


يستبدل جميع تكرارات نمط سلسلة الأحرف المحدد بسلسلة استبدال في ملف الإدخال. يُظهر المخرجات كصور.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String | اسم ملف الإدخال. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | خيارات الحفظ. |
| نمط | java.lang.String | سلسلة لتستبدل. |
| استبدال | java.lang.String | سلسلة لاستبدال جميع تكرارات النمط. |

**Returns:**
java.io.OutputStream[]
### replaceToImages(String inputFileName, ImageSaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options) {#replaceToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static OutputStream[] replaceToImages(String inputFileName, ImageSaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options)
```


يستبدل جميع تكرارات نمط سلسلة الأحرف المحدد بسلسلة استبدال في ملف الإدخال. يُظهر المخرجات كصور.

 **Examples:** 

يعرض كيفية استبدال النص في المستند وحفظ النتيجة كصور.

```

 // There is a several ways to replace string in the document:
 String doc = getMyDir() + "Footer.docx";
 String pattern = "(C)2006 Aspose Pty Ltd.";
 String replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

 OutputStream[] images = Replacer.replaceToImages(doc, new ImageSaveOptions(SaveFormat.PNG), pattern, replacement);

 FindReplaceOptions options = new FindReplaceOptions();
 options.setFindWholeWordsOnly(false);
 images = Replacer.replaceToImages(doc, new ImageSaveOptions(SaveFormat.PNG), pattern, replacement, options);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String | اسم ملف الإدخال. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | خيارات الحفظ. |
| نمط | java.lang.String | سلسلة لتستبدل. |
| استبدال | java.lang.String | سلسلة لاستبدال جميع تكرارات النمط. |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) كائن لتحديد خيارات إضافية. |

**Returns:**
java.io.OutputStream[]
### replaceToImages(String inputFileName, ImageSaveOptions saveOptions, Pattern pattern, String replacement) {#replaceToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.util.regex.Pattern-java.lang.String}
```
public static OutputStream[] replaceToImages(String inputFileName, ImageSaveOptions saveOptions, Pattern pattern, String replacement)
```


يستبدل جميع تكرارات نمط التعبير العادي المحدد بسلسلة استبدال في ملف الإدخال. يُظهر المخرجات كصور.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String | اسم ملف الإدخال. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | خيارات الحفظ. |
| نمط | java.util.regex.Pattern | نمط تعبير عادي يُستخدم للعثور على التطابقات. |
| استبدال | java.lang.String | سلسلة لاستبدال جميع تكرارات النمط. |

**Returns:**
java.io.OutputStream[]
### replaceToImages(String inputFileName, ImageSaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options) {#replaceToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static OutputStream[] replaceToImages(String inputFileName, ImageSaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options)
```


يستبدل جميع تكرارات نمط التعبير العادي المحدد بسلسلة استبدال في ملف الإدخال. يُظهر المخرجات كصور.

 **Examples:** 

يعرض كيفية استبدال النص باستخدام regex في المستند وحفظ النتيجة كصور.

```

 // There is a several ways to replace string with regex in the document:
 String doc = getMyDir() + "Footer.docx";
 Pattern pattern = Pattern.compile("gr(a|e)y");
 String replacement = "lavender";

 OutputStream[] images = Replacer.replaceToImages(doc, new ImageSaveOptions(SaveFormat.PNG), pattern, replacement);
 FindReplaceOptions options = new FindReplaceOptions();
 options.setFindWholeWordsOnly(false);
 images = Replacer.replaceToImages(doc, new ImageSaveOptions(SaveFormat.PNG), pattern, replacement, options);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String | اسم ملف الإدخال. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | خيارات الحفظ. |
| نمط | java.util.regex.Pattern | نمط تعبير عادي يُستخدم للعثور على التطابقات. |
| استبدال | java.lang.String | سلسلة لاستبدال جميع تكرارات النمط. |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) كائن لتحديد خيارات إضافية. |

**Returns:**
java.io.OutputStream[]
### to(OutputStream output, SaveOptions saveOptions) {#to-java.io.OutputStream-com.aspose.words.SaveOptions}
```
public Processor to(OutputStream output, SaveOptions saveOptions)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| إخراج | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(OutputStream output, int saveFormat) {#to-java.io.OutputStream-int}
```
public Processor to(OutputStream output, int saveFormat)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| إخراج | java.io.OutputStream |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(String output) {#to-java.lang.String}
```
public Processor to(String output)
```


يحدد ملف الإخراج للمعالج.

 **Remarks:** 

إذا كان الإخراج يتكون من ملفات متعددة، يتم استخدام اسم ملف الإخراج المحدد لتوليد اسم الملف لكل جزء وفق القاعدة: 'outputFile\_partIndex.extension'.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| إخراج | java.lang.String | اسم ملف الإخراج. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified output file.
### to(String output, SaveOptions saveOptions) {#to-java.lang.String-com.aspose.words.SaveOptions}
```
public Processor to(String output, SaveOptions saveOptions)
```


يحدد ملف الإخراج للمعالج.

 **Remarks:** 

إذا كان الإخراج يتكون من ملفات متعددة، يتم استخدام اسم ملف الإخراج المحدد لتوليد اسم الملف لكل جزء وفق القاعدة: 'outputFile\_partIndex.extension'.

 **Examples:** 

يعرض كيفية دمج المستندات في مستند إخراج واحد باستخدام السياق.

```

 //There is a several ways to merge documents:
 String inputDoc1 = getMyDir() + "Big document.docx";
 String inputDoc2 = getMyDir() + "Tables.docx";

 MergerContext mergerContext = new MergerContext();
 mergerContext.setMergeFormatMode(MergeFormatMode.KEEP_SOURCE_FORMATTING);

 Merger.create(mergerContext)
         .from(inputDoc1)
         .from(inputDoc2)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.1.docx")
         .execute();

 LoadOptions firstLoadOptions = new LoadOptions();
 {
     firstLoadOptions.setIgnoreOleData(true);
 }
 LoadOptions secondLoadOptions = new LoadOptions();
 {
     secondLoadOptions.setIgnoreOleData(false);
 }
 Merger.create(mergerContext)
         .from(inputDoc1, firstLoadOptions)
         .from(inputDoc2, secondLoadOptions)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.2.docx", SaveFormat.DOCX)
         .execute();

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 Merger.create(mergerContext)
         .from(inputDoc1)
         .from(inputDoc2)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.3.docx", saveOptions)
         .execute();
 
```

يعرض كيفية تحويل المستندات بسطر واحد من الشيفرة باستخدام السياق.

```

 String doc = getMyDir() + "Big document.docx";

 ConverterContext converterContext = new ConverterContext();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.1.pdf")
         .execute();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.2.pdf", SaveFormat.RTF)
         .execute();

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 LoadOptions loadOptions = new LoadOptions();
 {
     loadOptions.setIgnoreOleData(true);
 }
 Converter.create(converterContext)
         .from(doc, loadOptions)
         .to(getArtifactsDir() + "LowCode.ConvertContext.3.docx", saveOptions)
         .execute();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.4.png", new ImageSaveOptions(SaveFormat.PNG))
         .execute();
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| إخراج | java.lang.String | اسم ملف الإخراج. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | خيارات الحفظ الاختيارية. إذا لم يتم تحديدها، يتم تحديد تنسيق الحفظ بناءً على امتداد الملف. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified output file.
### to(String output, int saveFormat) {#to-java.lang.String-int}
```
public Processor to(String output, int saveFormat)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| إخراج | java.lang.String |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(ArrayList output, SaveOptions saveOptions) {#to-java.util.ArrayList-com.aspose.words.SaveOptions}
```
public Processor to(ArrayList output, SaveOptions saveOptions)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| إخراج | java.util.ArrayList |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(ArrayList output, int saveFormat) {#to-java.util.ArrayList-int}
```
public Processor to(ArrayList output, int saveFormat)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| إخراج | java.util.ArrayList |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### toOutput(ArrayList output, SaveOptions saveOptions) {#toOutput-java.util.ArrayList-com.aspose.words.SaveOptions}
```
public Processor toOutput(ArrayList output, SaveOptions saveOptions)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| إخراج | java.util.ArrayList |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### toOutput(ArrayList output, int saveFormat) {#toOutput-java.util.ArrayList-int}
```
public Processor toOutput(ArrayList output, int saveFormat)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| إخراج | java.util.ArrayList |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
