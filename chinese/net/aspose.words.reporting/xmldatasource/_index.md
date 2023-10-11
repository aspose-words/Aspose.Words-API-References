---
title: Class XmlDataSource
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Reporting.XmlDataSource 班级. 提供对要在报告中使用的 XML 文件或流的数据的访问
type: docs
weight: 4750
url: /zh/net/aspose.words.reporting/xmldatasource/
---
## XmlDataSource class

提供对要在报告中使用的 XML 文件或流的数据的访问。

要了解更多信息，请访问[LINQ 报告引擎](https://docs.aspose.com/words/net/linq-reporting-engine/)文档文章。

```csharp
public class XmlDataSource
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [XmlDataSource](xmldatasource/#constructor)(Stream) | 使用 XML 数据加载的默认选项，使用来自 XML 流的数据创建新数据源。 |
| [XmlDataSource](xmldatasource/#constructor_4)(string) | 使用 XML 数据加载的默认选项，使用 XML 文件中的数据创建新数据源。 |
| [XmlDataSource](xmldatasource/#constructor_2)(Stream, Stream) | 使用 XML 架构定义流，使用 XML 流中的数据创建新数据源。默认选项 用于XML数据加载。 |
| [XmlDataSource](xmldatasource/#constructor_1)(Stream, XmlDataLoadOptions) | 使用指定的 XML 数据加载选项，使用 XML 流中的数据创建新数据源。 |
| [XmlDataSource](xmldatasource/#constructor_6)(string, string) | 使用 XML 架构定义文件使用 XML 文件中的数据创建新数据源。默认选项 用于XML数据加载。 |
| [XmlDataSource](xmldatasource/#constructor_5)(string, XmlDataLoadOptions) | 使用 XML 数据加载的指定选项，使用 XML 文件中的数据创建新数据源。 |
| [XmlDataSource](xmldatasource/#constructor_3)(Stream, Stream, XmlDataLoadOptions) | 使用 XML 架构定义流，使用来自 XML 流的数据创建新数据源。指定的 选项用于XML数据加载。 |
| [XmlDataSource](xmldatasource/#constructor_7)(string, string, XmlDataLoadOptions) | 使用 XML 架构定义文件使用 XML 文件中的数据创建新数据源。指定的 选项用于XML数据加载。 |

### 评论

要在生成报告时访问相应文件或流的数据，请将此类的实例作为 数据源传递给以下之一：[`ReportingEngine`](../reportingengine/) .BuildReport 重载.

在模板文档中，如果顶级 XML 元素仅包含相同类型的元素列表，则 `XmlDataSource`实例应以与 a 相同的方式处理DataTable 实例。否则，一个`XmlDataSource`实例应以与 a 相同的方式处理DataRow 实例。有关详细信息，请参阅模板语法参考 (https://docs.aspose.com/display/wordsnet/Template+Syntax)。

当 XML 模式定义传递给此类的构造函数时，简单 XML 元素 和属性的值的数据类型根据模式确定。因此，在模板文档中，您可以使用键入的值 而不仅仅是字符串。

当 XML 架构定义未传递给此类的构造函数时，简单 XML 元素 和属性的值的数据类型将根据其字符串表示形式自动确定。因此，在模板文档中，在这种情况下您也可以使用 处理键入的值。引擎能够自动识别以下类型的值：

* Nullable
* Nullable
* Nullable
* Nullable
* String

请注意，要自动识别数据类型，应使用不变的区域性设置形成简单 XML 元素 和属性的值的字符串表示形式。

要覆盖 XML 数据加载的默认行为，请初始化并传递[`XmlDataLoadOptions`](../xmldataloadoptions/) 此类构造函数的实例。

### 也可以看看

* 命名空间 [Aspose.Words.Reporting](../../aspose.words.reporting/)
* 部件 [Aspose.Words](../../)


