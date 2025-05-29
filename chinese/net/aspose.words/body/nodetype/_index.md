---
title: Body.NodeType
linktitle: NodeType
articleTitle: NodeType
second_title: Aspose.Words for .NET
description: 发现 Body NodeType 属性可有效返回正文内容，增强您的 Web 开发体验并简化您的项目。
type: docs
weight: 20
url: /zh/net/aspose.words/body/nodetype/
---
## Body.NodeType property

返回Body.

```csharp
public override NodeType NodeType { get; }
```

## 例子

展示如何迭代复合节点的子节点。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Primary header");
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("Primary footer");

Section section = doc.FirstSection;

// Section 是一个复合节点，可以包含子节点，
// 但只有当这些子节点属于“Body”或“HeaderFooter”节点类型时才如此。
foreach (Node node in section)
{
    switch (node.NodeType)
    {
        case NodeType.Body:
        {
            Body body = (Body)node;

            Console.WriteLine("Body:");
            Console.WriteLine($"\t\"{body.GetText().Trim()}\"");
            break;
        }
        case NodeType.HeaderFooter:
        {
            HeaderFooter headerFooter = (HeaderFooter)node;

            Console.WriteLine($"HeaderFooter type: {headerFooter.HeaderFooterType}:");
            Console.WriteLine($"\t\"{headerFooter.GetText().Trim()}\"");
            break;
        }
        default:
        {
            throw new Exception("Unexpected node type in a section.");
        }
    }
}
```

### 也可以看看

* enum [NodeType](../../nodetype/)
* class [Body](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
