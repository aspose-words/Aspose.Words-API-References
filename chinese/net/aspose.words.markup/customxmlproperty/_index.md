---
title: CustomXmlProperty Class
linktitle: CustomXmlProperty
articleTitle: CustomXmlProperty
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Markup.CustomXmlProperty 类，旨在简化管理自定义 XML 属性和智能标签属性，以增强文档控制。
type: docs
weight: 4630
url: /zh/net/aspose.words.markup/customxmlproperty/
---
## CustomXmlProperty class

代表单个自定义 XML 属性或智能标记属性。

要了解更多信息，请访问[结构化文档标签或内容控制](https://docs.aspose.com/words/net/working-with-content-control-sdt/)文档文章。

```csharp
public class CustomXmlProperty
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [CustomXmlProperty](customxmlproperty/)(*string, string, string*) | 初始化此类的新实例。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Name](../../aspose.words.markup/customxmlproperty/name/) { get; } | 指定自定义 XML 属性或智能标记属性的名称。 |
| [Uri](../../aspose.words.markup/customxmlproperty/uri/) { get; set; } | 获取或设置自定义 XML 属性或智能标记属性的命名空间 URI。 |
| [Value](../../aspose.words.markup/customxmlproperty/value/) { get; set; } | 获取或设置自定义 XML 属性或智能标记属性的值。 |

## 评论

用作[`CustomXmlPropertyCollection`](../customxmlpropertycollection/)收藏。

## 例子

展示如何创建智能标签。

```csharp
public void Create()
{
    Document doc = new Document();

    // 智能标签出现在 Microsoft Word 的文档中，它将其部分文本识别为某种形式的数据，
    // 例如姓名、日期或地址，并将其转换为显示紫色虚线下划线的超链接。
    SmartTag smartTag = new SmartTag(doc);

    // 智能标签是包含其识别的全部文本的复合节点。
    // 手动将内容添加到此智能标签。
    smartTag.AppendChild(new Run(doc, "May 29, 2019"));

    // Microsoft Word 可能会将上述内容识别为日期。
    // 智能标签使用“元素”属性来反映它们包含的数据类型。
    smartTag.Element = "date";

    // 一些智能标记类型将其内容进一步处理为自定义 XML 属性。
    smartTag.Properties.Add(new CustomXmlProperty("Day", string.Empty, "29"));
    smartTag.Properties.Add(new CustomXmlProperty("Month", string.Empty, "5"));
    smartTag.Properties.Add(new CustomXmlProperty("Year", string.Empty, "2019"));

    // 将智能标记的 URI 设置为默认值。
    smartTag.Uri = "urn:schemas-microsoft-com:office:smarttags";

    doc.FirstSection.Body.FirstParagraph.AppendChild(smartTag);
    doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, " is a date. "));

    // 为股票行情自动收录器创建另一个智能标签。
    smartTag = new SmartTag(doc);
    smartTag.Element = "stockticker";
    smartTag.Uri = "urn:schemas-microsoft-com:office:smarttags";

    smartTag.AppendChild(new Run(doc, "MSFT"));

    doc.FirstSection.Body.FirstParagraph.AppendChild(smartTag);
    doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, " is a stock ticker."));

    // 使用文档访问器打印文档中的所有智能标签。
    doc.Accept(new SmartTagPrinter());

    // 旧版本的 Microsoft Word 支持智能标签。
    doc.Save(ArtifactsDir + "SmartTag.Create.doc");

    // 使用“RemoveSmartTags”方法从文档中删除所有智能标签。
    Assert.AreEqual(2, doc.GetChildNodes(NodeType.SmartTag, true).Count);

    doc.RemoveSmartTags();

    Assert.AreEqual(0, doc.GetChildNodes(NodeType.SmartTag, true).Count);
}

/// <summary>
/// 打印访问过的智能标签及其内容。
/// </summary>
private class SmartTagPrinter : DocumentVisitor
{
    /// <summary>
    /// 当在文档中遇到 SmartTag 节点时调用。
    /// </summary>
    public override VisitorAction VisitSmartTagStart(SmartTag smartTag)
    {
        Console.WriteLine($"Smart tag type: {smartTag.Element}");
        return VisitorAction.Continue;
    }

    /// <summary>
    /// 当对 SmartTag 节点的访问结束时调用。
    /// </summary>
    public override VisitorAction VisitSmartTagEnd(SmartTag smartTag)
    {
        Console.WriteLine($"\tContents: \"{smartTag.ToString(SaveFormat.Text)}\"");

        if (smartTag.Properties.Count == 0)
        {
            Console.WriteLine("\tContains no properties");
        }
        else
        {
            Console.Write("\tProperties: ");
            string[] properties = new string[smartTag.Properties.Count];
            int index = 0;

            foreach (CustomXmlProperty cxp in smartTag.Properties)
                properties[index++] = $"\"{cxp.Name}\" = \"{cxp.Value}\"";

            Console.WriteLine(string.Join(", ", properties));
        }

        return VisitorAction.Continue;
    }
}
```

### 也可以看看

* 命名空间 [Aspose.Words.Markup](../../aspose.words.markup/)
* 部件 [Aspose.Words](../../)
