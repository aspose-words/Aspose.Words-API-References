---
title: StructuredDocumentTag.Accept
linktitle: Accept
articleTitle: Accept
second_title: 用于 .NET 的 Aspose.Words
description: StructuredDocumentTag Accept 方法. 接受访客 在 C#.
type: docs
weight: 330
url: /zh/net/aspose.words.markup/structureddocumenttag/accept/
---
## StructuredDocumentTag.Accept method

接受访客。

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| visitor | DocumentVisitor | 将访问节点的访问者。 |

### 返回值

如果访问了所有节点，则为 True；假如果[`DocumentVisitor`](../../../aspose.words/documentvisitor/)在访问所有节点之前停止操作。

## 评论

枚举该节点及其所有子节点。每个节点调用相应的方法[`DocumentVisitor`](../../../aspose.words/documentvisitor/)。

有关更多信息，请参阅访客设计模式。

通话[`VisitStructuredDocumentTagStart`](../../../aspose.words/documentvisitor/visitstructureddocumenttagstart/)，然后调用[`Accept`](../../../aspose.words/node/accept/)对于智能标记的 all 子节点并调用[`VisitStructuredDocumentTagEnd`](../../../aspose.words/documentvisitor/visitstructureddocumenttagend/)最后.

## 例子

演示如何打印文档中每个结构化文档标签的节点结构。

```csharp
public void StructuredDocumentTagToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    StructuredDocumentTagNodePrinter visitor = new StructuredDocumentTagNodePrinter();

    // 当我们得到一个复合节点来接受文档访问者时，访问者访问接受节点，
    // 然后以深度优先的方式遍历该节点的所有子节点。
    // 访问者可以读取和修改每个访问过的节点。
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// 遍历节点的子节点的非二叉树。
/// 以字符串形式创建所有遇到的 StructuredDocumentTag 节点及其子节点的映射。
/// </summary>
public class StructuredDocumentTagNodePrinter : DocumentVisitor
{
    public StructuredDocumentTagNodePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideStructuredDocumentTag = false;
    }

    /// <summary>
    /// 获取访问者积累的文档的纯文本。
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// 在文档中遇到 Run 节点时调用。
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideStructuredDocumentTag) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 在文档中遇到 StructuredDocumentTag 节点时调用。
    /// </summary>
    public override VisitorAction VisitStructuredDocumentTagStart(StructuredDocumentTag sdt)
    {
        IndentAndAppendLine("[StructuredDocumentTag start] Title: " + sdt.Title);
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 在访问 StructuredDocumentTag 节点的所有子节点后调用。
    /// </summary>
    public override VisitorAction VisitStructuredDocumentTagEnd(StructuredDocumentTag sdt)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[StructuredDocumentTag end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 将一行追加到 StringBuilder 并根据访问者在文档树中的深度对其进行缩进。
    /// </summary>
    /// <param name="text"></param>;
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++) mBuilder.Append("|  ");

        mBuilder.AppendLine(text);
    }

    private readonly bool mVisitorIsInsideStructuredDocumentTag;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### 也可以看看

* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [StructuredDocumentTag](../)
* 命名空间 [Aspose.Words.Markup](../../../aspose.words.markup/)
* 部件 [Aspose.Words](../../../)
