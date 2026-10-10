---
title: "Converter"
linktitle: "Converter"
second_title: "Aspose.Words لـ Java"
description: "يمثل مجموعة من الطرق المصممة لتحويل مجموعة متنوعة من أنواع المستندات باستخدام سطر واحد من الشيفرة في جافا."
type: docs
weight: 132
url: /ar/java/com.aspose.words/converter/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Processor](../../com.aspose.words/processor/)
```
public class Converter extends Processor
```

يمثل مجموعة من الأساليب المقصودة لتحويل مجموعة متنوعة من أنواع المستندات باستخدام سطر واحد من الشيفرة.

 **Remarks:** 

تُستخدم ملفات أو تدفقات الإدخال والإخراج المحددة، إلى جانب تنسيق الحفظ المطلوب، لتحويل المستند الإدخالي المعطى من تنسيق إلى المستند الإخراجي بالتنسيق المحدد الآخر.

تدعم وظيفة التحويل أكثر من 35 تنسيق ملف مختلف.

مجموعة **M:Aspose.Words.LowCode.Converter.ConvertToImages(System.String,Aspose.Words.SaveFormat)** من الطرق مصممة لتحويل المستندات إلى صور، حيث يتم تحويل كل صفحة إلى ملف صورة منفصل. كما تقوم هذه الطرق بتحويل مستندات PDF مباشرة إلى تنسيقات صفحات ثابتة دون تحميلها إلى نموذج المستند، مما يعزز كلًا من الأداء والدقة.

باستخدام [ImageSaveOptions.getPageSet()](../../com.aspose.words/imagesaveoptions/\#getPageSet) / [ImageSaveOptions.setPageSet(com.aspose.words.PageSet)](../../com.aspose.words/imagesaveoptions/\#setPageSet-com.aspose.words.PageSet)، يمكنك تحديد مجموعة معينة من الصفحات لتحويلها إلى صور.
## الطرق

| طريقة | الوصف |
| --- | --- |
| [convert(InputStream inputStream, LoadOptions loadOptions, OutputStream outputStream, SaveOptions saveOptions)](#convert-java.io.InputStream-com.aspose.words.LoadOptions-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [convert(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions)](#convert-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [convert(InputStream inputStream, OutputStream outputStream, int saveFormat)](#convert-java.io.InputStream-java.io.OutputStream-int) |  |
| [convert(String inputFile, LoadOptions loadOptions, String outputFile, SaveOptions saveOptions)](#convert-java.lang.String-com.aspose.words.LoadOptions-java.lang.String-com.aspose.words.SaveOptions) | يقوم بتحويل المستند الإدخالي المعطى إلى المستند الإخراجي باستخدام أسماء ملفات الإدخال والإخراج المحددة وخيارات التحميل/الحفظ الخاصة بها. |
| [convert(String inputFile, String outputFile)](#convert-java.lang.String-java.lang.String) | يقوم بتحويل المستند الإدخالي المحدد إلى المستند الإخراجي باستخدام أسماء ملفات الإدخال والإخراج المحددة وامتداداتها. |
| [convert(String inputFile, String outputFile, SaveOptions saveOptions)](#convert-java.lang.String-java.lang.String-com.aspose.words.SaveOptions) | يقوم بتحويل المستند الإدخالي المحدد إلى المستند الإخراجي باستخدام أسماء ملفات الإدخال والإخراج المحددة وخيارات الحفظ. |
| [convert(String inputFile, String outputFile, int saveFormat)](#convert-java.lang.String-java.lang.String-int) |  |
| [convertToImages(Document doc, ImageSaveOptions saveOptions)](#convertToImages-com.aspose.words.Document-com.aspose.words.ImageSaveOptions) | يقوم بتحويل صفحات المستند المحدد إلى صور باستخدام خيارات الحفظ المحددة ويعيد مصفوفة من التدفقات التي تحتوي على الصور. |
| [convertToImages(Document doc, int saveFormat)](#convertToImages-com.aspose.words.Document-int) |  |
| [convertToImages(InputStream inputStream, ImageSaveOptions saveOptions)](#convertToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions) | يقوم بتحويل صفحات تدفق الإدخال المحدد إلى صور باستخدام خيارات الحفظ المحددة ويعيد مصفوفة من التدفقات التي تحتوي على الصور. |
| [convertToImages(InputStream inputStream, LoadOptions loadOptions, ImageSaveOptions saveOptions)](#convertToImages-java.io.InputStream-com.aspose.words.LoadOptions-com.aspose.words.ImageSaveOptions) | يقوم بتحويل صفحات تدفق الإدخال المحدد إلى صور باستخدام خيارات التحميل والحفظ المقدمة، ويعيد مصفوفة من التدفقات التي تحتوي على الصور. |
| [convertToImages(InputStream inputStream, int saveFormat)](#convertToImages-java.io.InputStream-int) |  |
| [convertToImages(String inputFile, ImageSaveOptions saveOptions)](#convertToImages-java.lang.String-com.aspose.words.ImageSaveOptions) | يقوم بتحويل صفحات ملف الإدخال المحدد إلى صور باستخدام خيارات الحفظ المحددة ويعيد مصفوفة من التدفقات التي تحتوي على الصور. |
| [convertToImages(String inputFile, LoadOptions loadOptions, String outputFile, ImageSaveOptions saveOptions)](#convertToImages-java.lang.String-com.aspose.words.LoadOptions-java.lang.String-com.aspose.words.ImageSaveOptions) | يقوم بتحويل صفحات ملف الإدخال المحدد إلى ملفات صورة باستخدام خيارات التحميل والحفظ المقدمة. |
| [convertToImages(String inputFile, int saveFormat)](#convertToImages-java.lang.String-int) |  |
| [convertToImages(String inputFile, String outputFile)](#convertToImages-java.lang.String-java.lang.String) | يقوم بتحويل صفحات ملف الإدخال المحدد إلى ملفات صورة. |
| [convertToImages(String inputFile, String outputFile, ImageSaveOptions saveOptions)](#convertToImages-java.lang.String-java.lang.String-com.aspose.words.ImageSaveOptions) | يقوم بتحويل صفحات ملف الإدخال المحدد إلى ملفات صورة باستخدام خيارات الحفظ المحددة. |
| [convertToImages(String inputFile, String outputFile, int saveFormat)](#convertToImages-java.lang.String-java.lang.String-int) |  |
| [create()](#create) | ينشئ نسخة جديدة من معالج التحويل. |
| [create(ConverterContext context)](#create-com.aspose.words.ConverterContext) | ينشئ نسخة جديدة من معالج التحويل. |
| [execute()](#execute) | نفّذ إجراء المعالج. |
| [from(InputStream input)](#from-java.io.InputStream) | يحدد المستند الإدخالي للمعالجة. |
| [from(InputStream input, LoadOptions loadOptions)](#from-java.io.InputStream-com.aspose.words.LoadOptions) | يحدد المستند الإدخالي للمعالجة. |
| [from(String input)](#from-java.lang.String) | يحدد المستند الإدخالي للمعالجة. |
| [from(String input, LoadOptions loadOptions)](#from-java.lang.String-com.aspose.words.LoadOptions) | يحدد المستند الإدخالي للمعالجة. |
| [to(OutputStream output, SaveOptions saveOptions)](#to-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [to(OutputStream output, int saveFormat)](#to-java.io.OutputStream-int) |  |
| [to(String output)](#to-java.lang.String) | يحدد ملف الإخراج للمعالج. |
| [to(String output, SaveOptions saveOptions)](#to-java.lang.String-com.aspose.words.SaveOptions) | يحدد ملف الإخراج للمعالج. |
| [to(String output, int saveFormat)](#to-java.lang.String-int) |  |
| [to(ArrayList output, SaveOptions saveOptions)](#to-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [to(ArrayList output, int saveFormat)](#to-java.util.ArrayList-int) |  |
| [toOutput(ArrayList output, SaveOptions saveOptions)](#toOutput-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [toOutput(ArrayList output, int saveFormat)](#toOutput-java.util.ArrayList-int) |  |
### convert(InputStream inputStream, LoadOptions loadOptions, OutputStream outputStream, SaveOptions saveOptions) {#convert-java.io.InputStream-com.aspose.words.LoadOptions-java.io.OutputStream-com.aspose.words.SaveOptions}
```
public static void convert(InputStream inputStream, LoadOptions loadOptions, OutputStream outputStream, SaveOptions saveOptions)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

### convert(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions) {#convert-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions}
```
public static void convert(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

### convert(InputStream inputStream, OutputStream outputStream, int saveFormat) {#convert-java.io.InputStream-java.io.OutputStream-int}
```
public static void convert(InputStream inputStream, OutputStream outputStream, int saveFormat)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |

### convert(String inputFile, LoadOptions loadOptions, String outputFile, SaveOptions saveOptions) {#convert-java.lang.String-com.aspose.words.LoadOptions-java.lang.String-com.aspose.words.SaveOptions}
```
public static void convert(String inputFile, LoadOptions loadOptions, String outputFile, SaveOptions saveOptions)
```


يقوم بتحويل المستند الإدخالي المعطى إلى المستند الإخراجي باستخدام أسماء ملفات الإدخال والإخراج المحددة وخيارات التحميل/الحفظ الخاصة بها.

 **Remarks:** 

إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile\_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

 **Examples:** 

يوضح كيفية تحويل المستندات بسطر واحد من الشيفرة.

```

 String doc = getMyDir() + "Document.docx";

 Converter.convert(doc, getArtifactsDir() + "LowCode.Convert.pdf");

 Converter.convert(doc, getArtifactsDir() + "LowCode.Convert.SaveFormat.rtf", SaveFormat.RTF);

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 LoadOptions loadOptions = new LoadOptions();
 {
     loadOptions.setIgnoreOleData(true);
 }
 Converter.convert(doc, loadOptions, getArtifactsDir() + "LowCode.Convert.LoadOptions.docx", saveOptions);

 Converter.convert(doc, getArtifactsDir() + "LowCode.Convert.SaveOptions.docx", saveOptions);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFile | java.lang.String | اسم ملف الإدخال. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | خيارات تحميل المستند الإدخالي. |
| outputFile | java.lang.String | اسم ملف الإخراج. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | خيارات الحفظ. |

### convert(String inputFile, String outputFile) {#convert-java.lang.String-java.lang.String}
```
public static void convert(String inputFile, String outputFile)
```


يقوم بتحويل المستند الإدخالي المحدد إلى المستند الإخراجي باستخدام أسماء ملفات الإدخال والإخراج المحددة وامتداداتها.

 **Remarks:** 

إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile\_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

 **Examples:** 

يوضح كيفية تحويل المستندات بسطر واحد من الشيفرة.

```

 String doc = getMyDir() + "Document.docx";

 Converter.convert(doc, getArtifactsDir() + "LowCode.Convert.pdf");

 Converter.convert(doc, getArtifactsDir() + "LowCode.Convert.SaveFormat.rtf", SaveFormat.RTF);

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 LoadOptions loadOptions = new LoadOptions();
 {
     loadOptions.setIgnoreOleData(true);
 }
 Converter.convert(doc, loadOptions, getArtifactsDir() + "LowCode.Convert.LoadOptions.docx", saveOptions);

 Converter.convert(doc, getArtifactsDir() + "LowCode.Convert.SaveOptions.docx", saveOptions);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFile | java.lang.String | اسم ملف الإدخال. |
| outputFile | java.lang.String | اسم ملف الإخراج. |

### convert(String inputFile, String outputFile, SaveOptions saveOptions) {#convert-java.lang.String-java.lang.String-com.aspose.words.SaveOptions}
```
public static void convert(String inputFile, String outputFile, SaveOptions saveOptions)
```


يقوم بتحويل المستند الإدخالي المحدد إلى المستند الإخراجي باستخدام أسماء ملفات الإدخال والإخراج المحددة وخيارات الحفظ.

 **Remarks:** 

إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile\_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

 **Examples:** 

يوضح كيفية تحويل المستندات بسطر واحد من الشيفرة.

```

 String doc = getMyDir() + "Document.docx";

 Converter.convert(doc, getArtifactsDir() + "LowCode.Convert.pdf");

 Converter.convert(doc, getArtifactsDir() + "LowCode.Convert.SaveFormat.rtf", SaveFormat.RTF);

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 LoadOptions loadOptions = new LoadOptions();
 {
     loadOptions.setIgnoreOleData(true);
 }
 Converter.convert(doc, loadOptions, getArtifactsDir() + "LowCode.Convert.LoadOptions.docx", saveOptions);

 Converter.convert(doc, getArtifactsDir() + "LowCode.Convert.SaveOptions.docx", saveOptions);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFile | java.lang.String | اسم ملف الإدخال. |
| outputFile | java.lang.String | اسم ملف الإخراج. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | خيارات الحفظ. |

### convert(String inputFile, String outputFile, int saveFormat) {#convert-java.lang.String-java.lang.String-int}
```
public static void convert(String inputFile, String outputFile, int saveFormat)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFile | java.lang.String |  |
| outputFile | java.lang.String |  |
| saveFormat | int |  |

### convertToImages(Document doc, ImageSaveOptions saveOptions) {#convertToImages-com.aspose.words.Document-com.aspose.words.ImageSaveOptions}
```
public static OutputStream[] convertToImages(Document doc, ImageSaveOptions saveOptions)
```


يقوم بتحويل صفحات المستند المحدد إلى صور باستخدام خيارات الحفظ المحددة ويعيد مصفوفة من التدفقات التي تحتوي على الصور.

 **Examples:** 

يوضح كيفية تحويل المستند إلى تدفق صور.

```

 String doc = getMyDir() + "Big document.docx";

 OutputStream[] streams = Converter.convertToImages(doc, SaveFormat.PNG);

 ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.PNG);
 imageSaveOptions.setPageSet(new PageSet(1));
 streams = Converter.convertToImages(doc, imageSaveOptions);

 streams = Converter.convertToImages(new Document(doc), SaveFormat.PNG);

 streams = Converter.convertToImages(new Document(doc), imageSaveOptions);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document/) | المستند الإدخالي. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | خيارات حفظ الصورة. |

**Returns:**
java.io.OutputStream[] - يعيد مصفوفة من تدفقات الصور. يجب على المستخدم النهائي التخلص من التدفقات.
### convertToImages(Document doc, int saveFormat) {#convertToImages-com.aspose.words.Document-int}
```
public static OutputStream[] convertToImages(Document doc, int saveFormat)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document/) |  |
| saveFormat | int |  |

**Returns:**
java.io.OutputStream[]
### convertToImages(InputStream inputStream, ImageSaveOptions saveOptions) {#convertToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions}
```
public static OutputStream[] convertToImages(InputStream inputStream, ImageSaveOptions saveOptions)
```


يقوم بتحويل صفحات تدفق الإدخال المحدد إلى صور باستخدام خيارات الحفظ المحددة ويعيد مصفوفة من التدفقات التي تحتوي على الصور.

 **Examples:** 

يوضح كيفية تحويل المستند إلى صور من تدفق.

```

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Big document.docx")) {
     OutputStream[] streams = Converter.convertToImages(streamIn, SaveFormat.JPEG);

     ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.PNG);
     imageSaveOptions.setPageSet(new PageSet(1));
     streams = Converter.convertToImages(streamIn, imageSaveOptions);

     LoadOptions loadOptions = new LoadOptions();
     {
         loadOptions.setIgnoreOleData(false);
     }
     Converter.convertToImages(streamIn, loadOptions, imageSaveOptions);
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream | دفق الإدخال. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | خيارات حفظ الصورة. |

**Returns:**
java.io.OutputStream[] - يعيد مصفوفة من تدفقات الصور. يجب على المستخدم النهائي التخلص من التدفقات.
### convertToImages(InputStream inputStream, LoadOptions loadOptions, ImageSaveOptions saveOptions) {#convertToImages-java.io.InputStream-com.aspose.words.LoadOptions-com.aspose.words.ImageSaveOptions}
```
public static OutputStream[] convertToImages(InputStream inputStream, LoadOptions loadOptions, ImageSaveOptions saveOptions)
```


يقوم بتحويل صفحات تدفق الإدخال المحدد إلى صور باستخدام خيارات التحميل والحفظ المقدمة، ويعيد مصفوفة من التدفقات التي تحتوي على الصور.

 **Examples:** 

يوضح كيفية تحويل المستند إلى صور من تدفق.

```

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Big document.docx")) {
     OutputStream[] streams = Converter.convertToImages(streamIn, SaveFormat.JPEG);

     ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.PNG);
     imageSaveOptions.setPageSet(new PageSet(1));
     streams = Converter.convertToImages(streamIn, imageSaveOptions);

     LoadOptions loadOptions = new LoadOptions();
     {
         loadOptions.setIgnoreOleData(false);
     }
     Converter.convertToImages(streamIn, loadOptions, imageSaveOptions);
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream | دفق الإدخال. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | خيارات تحميل المستند الإدخالي. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | خيارات حفظ الصورة. |

**Returns:**
java.io.OutputStream[] - يعيد مصفوفة من تدفقات الصور. يجب على المستخدم النهائي التخلص من التدفقات.
### convertToImages(InputStream inputStream, int saveFormat) {#convertToImages-java.io.InputStream-int}
```
public static OutputStream[] convertToImages(InputStream inputStream, int saveFormat)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| saveFormat | int |  |

**Returns:**
java.io.OutputStream[]
### convertToImages(String inputFile, ImageSaveOptions saveOptions) {#convertToImages-java.lang.String-com.aspose.words.ImageSaveOptions}
```
public static OutputStream[] convertToImages(String inputFile, ImageSaveOptions saveOptions)
```


يقوم بتحويل صفحات ملف الإدخال المحدد إلى صور باستخدام خيارات الحفظ المحددة ويعيد مصفوفة من التدفقات التي تحتوي على الصور.

 **Examples:** 

يوضح كيفية تحويل المستند إلى تدفق صور.

```

 String doc = getMyDir() + "Big document.docx";

 OutputStream[] streams = Converter.convertToImages(doc, SaveFormat.PNG);

 ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.PNG);
 imageSaveOptions.setPageSet(new PageSet(1));
 streams = Converter.convertToImages(doc, imageSaveOptions);

 streams = Converter.convertToImages(new Document(doc), SaveFormat.PNG);

 streams = Converter.convertToImages(new Document(doc), imageSaveOptions);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFile | java.lang.String | اسم ملف الإدخال. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | خيارات حفظ الصورة. |

**Returns:**
java.io.OutputStream[] - يعيد مصفوفة من تدفقات الصور. يجب على المستخدم النهائي التخلص من التدفقات.
### convertToImages(String inputFile, LoadOptions loadOptions, String outputFile, ImageSaveOptions saveOptions) {#convertToImages-java.lang.String-com.aspose.words.LoadOptions-java.lang.String-com.aspose.words.ImageSaveOptions}
```
public static void convertToImages(String inputFile, LoadOptions loadOptions, String outputFile, ImageSaveOptions saveOptions)
```


يقوم بتحويل صفحات ملف الإدخال المحدد إلى ملفات صورة باستخدام خيارات التحميل والحفظ المقدمة.

 **Examples:** 

يوضح كيفية تحويل المستند إلى صور.

```

 String doc = getMyDir() + "Big document.docx";

 Converter.convertToImages(doc, getArtifactsDir() + "LowCode.ConvertToImages.1.png");

 Converter.convertToImages(doc, getArtifactsDir() + "LowCode.ConvertToImages.2.jpeg", SaveFormat.JPEG);

 LoadOptions loadOptions = new LoadOptions();
 {
     loadOptions.setIgnoreOleData(false);
 }
 ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.PNG);
 imageSaveOptions.setPageSet(new PageSet(1));
 Converter.convertToImages(doc, loadOptions, getArtifactsDir() + "LowCode.ConvertToImages.3.png", imageSaveOptions);

 Converter.convertToImages(doc, getArtifactsDir() + "LowCode.ConvertToImages.4.png", imageSaveOptions);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFile | java.lang.String | اسم ملف الإدخال. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | خيارات تحميل المستند الإدخالي. |
| outputFile | java.lang.String | اسم ملف الإخراج المستخدم لإنشاء اسم ملف لصور الصفحات باستخدام القاعدة "outputFile\\_pageIndex.extension" |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | خيارات حفظ الصورة. |

### convertToImages(String inputFile, int saveFormat) {#convertToImages-java.lang.String-int}
```
public static OutputStream[] convertToImages(String inputFile, int saveFormat)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFile | java.lang.String |  |
| saveFormat | int |  |

**Returns:**
java.io.OutputStream[]
### convertToImages(String inputFile, String outputFile) {#convertToImages-java.lang.String-java.lang.String}
```
public static void convertToImages(String inputFile, String outputFile)
```


يقوم بتحويل صفحات ملف الإدخال المحدد إلى ملفات صورة.

 **Examples:** 

يوضح كيفية تحويل المستند إلى صور.

```

 String doc = getMyDir() + "Big document.docx";

 Converter.convertToImages(doc, getArtifactsDir() + "LowCode.ConvertToImages.1.png");

 Converter.convertToImages(doc, getArtifactsDir() + "LowCode.ConvertToImages.2.jpeg", SaveFormat.JPEG);

 LoadOptions loadOptions = new LoadOptions();
 {
     loadOptions.setIgnoreOleData(false);
 }
 ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.PNG);
 imageSaveOptions.setPageSet(new PageSet(1));
 Converter.convertToImages(doc, loadOptions, getArtifactsDir() + "LowCode.ConvertToImages.3.png", imageSaveOptions);

 Converter.convertToImages(doc, getArtifactsDir() + "LowCode.ConvertToImages.4.png", imageSaveOptions);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFile | java.lang.String | اسم ملف الإدخال. |
| outputFile | java.lang.String | اسم ملف الإخراج المستخدم لإنشاء اسم ملف لصور الصفحات باستخدام القاعدة "outputFile\\_pageIndex.extension" |

### convertToImages(String inputFile, String outputFile, ImageSaveOptions saveOptions) {#convertToImages-java.lang.String-java.lang.String-com.aspose.words.ImageSaveOptions}
```
public static void convertToImages(String inputFile, String outputFile, ImageSaveOptions saveOptions)
```


يقوم بتحويل صفحات ملف الإدخال المحدد إلى ملفات صورة باستخدام خيارات الحفظ المحددة.

 **Examples:** 

يوضح كيفية تحويل المستند إلى صور.

```

 String doc = getMyDir() + "Big document.docx";

 Converter.convertToImages(doc, getArtifactsDir() + "LowCode.ConvertToImages.1.png");

 Converter.convertToImages(doc, getArtifactsDir() + "LowCode.ConvertToImages.2.jpeg", SaveFormat.JPEG);

 LoadOptions loadOptions = new LoadOptions();
 {
     loadOptions.setIgnoreOleData(false);
 }
 ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.PNG);
 imageSaveOptions.setPageSet(new PageSet(1));
 Converter.convertToImages(doc, loadOptions, getArtifactsDir() + "LowCode.ConvertToImages.3.png", imageSaveOptions);

 Converter.convertToImages(doc, getArtifactsDir() + "LowCode.ConvertToImages.4.png", imageSaveOptions);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFile | java.lang.String | اسم ملف الإدخال. |
| outputFile | java.lang.String | اسم ملف الإخراج المستخدم لإنشاء اسم ملف لصور الصفحات باستخدام القاعدة "outputFile\\_pageIndex.extension" |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | خيارات حفظ الصورة. |

### convertToImages(String inputFile, String outputFile, int saveFormat) {#convertToImages-java.lang.String-java.lang.String-int}
```
public static void convertToImages(String inputFile, String outputFile, int saveFormat)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFile | java.lang.String |  |
| outputFile | java.lang.String |  |
| saveFormat | int |  |

### create() {#create}
```
public static Converter create()
```


ينشئ نسخة جديدة من معالج التحويل.

**Returns:**
[Converter](../../com.aspose.words/converter/)
### create(ConverterContext context) {#create-com.aspose.words.ConverterContext}
```
public static Converter create(ConverterContext context)
```


ينشئ نسخة جديدة من معالج التحويل.

 **Examples:** 

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

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| context | [ConverterContext](../../com.aspose.words/convertercontext/) |  |

**Returns:**
[Converter](../../com.aspose.words/converter/)
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
