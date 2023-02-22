---
title: DocumentVisitor.VisitHeaderFooterStart
second_title: Aspose.Words for .NET API 参考
description: DocumentVisitor 方法. 在开始枚举节中的页眉或页脚时调用
type: docs
weight: 290
url: /zh/net/aspose.words/documentvisitor/visitheaderfooterstart/
---
## DocumentVisitor.VisitHeaderFooterStart method

在开始枚举节中的页眉或页脚时调用。

```csharp
public virtual VisitorAction VisitHeaderFooterStart(HeaderFooter headerFooter)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| headerFooter | HeaderFooter | 正在访问的对象。 |

### 返回值

一个[`VisitorAction`](../../visitoraction/)指定如何继续枚举的值。

### 例子

显示如何打印文档中每个页眉和页脚的节点结构。

```csharp
public void HeaderFooterToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    HeaderFooterStructurePrinter visitor = new HeaderFooterStructurePrinter();

    // 当我们得到一个复合节点来接受一个文档访问者时，访问者访问接受节点，
    // 然后以深度优先的方式遍历所有节点的子节点。
    // 访问者可以读取和修改每个访问的节点。
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());

    // 逐节访问文档页眉/页脚的另一种方法是访问集合。
    HeaderFooter[] headerFooters = doc.FirstSection.HeadersFooters.ToArray();
    Assert.AreEqual(3, headerFooters.Length);
}

/// <summary>
/// 遍历一个节点的子节点的非二叉树。
/// 以所有遇到的 HeaderFooter 节点及其子节点的字符串形式创建映射。
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
    /// 在文档中遇到 HeaderFooter 节点时调用。
    /// </summary>
    public override VisitorAction VisitHeaderFooterStart(HeaderFooter headerFooter)
    {
        IndentAndAppendLine("[HeaderFooter start] HeaderFooterType: " + headerFooter.HeaderFooterType);
        mDocTraversalDepth++;
        mVisitorIsInsideHeaderFooter = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 在访问了 HeaderFooter 节点的所有子节点后调用。
    /// </summary>
    public override VisitorAction VisitHeaderFooterEnd(HeaderFooter headerFooter)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[HeaderFooter end]");
        mVisitorIsInsideHeaderFooter = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 向 StringBuilder 添加一行，并根据访问者在文档树中的深度缩进。
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

* enum [VisitorAction](../../visitoraction/)
* class [HeaderFooter](../../headerfooter/)
* class [DocumentVisitor](../)
* 命名空间 [Aspose.Words](../../documentvisitor/)
* 部件 [Aspose.Words](../../../)


