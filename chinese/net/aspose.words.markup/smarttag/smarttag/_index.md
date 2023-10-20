---
title: SmartTag
linktitle: SmartTag
articleTitle: SmartTag
second_title: 用于 .NET 的 Aspose.Words
description: SmartTag 构造函数. 初始化一个新实例SmartTag类 在 C#.
type: docs
weight: 10
url: /zh/net/aspose.words.markup/smarttag/smarttag/
---
## SmartTag constructor

初始化一个新实例[`SmartTag`](../)类.

```csharp
public SmartTag(DocumentBase doc)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| doc | DocumentBase | 所有者文件。 |

## 评论

创建新节点时，需要指定该节点所属的文档。 节点不能没有文档而存在，因为它依赖于文档范围的结构 ，例如列表和样式。尽管节点始终属于文档，但节点可能是也可能 不是文档树的一部分。

当一个节点被创建时，它属于一个文档，但还不是文档tree 的一部分并且[`ParentNode`](../../../aspose.words/node/parentnode/)是`无效的`。要将节点插入到文档中，请使用 the [`InsertAfter`](../../../aspose.words/compositenode/insertafter/)或者[`InsertBefore`](../../../aspose.words/compositenode/insertbefore/)父节点上的methods 。

## 例子

展示如何创建智能标签。

```csharp
public void Create()
{
    Document doc = new Document();

    // 智能标签出现在 Microsoft Word 文档中，将其文本的一部分识别为某种形式的数据，
    // 例如名称、日期或地址，并将其转换为显示紫色点状下划线的超链接。
    SmartTag smartTag = new SmartTag(doc);

    // 智能标签是复合节点，包含完整的已识别文本。
    // 手动将内容添加到此智能标签。
    smartTag.AppendChild(new Run(doc, "May 29, 2019"));

    // Microsoft Word 可能会将上述内容识别为日期。
    // 智能标签使用“Element”属性来反映它们包含的数据类型。
    smartTag.Element = "date";

    // 某些智能标记类型将其内容进一步处理为自定义 XML 属性。
    smartTag.Properties.Add(new CustomXmlProperty("Day", string.Empty, "29"));
    smartTag.Properties.Add(new CustomXmlProperty("Month", string.Empty, "5"));
    smartTag.Properties.Add(new CustomXmlProperty("Year", string.Empty, "2019"));

    // 将智能标记的 URI 设置为默认值。
    smartTag.Uri = "urn:schemas-microsoft-com:office:smarttags";

    doc.FirstSection.Body.FirstParagraph.AppendChild(smartTag);
    doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, " is a date. "));

    // 为股票行情创建另一个智能标签。
    smartTag = new SmartTag(doc);
    smartTag.Element = "stockticker";
    smartTag.Uri = "urn:schemas-microsoft-com:office:smarttags";

    smartTag.AppendChild(new Run(doc, "MSFT"));

    doc.FirstSection.Body.FirstParagraph.AppendChild(smartTag);
    doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, " is a stock ticker."));

    // 使用文档访问者打印文档中的所有智能标签。
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
    /// 在文档中遇到 SmartTag 节点时调用。
    /// </summary>
    public override VisitorAction VisitSmartTagStart(SmartTag smartTag)
    {
        Console.WriteLine($"Smart tag type: {smartTag.Element}");
        return VisitorAction.Continue;
    }

    /// <summary>
    /// 当SmartTag节点的访问结束时调用。
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

* class [DocumentBase](../../../aspose.words/documentbase/)
* class [SmartTag](../)
* 命名空间 [Aspose.Words.Markup](../../../aspose.words.markup/)
* 部件 [Aspose.Words](../../../)
