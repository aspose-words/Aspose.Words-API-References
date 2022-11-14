---
title: DataSet
second_title: Aspose.Words for Java API 参考
description: 表示数据的内存缓存。
type: docs
weight: 24
url: /zh/java/com.aspose.words.net.system.data/dataset/
---

**遗产:**
java.lang.Object
```
public class DataSet
```

表示数据的内存缓存。
## 构造函数

| 构造函数 | 描述 |
| --- | --- |
| [DataSet()](#DataSet--) | 初始化一个新的实例[DataSet](../../com.aspose.words.net.system.data/dataset)班级。 |
| [DataSet(Connection connection)](#DataSet-java.sql.Connection-) | 使用从 Connection 获取的数据初始化 DataSet 类的新实例。 |
| [DataSet(Connection connection, String schemaName)](#DataSet-java.sql.Connection-java.lang.String-) | 使用从 Connection 获取的数据初始化 DataSet 类的新实例。 |
| [DataSet(String dataSetName)](#DataSet-java.lang.String-) | 初始化 a 的新实例[DataSet](../../com.aspose.words.net.system.data/dataset)具有给定名称的类。 |
## 方法

| 方法 | 描述 |
| --- | --- |
| [IsSchemaWasRead()](#IsSchemaWasRead--) |  |
| [clear()](#clear--) | 清除[DataSet](../../com.aspose.words.net.system.data/dataset)通过删除所有表中的所有行来删除任何数据。 |
| [close()](#close--) |  |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getDataSetName()](#getDataSetName--) | 获取当前名称[DataSet](../../com.aspose.words.net.system.data/dataset). |
| [getEnforceConstraints()](#getEnforceConstraints--) | 获取一个值，该值指示在尝试任何更新操作时是否遵循约束规则。 |
| [getNamespace()](#getNamespace--) | 获取的命名空间[DataSet](../../com.aspose.words.net.system.data/dataset). |
| [getRelations()](#getRelations--) | 获取链接表并允许从父表导航到子表的关系集合。 |
| [getTables()](#getTables--) | 获取包含在[DataSet](../../com.aspose.words.net.system.data/dataset). |
| [hashCode()](#hashCode--) |  |
| [isLocaleSpecified()](#isLocaleSpecified--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [readXml(InputStream stream)](#readXml-java.io.InputStream-) | 将 XML 模式和数据读入[DataSet](../../com.aspose.words.net.system.data/dataset)使用指定的 java.io.InputStream。 |
| [readXml(InputStream xmlStream, System.Data.XmlReadMode mode)](#readXml-java.io.InputStream-com.aspose.words.net.System.Data.XmlReadMode-) | 使用指定的 java.io.InputStream 和[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode). |
| [readXml(String fileName)](#readXml-java.lang.String-) | 将 XML 模式和数据读入[DataSet](../../com.aspose.words.net.system.data/dataset)使用指定的文件。 |
| [readXml(String xmlPath, System.Data.XmlReadMode readMode)](#readXml-java.lang.String-com.aspose.words.net.System.Data.XmlReadMode-) | 使用指定的文件将 XML 模式和数据读入数据集中[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode). |
| [readXmlSchema(InputStream stream)](#readXmlSchema-java.io.InputStream-) | 从指定的 java.io.InputStream 读取 XML 模式到[DataSet](../../com.aspose.words.net.system.data/dataset). |
| [readXmlSchema(String fileName)](#readXmlSchema-java.lang.String-) | 将指定文件中的 XML 模式读入[DataSet](../../com.aspose.words.net.system.data/dataset). |
| [reset()](#reset--) | 重置[DataSet](../../com.aspose.words.net.system.data/dataset)到原来的状态。 |
| [setDataSetName(String value)](#setDataSetName-java.lang.String-) | 设置当前的名称[DataSet](../../com.aspose.words.net.system.data/dataset). |
| [setEnforceConstraints(boolean value)](#setEnforceConstraints-boolean-) | 设置一个值，指示在尝试任何更新操作时是否遵循约束规则。 |
| [setLocale(Locale locale)](#setLocale-java.util.Locale-) | 设置用于比较表中字符串的语言环境信息。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### DataSet() {#DataSet--}
```
public DataSet()
```


初始化一个新的实例[DataSet](../../com.aspose.words.net.system.data/dataset)班级。

### DataSet(Connection connection) {#DataSet-java.sql.Connection-}
```
public DataSet(Connection connection)
```


使用从 Connection 获取的数据初始化 DataSet 类的新实例。表、关系、约束和索引将被复制到数据集中。

默认情况下不会使用模式名称。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| connection | java.sql.Connection | 其中包含数据库数据。 |

### DataSet(Connection connection, String schemaName) {#DataSet-java.sql.Connection-java.lang.String-}
```
public DataSet(Connection connection, String schemaName)
```


使用从 Connection 获取的数据初始化 DataSet 类的新实例。表、关系、约束和索引将被复制到数据集中。

`DataSet dataSet = new DataSet(conn, "PUBLIC"); // HSQLDB`

或者

`DataSet dataSet = new DataSet(conn); // MYSQL's default schema name.`

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| connection | java.sql.Connection | 其中包含数据库数据。 |
| schemaName | java.lang.String | 其中包含要导入的表。 |

### DataSet(String dataSetName) {#DataSet-java.lang.String-}
```
public DataSet(String dataSetName)
```


初始化 a 的新实例[DataSet](../../com.aspose.words.net.system.data/dataset)具有给定名称的类。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| dataSetName | java.lang.String | 的名称[DataSet](../../com.aspose.words.net.system.data/dataset). |

### IsSchemaWasRead() {#IsSchemaWasRead--}
```
public boolean IsSchemaWasRead()
```




**退货:**
boolean - 如果模式被读取则为真
### clear() {#clear--}
```
public void clear()
```


清除[DataSet](../../com.aspose.words.net.system.data/dataset)通过删除所有表中的所有行来删除任何数据。

### close() {#close--}
```
public void close()
```




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
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货:**
java.lang.Class<?>
### getDataSetName() {#getDataSetName--}
```
public String getDataSetName()
```


获取当前名称[DataSet](../../com.aspose.words.net.system.data/dataset).

**退货:**
java.lang.String - 的名称[DataSet](../../com.aspose.words.net.system.data/dataset).
### getEnforceConstraints() {#getEnforceConstraints--}
```
public boolean getEnforceConstraints()
```


获取一个值，该值指示在尝试任何更新操作时是否遵循约束规则。

**退货:**
布尔值 - 如果强制执行规则则为真；否则为假。默认为真。
### getNamespace() {#getNamespace--}
```
public String getNamespace()
```


获取的命名空间[DataSet](../../com.aspose.words.net.system.data/dataset).

**退货:**
 java.lang.String - 的命名空间[DataSet](../../com.aspose.words.net.system.data/dataset).
### getRelations() {#getRelations--}
```
public System.Data.DataRelationCollection getRelations()
```


获取链接表并允许从父表导航到子表的关系集合。

**退货:**
[DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection) - 一个[DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection)包含的集合[DataRelation](../../com.aspose.words.net.system.data/datarelation)对象。如果没有，则返回一个空集合[DataRelation](../../com.aspose.words.net.system.data/datarelation)对象存在。
### getTables() {#getTables--}
```
public System.Data.DataTableCollection getTables()
```


获取包含在[DataSet](../../com.aspose.words.net.system.data/dataset).

**退货:**
[DataTableCollection](../../com.aspose.words.net.system.data/datatablecollection) - 这[DataTableCollection](../../com.aspose.words.net.system.data/datatablecollection)包含在这个[DataSet](../../com.aspose.words.net.system.data/dataset).如果没有，则返回一个空集合[DataTable](../../com.aspose.words.net.system.data/datatable)对象存在。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### isLocaleSpecified() {#isLocaleSpecified--}
```
public boolean isLocaleSpecified()
```




**退货:**
boolean - 如果设置了语言环境，则为 true
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### readXml(InputStream stream) {#readXml-java.io.InputStream-}
```
public System.Data.XmlReadMode readXml(InputStream stream)
```


将 XML 模式和数据读入[DataSet](../../com.aspose.words.net.system.data/dataset)使用指定的 java.io.InputStream。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| stream | java.io.InputStream | 从 java.io.InputStream 派生的对象。 |

**退货:**
[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode) - 这[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode)用于读取数据。返回值是以下之一[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode)常数。
### readXml(InputStream xmlStream, System.Data.XmlReadMode mode) {#readXml-java.io.InputStream-com.aspose.words.net.System.Data.XmlReadMode-}
```
public System.Data.XmlReadMode readXml(InputStream xmlStream, System.Data.XmlReadMode mode)
```


使用指定的 java.io.InputStream 和[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| xmlStream | java.io.InputStream | 要从中读取的 Stream。 |
| mode | [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode) | 中的一个[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode)值。 |

**退货:**
[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode) - 用于读取数据的 XmlReadMode。
### readXml(String fileName) {#readXml-java.lang.String-}
```
public System.Data.XmlReadMode readXml(String fileName)
```


将 XML 模式和数据读入[DataSet](../../com.aspose.words.net.system.data/dataset)使用指定的文件。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | java.lang.String | 要从中读取的文件名（包括路径）。 |

**退货:**
[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode) - 用于读取数据的 XmlReadMode。返回值是以下之一[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode)常数。
### readXml(String xmlPath, System.Data.XmlReadMode readMode) {#readXml-java.lang.String-com.aspose.words.net.System.Data.XmlReadMode-}
```
public System.Data.XmlReadMode readXml(String xmlPath, System.Data.XmlReadMode readMode)
```


使用指定的文件将 XML 模式和数据读入数据集中[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| xmlPath | java.lang.String | 指定的文件 |
| readMode | [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode) | \{[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode) |

**退货:**
[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode) 阅读时使用的模式
### readXmlSchema(InputStream stream) {#readXmlSchema-java.io.InputStream-}
```
public void readXmlSchema(InputStream stream)
```


从指定的 java.io.InputStream 读取 XML 模式到[DataSet](../../com.aspose.words.net.system.data/dataset).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| stream | java.io.InputStream | 要从中读取的 java.io.InputStream。 |

### readXmlSchema(String fileName) {#readXmlSchema-java.lang.String-}
```
public void readXmlSchema(String fileName)
```


将指定文件中的 XML 模式读入[DataSet](../../com.aspose.words.net.system.data/dataset).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | java.lang.String | 要从中读取的文件名（包括路径）。 |

### reset() {#reset--}
```
public void reset()
```


重置[DataSet](../../com.aspose.words.net.system.data/dataset)回到原来的状态。子类应该覆盖[reset()](../../com.aspose.words.net.system.data/dataset\#reset--)恢复一个[DataSet](../../com.aspose.words.net.system.data/dataset)到原来的状态。

### setDataSetName(String value) {#setDataSetName-java.lang.String-}
```
public void setDataSetName(String value)
```


设置当前的名称[DataSet](../../com.aspose.words.net.system.data/dataset).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 的名称[DataSet](../../com.aspose.words.net.system.data/dataset). |

### setEnforceConstraints(boolean value) {#setEnforceConstraints-boolean-}
```
public void setEnforceConstraints(boolean value)
```


设置一个值，指示在尝试任何更新操作时是否遵循约束规则。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 如果规则被强制执行，则为 true；否则为假。默认值为真。 |

### setLocale(Locale locale) {#setLocale-java.util.Locale-}
```
public void setLocale(Locale locale)
```


设置用于比较表中字符串的语言环境信息。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| locale | java.util.Locale | 这个数据集的 |

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
