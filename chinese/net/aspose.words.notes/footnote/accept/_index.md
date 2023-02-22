---
title: Footnote.Accept
second_title: Aspose.Words for .NET API 参考
description: Footnote 方法. 接受访客
type: docs
weight: 70
url: /zh/net/aspose.words.notes/footnote/accept/
---
## Footnote.Accept method

接受访客。

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| visitor | DocumentVisitor | 将访问节点的访问者。 |

### 返回值

如果访问了所有节点，则为真；如果 DocumentVisitor 在访问所有节点之前停止操作，则返回 false。

### 评论

枚举此节点及其所有子节点。每个节点调用 DocumentVisitor 上的相应方法。

有关更多信息，请参阅访问者设计模式。

调用 DocumentVisitor.VisitFootnoteStart，然后为 footnote 的所有子节点调用 Accept，最后调用 DocumentVisitor.VisitFootnoteEnd。

### 例子

显示如何打印文档中每个脚注的节点结构。

```csharp
public void FootnoteToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    FootnoteStructurePrinter visitor = new FootnoteStructurePrinter();

    // 当我们得到一个复合节点来接受一个文档访问者时，访问者访问接受节点，
    // 然后以深度优先的方式遍历所有节点的子节点。
    // 访问者可以读取和修改每个访问的节点。
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// 遍历一个节点的子节点的非二叉树。
/// 以所有遇到的脚注节点及其子节点的字符串形式创建一个映射。
/// </summary>
public class FootnoteStructurePrinter : DocumentVisitor
{
    public FootnoteStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideFootnote = false;
    }

    /// <summary>
    /// 获取访问者积累的文档的纯文本。
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// 在文档中遇到脚注节点时调用。
    /// </summary>
    public override VisitorAction VisitFootnoteStart(Footnote footnote)
    {
        IndentAndAppendLine("[Footnote start] Type: " + footnote.FootnoteType);
        mDocTraversalDepth++;
        mVisitorIsInsideFootnote = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 在访问脚注节点的所有子节点后调用。
    /// </summary>
    public override VisitorAction VisitFootnoteEnd(Footnote footnote)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Footnote end]");
        mVisitorIsInsideFootnote = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 在文档中遇到 Run 节点时调用。
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideFootnote) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 将一行添加到 StringBuilder 并根据访问者在文档树中的深度缩进。
    /// </summary>
    /// <param name="text"></param>
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++) mBuilder.Append("|  ");

        mBuilder.AppendLine(text);
    }

    private bool mVisitorIsInsideFootnote;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### 也可以看看

* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [Footnote](../)
* 命名空间 [Aspose.Words.Notes](../../footnote/)
* 部件 [Aspose.Words](../../../)


