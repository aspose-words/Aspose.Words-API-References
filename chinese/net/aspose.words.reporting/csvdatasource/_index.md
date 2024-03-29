---
title: CsvDataSource Class
linktitle: CsvDataSource
articleTitle: CsvDataSource
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Reporting.CsvDataSource 班级. 提供对要在报告中使用的 CSV 文件或流的数据的访问 在 C#.
type: docs
weight: 4670
url: /zh/net/aspose.words.reporting/csvdatasource/
---
## CsvDataSource class

提供对要在报告中使用的 CSV 文件或流的数据的访问。

要了解更多信息，请访问[LINQ 报告引擎](https://docs.aspose.com/words/net/linq-reporting-engine/)文档文章。

```csharp
public class CsvDataSource
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [CsvDataSource](csvdatasource/#constructor)(*Stream*) | 使用解析 CSV 数据的默认选项，使用来自 CSV 流的数据创建新数据源。 |
| [CsvDataSource](csvdatasource/#constructor_2)(*string*) | 使用解析 CSV 数据的默认选项，使用 CSV 文件中的数据创建新数据源。 |
| [CsvDataSource](csvdatasource/#constructor_1)(*Stream, [CsvDataLoadOptions](../csvdataloadoptions/)*) | 使用解析 CSV 数据的指定选项，使用 CSV 流中的数据创建新数据源。 |
| [CsvDataSource](csvdatasource/#constructor_3)(*string, [CsvDataLoadOptions](../csvdataloadoptions/)*) | 使用用于解析 CSV 数据的指定选项，使用 CSV 文件中的数据创建新数据源。 |

## 评论

要在生成报告时访问相应文件或流的数据，请将此类的实例作为 数据源传递给以下之一：[`ReportingEngine`](../reportingengine/) .BuildReport 重载.

在模板文档中，`CsvDataSource`实例应以与 was a 相同的方式处理DataTable 实例。有关详细信息，请参阅模板语法参考 (https://docs.aspose.com/display/wordsnet/Template+Syntax)。

逗号分隔值的数据类型根据其字符串表示形式自动确定。因此，在 template 文档中，您可以使用键入的值而不仅仅是字符串。该引擎能够自动识别以下类型的 值：

* Nullable
* Nullable
* Nullable
* Nullable
* String

请注意，要自动识别数据类型，应使用不变区域性设置形成逗号分隔值的字符串表示形式。

要覆盖 CSV 数据加载的默认行为，请初始化并传递[`CsvDataLoadOptions`](../csvdataloadoptions/)instance 到此类的构造函数。

### 也可以看看

* 命名空间 [Aspose.Words.Reporting](../../aspose.words.reporting/)
* 部件 [Aspose.Words](../../)
