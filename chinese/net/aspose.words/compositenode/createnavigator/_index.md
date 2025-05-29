---
title: CompositeNode.CreateNavigator
linktitle: CreateNavigator
articleTitle: CreateNavigator
second_title: Aspose.Words for .NET
description: 探索 CompositeNode CreateNavigator 方法，轻松遍历和读取节点，增强您的数据导航体验。
type: docs
weight: 90
url: /zh/net/aspose.words/compositenode/createnavigator/
---
## CompositeNode.CreateNavigator method

创建可用于遍历和读取节点的导航器。

```csharp
[EditorBrowsable(EditorBrowsableState.Never)]
public XPathNavigator CreateNavigator()
```

## 例子

展示如何创建 XPathNavigator，然后使用它来遍历和读取节点。

```csharp
public void NodeXPathNavigator()
{
    Document doc = new Document();
    XPathNavigator navigator = doc.CreateNavigator();

    if (navigator != null)
    {
        Assert.AreEqual("Document", navigator.Name);
        Assert.AreEqual(false, navigator.MoveToNext());
        Assert.AreEqual(1, navigator.SelectChildren(XPathNodeType.All).Count);

        // 文档树包含文档第一部分，
        // 正文和第一段作为节点，每个节点都是前一个节点的唯一子节点。
        // 我们可以添加更多内容来为导航器提供一些可供遍历的树分支。
        DocumentBuilder docBuilder = new DocumentBuilder(doc);
        docBuilder.Write("Section 1, Paragraph 1. ");
        docBuilder.InsertParagraph();
        docBuilder.Write("Section 1, Paragraph 2. ");
        doc.AppendChild(new Section(doc));
        docBuilder.MoveToSection(1);
        docBuilder.Write("Section 2, Paragraph 1. ");

        // 使用我们的导航器将文档中所有节点的地图打印到控制台。
        StringBuilder stringBuilder = new StringBuilder();
        MapDocument(navigator, stringBuilder, 0);
        Console.Write(stringBuilder.ToString());
    }
}

/// <summary>
/// 遍历复合节点的所有子节点并以目录树的形式映射结构。
/// 空间缩进量表示相对于初始节点的深度。
/// 仅当它是运行时才打印当前节点的文本内容。
/// </summary>
private static void MapDocument(XPathNavigator navigator, StringBuilder stringBuilder, int depth)
{
    do
    {
        stringBuilder.Append(' ', depth);
        stringBuilder.Append(navigator.Name + ": ");

        if (navigator.Name == "Run")
        {
            stringBuilder.Append(navigator.Value);
        }

        stringBuilder.Append('\n');

        if (navigator.HasChildren)
        {
            navigator.MoveToFirstChild();
            MapDocument(navigator, stringBuilder, depth + 1);
            navigator.MoveToParent();
        }
    } while (navigator.MoveToNext());
}
```

### 也可以看看

* class [CompositeNode](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
