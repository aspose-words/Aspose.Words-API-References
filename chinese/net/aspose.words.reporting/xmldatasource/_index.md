---
title: XmlDataSource Class
linktitle: XmlDataSource
articleTitle: XmlDataSource
second_title: Aspose.Words for .NET
description: 使用 Aspose.Words.XmlDataSource 解锁强大的报表功能。轻松访问 XML 数据，无缝集成到您的报表中，并增强数据可视化。
type: docs
weight: 5490
url: /zh/net/aspose.words.reporting/xmldatasource/
---
## XmlDataSource class

提供对报告中使用的 XML 文件或流的数据的访问。

要了解更多信息，请访问[LINQ 报告引擎](https://docs.aspose.com/words/net/linq-reporting-engine/)文档文章。

```csharp
public class XmlDataSource
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [XmlDataSource](xmldatasource/#constructor)(*Stream*) | 使用 XML 数据加载的默认选项，通过 XML 流中的数据创建新的数据源。 |
| [XmlDataSource](xmldatasource/#constructor_4)(*string*) | 使用 XML 数据加载的默认选项，从 XML 文件创建新的数据源。 |
| [XmlDataSource](xmldatasource/#constructor_2)(*Stream, Stream*) | 使用 XML Schema Definition 流创建一个包含 XML 流数据的新数据源。默认选项 用于加载 XML 数据。 |
| [XmlDataSource](xmldatasource/#constructor_1)(*Stream, [XmlDataLoadOptions](../xmldataloadoptions/)*) | 使用指定的 XML 数据加载选项，从 XML 流中创建新的数据源。 |
| [XmlDataSource](xmldatasource/#constructor_6)(*string, string*) | 使用 XML Schema Definition 文件创建一个包含 XML 文件中数据的新数据源。默认选项 用于加载 XML 数据。 |
| [XmlDataSource](xmldatasource/#constructor_5)(*string, [XmlDataLoadOptions](../xmldataloadoptions/)*) | 使用指定的 XML 数据加载选项，从 XML 文件创建新的数据源。 |
| [XmlDataSource](xmldatasource/#constructor_3)(*Stream, Stream, [XmlDataLoadOptions](../xmldataloadoptions/)*) | 使用 XML Schema Definition 流创建一个包含 XML 流数据的新数据源。指定的 选项用于加载 XML 数据。 |
| [XmlDataSource](xmldatasource/#constructor_7)(*string, string, [XmlDataLoadOptions](../xmldataloadoptions/)*) | 使用 XML 架构定义文件，使用 XML 文件中的数据创建新的数据源。指定的 选项用于加载 XML 数据。 |

## 评论

要在生成报告时访问相应文件或流的数据，请将此类的实例作为 数据源传递给以下之一[`ReportingEngine`](../reportingengine/).BuildReport 重载.

在模板文档中，如果顶级 XML 元素仅包含相同类型的元素列表，则 `XmlDataSource`实例应该以与 相同的方式处理DataTable 实例。否则，`XmlDataSource`实例应该以与 相同的方式处理DataRow 实例。有关更多信息，请参阅模板语法参考 (https://docs.aspose.com/display/wordsnet/Template+Syntax)。

当 XML Schema Definition 传递给此类的构造函数时，简单 XML 元素 和属性的值的数据类型将根据该 Schema 确定。因此，在模板文档中，您可以使用类型化的值 ，而不仅仅是字符串。

如果未将 XML 模式定义传递给此类的构造函数，则简单 XML 元素 和属性的值的数据类型将根据其字符串表示形式自动确定。因此，在模板文档中，在这种情况下，您也可以使用 来处理类型化的值。引擎能够自动识别以下类型的值：

* Nullable
* Nullable
* Nullable
* Nullable
* String

请注意，为了使数据类型自动识别能够正常工作，简单 XML 元素 和属性的值的字符串表示形式应使用不变的文化设置形成。

要覆盖 XML 数据加载的默认行为，请初始化并传递[`XmlDataLoadOptions`](../xmldataloadoptions/) 实例到此类的构造函数。

## 例子

展示如何使用 XML 作为数据源（字符串）。

```csharp
Document doc = new Document(MyDir + "Reporting engine template - XML data destination.docx");

XmlDataSource dataSource = new XmlDataSource(MyDir + "List of people.xml");
BuildReport(doc, dataSource, "persons");

doc.Save(ArtifactsDir + "ReportingEngine.XmlDataString.docx");
```

展示如何使用 XML 作为数据源（流）。

```csharp
Document doc = new Document(MyDir + "Reporting engine template - XML data destination.docx");

using (FileStream stream = File.OpenRead(MyDir + "List of people.xml"))
{
    XmlDataSource dataSource = new XmlDataSource(stream);
    BuildReport(doc, dataSource, "persons");
}

doc.Save(ArtifactsDir + "ReportingEngine.XmlDataStream.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words.Reporting](../../aspose.words.reporting/)
* 部件 [Aspose.Words](../../)
