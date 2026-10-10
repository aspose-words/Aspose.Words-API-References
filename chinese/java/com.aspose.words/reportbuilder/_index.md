---
title: "ReportBuilder"
linktitle: "ReportBuilder"
second_title: "Aspose.Words for Java"
description: "提供使用 Java 中 LINQ Reporting Engine 填充模板数据的方法。"
type: docs
weight: 571
url: /zh/java/com.aspose.words/reportbuilder/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Processor](../../com.aspose.words/processor/)
```
public class ReportBuilder extends Processor
```

提供使用 LINQ Reporting Engine 填充模板数据的方法。
## 方法

| 方法 | 描述 |
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
| [buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object data)](#buildReport-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.Object) | 使用指定来源的数据填充模板文档，生成具有指定输出格式和其他选项的完整报告。 |
| [buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object data, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.Object-com.aspose.words.ReportBuilderOptions) | 使用指定来源的数据填充模板文档，生成具有指定输出格式和其他选项的完整报告。 |
| [buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object data, String dataSourceName)](#buildReport-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.Object-java.lang.String) | 使用指定来源的数据填充模板文档，生成具有指定输出格式、具名数据源引用以及其他选项的完整报告。 |
| [buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.Object-java.lang.String-com.aspose.words.ReportBuilderOptions) | 使用指定来源的数据填充模板文档，生成具有指定输出格式、具名数据源引用以及其他选项的完整报告。 |
| [buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object[] data, String[] dataSourceNames)](#buildReport-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.Object---java.lang.String) | 使用多个来源的数据填充模板文档，生成具有指定输出格式和其他选项的完整报告。 |
| [buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions) | 使用多个来源的数据填充模板文档，生成具有指定输出格式和其他选项的完整报告。 |
| [buildReport(String inputFileName, String outputFileName, int saveFormat, Object data)](#buildReport-java.lang.String-java.lang.String-int-java.lang.Object) |  |
| [buildReport(String inputFileName, String outputFileName, int saveFormat, Object data, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.lang.String-java.lang.String-int-java.lang.Object-com.aspose.words.ReportBuilderOptions) |  |
| [buildReport(String inputFileName, String outputFileName, int saveFormat, Object data, String dataSourceName)](#buildReport-java.lang.String-java.lang.String-int-java.lang.Object-java.lang.String) |  |
| [buildReport(String inputFileName, String outputFileName, int saveFormat, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.lang.String-java.lang.String-int-java.lang.Object-java.lang.String-com.aspose.words.ReportBuilderOptions) |  |
| [buildReport(String inputFileName, String outputFileName, int saveFormat, Object[] data, String[] dataSourceNames)](#buildReport-java.lang.String-java.lang.String-int-java.lang.Object---java.lang.String) |  |
| [buildReport(String inputFileName, String outputFileName, int saveFormat, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.lang.String-java.lang.String-int-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions) |  |
| [buildReport(String inputFileName, String outputFileName, Object data)](#buildReport-java.lang.String-java.lang.String-java.lang.Object) | 使用指定来源的数据填充模板文档，生成带有附加选项的完整报告。 |
| [buildReport(String inputFileName, String outputFileName, Object data, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.lang.String-java.lang.String-java.lang.Object-com.aspose.words.ReportBuilderOptions) | 使用指定来源的数据填充模板文档，生成带有附加选项的完整报告。 |
| [buildReport(String inputFileName, String outputFileName, Object data, String dataSourceName)](#buildReport-java.lang.String-java.lang.String-java.lang.Object-java.lang.String) | 使用指定来源的数据填充模板文档，生成带有命名数据源引用和附加选项的完整报告。 |
| [buildReport(String inputFileName, String outputFileName, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.lang.String-java.lang.String-java.lang.Object-java.lang.String-com.aspose.words.ReportBuilderOptions) | 使用指定来源的数据填充模板文档，生成带有命名数据源引用和附加选项的完整报告。 |
| [buildReport(String inputFileName, String outputFileName, Object[] data, String[] dataSourceNames)](#buildReport-java.lang.String-java.lang.String-java.lang.Object---java.lang.String) | 使用多个来源的数据填充模板文档，生成带有附加选项的完整报告。 |
| [buildReport(String inputFileName, String outputFileName, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)](#buildReport-java.lang.String-java.lang.String-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions) | 使用多个来源的数据填充模板文档，生成带有附加选项的完整报告。 |
| [buildReportToImages(InputStream inputStream, ImageSaveOptions saveOptions, Object[] data, String[] dataSourceNames)](#buildReportToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.Object---java.lang.String) | 使用多个来源的数据填充模板文档。 |
| [buildReportToImages(InputStream inputStream, ImageSaveOptions saveOptions, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)](#buildReportToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions) | 使用多个来源的数据填充模板文档。 |
| [buildReportToImages(String inputFileName, ImageSaveOptions saveOptions, Object[] data, String[] dataSourceNames)](#buildReportToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.Object---java.lang.String) | 使用多个来源的数据填充模板文档。 |
| [buildReportToImages(String inputFileName, ImageSaveOptions saveOptions, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)](#buildReportToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions) | 使用多个来源的数据填充模板文档。 |
| [create()](#create) | 创建报告生成器处理器的新实例。 |
| [create(ReportBuilderContext context)](#create-com.aspose.words.ReportBuilderContext) | 创建报告生成器处理器的新实例。 |
| [execute()](#execute) | 执行处理器操作。 |
| [from(InputStream input)](#from-java.io.InputStream) | 指定用于处理的输入文档。 |
| [from(InputStream input, LoadOptions loadOptions)](#from-java.io.InputStream-com.aspose.words.LoadOptions) | 指定用于处理的输入文档。 |
| [from(String input)](#from-java.lang.String) | 指定用于处理的输入文档。 |
| [from(String input, LoadOptions loadOptions)](#from-java.lang.String-com.aspose.words.LoadOptions) | 指定用于处理的输入文档。 |
| [to(OutputStream output, SaveOptions saveOptions)](#to-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [to(OutputStream output, int saveFormat)](#to-java.io.OutputStream-int) |  |
| [to(String output)](#to-java.lang.String) | 指定处理器的输出文件。 |
| [to(String output, SaveOptions saveOptions)](#to-java.lang.String-com.aspose.words.SaveOptions) | 指定处理器的输出文件。 |
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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| 数据 | java.lang.Object |  |

### buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object data, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.Object-com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object data, ReportBuilderOptions reportBuilderOptions)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| 数据 | java.lang.Object |  |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) |  |

### buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object data, String dataSourceName) {#buildReport-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.Object-java.lang.String}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object data, String dataSourceName)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| 数据 | java.lang.Object |  |
| dataSourceName | java.lang.String |  |

### buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.Object-java.lang.String-com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| 数据 | java.lang.Object |  |
| dataSourceName | java.lang.String |  |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) |  |

### buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object[] data, String[] dataSourceNames) {#buildReport-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.Object---java.lang.String}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object[] data, String[] dataSourceNames)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| 数据 | java.lang.Object[] |  |
| dataSourceNames | java.lang.String[] |  |

### buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| 数据 | java.lang.Object[] |  |
| dataSourceNames | java.lang.String[] |  |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) |  |

### buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object data) {#buildReport-java.io.InputStream-java.io.OutputStream-int-java.lang.Object}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object data)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| 数据 | java.lang.Object |  |

### buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object data, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.io.InputStream-java.io.OutputStream-int-java.lang.Object-com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object data, ReportBuilderOptions reportBuilderOptions)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| 数据 | java.lang.Object |  |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) |  |

### buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object data, String dataSourceName) {#buildReport-java.io.InputStream-java.io.OutputStream-int-java.lang.Object-java.lang.String}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object data, String dataSourceName)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| 数据 | java.lang.Object |  |
| dataSourceName | java.lang.String |  |

### buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.io.InputStream-java.io.OutputStream-int-java.lang.Object-java.lang.String-com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| 数据 | java.lang.Object |  |
| dataSourceName | java.lang.String |  |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) |  |

### buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object[] data, String[] dataSourceNames) {#buildReport-java.io.InputStream-java.io.OutputStream-int-java.lang.Object---java.lang.String}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object[] data, String[] dataSourceNames)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| 数据 | java.lang.Object[] |  |
| dataSourceNames | java.lang.String[] |  |

### buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.io.InputStream-java.io.OutputStream-int-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(InputStream inputStream, OutputStream outputStream, int saveFormat, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| 数据 | java.lang.Object[] |  |
| dataSourceNames | java.lang.String[] |  |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) |  |

### buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object data) {#buildReport-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.Object}
```
public static void buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object data)
```


使用指定来源的数据填充模板文档，生成具有指定输出格式和其他选项的完整报告。

 **Remarks:** 

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则 outputFile\_partIndex.extension 为每个部分生成文件名。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| outputFileName | java.lang.String | 输出文件名。 |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | 输出的保存选项。 |
| 数据 | java.lang.Object | 数据源对象。 |

### buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object data, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.Object-com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object data, ReportBuilderOptions reportBuilderOptions)
```


使用指定来源的数据填充模板文档，生成具有指定输出格式和其他选项的完整报告。

 **Remarks:** 

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则 outputFile\_partIndex.extension 为每个部分生成文件名。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| outputFileName | java.lang.String | 输出文件名。 |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | 输出的保存选项。 |
| 数据 | java.lang.Object | 数据源对象。 |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) | 附加的报告生成选项。 |

### buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object data, String dataSourceName) {#buildReport-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.Object-java.lang.String}
```
public static void buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object data, String dataSourceName)
```


使用指定来源的数据填充模板文档，生成具有指定输出格式、具名数据源引用以及其他选项的完整报告。

 **Remarks:** 

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则 outputFile\_partIndex.extension 为每个部分生成文件名。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| outputFileName | java.lang.String | 输出文件名。 |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | 输出的保存选项。 |
| 数据 | java.lang.Object | 数据源对象。 |
| dataSourceName | java.lang.String | 用于在模板中引用数据源对象的名称。 |

### buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.Object-java.lang.String-com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions)
```


使用指定来源的数据填充模板文档，生成具有指定输出格式、具名数据源引用以及其他选项的完整报告。

 **Remarks:** 

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则 outputFile\_partIndex.extension 为每个部分生成文件名。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| outputFileName | java.lang.String | 输出文件名。 |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | 输出的保存选项。 |
| 数据 | java.lang.Object | 数据源对象。 |
| dataSourceName | java.lang.String | 用于在模板中引用数据源对象的名称。 |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) | 附加的报告生成选项。 |

### buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object[] data, String[] dataSourceNames) {#buildReport-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.Object---java.lang.String}
```
public static void buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object[] data, String[] dataSourceNames)
```


使用多个来源的数据填充模板文档，生成具有指定输出格式和其他选项的完整报告。

 **Remarks:** 

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则 outputFile\_partIndex.extension 为每个部分生成文件名。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| outputFileName | java.lang.String | 输出文件名。 |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | 输出的保存选项。 |
| 数据 | java.lang.Object[] | 数据源对象数组。 |
| dataSourceNames | java.lang.String[] | 用于在模板中引用数据源对象的名称数组。 |

### buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(String inputFileName, String outputFileName, SaveOptions saveOptions, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)
```


使用多个来源的数据填充模板文档，生成具有指定输出格式和其他选项的完整报告。

 **Remarks:** 

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则 outputFile\_partIndex.extension 为每个部分生成文件名。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| outputFileName | java.lang.String | 输出文件名。 |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | 输出的保存选项。 |
| 数据 | java.lang.Object[] | 数据源对象数组。 |
| dataSourceNames | java.lang.String[] | 用于在模板中引用数据源对象的名称数组。 |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) | 附加的报告生成选项。 |

### buildReport(String inputFileName, String outputFileName, int saveFormat, Object data) {#buildReport-java.lang.String-java.lang.String-int-java.lang.Object}
```
public static void buildReport(String inputFileName, String outputFileName, int saveFormat, Object data)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| 数据 | java.lang.Object |  |

### buildReport(String inputFileName, String outputFileName, int saveFormat, Object data, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.lang.String-java.lang.String-int-java.lang.Object-com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(String inputFileName, String outputFileName, int saveFormat, Object data, ReportBuilderOptions reportBuilderOptions)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| 数据 | java.lang.Object |  |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) |  |

### buildReport(String inputFileName, String outputFileName, int saveFormat, Object data, String dataSourceName) {#buildReport-java.lang.String-java.lang.String-int-java.lang.Object-java.lang.String}
```
public static void buildReport(String inputFileName, String outputFileName, int saveFormat, Object data, String dataSourceName)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| 数据 | java.lang.Object |  |
| dataSourceName | java.lang.String |  |

### buildReport(String inputFileName, String outputFileName, int saveFormat, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.lang.String-java.lang.String-int-java.lang.Object-java.lang.String-com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(String inputFileName, String outputFileName, int saveFormat, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| 数据 | java.lang.Object |  |
| dataSourceName | java.lang.String |  |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) |  |

### buildReport(String inputFileName, String outputFileName, int saveFormat, Object[] data, String[] dataSourceNames) {#buildReport-java.lang.String-java.lang.String-int-java.lang.Object---java.lang.String}
```
public static void buildReport(String inputFileName, String outputFileName, int saveFormat, Object[] data, String[] dataSourceNames)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| 数据 | java.lang.Object[] |  |
| dataSourceNames | java.lang.String[] |  |

### buildReport(String inputFileName, String outputFileName, int saveFormat, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.lang.String-java.lang.String-int-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(String inputFileName, String outputFileName, int saveFormat, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| 数据 | java.lang.Object[] |  |
| dataSourceNames | java.lang.String[] |  |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) |  |

### buildReport(String inputFileName, String outputFileName, Object data) {#buildReport-java.lang.String-java.lang.String-java.lang.Object}
```
public static void buildReport(String inputFileName, String outputFileName, Object data)
```


使用指定来源的数据填充模板文档，生成带有附加选项的完整报告。

 **Remarks:** 

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则 outputFile\_partIndex.extension 为每个部分生成文件名。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| outputFileName | java.lang.String | 输出文件名。 |
| 数据 | java.lang.Object | 数据源对象。 |

### buildReport(String inputFileName, String outputFileName, Object data, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.lang.String-java.lang.String-java.lang.Object-com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(String inputFileName, String outputFileName, Object data, ReportBuilderOptions reportBuilderOptions)
```


使用指定来源的数据填充模板文档，生成带有附加选项的完整报告。

 **Remarks:** 

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则 outputFile\_partIndex.extension 为每个部分生成文件名。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

 **Examples:** 

展示如何使用数据填充文档。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| outputFileName | java.lang.String | 输出文件名。 |
| 数据 | java.lang.Object | 数据源对象。 |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) | 附加的报告生成选项。 |

### buildReport(String inputFileName, String outputFileName, Object data, String dataSourceName) {#buildReport-java.lang.String-java.lang.String-java.lang.Object-java.lang.String}
```
public static void buildReport(String inputFileName, String outputFileName, Object data, String dataSourceName)
```


使用指定来源的数据填充模板文档，生成带有命名数据源引用和附加选项的完整报告。

 **Remarks:** 

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则 outputFile\_partIndex.extension 为每个部分生成文件名。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| outputFileName | java.lang.String | 输出文件名。 |
| 数据 | java.lang.Object | 数据源对象。 |
| dataSourceName | java.lang.String | 用于在模板中引用数据源对象的名称。 |

### buildReport(String inputFileName, String outputFileName, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.lang.String-java.lang.String-java.lang.Object-java.lang.String-com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(String inputFileName, String outputFileName, Object data, String dataSourceName, ReportBuilderOptions reportBuilderOptions)
```


使用指定来源的数据填充模板文档，生成带有命名数据源引用和附加选项的完整报告。

 **Remarks:** 

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则 outputFile\_partIndex.extension 为每个部分生成文件名。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

 **Examples:** 

展示如何使用数据源填充文档。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| outputFileName | java.lang.String | 输出文件名。 |
| 数据 | java.lang.Object | 数据源对象。 |
| dataSourceName | java.lang.String | 用于在模板中引用数据源对象的名称。 |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) | 附加的报告生成选项。 |

### buildReport(String inputFileName, String outputFileName, Object[] data, String[] dataSourceNames) {#buildReport-java.lang.String-java.lang.String-java.lang.Object---java.lang.String}
```
public static void buildReport(String inputFileName, String outputFileName, Object[] data, String[] dataSourceNames)
```


使用多个来源的数据填充模板文档，生成带有附加选项的完整报告。此重载会根据输出文件扩展名自动确定保存格式。

 **Remarks:** 

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则 outputFile\_partIndex.extension 为每个部分生成文件名。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| outputFileName | java.lang.String | 输出文件名。 |
| 数据 | java.lang.Object[] | 数据源对象数组。 |
| dataSourceNames | java.lang.String[] | 用于在模板中引用数据源对象的名称数组。 |

### buildReport(String inputFileName, String outputFileName, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions) {#buildReport-java.lang.String-java.lang.String-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions}
```
public static void buildReport(String inputFileName, String outputFileName, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)
```


使用多个来源的数据填充模板文档，生成带有附加选项的完整报告。此重载会根据输出文件扩展名自动确定保存格式。

 **Remarks:** 

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），输出的每一页将保存为单独的文件。指定的输出文件名将用于按照规则 outputFile\_partIndex.extension 为每个部分生成文件名。

如果输出格式是 TIFF，输出将保存为单个多帧 TIFF 文件。

 **Examples:** 

展示如何使用数据源填充文档。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| outputFileName | java.lang.String | 输出文件名。 |
| 数据 | java.lang.Object[] | 数据源对象数组。 |
| dataSourceNames | java.lang.String[] | 用于在模板中引用数据源对象的名称数组。 |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) | 附加的报告生成选项。 |

### buildReportToImages(InputStream inputStream, ImageSaveOptions saveOptions, Object[] data, String[] dataSourceNames) {#buildReportToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.Object---java.lang.String}
```
public static OutputStream[] buildReportToImages(InputStream inputStream, ImageSaveOptions saveOptions, Object[] data, String[] dataSourceNames)
```


使用多个来源的数据填充模板文档。将输出渲染为图像。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream | 输入文件流。 |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | 输出的保存选项。 |
| 数据 | java.lang.Object[] | 数据源对象数组。 |
| dataSourceNames | java.lang.String[] | 用于在模板中引用数据源对象的名称数组。 |

**Returns:**
java.io.OutputStream[]
### buildReportToImages(InputStream inputStream, ImageSaveOptions saveOptions, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions) {#buildReportToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions}
```
public static OutputStream[] buildReportToImages(InputStream inputStream, ImageSaveOptions saveOptions, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)
```


使用多个来源的数据填充模板文档。将输出渲染为图像。

 **Examples:** 

展示如何使用来自流的文档和数据源填充文档。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | java.io.InputStream | 输入文件流。 |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | 输出的保存选项。 |
| 数据 | java.lang.Object[] | 数据源对象数组。 |
| dataSourceNames | java.lang.String[] | 用于在模板中引用数据源对象的名称数组。 |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) | 附加的报告生成选项。 |

**Returns:**
java.io.OutputStream[]
### buildReportToImages(String inputFileName, ImageSaveOptions saveOptions, Object[] data, String[] dataSourceNames) {#buildReportToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.Object---java.lang.String}
```
public static OutputStream[] buildReportToImages(String inputFileName, ImageSaveOptions saveOptions, Object[] data, String[] dataSourceNames)
```


使用多个来源的数据填充模板文档。将输出渲染为图像。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | 输出的保存选项。 |
| 数据 | java.lang.Object[] | 数据源对象数组。 |
| dataSourceNames | java.lang.String[] | 用于在模板中引用数据源对象的名称数组。 |

**Returns:**
java.io.OutputStream[]
### buildReportToImages(String inputFileName, ImageSaveOptions saveOptions, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions) {#buildReportToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.Object---java.lang.String---com.aspose.words.ReportBuilderOptions}
```
public static OutputStream[] buildReportToImages(String inputFileName, ImageSaveOptions saveOptions, Object[] data, String[] dataSourceNames, ReportBuilderOptions reportBuilderOptions)
```


使用多个来源的数据填充模板文档。将输出渲染为图像。

 **Examples:** 

展示如何使用数据源填充文档。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | java.lang.String | 输入文件名。 |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | 输出的保存选项。 |
| 数据 | java.lang.Object[] | 数据源对象数组。 |
| dataSourceNames | java.lang.String[] | 用于在模板中引用数据源对象的名称数组。 |
| reportBuilderOptions | [ReportBuilderOptions](../../com.aspose.words/reportbuilderoptions/) | 附加的报告生成选项。 |

**Returns:**
java.io.OutputStream[]
### create() {#create}
```
public static ReportBuilder create()
```


创建报告生成器处理器的新实例。

**Returns:**
[ReportBuilder](../../com.aspose.words/reportbuilder/)
### create(ReportBuilderContext context) {#create-com.aspose.words.ReportBuilderContext}
```
public static ReportBuilder create(ReportBuilderContext context)
```


创建报告生成器处理器的新实例。

 **Examples:** 

展示如何使用数据源填充文档。

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

展示如何使用来自流的文档和数据源填充文档。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| context | [ReportBuilderContext](../../com.aspose.words/reportbuildercontext/) |  |

**Returns:**
[ReportBuilder](../../com.aspose.words/reportbuilder/)
### execute() {#execute}
```
public void execute()
```


执行处理器操作。

 **Examples:** 

展示如何在上下文中将文档合并为单个输出文档。

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

展示如何在上下文中将来自流的文档合并为单个输出文档。

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

展示如何在上下文中使用一行代码转换文档。

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

展示如何在上下文中使用一行代码将来自流的文档转换。

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


指定用于处理的输入文档。

 **Remarks:** 

如果处理器仅接受单个文件作为输入，则只会处理最后指定的文件。 [Merger](../../com.aspose.words/merger/) 处理器接受多个文件作为输入，结果是所有指定的文档将被合并。 [Converter](../../com.aspose.words/converter/) 处理器仅接受单个文件作为输入，因此只会转换最后指定的文件。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 输入 | java.io.InputStream | 输入文档流。 |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file stream.
### from(InputStream input, LoadOptions loadOptions) {#from-java.io.InputStream-com.aspose.words.LoadOptions}
```
public Processor from(InputStream input, LoadOptions loadOptions)
```


指定用于处理的输入文档。

 **Remarks:** 

如果处理器仅接受单个文件作为输入，则只会处理最后指定的文件。 [Merger](../../com.aspose.words/merger/) 处理器接受多个文件作为输入，结果是所有指定的文档将被合并。 [Converter](../../com.aspose.words/converter/) 处理器仅接受单个文件作为输入，因此只会转换最后指定的文件。

 **Examples:** 

展示如何在上下文中将来自流的文档合并为单个输出文档。

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

展示如何在上下文中使用一行代码将来自流的文档转换。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 输入 | java.io.InputStream | 输入文档流。 |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | 用于加载文档的可选加载选项。 |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file stream.
### from(String input) {#from-java.lang.String}
```
public Processor from(String input)
```


指定用于处理的输入文档。

 **Remarks:** 

如果处理器仅接受单个文件作为输入，则只会处理最后指定的文件。 [Merger](../../com.aspose.words/merger/) 处理器接受多个文件作为输入，结果是所有指定的文档将被合并。 [Converter](../../com.aspose.words/converter/) 处理器仅接受单个文件作为输入，因此只会转换最后指定的文件。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 输入 | java.lang.String | 输入文档文件名。 |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file.
### from(String input, LoadOptions loadOptions) {#from-java.lang.String-com.aspose.words.LoadOptions}
```
public Processor from(String input, LoadOptions loadOptions)
```


指定用于处理的输入文档。

 **Remarks:** 

如果处理器仅接受单个文件作为输入，则只会处理最后指定的文件。 [Merger](../../com.aspose.words/merger/) 处理器接受多个文件作为输入，结果是所有指定的文档将被合并。 [Converter](../../com.aspose.words/converter/) 处理器仅接受单个文件作为输入，因此只会转换最后指定的文件。

 **Examples:** 

展示如何在上下文中将文档合并为单个输出文档。

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

展示如何在上下文中使用一行代码转换文档。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 输入 | java.lang.String | 输入文档文件名。 |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | 用于加载文档的可选加载选项。 |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file.
### to(OutputStream output, SaveOptions saveOptions) {#to-java.io.OutputStream-com.aspose.words.SaveOptions}
```
public Processor to(OutputStream output, SaveOptions saveOptions)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 输出 | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(OutputStream output, int saveFormat) {#to-java.io.OutputStream-int}
```
public Processor to(OutputStream output, int saveFormat)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 输出 | java.io.OutputStream |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(String output) {#to-java.lang.String}
```
public Processor to(String output)
```


指定处理器的输出文件。

 **Remarks:** 

如果输出包含多个文件，则使用指定的输出文件名按照规则 'outputFile\\_partIndex.extension' 为每个部分生成文件名。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 输出 | java.lang.String | 输出文件名。 |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified output file.
### to(String output, SaveOptions saveOptions) {#to-java.lang.String-com.aspose.words.SaveOptions}
```
public Processor to(String output, SaveOptions saveOptions)
```


指定处理器的输出文件。

 **Remarks:** 

如果输出包含多个文件，则使用指定的输出文件名按照规则 'outputFile\\_partIndex.extension' 为每个部分生成文件名。

 **Examples:** 

展示如何在上下文中将文档合并为单个输出文档。

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

展示如何在上下文中使用一行代码转换文档。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 输出 | java.lang.String | 输出文件名。 |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | 可选的保存选项。如果未指定，保存格式将由文件扩展名决定。 |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified output file.
### to(String output, int saveFormat) {#to-java.lang.String-int}
```
public Processor to(String output, int saveFormat)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 输出 | java.lang.String |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(ArrayList output, SaveOptions saveOptions) {#to-java.util.ArrayList-com.aspose.words.SaveOptions}
```
public Processor to(ArrayList output, SaveOptions saveOptions)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 输出 | java.util.ArrayList |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(ArrayList output, int saveFormat) {#to-java.util.ArrayList-int}
```
public Processor to(ArrayList output, int saveFormat)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 输出 | java.util.ArrayList |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### toOutput(ArrayList output, SaveOptions saveOptions) {#toOutput-java.util.ArrayList-com.aspose.words.SaveOptions}
```
public Processor toOutput(ArrayList output, SaveOptions saveOptions)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 输出 | java.util.ArrayList |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### toOutput(ArrayList output, int saveFormat) {#toOutput-java.util.ArrayList-int}
```
public Processor toOutput(ArrayList output, int saveFormat)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 输出 | java.util.ArrayList |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
