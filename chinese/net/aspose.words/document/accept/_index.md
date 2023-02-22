---
title: Document.Accept
second_title: Aspose.Words for .NET API 参考
description: Document 方法. 接受访客
type: docs
weight: 490
url: /zh/net/aspose.words/document/accept/
---
## Document.Accept method

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

调用 DocumentVisitor.VisitDocumentStart，然后为 document 的所有子节点调用 Accept，最后调用 DocumentVisitor.VisitDocumentEnd。

### 例子

展示如何使用文档访问者打印文档的节点结构。

```csharp
public void DocStructureToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    DocStructurePrinter visitor = new DocStructurePrinter();

    // 当我们得到一个复合节点来接受一个文档访问者时，访问者访问接受节点，
    // 然后以深度优先的方式遍历所有节点的子节点。
    // 访问者可以读取和修改每个访问的节点。
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// 遍历一个节点的子节点树。
/// 以字符串的形式创建这棵树的映射。
/// </summary>
public class DocStructurePrinter : DocumentVisitor
{
    public DocStructurePrinter()
    {
        mAcceptingNodeChildTree = new StringBuilder();
    }

    public string GetText()
    {
        return mAcceptingNodeChildTree.ToString();
    }

    /// <summary>
    /// 在遇到 Document 节点时调用。
    /// </summary>
    public override VisitorAction VisitDocumentStart(Document doc)
    {
        int childNodeCount = doc.GetChildNodes(NodeType.Any, true).Count;

        IndentAndAppendLine("[Document start] Child nodes: " + childNodeCount);
        mDocTraversalDepth++;

        // 允许访问者继续访问其他节点。
        return VisitorAction.Continue;
    }

    /// <summary>
    /// 在访问完 Document 节点的所有子节点后调用。
    /// </summary>
    public override VisitorAction VisitDocumentEnd(Document doc)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Document end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 在文档中遇到 Section 节点时调用。
    /// </summary>
    public override VisitorAction VisitSectionStart(Section section)
    {
        // 获取文档中我们部分的索引。
        NodeCollection docSections = section.Document.GetChildNodes(NodeType.Section, false);
        int sectionIndex = docSections.IndexOf(section);

        IndentAndAppendLine("[Section start] Section index: " + sectionIndex);
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 在访问了 Section 节点的所有子节点后调用。
    /// </summary>
    public override VisitorAction VisitSectionEnd(Section section)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Section end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 在文档中遇到 Body 节点时调用。
    /// </summary>
    public override VisitorAction VisitBodyStart(Body body)
    {
        int paragraphCount = body.Paragraphs.Count;
        IndentAndAppendLine("[Body start] Paragraphs: " + paragraphCount);
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 在访问完 Body 节点的所有子节点后调用。
    /// </summary>
    public override VisitorAction VisitBodyEnd(Body body)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Body end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 在文档中遇到段落节点时调用。
    /// </summary>
    public override VisitorAction VisitParagraphStart(Paragraph paragraph)
    {
        IndentAndAppendLine("[Paragraph start]");
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 在访问完一个段落节点的所有子节点后调用。
    /// </summary>
    public override VisitorAction VisitParagraphEnd(Paragraph paragraph)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Paragraph end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 在文档中遇到 Run 节点时调用。
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 在文档中遇到子文档节点时调用。
    /// </summary>
    public override VisitorAction VisitSubDocument(SubDocument subDocument)
    {
        IndentAndAppendLine("[SubDocument]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 将一行添加到 StringBuilder 并根据访问者在文档树中的深度缩进。
    /// </summary>
    /// <param name="text"></param>
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++) mAcceptingNodeChildTree.Append("|  ");

        mAcceptingNodeChildTree.AppendLine(text);
    }

    private int mDocTraversalDepth;
    private readonly StringBuilder mAcceptingNodeChildTree;
}
```

### 也可以看看

* class [DocumentVisitor](../../documentvisitor/)
* class [Document](../)
* 命名空间 [Aspose.Words](../../document/)
* 部件 [Aspose.Words](../../../)


