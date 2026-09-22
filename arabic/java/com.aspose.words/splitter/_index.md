---
title: "Splitter"
linktitle: "Splitter"
second_title: "Aspose.Words لـ Java"
description: "يوفر طرقًا تهدف إلى تقسيم المستندات إلى أجزاء باستخدام معايير مختلفة في Java."
type: docs
weight: 631
url: /ar/java/com.aspose.words/splitter/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Processor](../../com.aspose.words/processor/)
```
public class Splitter extends Processor
```

يوفر طرقًا تهدف إلى تقسيم المستندات إلى أجزاء باستخدام معايير مختلفة.
## الطرق

| طريقة | الوصف |
| --- | --- |
| [create(SplitterContext context)](#create-com.aspose.words.SplitterContext) | ينشئ مثيلًا جديدًا لمعالج القسّام. |
| [execute()](#execute) | نفّذ إجراء المعالج. |
| [extractPages(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, int startPageIndex, int pageCount)](#extractPages-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-int-int) |  |
| [extractPages(InputStream inputStream, OutputStream outputStream, int saveFormat, int startPageIndex, int pageCount)](#extractPages-java.io.InputStream-java.io.OutputStream-int-int-int) |  |
| [extractPages(String inputFileName, String outputFileName, SaveOptions saveOptions, int startPageIndex, int pageCount)](#extractPages-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-int-int) | يستخرج نطاقًا محددًا من الصفحات من ملف مستند ويحفظ الصفحات المستخرجة في ملف جديد باستخدام تنسيق الحفظ المحدد. |
| [extractPages(String inputFileName, String outputFileName, int startPageIndex, int pageCount)](#extractPages-java.lang.String-java.lang.String-int-int) | يستخرج نطاقًا محددًا من الصفحات من ملف مستند ويحفظ الصفحات المستخرجة في ملف جديد. |
| [extractPages(String inputFileName, String outputFileName, int saveFormat, int startPageIndex, int pageCount)](#extractPages-java.lang.String-java.lang.String-int-int-int) |  |
| [from(InputStream input)](#from-java.io.InputStream) | يحدد المستند الإدخالي للمعالجة. |
| [from(InputStream input, LoadOptions loadOptions)](#from-java.io.InputStream-com.aspose.words.LoadOptions) | يحدد المستند الإدخالي للمعالجة. |
| [from(String input)](#from-java.lang.String) | يحدد المستند الإدخالي للمعالجة. |
| [from(String input, LoadOptions loadOptions)](#from-java.lang.String-com.aspose.words.LoadOptions) | يحدد المستند الإدخالي للمعالجة. |
| [removeBlankPages(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions)](#removeBlankPages-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [removeBlankPages(InputStream inputStream, OutputStream outputStream, int saveFormat)](#removeBlankPages-java.io.InputStream-java.io.OutputStream-int) |  |
| [removeBlankPages(String inputFileName, String outputFileName)](#removeBlankPages-java.lang.String-java.lang.String) | يزيل الصفحات الفارغة من المستند ويحفظ الناتج. |
| [removeBlankPages(String inputFileName, String outputFileName, SaveOptions saveOptions)](#removeBlankPages-java.lang.String-java.lang.String-com.aspose.words.SaveOptions) | يزيل الصفحات الفارغة من المستند ويحفظ الناتج بالتنسيق المحدد. |
| [removeBlankPages(String inputFileName, String outputFileName, int saveFormat)](#removeBlankPages-java.lang.String-java.lang.String-int) |  |
| [split(InputStream inputStream, SaveOptions saveOptions, SplitOptions options)](#split-java.io.InputStream-com.aspose.words.SaveOptions-com.aspose.words.SplitOptions) | يقسم مستندًا من تدفق إدخال إلى أجزاء متعددة بناءً على خيارات التقسيم المحددة ويعيد الأجزاء الناتجة كمصفوفة من التدفقات بالتنسيق المحدد للحفظ. |
| [split(InputStream inputStream, int saveFormat, SplitOptions options)](#split-java.io.InputStream-int-com.aspose.words.SplitOptions) |  |
| [split(String inputFileName, String outputFileName, SaveOptions saveOptions, SplitOptions options)](#split-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.SplitOptions) | يقسم مستندًا إلى أجزاء متعددة بناءً على خيارات التقسيم المحددة ويحفظ الأجزاء الناتجة في ملفات بالتنسيق المحدد للحفظ. |
| [split(String inputFileName, String outputFileName, SplitOptions options)](#split-java.lang.String-java.lang.String-com.aspose.words.SplitOptions) | يقسم مستندًا إلى أجزاء متعددة بناءً على خيارات التقسيم المحددة ويحفظ الأجزاء الناتجة في ملفات. |
| [split(String inputFileName, String outputFileName, int saveFormat, SplitOptions options)](#split-java.lang.String-java.lang.String-int-com.aspose.words.SplitOptions) |  |
| [to(OutputStream output, SaveOptions saveOptions)](#to-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [to(OutputStream output, int saveFormat)](#to-java.io.OutputStream-int) |  |
| [to(String output)](#to-java.lang.String) | يحدد ملف الإخراج للمعالج. |
| [to(String output, SaveOptions saveOptions)](#to-java.lang.String-com.aspose.words.SaveOptions) | يحدد ملف الإخراج للمعالج. |
| [to(String output, int saveFormat)](#to-java.lang.String-int) |  |
| [to(ArrayList output, SaveOptions saveOptions)](#to-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [to(ArrayList output, int saveFormat)](#to-java.util.ArrayList-int) |  |
| [toOutput(ArrayList output, SaveOptions saveOptions)](#toOutput-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [toOutput(ArrayList output, int saveFormat)](#toOutput-java.util.ArrayList-int) |  |
### create(SplitterContext context) {#create-com.aspose.words.SplitterContext}
```
public static Splitter create(SplitterContext context)
```


ينشئ مثيلًا جديدًا لمعالج القسّام.

 **Examples:** 

يعرض كيفية تقسيم المستند إلى صفحات باستخدام السياق.

```

 String doc = getMyDir() + "Big document.docx";

 SplitterContext splitterContext = new SplitterContext();
 splitterContext.getSplitOptions().setSplitCriteria(SplitCriteria.PAGE);

 Splitter.create(splitterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.SplitContextDocument.docx")
         .execute();
 
```

يعرض كيفية تقسيم المستند من الدفق إلى صفحات باستخدام السياق.

```

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Big document.docx")) {
     SplitterContext splitterContext = new SplitterContext();
     splitterContext.getSplitOptions().setSplitCriteria(SplitCriteria.PAGE);

     ArrayList pages = new ArrayList<>();
     Splitter.create(splitterContext)
             .from(streamIn)
             .toOutput(pages, SaveFormat.DOCX)
             .execute();
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| context | [SplitterContext](../../com.aspose.words/splittercontext/) |  |

**Returns:**
[Splitter](../../com.aspose.words/splitter/)
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

### extractPages(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, int startPageIndex, int pageCount) {#extractPages-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-int-int}
```
public static void extractPages(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, int startPageIndex, int pageCount)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| startPageIndex | int |  |
| pageCount | int |  |

### extractPages(InputStream inputStream, OutputStream outputStream, int saveFormat, int startPageIndex, int pageCount) {#extractPages-java.io.InputStream-java.io.OutputStream-int-int-int}
```
public static void extractPages(InputStream inputStream, OutputStream outputStream, int saveFormat, int startPageIndex, int pageCount)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| startPageIndex | int |  |
| pageCount | int |  |

### extractPages(String inputFileName, String outputFileName, SaveOptions saveOptions, int startPageIndex, int pageCount) {#extractPages-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-int-int}
```
public static void extractPages(String inputFileName, String outputFileName, SaveOptions saveOptions, int startPageIndex, int pageCount)
```


يستخرج نطاقًا محددًا من الصفحات من ملف مستند ويحفظ الصفحات المستخرجة في ملف جديد باستخدام تنسيق الحفظ المحدد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String | اسم ملف الإدخال. |
| outputFileName | java.lang.String | اسم ملف الإخراج. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | خيارات الحفظ. |
| startPageIndex | int | الفهرس الصفري للصفحة الأولى التي سيتم استخراجها. |
| pageCount | int | عدد الصفحات التي سيتم استخراجها. |

### extractPages(String inputFileName, String outputFileName, int startPageIndex, int pageCount) {#extractPages-java.lang.String-java.lang.String-int-int}
```
public static void extractPages(String inputFileName, String outputFileName, int startPageIndex, int pageCount)
```


يستخرج نطاقًا محددًا من الصفحات من ملف المستند ويحفظ الصفحات المستخرجة في ملف جديد. يتم تحديد تنسيق ملف الإخراج بناءً على امتداد اسم ملف الإخراج.

 **Examples:** 

يوضح كيفية استخراج الصفحات من المستند.

```

 // There is a several ways to extract pages from the document:
 String doc = getMyDir() + "Big document.docx";

 Splitter.extractPages(doc, getArtifactsDir() + "LowCode.ExtractPages.1.docx", 0, 2);
 Splitter.extractPages(doc, getArtifactsDir() + "LowCode.ExtractPages.2.docx", SaveFormat.DOCX, 0, 2);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String | اسم ملف الإدخال. |
| outputFileName | java.lang.String | اسم ملف الإخراج. |
| startPageIndex | int | الفهرس الصفري للصفحة الأولى التي سيتم استخراجها. |
| pageCount | int | عدد الصفحات التي سيتم استخراجها. |

### extractPages(String inputFileName, String outputFileName, int saveFormat, int startPageIndex, int pageCount) {#extractPages-java.lang.String-java.lang.String-int-int-int}
```
public static void extractPages(String inputFileName, String outputFileName, int saveFormat, int startPageIndex, int pageCount)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| startPageIndex | int |  |
| pageCount | int |  |

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
### removeBlankPages(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions) {#removeBlankPages-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions}
```
public static ArrayList removeBlankPages(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
java.util.ArrayList
### removeBlankPages(InputStream inputStream, OutputStream outputStream, int saveFormat) {#removeBlankPages-java.io.InputStream-java.io.OutputStream-int}
```
public static ArrayList removeBlankPages(InputStream inputStream, OutputStream outputStream, int saveFormat)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |

**Returns:**
java.util.ArrayList
### removeBlankPages(String inputFileName, String outputFileName) {#removeBlankPages-java.lang.String-java.lang.String}
```
public static ArrayList removeBlankPages(String inputFileName, String outputFileName)
```


يزيل الصفحات الفارغة من المستند ويحفظ الناتج. يُرجع قائمة بأرقام الصفحات التي تمت إزالتها.

 **Examples:** 

يوضح كيفية إزالة الصفحات الفارغة من المستند.

```

 // There is a several ways to remove empty pages from the document:
 String doc = getMyDir() + "Blank pages.docx";

 Splitter.removeBlankPages(doc, getArtifactsDir() + "LowCode.RemoveBlankPages.1.docx");
 Splitter.removeBlankPages(doc, getArtifactsDir() + "LowCode.RemoveBlankPages.2.docx", SaveFormat.DOCX);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String | اسم ملف الإدخال. |
| outputFileName | java.lang.String | اسم ملف الإخراج. |

**Returns:**
java.util.ArrayList - تم اعتبار قائمة أرقام الصفحات كفارغة وإزالتها.
### removeBlankPages(String inputFileName, String outputFileName, SaveOptions saveOptions) {#removeBlankPages-java.lang.String-java.lang.String-com.aspose.words.SaveOptions}
```
public static ArrayList removeBlankPages(String inputFileName, String outputFileName, SaveOptions saveOptions)
```


يزيل الصفحات الفارغة من المستند ويحفظ الناتج بالتنسيق المحدد. يُرجع قائمة بأرقام الصفحات التي تمت إزالتها.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String | اسم ملف الإدخال. |
| outputFileName | java.lang.String | اسم ملف الإخراج. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | خيارات الحفظ. |

**Returns:**
java.util.ArrayList - تم اعتبار قائمة أرقام الصفحات كفارغة وإزالتها.
### removeBlankPages(String inputFileName, String outputFileName, int saveFormat) {#removeBlankPages-java.lang.String-java.lang.String-int}
```
public static ArrayList removeBlankPages(String inputFileName, String outputFileName, int saveFormat)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |

**Returns:**
java.util.ArrayList
### split(InputStream inputStream, SaveOptions saveOptions, SplitOptions options) {#split-java.io.InputStream-com.aspose.words.SaveOptions-com.aspose.words.SplitOptions}
```
public static OutputStream[] split(InputStream inputStream, SaveOptions saveOptions, SplitOptions options)
```


يقسم مستندًا من تدفق إدخال إلى أجزاء متعددة بناءً على خيارات التقسيم المحددة ويعيد الأجزاء الناتجة كمصفوفة من التدفقات بالتنسيق المحدد للحفظ.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream | دفق الإدخال. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | خيارات الحفظ. |
| options | [SplitOptions](../../com.aspose.words/splitoptions/) | خيارات تقسيم المستند. |

**Returns:**
java.io.OutputStream[]
### split(InputStream inputStream, int saveFormat, SplitOptions options) {#split-java.io.InputStream-int-com.aspose.words.SplitOptions}
```
public static OutputStream[] split(InputStream inputStream, int saveFormat, SplitOptions options)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| saveFormat | int |  |
| options | [SplitOptions](../../com.aspose.words/splitoptions/) |  |

**Returns:**
java.io.OutputStream[]
### split(String inputFileName, String outputFileName, SaveOptions saveOptions, SplitOptions options) {#split-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.SplitOptions}
```
public static void split(String inputFileName, String outputFileName, SaveOptions saveOptions, SplitOptions options)
```


يقسم مستندًا إلى أجزاء متعددة بناءً على خيارات التقسيم المحددة ويحفظ الأجزاء الناتجة في ملفات بالتنسيق المحدد للحفظ.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String | اسم ملف الإدخال. |
| outputFileName | java.lang.String | اسم ملف الإخراج المستخدم لتوليد أسماء الملفات لأجزاء المستند باستخدام القاعدة "outputFile\_partIndex.extension" |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | خيارات الحفظ. |
| options | [SplitOptions](../../com.aspose.words/splitoptions/) | خيارات تقسيم المستند. |

### split(String inputFileName, String outputFileName, SplitOptions options) {#split-java.lang.String-java.lang.String-com.aspose.words.SplitOptions}
```
public static void split(String inputFileName, String outputFileName, SplitOptions options)
```


يقسم مستندًا إلى أجزاء متعددة بناءً على خيارات التقسيم المحددة ويحفظ الأجزاء الناتجة في ملفات. يتم تحديد تنسيق ملف الإخراج بناءً على امتداد اسم ملف الإخراج.

 **Examples:** 

يوضح كيفية تقسيم المستند حسب الصفحات.

```

 String doc = getMyDir() + "Big document.docx";

 SplitOptions options = new SplitOptions();
 options.setSplitCriteria(SplitCriteria.PAGE);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.1.docx", options);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.2.docx", SaveFormat.DOCX, options);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String | اسم ملف الإدخال. |
| outputFileName | java.lang.String | اسم ملف الإخراج المستخدم لتوليد أسماء الملفات لأجزاء المستند باستخدام القاعدة "outputFile\_partIndex.extension" |
| options | [SplitOptions](../../com.aspose.words/splitoptions/) | خيارات تقسيم المستند. |

### split(String inputFileName, String outputFileName, int saveFormat, SplitOptions options) {#split-java.lang.String-java.lang.String-int-com.aspose.words.SplitOptions}
```
public static void split(String inputFileName, String outputFileName, int saveFormat, SplitOptions options)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| options | [SplitOptions](../../com.aspose.words/splitoptions/) |  |

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
