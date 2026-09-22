---
title: "ReportBuilder"
linktitle: "ReportBuilder"
second_title: "Aspose.Words لـ Java"
description: "يوفر طرقًا تهدف إلى ملء القالب بالبيانات باستخدام LINQ Reporting Engine في Java."
type: docs
weight: 571
url: /ar/java/com.aspose.words/reportbuilder/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Processor](../../com.aspose.words/processor/)
```
public class ReportBuilder extends Processor
```

يوفر طرقًا تهدف إلى ملء القالب بالبيانات باستخدام LINQ Reporting Engine.
## الطرق

| طريقة | الوصف |
| --- | --- |
| [buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object data)](#buildReport-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.Object) |  |
| [buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object data, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.Object-com.aspose.words.ReportBuilderOptions) |  |
| [buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object data, String dataSourceName)](#buildReport-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.Object-java.lang.String) |  |
| [buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.Object-java.lang.String-com.aspose.words.ReportBuilderOptions) |  |
| [buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object[] data, String[] dataSourceNames)](#buildReport-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.Object---java.lang.String) |  |
| [buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions) |  |
| [buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object data)](#buildReport-java.io.InputStream-java.io.OutputStream-int-java.lang.Object) |  |
| [buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object data, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.io.InputStream-java.io.OutputStream-int-java.lang.Object-com.aspose.words.ReportBuilderOptions) |  |
| [buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object data, String dataSourceName)](#buildReport-java.io.InputStream-java.io.OutputStream-int-java.lang.Object-java.lang.String) |  |
| [buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.io.InputStream-java.io.OutputStream-int-java.lang.Object-java.lang.String-com.aspose.words.ReportBuilderOptions) |  |
| [buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object[] data, String[] dataSourceNames)](#buildReport-java.io.InputStream-java.io.OutputStream-int-java.lang.Object---java.lang.String) |  |
| [buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.io.InputStream-java.io.OutputStream-int-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions) |  |
| [buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object data)](#buildReport-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.Object) | يملأ مستند القالب بالبيانات من المصدر المحدد، مُنتجًا تقريرًا مكتملًا بالتنسيق المحدد للإخراج وخيارات إضافية. |
| [buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object data, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.Object-com.aspose.words.ReportBuilderOptions) | يملأ مستند القالب بالبيانات من المصدر المحدد، مُنتجًا تقريرًا مكتملًا بالتنسيق المحدد للإخراج وخيارات إضافية. |
| [buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object data, String dataSourceName)](#buildReport-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.Object-java.lang.String) | يملأ مستند القالب بالبيانات من المصدر المحدد، مُنتجًا تقريرًا مكتملًا بالتنسيق المحدد للإخراج، وإشارة مصدر بيانات مسماة، وخيارات إضافية. |
| [buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.Object-java.lang.String-com.aspose.words.ReportBuilderOptions) | يملأ مستند القالب بالبيانات من المصدر المحدد، مُنتجًا تقريرًا مكتملًا بالتنسيق المحدد للإخراج، وإشارة مصدر بيانات مسماة، وخيارات إضافية. |
| [buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object[] data, String[] dataSourceNames)](#buildReport-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.Object---java.lang.String) | يملأ مستند القالب بالبيانات من مصادر متعددة، مُنتجًا تقريرًا مكتملًا بالتنسيق المحدد للإخراج وخيارات إضافية. |
| [buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions) | يملأ مستند القالب بالبيانات من مصادر متعددة، مُنتجًا تقريرًا مكتملًا بالتنسيق المحدد للإخراج وخيارات إضافية. |
| [buildReport(String inputFileName, String outputFileName, int saveFormat, Object data)](#buildReport-java.lang.String-java.lang.String-int-java.lang.Object) |  |
| [buildReport(String inputFileName, String outputFileName, int saveFormat, Object data, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.lang.String-java.lang.String-int-java.lang.Object-com.aspose.words.ReportBuilderOptions) |  |
| [buildReport(String inputFileName, String outputFileName, int saveFormat, Object data, String dataSourceName)](#buildReport-java.lang.String-java.lang.String-int-java.lang.Object-java.lang.String) |  |
| [buildReport(String inputFileName, String outputFileName, int saveFormat, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.lang.String-java.lang.String-int-java.lang.Object-java.lang.String-com.aspose.words.ReportBuilderOptions) |  |
| [buildReport(String inputFileName, String outputFileName, int saveFormat, Object[] data, String[] dataSourceNames)](#buildReport-java.lang.String-java.lang.String-int-java.lang.Object---java.lang.String) |  |
| [buildReport(String inputFileName, String outputFileName, int saveFormat, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.lang.String-java.lang.String-int-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions) |  |
| [buildReport(String inputFileName, String outputFileName, Object data)](#buildReport-java.lang.String-java.lang.String-java.lang.Object) | يملأ مستند القالب بالبيانات من المصدر المحدد، مُنتجًا تقريرًا مكتملًا بخيارات إضافية. |
| [buildReport(String inputFileName, String outputFileName, Object data, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.lang.String-java.lang.String-java.lang.Object-com.aspose.words.ReportBuilderOptions) | يملأ مستند القالب بالبيانات من المصدر المحدد، مُنتجًا تقريرًا مكتملًا بخيارات إضافية. |
| [buildReport(String inputFileName, String outputFileName, Object data, String dataSourceName)](#buildReport-java.lang.String-java.lang.String-java.lang.Object-java.lang.String) | يملأ مستند القالب بالبيانات من المصدر المحدد، مُنتجًا تقريرًا مكتملًا بإشارة مصدر بيانات مسماة وخيارات إضافية. |
| [buildReport(String inputFileName, String outputFileName, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.lang.String-java.lang.String-java.lang.Object-java.lang.String-com.aspose.words.ReportBuilderOptions) | يملأ مستند القالب بالبيانات من المصدر المحدد، مُنتجًا تقريرًا مكتملًا بإشارة مصدر بيانات مسماة وخيارات إضافية. |
| [buildReport(String inputFileName, String outputFileName, Object[] data, String[] dataSourceNames)](#buildReport-java.lang.String-java.lang.String-java.lang.Object---java.lang.String) | يملأ مستند القالب بالبيانات من مصادر متعددة، مُنتجًا تقريرًا مكتملًا بخيارات إضافية. |
| [buildReport(String inputFileName, String outputFileName, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.lang.String-java.lang.String-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions) | يملأ مستند القالب بالبيانات من مصادر متعددة، مُنتجًا تقريرًا مكتملًا بخيارات إضافية. |
| [buildReportToImages(InputStream inputStream, ImageSaveOptions saveOptions, Object[] data, String[] dataSourceNames)](#buildReportToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.Object---java.lang.String) | يملأ مستند القالب بالبيانات من مصادر متعددة. |
| [buildReportToImages(InputStream inputStream, ImageSaveOptions saveOptions, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)](#buildReportToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions) | يملأ مستند القالب بالبيانات من مصادر متعددة. |
| [buildReportToImages(String inputFileName, ImageSaveOptions saveOptions, Object[] data, String[] dataSourceNames)](#buildReportToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.Object---java.lang.String) | يملأ مستند القالب بالبيانات من مصادر متعددة. |
| [buildReportToImages(String inputFileName, ImageSaveOptions saveOptions, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)](#buildReportToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions) | يملأ مستند القالب بالبيانات من مصادر متعددة. |
| [create()](#create) | ينشئ نسخة جديدة من معالج بناء التقرير. |
| [create(ReportBuilderContext context)](#create-com.aspose.words.ReportBuilderContext) | ينشئ نسخة جديدة من معالج بناء التقرير. |
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
### buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object data) {#buildReport-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.Object}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object data)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| بيانات | java.lang.Object |  |

### buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object data, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.Object-com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object data, ReportBuilderOptions reportBuilderOptions)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| بيانات | java.lang.Object |  |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) |  |

### buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object data, String dataSourceName) {#buildReport-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.Object-java.lang.String}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object data, String dataSourceName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| بيانات | java.lang.Object |  |
| dataSourceName | java.lang.String |  |

### buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.Object-java.lang.String-com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| بيانات | java.lang.Object |  |
| dataSourceName | java.lang.String |  |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) |  |

### buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object[] data, String[] dataSourceNames) {#buildReport-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.Object---java.lang.String}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object[] data, String[] dataSourceNames)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| بيانات | java.lang.Object[] |  |
| dataSourceNames | java.lang.String[] |  |

### buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| بيانات | java.lang.Object[] |  |
| dataSourceNames | java.lang.String[] |  |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) |  |

### buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object data) {#buildReport-java.io.InputStream-java.io.OutputStream-int-java.lang.Object}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object data)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| بيانات | java.lang.Object |  |

### buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object data, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.io.InputStream-java.io.OutputStream-int-java.lang.Object-com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object data, ReportBuilderOptions reportBuilderOptions)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| بيانات | java.lang.Object |  |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) |  |

### buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object data, String dataSourceName) {#buildReport-java.io.InputStream-java.io.OutputStream-int-java.lang.Object-java.lang.String}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object data, String dataSourceName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| بيانات | java.lang.Object |  |
| dataSourceName | java.lang.String |  |

### buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.io.InputStream-java.io.OutputStream-int-java.lang.Object-java.lang.String-com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| بيانات | java.lang.Object |  |
| dataSourceName | java.lang.String |  |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) |  |

### buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object[] data, String[] dataSourceNames) {#buildReport-java.io.InputStream-java.io.OutputStream-int-java.lang.Object---java.lang.String}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object[] data, String[] dataSourceNames)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| بيانات | java.lang.Object[] |  |
| dataSourceNames | java.lang.String[] |  |

### buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.io.InputStream-java.io.OutputStream-int-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| بيانات | java.lang.Object[] |  |
| dataSourceNames | java.lang.String[] |  |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) |  |

### buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object data) {#buildReport-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.Object}
```
public static void buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object data)
```


يملأ مستند القالب بالبيانات من المصدر المحدد، مُنتجًا تقريرًا مكتملًا بالتنسيق المحدد للإخراج وخيارات إضافية.

 **Remarks:** 

إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile\_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String | اسم ملف الإدخال. |
| outputFileName | java.lang.String | اسم ملف الإخراج. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | خيارات حفظ الإخراج. |
| بيانات | java.lang.Object | كائن مصدر بيانات. |

### buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object data, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.Object-com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object data, ReportBuilderOptions reportBuilderOptions)
```


يملأ مستند القالب بالبيانات من المصدر المحدد، مُنتجًا تقريرًا مكتملًا بالتنسيق المحدد للإخراج وخيارات إضافية.

 **Remarks:** 

إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile\_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String | اسم ملف الإدخال. |
| outputFileName | java.lang.String | اسم ملف الإخراج. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | خيارات حفظ الإخراج. |
| بيانات | java.lang.Object | كائن مصدر بيانات. |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) | خيارات إضافية لبناء التقرير. |

### buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object data, String dataSourceName) {#buildReport-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.Object-java.lang.String}
```
public static void buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object data, String dataSourceName)
```


يملأ مستند القالب بالبيانات من المصدر المحدد، مُنتجًا تقريرًا مكتملًا بالتنسيق المحدد للإخراج، وإشارة مصدر بيانات مسماة، وخيارات إضافية.

 **Remarks:** 

إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile\_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String | اسم ملف الإدخال. |
| outputFileName | java.lang.String | اسم ملف الإخراج. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | خيارات حفظ الإخراج. |
| بيانات | java.lang.Object | كائن مصدر بيانات. |
| dataSourceName | java.lang.String | اسم للإشارة إلى كائن مصدر البيانات في القالب. |

### buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.Object-java.lang.String-com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions)
```


يملأ مستند القالب بالبيانات من المصدر المحدد، مُنتجًا تقريرًا مكتملًا بالتنسيق المحدد للإخراج، وإشارة مصدر بيانات مسماة، وخيارات إضافية.

 **Remarks:** 

إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile\_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String | اسم ملف الإدخال. |
| outputFileName | java.lang.String | اسم ملف الإخراج. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | خيارات حفظ الإخراج. |
| بيانات | java.lang.Object | كائن مصدر بيانات. |
| dataSourceName | java.lang.String | اسم للإشارة إلى كائن مصدر البيانات في القالب. |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) | خيارات إضافية لبناء التقرير. |

### buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object[] data, String[] dataSourceNames) {#buildReport-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.Object---java.lang.String}
```
public static void buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object[] data, String[] dataSourceNames)
```


يملأ مستند القالب بالبيانات من مصادر متعددة، مُنتجًا تقريرًا مكتملًا بالتنسيق المحدد للإخراج وخيارات إضافية.

 **Remarks:** 

إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile\_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String | اسم ملف الإدخال. |
| outputFileName | java.lang.String | اسم ملف الإخراج. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | خيارات حفظ الإخراج. |
| بيانات | java.lang.Object[] | مصفوفة من كائنات مصدر البيانات. |
| dataSourceNames | java.lang.String[] | مصفوفة من الأسماء للإشارة إلى كائنات مصدر البيانات داخل القالب. |

### buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)
```


يملأ مستند القالب بالبيانات من مصادر متعددة، مُنتجًا تقريرًا مكتملًا بالتنسيق المحدد للإخراج وخيارات إضافية.

 **Remarks:** 

إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile\_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String | اسم ملف الإدخال. |
| outputFileName | java.lang.String | اسم ملف الإخراج. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | خيارات حفظ الإخراج. |
| بيانات | java.lang.Object[] | مصفوفة من كائنات مصدر البيانات. |
| dataSourceNames | java.lang.String[] | مصفوفة من الأسماء للإشارة إلى كائنات مصدر البيانات داخل القالب. |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) | خيارات إضافية لبناء التقرير. |

### buildReport(String inputFileName, String outputFileName, int saveFormat, Object data) {#buildReport-java.lang.String-java.lang.String-int-java.lang.Object}
```
public static void buildReport(String inputFileName, String outputFileName, int saveFormat, Object data)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| بيانات | java.lang.Object |  |

### buildReport(String inputFileName, String outputFileName, int saveFormat, Object data, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.lang.String-java.lang.String-int-java.lang.Object-com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(String inputFileName, String outputFileName, int saveFormat, Object data, ReportBuilderOptions reportBuilderOptions)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| بيانات | java.lang.Object |  |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) |  |

### buildReport(String inputFileName, String outputFileName, int saveFormat, Object data, String dataSourceName) {#buildReport-java.lang.String-java.lang.String-int-java.lang.Object-java.lang.String}
```
public static void buildReport(String inputFileName, String outputFileName, int saveFormat, Object data, String dataSourceName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| بيانات | java.lang.Object |  |
| dataSourceName | java.lang.String |  |

### buildReport(String inputFileName, String outputFileName, int saveFormat, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.lang.String-java.lang.String-int-java.lang.Object-java.lang.String-com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(String inputFileName, String outputFileName, int saveFormat, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| بيانات | java.lang.Object |  |
| dataSourceName | java.lang.String |  |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) |  |

### buildReport(String inputFileName, String outputFileName, int saveFormat, Object[] data, String[] dataSourceNames) {#buildReport-java.lang.String-java.lang.String-int-java.lang.Object---java.lang.String}
```
public static void buildReport(String inputFileName, String outputFileName, int saveFormat, Object[] data, String[] dataSourceNames)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| بيانات | java.lang.Object[] |  |
| dataSourceNames | java.lang.String[] |  |

### buildReport(String inputFileName, String outputFileName, int saveFormat, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.lang.String-java.lang.String-int-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(String inputFileName, String outputFileName, int saveFormat, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| بيانات | java.lang.Object[] |  |
| dataSourceNames | java.lang.String[] |  |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) |  |

### buildReport(String inputFileName, String outputFileName, Object data) {#buildReport-java.lang.String-java.lang.String-java.lang.Object}
```
public static void buildReport(String inputFileName, String outputFileName, Object data)
```


يملأ مستند القالب بالبيانات من المصدر المحدد، مُنتجًا تقريرًا مكتملًا بخيارات إضافية.

 **Remarks:** 

إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile\_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String | اسم ملف الإدخال. |
| outputFileName | java.lang.String | اسم ملف الإخراج. |
| بيانات | java.lang.Object | كائن مصدر بيانات. |

### buildReport(String inputFileName, String outputFileName, Object data, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.lang.String-java.lang.String-java.lang.Object-com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(String inputFileName, String outputFileName, Object data, ReportBuilderOptions reportBuilderOptions)
```


يملأ مستند القالب بالبيانات من المصدر المحدد، مُنتجًا تقريرًا مكتملًا بخيارات إضافية.

 **Remarks:** 

إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile\_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

 **Examples:** 

يظهر كيفية تعبئة المستند بالبيانات.

```

 public void buildReportData() throws Exception {
     // There is a several ways to populate document with data:
     String doc = getMyDir() + "Reporting engine template - If greedy (Java).docx";

     AsposeData obj = new AsposeData();
     {
         obj.setList(new ArrayList<>());
         {
             obj.getList().add("abc");
         }
     }

     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.1.docx", obj);
     ReportBuilderOptions options = new ReportBuilderOptions();
     options.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.2.docx", obj, options);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.3.docx", SaveFormat.DOCX, obj);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.4.docx", SaveFormat.DOCX, obj, options);
 }

 public static class AsposeData {
     public ArrayList getList() {
         return mList;
     }

     ;

     public void setList(ArrayList value) {
         mList = value;
     }

     ;

     private ArrayList mList;
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String | اسم ملف الإدخال. |
| outputFileName | java.lang.String | اسم ملف الإخراج. |
| بيانات | java.lang.Object | كائن مصدر بيانات. |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) | خيارات إضافية لبناء التقرير. |

### buildReport(String inputFileName, String outputFileName, Object data, String dataSourceName) {#buildReport-java.lang.String-java.lang.String-java.lang.Object-java.lang.String}
```
public static void buildReport(String inputFileName, String outputFileName, Object data, String dataSourceName)
```


يملأ مستند القالب بالبيانات من المصدر المحدد، مُنتجًا تقريرًا مكتملًا بإشارة مصدر بيانات مسماة وخيارات إضافية.

 **Remarks:** 

إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile\_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String | اسم ملف الإدخال. |
| outputFileName | java.lang.String | اسم ملف الإخراج. |
| بيانات | java.lang.Object | كائن مصدر بيانات. |
| dataSourceName | java.lang.String | اسم للإشارة إلى كائن مصدر البيانات في القالب. |

### buildReport(String inputFileName, String outputFileName, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.lang.String-java.lang.String-java.lang.Object-java.lang.String-com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(String inputFileName, String outputFileName, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions)
```


يملأ مستند القالب بالبيانات من المصدر المحدد، مُنتجًا تقريرًا مكتملًا بإشارة مصدر بيانات مسماة وخيارات إضافية.

 **Remarks:** 

إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile\_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

 **Examples:** 

يعرض كيفية تعبئة المستند بمصادر البيانات.

```

 public void buildReportDataSource() throws Exception {
     // There is a several ways to populate document with data sources:
     String doc = getMyDir() + "Report building.docx";

     MessageTestClass sender = new MessageTestClass("LINQ Reporting Engine", "Hello World");

     ReportBuilderOptions options = new ReportBuilderOptions();
     options.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);

     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.1.docx", sender, "s");
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.2.docx", new Object[]{sender}, new String[]{"s"});
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.3.docx", sender, "s", options);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.4.docx", SaveFormat.DOCX, sender, "s");
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.5.docx", SaveFormat.DOCX, new Object[]{sender}, new String[]{"s"});
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.6.docx", SaveFormat.DOCX, sender, "s", options);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.7.docx", SaveFormat.DOCX, new Object[]{sender}, new String[]{"s"}, options);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.8.docx", new Object[]{sender}, new String[]{"s"}, options);

     options = new ReportBuilderOptions();
     options.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);
     OutputStream[] images = ReportBuilder.buildReportToImages(doc, new ImageSaveOptions(SaveFormat.PNG), new Object[]{sender}, new String[]{"s"}, options);

     ReportBuilderContext reportBuilderContext = new ReportBuilderContext();
     reportBuilderContext.getReportBuilderOptions().setMissingMemberMessage("Missed members");
     reportBuilderContext.getDataSources().put(sender, "s");

     ReportBuilder.create(reportBuilderContext)
             .from(doc)
             .to(getArtifactsDir() + "LowCode.BuildReportDataSource.9.docx")
             .execute();
 }

 public static class MessageTestClass {
     public String getName() {
         return mName;
     }

     public void setName(String value) {
         mName = value;
     }

     private String mName;

     public String getMessage() {
         return mMessage;
     }

     public void setMessage(String value) {
         mMessage = value;
     }

     private String mMessage;

     public MessageTestClass(String name, String message) {
         setName(name);
         setMessage(message);
     }
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String | اسم ملف الإدخال. |
| outputFileName | java.lang.String | اسم ملف الإخراج. |
| بيانات | java.lang.Object | كائن مصدر بيانات. |
| dataSourceName | java.lang.String | اسم للإشارة إلى كائن مصدر البيانات في القالب. |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) | خيارات إضافية لبناء التقرير. |

### buildReport(String inputFileName, String outputFileName, Object[] data, String[] dataSourceNames) {#buildReport-java.lang.String-java.lang.String-java.lang.Object---java.lang.String}
```
public static void buildReport(String inputFileName, String outputFileName, Object[] data, String[] dataSourceNames)
```


يملأ مستند القالب بالبيانات من مصادر متعددة، مُنتجًا تقريرًا مكتملًا بخيارات إضافية. هذا التحميل الزائد يحدد تلقائيًا تنسيق الحفظ بناءً على امتداد ملف الإخراج.

 **Remarks:** 

إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile\_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String | اسم ملف الإدخال. |
| outputFileName | java.lang.String | اسم ملف الإخراج. |
| بيانات | java.lang.Object[] | مصفوفة من كائنات مصدر البيانات. |
| dataSourceNames | java.lang.String[] | مصفوفة من الأسماء للإشارة إلى كائنات مصدر البيانات داخل القالب. |

### buildReport(String inputFileName, String outputFileName, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.lang.String-java.lang.String-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(String inputFileName, String outputFileName, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)
```


يملأ مستند القالب بالبيانات من مصادر متعددة، مُنتجًا تقريرًا مكتملًا بخيارات إضافية. هذا التحميل الزائد يحدد تلقائيًا تنسيق الحفظ بناءً على امتداد ملف الإخراج.

 **Remarks:** 

إذا كان تنسيق الإخراج صورة (BMP، EMF، EPS، GIF، JPEG، PNG، أو WebP)، سيتم حفظ كل صفحة من الإخراج كملف منفصل. سيُستخدم اسم ملف الإخراج المحدد لتوليد أسماء الملفات لكل جزء وفق القاعدة: outputFile\_partIndex.extension.

إذا كان تنسيق الإخراج TIFF، سيتم حفظ الإخراج كملف TIFF متعدد الإطارات واحد.

 **Examples:** 

يعرض كيفية تعبئة المستند بمصادر البيانات.

```

 public void buildReportDataSource() throws Exception {
     // There is a several ways to populate document with data sources:
     String doc = getMyDir() + "Report building.docx";

     MessageTestClass sender = new MessageTestClass("LINQ Reporting Engine", "Hello World");

     ReportBuilderOptions options = new ReportBuilderOptions();
     options.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);

     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.1.docx", sender, "s");
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.2.docx", new Object[]{sender}, new String[]{"s"});
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.3.docx", sender, "s", options);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.4.docx", SaveFormat.DOCX, sender, "s");
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.5.docx", SaveFormat.DOCX, new Object[]{sender}, new String[]{"s"});
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.6.docx", SaveFormat.DOCX, sender, "s", options);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.7.docx", SaveFormat.DOCX, new Object[]{sender}, new String[]{"s"}, options);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.8.docx", new Object[]{sender}, new String[]{"s"}, options);

     options = new ReportBuilderOptions();
     options.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);
     OutputStream[] images = ReportBuilder.buildReportToImages(doc, new ImageSaveOptions(SaveFormat.PNG), new Object[]{sender}, new String[]{"s"}, options);

     ReportBuilderContext reportBuilderContext = new ReportBuilderContext();
     reportBuilderContext.getReportBuilderOptions().setMissingMemberMessage("Missed members");
     reportBuilderContext.getDataSources().put(sender, "s");

     ReportBuilder.create(reportBuilderContext)
             .from(doc)
             .to(getArtifactsDir() + "LowCode.BuildReportDataSource.9.docx")
             .execute();
 }

 public static class MessageTestClass {
     public String getName() {
         return mName;
     }

     public void setName(String value) {
         mName = value;
     }

     private String mName;

     public String getMessage() {
         return mMessage;
     }

     public void setMessage(String value) {
         mMessage = value;
     }

     private String mMessage;

     public MessageTestClass(String name, String message) {
         setName(name);
         setMessage(message);
     }
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String | اسم ملف الإدخال. |
| outputFileName | java.lang.String | اسم ملف الإخراج. |
| بيانات | java.lang.Object[] | مصفوفة من كائنات مصدر البيانات. |
| dataSourceNames | java.lang.String[] | مصفوفة من الأسماء للإشارة إلى كائنات مصدر البيانات داخل القالب. |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) | خيارات إضافية لبناء التقرير. |

### buildReportToImages(InputStream inputStream, ImageSaveOptions saveOptions, Object[] data, String[] dataSourceNames) {#buildReportToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.Object---java.lang.String}
```
public static OutputStream[] buildReportToImages(InputStream inputStream, ImageSaveOptions saveOptions, Object[] data, String[] dataSourceNames)
```


يملأ مستند القالب بالبيانات من مصادر متعددة. يُحوِّل الإخراج إلى صور.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream | دفق ملف الإدخال. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | خيارات حفظ الإخراج. |
| بيانات | java.lang.Object[] | مصفوفة من كائنات مصدر البيانات. |
| dataSourceNames | java.lang.String[] | مصفوفة من الأسماء للإشارة إلى كائنات مصدر البيانات داخل القالب. |

**Returns:**
java.io.OutputStream[]
### buildReportToImages(InputStream inputStream, ImageSaveOptions saveOptions, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions) {#buildReportToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions}
```
public static OutputStream[] buildReportToImages(InputStream inputStream, ImageSaveOptions saveOptions, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)
```


يملأ مستند القالب بالبيانات من مصادر متعددة. يُحوِّل الإخراج إلى صور.

 **Examples:** 

يعرض كيفية تعبئة المستند بمصادر البيانات باستخدام المستندات من الدفق.

```

 // There is a several ways to populate document with data sources using documents from the stream:
 MessageTestClass sender = new MessageTestClass("LINQ Reporting Engine", "Hello World");

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Report building.docx")) {
     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.BuildReportDataSourceStream.1.docx")) {
         ReportBuilder.buildReport(streamIn, streamOut, SaveFormat.DOCX, new Object[]{sender}, new String[]{"s"});
     }

     try (FileOutputStream streamOut1 = new FileOutputStream(getArtifactsDir() + "LowCode.BuildReportDataSourceStream.2.docx")) {
         ReportBuilder.buildReport(streamIn, streamOut1, SaveFormat.DOCX, sender, "s");
     }

     try (FileOutputStream streamOut2 = new FileOutputStream(getArtifactsDir() + "LowCode.BuildReportDataSourceStream.3.docx")) {
         ReportBuilderOptions options = new ReportBuilderOptions();
         options.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);
         ReportBuilder.buildReport(streamIn, streamOut2, SaveFormat.DOCX, sender, "s", options);
     }

     ReportBuilderOptions options = new ReportBuilderOptions();
     options.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);
     OutputStream[] images = ReportBuilder.buildReportToImages(streamIn, new ImageSaveOptions(SaveFormat.PNG), new Object[]{sender}, new String[]{"s"}, options);

     ReportBuilderContext reportBuilderContext = new ReportBuilderContext();
     reportBuilderContext.getReportBuilderOptions().setMissingMemberMessage("Missed members");
     reportBuilderContext.getDataSources().put(sender, "s");

     try (FileOutputStream streamOut3 = new FileOutputStream(getArtifactsDir() + "LowCode.BuildReportDataSourceStream.4.docx")) {
         ReportBuilder.create(reportBuilderContext)
                 .from(streamIn)
                 .to(streamOut3, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream | دفق ملف الإدخال. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | خيارات حفظ الإخراج. |
| بيانات | java.lang.Object[] | مصفوفة من كائنات مصدر البيانات. |
| dataSourceNames | java.lang.String[] | مصفوفة من الأسماء للإشارة إلى كائنات مصدر البيانات داخل القالب. |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) | خيارات إضافية لبناء التقرير. |

**Returns:**
java.io.OutputStream[]
### buildReportToImages(String inputFileName, ImageSaveOptions saveOptions, Object[] data, String[] dataSourceNames) {#buildReportToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.Object---java.lang.String}
```
public static OutputStream[] buildReportToImages(String inputFileName, ImageSaveOptions saveOptions, Object[] data, String[] dataSourceNames)
```


يملأ مستند القالب بالبيانات من مصادر متعددة. يُحوِّل الإخراج إلى صور.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String | اسم ملف الإدخال. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | خيارات حفظ الإخراج. |
| بيانات | java.lang.Object[] | مصفوفة من كائنات مصدر البيانات. |
| dataSourceNames | java.lang.String[] | مصفوفة من الأسماء للإشارة إلى كائنات مصدر البيانات داخل القالب. |

**Returns:**
java.io.OutputStream[]
### buildReportToImages(String inputFileName, ImageSaveOptions saveOptions, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions) {#buildReportToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions}
```
public static OutputStream[] buildReportToImages(String inputFileName, ImageSaveOptions saveOptions, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)
```


يملأ مستند القالب بالبيانات من مصادر متعددة. يُحوِّل الإخراج إلى صور.

 **Examples:** 

يعرض كيفية تعبئة المستند بمصادر البيانات.

```

 public void buildReportDataSource() throws Exception {
     // There is a several ways to populate document with data sources:
     String doc = getMyDir() + "Report building.docx";

     MessageTestClass sender = new MessageTestClass("LINQ Reporting Engine", "Hello World");

     ReportBuilderOptions options = new ReportBuilderOptions();
     options.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);

     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.1.docx", sender, "s");
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.2.docx", new Object[]{sender}, new String[]{"s"});
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.3.docx", sender, "s", options);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.4.docx", SaveFormat.DOCX, sender, "s");
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.5.docx", SaveFormat.DOCX, new Object[]{sender}, new String[]{"s"});
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.6.docx", SaveFormat.DOCX, sender, "s", options);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.7.docx", SaveFormat.DOCX, new Object[]{sender}, new String[]{"s"}, options);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.8.docx", new Object[]{sender}, new String[]{"s"}, options);

     options = new ReportBuilderOptions();
     options.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);
     OutputStream[] images = ReportBuilder.buildReportToImages(doc, new ImageSaveOptions(SaveFormat.PNG), new Object[]{sender}, new String[]{"s"}, options);

     ReportBuilderContext reportBuilderContext = new ReportBuilderContext();
     reportBuilderContext.getReportBuilderOptions().setMissingMemberMessage("Missed members");
     reportBuilderContext.getDataSources().put(sender, "s");

     ReportBuilder.create(reportBuilderContext)
             .from(doc)
             .to(getArtifactsDir() + "LowCode.BuildReportDataSource.9.docx")
             .execute();
 }

 public static class MessageTestClass {
     public String getName() {
         return mName;
     }

     public void setName(String value) {
         mName = value;
     }

     private String mName;

     public String getMessage() {
         return mMessage;
     }

     public void setMessage(String value) {
         mMessage = value;
     }

     private String mMessage;

     public MessageTestClass(String name, String message) {
         setName(name);
         setMessage(message);
     }
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputFileName | java.lang.String | اسم ملف الإدخال. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | خيارات حفظ الإخراج. |
| بيانات | java.lang.Object[] | مصفوفة من كائنات مصدر البيانات. |
| dataSourceNames | java.lang.String[] | مصفوفة من الأسماء للإشارة إلى كائنات مصدر البيانات داخل القالب. |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) | خيارات إضافية لبناء التقرير. |

**Returns:**
java.io.OutputStream[]
### create() {#create}
```
public static ReportBuilder create()
```


ينشئ نسخة جديدة من معالج بناء التقرير.

**Returns:**
[ReportBuilder](../../com.aspose.words/reportbuilder/)
### create(ReportBuilderContext context) {#create-com.aspose.words.ReportBuilderContext}
```
public static ReportBuilder create(ReportBuilderContext context)
```


ينشئ نسخة جديدة من معالج بناء التقرير.

 **Examples:** 

يعرض كيفية تعبئة المستند بمصادر البيانات.

```

 public void buildReportDataSource() throws Exception {
     // There is a several ways to populate document with data sources:
     String doc = getMyDir() + "Report building.docx";

     MessageTestClass sender = new MessageTestClass("LINQ Reporting Engine", "Hello World");

     ReportBuilderOptions options = new ReportBuilderOptions();
     options.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);

     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.1.docx", sender, "s");
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.2.docx", new Object[]{sender}, new String[]{"s"});
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.3.docx", sender, "s", options);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.4.docx", SaveFormat.DOCX, sender, "s");
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.5.docx", SaveFormat.DOCX, new Object[]{sender}, new String[]{"s"});
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.6.docx", SaveFormat.DOCX, sender, "s", options);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.7.docx", SaveFormat.DOCX, new Object[]{sender}, new String[]{"s"}, options);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportDataSource.8.docx", new Object[]{sender}, new String[]{"s"}, options);

     options = new ReportBuilderOptions();
     options.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);
     OutputStream[] images = ReportBuilder.buildReportToImages(doc, new ImageSaveOptions(SaveFormat.PNG), new Object[]{sender}, new String[]{"s"}, options);

     ReportBuilderContext reportBuilderContext = new ReportBuilderContext();
     reportBuilderContext.getReportBuilderOptions().setMissingMemberMessage("Missed members");
     reportBuilderContext.getDataSources().put(sender, "s");

     ReportBuilder.create(reportBuilderContext)
             .from(doc)
             .to(getArtifactsDir() + "LowCode.BuildReportDataSource.9.docx")
             .execute();
 }

 public static class MessageTestClass {
     public String getName() {
         return mName;
     }

     public void setName(String value) {
         mName = value;
     }

     private String mName;

     public String getMessage() {
         return mMessage;
     }

     public void setMessage(String value) {
         mMessage = value;
     }

     private String mMessage;

     public MessageTestClass(String name, String message) {
         setName(name);
         setMessage(message);
     }
 }
 
```

يعرض كيفية تعبئة المستند بمصادر البيانات باستخدام المستندات من الدفق.

```

 // There is a several ways to populate document with data sources using documents from the stream:
 MessageTestClass sender = new MessageTestClass("LINQ Reporting Engine", "Hello World");

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Report building.docx")) {
     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.BuildReportDataSourceStream.1.docx")) {
         ReportBuilder.buildReport(streamIn, streamOut, SaveFormat.DOCX, new Object[]{sender}, new String[]{"s"});
     }

     try (FileOutputStream streamOut1 = new FileOutputStream(getArtifactsDir() + "LowCode.BuildReportDataSourceStream.2.docx")) {
         ReportBuilder.buildReport(streamIn, streamOut1, SaveFormat.DOCX, sender, "s");
     }

     try (FileOutputStream streamOut2 = new FileOutputStream(getArtifactsDir() + "LowCode.BuildReportDataSourceStream.3.docx")) {
         ReportBuilderOptions options = new ReportBuilderOptions();
         options.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);
         ReportBuilder.buildReport(streamIn, streamOut2, SaveFormat.DOCX, sender, "s", options);
     }

     ReportBuilderOptions options = new ReportBuilderOptions();
     options.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);
     OutputStream[] images = ReportBuilder.buildReportToImages(streamIn, new ImageSaveOptions(SaveFormat.PNG), new Object[]{sender}, new String[]{"s"}, options);

     ReportBuilderContext reportBuilderContext = new ReportBuilderContext();
     reportBuilderContext.getReportBuilderOptions().setMissingMemberMessage("Missed members");
     reportBuilderContext.getDataSources().put(sender, "s");

     try (FileOutputStream streamOut3 = new FileOutputStream(getArtifactsDir() + "LowCode.BuildReportDataSourceStream.4.docx")) {
         ReportBuilder.create(reportBuilderContext)
                 .from(streamIn)
                 .to(streamOut3, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| context | [ReportBuilderContext](../../com.aspose.words/reportbuildercontext/) |  |

**Returns:**
[ReportBuilder](../../com.aspose.words/reportbuilder/)
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
