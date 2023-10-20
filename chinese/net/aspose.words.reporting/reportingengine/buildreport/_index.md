---
title: ReportingEngine.BuildReport
linktitle: BuildReport
articleTitle: BuildReport
second_title: 用于 .NET 的 Aspose.Words
description: ReportingEngine BuildReport 方法. 使用指定源的数据填充指定的模板文档使其成为就绪报告 在 C#.
type: docs
weight: 40
url: /zh/net/aspose.words.reporting/reportingengine/buildreport/
---
## BuildReport(*[Document](../../../aspose.words/document/), object*) {#buildreport}

使用指定源的数据填充指定的模板文档，使其成为就绪报告。

```csharp
public bool BuildReport(Document document, object dataSource)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| document | Document | 要填充数据的模板文档。 |
| dataSource | Object | 数据源对象。 |

### 返回值

指示模板文档解析是否成功的标志。 仅当以下值时返回的标志才有意义[`Options`](../options/)属性包括 InlineErrorMessages选项。

## 评论

使用此重载，您可以在模板文档中引用数据源的成员，但不能 引用数据源对象本身。您应该使用`BuildReport` 重载以实现此目的。

数据源对象可以是以下类型之一：

* [`XmlDataSource`](../../xmldatasource/)
* [`JsonDataSource`](../../jsondatasource/)
* [`CsvDataSource`](../../csvdatasource/)
* DataSet
* DataTable
* DataRow
* IDataReader
* IDataRecord
* DataView
* DataRowView
* 任何其他任意非动态和非匿名 .NET 类型

有关如何在模板文档中使用不同类型的数据源的信息，请参阅模板语法 参考 (https://docs.aspose.com/display/wordsnet/Template+Syntax)。

### 也可以看看

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* 命名空间 [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* 部件 [Aspose.Words](../../../)

---

## BuildReport(*[Document](../../../aspose.words/document/), object, string*) {#buildreport_1}

使用指定源的数据填充指定的模板文档，使其成为就绪报告。

```csharp
public bool BuildReport(Document document, object dataSource, string dataSourceName)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| document | Document | 要填充数据的模板文档。 |
| dataSource | Object | 数据源对象。 |
| dataSourceName | String | 用于引用模板中数据源对象的名称。 |

### 返回值

指示模板文档解析是否成功的标志。 仅当以下值时返回的标志才有意义[`Options`](../options/)属性包括 InlineErrorMessages选项。

## 评论

使用此重载，您可以在模板中引用数据源的成员和数据源对象本身。 如果您不打算引用数据源对象本身，则可以省略*dataSourceName* 路过`无效的`或使用`BuildReport`过载.

数据源对象可以是以下类型之一：

* [`XmlDataSource`](../../xmldatasource/)
* [`JsonDataSource`](../../jsondatasource/)
* [`CsvDataSource`](../../csvdatasource/)
* DataSet
* DataTable
* DataRow
* IDataReader
* IDataRecord
* DataView
* DataRowView
* 任何其他任意非动态和非匿名 .NET 类型

有关如何在模板文档中使用不同类型的数据源的信息，请参阅模板语法 参考 (https://docs.aspose.com/display/wordsnet/Template+Syntax)。

### 也可以看看

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* 命名空间 [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* 部件 [Aspose.Words](../../../)

---

## BuildReport(*[Document](../../../aspose.words/document/), object[], string[]*) {#buildreport_2}

使用指定源的数据填充指定的模板文档，使其成为就绪报告。

```csharp
public bool BuildReport(Document document, object[] dataSources, string[] dataSourceNames)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| document | Document | 要填充数据的模板文档。 |
| dataSources | Object[] | 数据源对象的数组。 |
| dataSourceNames | String[] | 用于引用模板内的数据源对象的名称数组。 |

### 返回值

指示模板文档解析是否成功的标志。 仅当以下值时返回的标志才有意义[`Options`](../options/)属性包括 InlineErrorMessages选项。

## 评论

使用此重载，您可以在模板中引用多个数据源对象及其成员。 第一个数据源的名称可以省略（即为空字符串或`无效的` 如果您要 引用数据源的成员而不是数据源对象本身。其他数据源 的名称必须指定且唯一。

如果您要使用单个数据源，请考虑使用 of`BuildReport` 和`BuildReport`相反，重载。

数据源对象可以是以下类型之一：

* [`XmlDataSource`](../../xmldatasource/)
* [`JsonDataSource`](../../jsondatasource/)
* [`CsvDataSource`](../../csvdatasource/)
* DataSet
* DataTable
* DataRow
* IDataReader
* IDataRecord
* DataView
* DataRowView
* 任何其他任意非动态和非匿名 .NET 类型

有关如何在模板文档中使用不同类型的数据源的信息，请参阅模板语法 参考 (https://docs.aspose.com/display/wordsnet/Template+Syntax)。

### 也可以看看

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* 命名空间 [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* 部件 [Aspose.Words](../../../)
