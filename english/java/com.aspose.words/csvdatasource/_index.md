---
title: CsvDataSource
second_title: Aspose.Words for Java API 参考
description: 提供对要在报告中使用的 CSV 文件或流的数据的访问。
type: docs
weight: 99
url: /zh/java/com.aspose.words/csvdatasource/
---

**遗产:**
java.lang.Object
```
public class CsvDataSource
```

提供对要在报告中使用的 CSV 文件或流的数据的访问。

要了解更多信息，请访问**LINQ Reporting Engine**文档文章。

要在生成报告时访问相应文件或流的数据，请将此类的实例作为数据源传递给其中一个[ReportingEngine](../../com.aspose.words/reportingengine)buildReport 重载。

在模板文档中，[CsvDataSource](../../com.aspose.words/csvdatasource)实例的处理方式应与它是[DataTable](../../com.aspose.words.net.system.data/datatable)实例。有关详细信息，请参阅模板语法参考 (https://docs.aspose.com/display/wordsjava/Template+Syntax)。

逗号分隔值的数据类型根据它们的字符串表示自动确定。因此，在模板文档中，您可以使用类型化的值而不仅仅是字符串。该引擎能够自动识别以下类型的值：

 *  
 *  
 *  
 *  
 *  

请注意，为了使数据类型的自动识别起作用，逗号分隔值的字符串表示应使用不变的区域性设置形成。

要覆盖 CSV 数据加载的默认行为，初始化并传递[CsvDataLoadOptions](../../com.aspose.words/csvdataloadoptions)实例到此类的构造函数。
## 构造函数s

| 构造函数 | 描述 |
| --- | --- |
| [CsvDataSource(String csvPath)](#CsvDataSource-java.lang.String-) | 使用解析 CSV 数据的默认选项使用来自 CSV 文件的数据创建新数据源。 |
| [CsvDataSource(String csvPath, CsvDataLoadOptions options)](#CsvDataSource-java.lang.String-com.aspose.words.CsvDataLoadOptions-) | 使用用于解析 CSV 数据的指定选项创建包含来自 CSV 文件的数据的新数据源。 |
| [CsvDataSource(InputStream csvStream)](#CsvDataSource-java.io.InputStream-) | 初始化此类的新实例。 |
| [CsvDataSource(InputStream csvStream, CsvDataLoadOptions options)](#CsvDataSource-java.io.InputStream-com.aspose.words.CsvDataLoadOptions-) | 初始化此类的新实例。 |
## 方法s

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get班级()](#get班级--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### CsvDataSource(String csvPath) {#CsvDataSource-java.lang.String-}
```
public CsvDataSource(String csvPath)
```


使用解析 CSV 数据的默认选项使用来自 CSV 文件的数据创建新数据源。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| csvPath | java.lang.String | 要用作数据源的 CSV 文件的路径。 |

### CsvDataSource(String csvPath, CsvDataLoadOptions options) {#CsvDataSource-java.lang.String-com.aspose.words.CsvDataLoadOptions-}
```
public CsvDataSource(String csvPath, CsvDataLoadOptions options)
```


使用用于解析 CSV 数据的指定选项创建包含来自 CSV 文件的数据的新数据源。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| csvPath | java.lang.String | 要用作数据源的 CSV 文件的路径。 |
| options | [CsvDataLoadOptions](../../com.aspose.words/csvdataloadoptions) | 用于解析 CSV 数据的选项。 |

### CsvDataSource(InputStream csvStream) {#CsvDataSource-java.io.InputStream-}
```
public CsvDataSource(InputStream csvStream)
```


初始化此类的新实例。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| csvStream | java.io.InputStream |  |

### CsvDataSource(InputStream csvStream, CsvDataLoadOptions options) {#CsvDataSource-java.io.InputStream-com.aspose.words.CsvDataLoadOptions-}
```
public CsvDataSource(InputStream csvStream, CsvDataLoadOptions options)
```


初始化此类的新实例。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| csvStream | java.io.InputStream |  |
| options | [CsvDataLoadOptions](../../com.aspose.words/csvdataloadoptions) |  |

### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**退货:**
布尔值
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### toString() {#toString--}
```
public String toString()
```




**退货:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
