---
title: HeaderFooter.Accept
linktitle: Accept
articleTitle: Accept
second_title: Aspose.Words for .NET
description: 探索 HeaderFooter Accept 方法，轻松增强访客参与度并简化网站上的互动。
type: docs
weight: 70
url: /zh/net/aspose.words/headerfooter/accept/
---
## HeaderFooter.Accept method

接受访客。

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| visitor | DocumentVisitor | 将访问节点的访问者。 |

### 返回值

如果访问了所有节点，则为 True；如果访问了所有节点，则为 false[`DocumentVisitor`](../../documentvisitor/)在访问所有节点之前停止操作。

## 评论

枚举此节点及其所有子节点。每个节点都会调用相应的方法[`DocumentVisitor`](../../documentvisitor/)。

欲了解更多信息，请参阅访客设计模式。

呼叫[`VisitHeaderFooterStart`](../../documentvisitor/visitheaderfooterstart/)，然后调用[`Accept`](../../node/accept/)对于 section 的所有子节点并调用[`VisitHeaderFooterEnd`](../../documentvisitor/visitheaderfooterend/)在最后。

## 例子

展示如何打印文档中每个页眉和页脚的节点结构。

```csharp
public void HeaderFooterToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    HeaderFooterStructurePrinter visitor = new HeaderFooterStructurePrinter();

    // 当我们得到一个复合节点来接受文档访问者时，访问者会访问接受节点，
    // 然后以深度优先的方式遍历该节点的所有子节点。
    // 访问者可以读取和修改每个访问的节点。
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());

    // 逐节访问文档的页眉/页脚的另一种方法是通过访问集合。
    HeaderFooter[] headerFooters = doc.FirstSection.HeadersFooters.ToArray();
    Assert.AreEqual(3, headerFooters.Length);
}

/// <summary>
/// 遍历节点的子节点非二叉树。
/// 以字符串的形式创建所有遇到的 HeaderFooter 节点及其子节点的映射。
/// </summary>
public class HeaderFooterStructurePrinter : DocumentVisitor
{
    public HeaderFooterStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideHeaderFooter = false;
    }

    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// 在文档中遇到 Run 节点时调用。
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideHeaderFooter) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 当在文档中遇到 HeaderFooter 节点时调用。
    /// </summary>
    public override VisitorAction VisitHeaderFooterStart(HeaderFooter headerFooter)
    {
        IndentAndAppendLine("[HeaderFooter start] HeaderFooterType: " + headerFooter.HeaderFooterType);
        mDocTraversalDepth++;
        mVisitorIsInsideHeaderFooter = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 在访问完 HeaderFooter 节点的所有子节点后调用。
    /// </summary>
    public override VisitorAction VisitHeaderFooterEnd(HeaderFooter headerFooter)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[HeaderFooter end]");
        mVisitorIsInsideHeaderFooter = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 向 StringBuilder 附加一行，并根据访问者在文档树中的深度进行缩进。
    /// </summary>
    /// <param name="text"></param>
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++) mBuilder.Append("|  ");

        mBuilder.AppendLine(text);
    }

    private bool mVisitorIsInsideHeaderFooter;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### 也可以看看

* class [DocumentVisitor](../../documentvisitor/)
* class [HeaderFooter](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
