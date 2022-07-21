---
title: SmartTag
second_title: Aspose.Words for .NET API 参考
description: 此元素指定一个或多个内联结构周围存在智能标记 运行图像字段等在段落中
type: docs
weight: 3810
url: /zh/net/aspose.words.markup/smarttag/
---
## SmartTag class

此元素指定一个或多个内联结构周围存在智能标记 （运行、图像、字段等）在段落中。

```csharp
public class SmartTag : CompositeNode
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [SmartTag](smarttag)(DocumentBase) | 初始化[`SmartTag`](../smarttag)类. |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | 获取该节点的所有直接子节点。 |
| [Count](../../aspose.words/compositenode/count) { get; } | 获取此节点的直接子节点数。 |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | 指定自定义节点标识符。 |
| virtual [Document](../../aspose.words/node/document) { get; } | 获取该节点所属的文档。 |
| [Element](../../aspose.words.markup/smarttag/element) { get; set; } | 指定文档中智能标记的名称。 |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | 获取节点的第一个子节点。 |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | 如果此节点有任何子节点，则返回 true。 |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | 返回真，因为该节点可以有子节点。 |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | 获取节点的最后一个子节点。 |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | 获取紧跟此节点的节点。 |
| override [NodeType](../../aspose.words.markup/smarttag/nodetype) { get; } | 返回 **NodeType.SmartTag**. |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | 获取此节点的直接父节点。 |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | 获取紧接在此节点之前的节点。 |
| [Properties](../../aspose.words.markup/smarttag/properties) { get; } | 智能标记属性的集合。 |
| [Range](../../aspose.words/node/range) { get; } | 返回一个 **范围**表示此节点中包含的文档部分的对象。 |
| [Uri](../../aspose.words.markup/smarttag/uri) { get; set; } | 指定智能标签的命名空间 URI。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| override [Accept](../../aspose.words.markup/smarttag/accept)(DocumentVisitor) | 接受访客。 |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | 将指定节点添加到该节点的子节点列表的末尾。 |
| [Clone](../../aspose.words/node/clone)(bool) | 创建节点的副本。 |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | 保留供系统使用。 IXPathNavigable. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | 获取指定的第一个祖先[`NodeType`](../../aspose.words/nodetype). |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | 获取指定对象类型的第一个祖先。 |
| [GetChild](../../aspose.words/compositenode/getchild)(NodeType, int, bool) | 返回与指定类型匹配的第 N 个子节点。 |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes)(NodeType, bool) | 返回与指定类型匹配的子节点的实时集合。 |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator)() | 为在该节点的子节点上的每个样式迭代提供支持。 |
| override [GetText](../../aspose.words/compositenode/gettext)() | 获取该节点及其所有子节点的文本。 |
| [IndexOf](../../aspose.words/compositenode/indexof)(Node) | 返回子节点数组中指定子节点的索引。 |
| [InsertAfter](../../aspose.words/compositenode/insertafter)(Node, Node) | 在指定参考节点之后立即插入指定节点。 |
| [InsertBefore](../../aspose.words/compositenode/insertbefore)(Node, Node) | 在指定的参考节点之前插入指定的节点。 |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | 根据前序树遍历算法获取下一个节点。 |
| [PrependChild](../../aspose.words/compositenode/prependchild)(Node) | 将指定节点添加到此节点的子节点列表的开头。 |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | 根据前序树遍历算法获取上一个节点。 |
| [Remove](../../aspose.words/node/remove)() | 从父级中移除自身。 |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren)() | 移除当前节点的所有子节点。 |
| [RemoveChild](../../aspose.words/compositenode/removechild)(Node) | 移除指定的子节点。 |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags)() | 删除所有[`SmartTag`](../smarttag)当前节点的后代节点。 |
| [SelectNodes](../../aspose.words/compositenode/selectnodes)(string) | 选择与 XPath 表达式匹配的节点列表。 |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode)(string) | 选择与 XPath 表达式匹配的第一个节点。 |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | 将节点的内容导出为指定格式的字符串。 |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | 使用指定的保存选项将节点的内容导出为字符串。 |

### 评论

智能标记是一种自定义 XML 标记。智能标签通过为文档中的运行或一组运行提供基本命名空间/name 的能力，为将客户定义的语义嵌入到文档中提供了便利。

[`SmartTag`](../smarttag)可以是一个孩子[`Paragraph`](../../aspose.words/paragraph)or 另一个[`SmartTag`](../smarttag)节点。

可以出现在智能标记内的子节点的完整列表包括 [`BookmarkStart`](../../aspose.words/bookmarkstart),[`BookmarkEnd`](../../aspose.words/bookmarkend), [`FieldStart`](../../aspose.words.fields/fieldstart),[`FieldSeparator`](../../aspose.words.fields/fieldseparator),[`FieldEnd`](../../aspose.words.fields/fieldend),[`FormField`](../../aspose.words.fields/formfield), [`Comment`](../../aspose.words/comment),[`Footnote`](../../aspose.words.notes/footnote), [`Run`](../../aspose.words/run),[`SpecialChar`](../../aspose.words/specialchar), [`Shape`](../../aspose.words.drawing/shape),[`GroupShape`](../../aspose.words.drawing/groupshape), [`CommentRangeStart`](../../aspose.words/commentrangestart), [`CommentRangeEnd`](../../aspose.words/commentrangeend), [`SmartTag`](../smarttag).

### 例子

展示如何创建智能标签。

```csharp
public void Create()
{
    Document doc = new Document();

    // 智能标记出现在文档中，Microsoft Word 将其文本的一部分识别为某种形式的数据，
    // 例如姓名、日期或地址，并将其转换为显示紫色虚线下划线的超链接。
    SmartTag smartTag = new SmartTag(doc);

    // 智能标签是包含其识别文本的完整的复合节点。
    // 手动添加内容到这个智能标签。
    smartTag.AppendChild(new Run(doc, "May 29, 2019"));

    // Microsoft Word 可能会将上述内容识别为日期。
    // 智能标签使用“元素”属性来反映它们包含的数据类型。
    smartTag.Element = "date";

    // 一些智能标记类型将其内容进一步处理为自定义 XML 属性。
    smartTag.Properties.Add(new CustomXmlProperty("Day", string.Empty, "29"));
    smartTag.Properties.Add(new CustomXmlProperty("Month", string.Empty, "5"));
    smartTag.Properties.Add(new CustomXmlProperty("Year", string.Empty, "2019"));

    // 将智能标签的 URI 设置为默认值。
    smartTag.Uri = "urn:schemas-microsoft-com:office:smarttags";

    doc.FirstSection.Body.FirstParagraph.AppendChild(smartTag);
    doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, " is a date. "));

    // 为股票代码创建另一个智能标签。
    smartTag = new SmartTag(doc);
    smartTag.Element = "stockticker";
    smartTag.Uri = "urn:schemas-microsoft-com:office:smarttags";

    smartTag.AppendChild(new Run(doc, "MSFT"));

    doc.FirstSection.Body.FirstParagraph.AppendChild(smartTag);
    doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, " is a stock ticker."));

    // 使用文档访问者打印我们文档中的所有智能标签。
    doc.Accept(new SmartTagPrinter());

    // 旧版本的 Microsoft Word 支持智能标记。
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
    /// SmartTag节点访问结束时调用。
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

* class [CompositeNode](../../aspose.words/compositenode)
* 命名空间 [Aspose.Words.Markup](../../aspose.words.markup)
* 部件 [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
