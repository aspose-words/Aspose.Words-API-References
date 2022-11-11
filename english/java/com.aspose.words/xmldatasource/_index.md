---
title: XmlDataSource
second_title: Aspose.Words for Java API Reference
description: 提供对要在报告中使用的 XML 文件或流的数据的访问。
type: docs
weight: 628
url: /zh/java/com.aspose.words/xmldatasource/
---

**遗产:**
java.lang.Object
```
public class XmlDataSource
```

提供对要在报告中使用的 XML 文件或流的数据的访问。

要了解更多信息，请访问**LINQ Reporting Engine**文档文章。

要在生成报告时访问相应文件或流的数据，请将此类的实例作为数据源传递给其中一个[ReportingEngine](../../com.aspose.words/reportingengine)buildReport 重载。

在模板文档中，如果顶级 XML 元素仅包含相同类型的元素列表，则[XmlDataSource](../../com.aspose.words/xmldatasource)实例的处理方式应与它是[DataTable](../../com.aspose.words.net.system.data/datatable)实例。否则，一个[XmlDataSource](../../com.aspose.words/xmldatasource)实例的处理方式应与它是[DataRow](../../com.aspose.words.net.system.data/datarow)实例。有关详细信息，请参阅模板语法参考 (https://docs.aspose.com/display/wordsjava/Template+Syntax)。

当 XML Schema Definition 被传递给该类的构造函数时，简单 XML 元素和属性的值的数据类型是根据该模式确定的。因此，在模板文档中，您可以使用类型化的值而不仅仅是字符串。

当 XML Schema Definition 不传递给此类的构造函数时，简单 XML 元素和属性的值的数据类型将根据其字符串表示形式自动确定。因此，在模板文档中，您也可以在这种情况下使用键入的值。该引擎能够自动识别以下类型的值：

 *  
 *  
 *  
 *  
 *  

请注意，为了使数据类型的自动识别起作用，简单 XML 元素和属性值的字符串表示应该使用不变的文化设置形成。

要覆盖 XML 数据加载的默认行为，请初始化并传递[XmlDataLoadOptions](../../com.aspose.words/xmldataloadoptions)实例到此类的构造函数。
## 构造函数s

| 构造函数 | 描述 |
| --- | --- |
| [XmlDataSource(String xmlPath)](#XmlDataSource-java.lang.String-) | 使用 XML 数据加载的默认选项使用 XML 文件中的数据创建新数据源。 |
| [XmlDataSource(InputStream xmlStream)](#XmlDataSource-java.io.InputStream-) | 初始化此类的新实例。 |
| [XmlDataSource(String xmlPath, String xmlSchemaPath)](#XmlDataSource-java.lang.String-java.lang.String-) | 使用 XML 架构定义文件使用 XML 文件中的数据创建新数据源。 |
| [XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream)](#XmlDataSource-java.io.InputStream-java.io.InputStream-) | 初始化此类的新实例。 |
| [XmlDataSource(String xmlPath, XmlDataLoadOptions options)](#XmlDataSource-java.lang.String-com.aspose.words.XmlDataLoadOptions-) | 使用 XML 数据加载的指定选项，使用来自 XML 文件的数据创建新数据源。 |
| [XmlDataSource(InputStream xmlStream, XmlDataLoadOptions options)](#XmlDataSource-java.io.InputStream-com.aspose.words.XmlDataLoadOptions-) | 初始化此类的新实例。 |
| [XmlDataSource(String xmlPath, String xmlSchemaPath, XmlDataLoadOptions options)](#XmlDataSource-java.lang.String-java.lang.String-com.aspose.words.XmlDataLoadOptions-) | 使用 XML 架构定义文件使用 XML 文件中的数据创建新数据源。 |
| [XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream, XmlDataLoadOptions options)](#XmlDataSource-java.io.InputStream-java.io.InputStream-com.aspose.words.XmlDataLoadOptions-) | 初始化此类的新实例。 |
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
### XmlDataSource(String xmlPath) {#XmlDataSource-java.lang.String-}
```
public XmlDataSource(String xmlPath)
```


使用 XML 数据加载的默认选项使用 XML 文件中的数据创建新数据源。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| xmlPath | java.lang.String | 要用作数据源的 XML 文件的路径。 |

### XmlDataSource(InputStream xmlStream) {#XmlDataSource-java.io.InputStream-}
```
public XmlDataSource(InputStream xmlStream)
```


初始化此类的新实例。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| xmlStream | java.io.InputStream |  |

### XmlDataSource(String xmlPath, String xmlSchemaPath) {#XmlDataSource-java.lang.String-java.lang.String-}
```
public XmlDataSource(String xmlPath, String xmlSchemaPath)
```


使用 XML 架构定义文件使用 XML 文件中的数据创建新数据源。默认选项用于 XML 数据加载。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| xmlPath | java.lang.String | 要用作数据源的 XML 文件的路径。 |
| xmlSchemaPath | java.lang.String | 为 XML 文件提供架构的 XML 架构定义文件的路径。 |

### XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream) {#XmlDataSource-java.io.InputStream-java.io.InputStream-}
```
public XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream)
```


初始化此类的新实例。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| xmlStream | java.io.InputStream |  |
| xmlSchemaStream | java.io.InputStream |  |

### XmlDataSource(String xmlPath, XmlDataLoadOptions options) {#XmlDataSource-java.lang.String-com.aspose.words.XmlDataLoadOptions-}
```
public XmlDataSource(String xmlPath, XmlDataLoadOptions options)
```


使用 XML 数据加载的指定选项，使用来自 XML 文件的数据创建新数据源。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| xmlPath | java.lang.String | 要用作数据源的 XML 文件的路径。 |
| options | [XmlDataLoadOptions](../../com.aspose.words/xmldataloadoptions) | XML 数据加载的选项。 |

### XmlDataSource(InputStream xmlStream, XmlDataLoadOptions options) {#XmlDataSource-java.io.InputStream-com.aspose.words.XmlDataLoadOptions-}
```
public XmlDataSource(InputStream xmlStream, XmlDataLoadOptions options)
```


初始化此类的新实例。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| xmlStream | java.io.InputStream |  |
| options | [XmlDataLoadOptions](../../com.aspose.words/xmldataloadoptions) |  |

### XmlDataSource(String xmlPath, String xmlSchemaPath, XmlDataLoadOptions options) {#XmlDataSource-java.lang.String-java.lang.String-com.aspose.words.XmlDataLoadOptions-}
```
public XmlDataSource(String xmlPath, String xmlSchemaPath, XmlDataLoadOptions options)
```


使用 XML 架构定义文件使用 XML 文件中的数据创建新数据源。指定的选项用于 XML 数据加载。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| xmlPath | java.lang.String | 要用作数据源的 XML 文件的路径。 |
| xmlSchemaPath | java.lang.String | 为 XML 文件提供架构的 XML 架构定义文件的路径。 |
| options | [XmlDataLoadOptions](../../com.aspose.words/xmldataloadoptions) | XML 数据加载的选项。 |

### XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream, XmlDataLoadOptions options) {#XmlDataSource-java.io.InputStream-java.io.InputStream-com.aspose.words.XmlDataLoadOptions-}
```
public XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream, XmlDataLoadOptions options)
```


初始化此类的新实例。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| xmlStream | java.io.InputStream |  |
| xmlSchemaStream | java.io.InputStream |  |
| options | [XmlDataLoadOptions](../../com.aspose.words/xmldataloadoptions) |  |

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
