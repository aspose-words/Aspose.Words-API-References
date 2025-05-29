---
title: CommentRangeEnd
linktitle: CommentRangeEnd
articleTitle: CommentRangeEnd
second_title: Aspose.Words for .NET
description: 发现 CommentRangeEnd 构造函数，轻松创建此类的新实例，实现无缝代码集成和增强功能。
type: docs
weight: 10
url: /zh/net/aspose.words/commentrangeend/commentrangeend/
---
## CommentRangeEnd constructor

初始化此类的新实例。

```csharp
public CommentRangeEnd(DocumentBase doc, int id)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| doc | DocumentBase | 所有者文件。 |
| id | Int32 | 此对象链接到的评论标识符。 |

## 评论

什么时候[`CommentRangeEnd`](../)已创建，它属于指定文档，但尚未成为文档的一部分，并且[`ParentNode`](../../node/parentnode/)是`无效的`。

附加[`CommentRangeEnd`](../)在文档中，在想要插入注释的段落上使用 InsertAfter 或 InsertBefore 。

## 例子

展示如何使用文档访问器打印所有评论的内容及其评论范围。

```csharp
public void CreateCommentsAndPrintAllInfo()
{
    Document doc = new Document();

    Comment newComment = new Comment(doc)
    {
        Author = "VDeryushev",
        Initial = "VD",
        DateTime = DateTime.Now
    };

    newComment.SetText("Comment regarding text.");

    // 将文本添加到文档，将其扭曲到注释范围内，然后添加您的注释。
    Paragraph para = doc.FirstSection.Body.FirstParagraph;
    para.AppendChild(new CommentRangeStart(doc, newComment.Id));
    para.AppendChild(new Run(doc, "Commented text."));
    para.AppendChild(new CommentRangeEnd(doc, newComment.Id));
    para.AppendChild(newComment); 

    // 为评论添加两条回复。
    newComment.AddReply("John Doe", "JD", DateTime.Now, "New reply.");
    newComment.AddReply("John Doe", "JD", DateTime.Now, "Another reply.");

    PrintAllCommentInfo(doc.GetChildNodes(NodeType.Comment, true));
}

/// <summary>
/// 遍历每个顶级评论并打印其评论范围、内容和回复。
/// </summary>
private static void PrintAllCommentInfo(NodeCollection comments)
{
    CommentInfoPrinter commentVisitor = new CommentInfoPrinter();

    // 遍历所有顶级评论。与回复类型的评论不同，顶级评论没有祖先。
    foreach (Comment comment in comments.Where(c => ((Comment)c).Ancestor == null).ToList())
    {
        // 首先，访问注释范围的开头。
        CommentRangeStart commentRangeStart = (CommentRangeStart)comment.PreviousSibling.PreviousSibling.PreviousSibling;
        commentRangeStart.Accept(commentVisitor);

        // 然后，访问该评论以及它可能有的任何回复。
        comment.Accept(commentVisitor);
        // 仅访问评论的开头。
        comment.AcceptStart(commentVisitor);
        // 仅访问注释的结尾。
        comment.AcceptEnd(commentVisitor);

        foreach (Comment reply in comment.Replies)
            reply.Accept(commentVisitor);

        // 最后访问评论范围的末尾，然后打印访问者的文本内容。
        CommentRangeEnd commentRangeEnd = (CommentRangeEnd)comment.PreviousSibling;
        commentRangeEnd.Accept(commentVisitor);

        Console.WriteLine(commentVisitor.GetText());
    }
}

/// <summary>
/// 打印文档中遇到的所有注释和注释范围的信息和内容。
/// </summary>
public class CommentInfoPrinter : DocumentVisitor
{
    public CommentInfoPrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideComment = false;
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
        if (mVisitorIsInsideComment) IndentAndAppendLine("[Run] \"" + run.Text + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 当在文档中遇到 CommentRangeStart 节点时调用。
    /// </summary>
    public override VisitorAction VisitCommentRangeStart(CommentRangeStart commentRangeStart)
    {
        IndentAndAppendLine("[Comment range start] ID: " + commentRangeStart.Id);
        mDocTraversalDepth++;
        mVisitorIsInsideComment = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 当在文档中遇到 CommentRangeEnd 节点时调用。
    /// </summary>
    public override VisitorAction VisitCommentRangeEnd(CommentRangeEnd commentRangeEnd)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Comment range end] ID: " + commentRangeEnd.Id + "\n");
        mVisitorIsInsideComment = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 当在文档中遇到注释节点时调用。
    /// </summary>
    public override VisitorAction VisitCommentStart(Comment comment)
    {
        IndentAndAppendLine(
            $"[Comment start] For comment range ID {comment.Id}, By {comment.Author} on {comment.DateTime}");
        mDocTraversalDepth++;
        mVisitorIsInsideComment = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 当文档中评论节点的访问结束时调用。
    /// </summary>
    public override VisitorAction VisitCommentEnd(Comment comment)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Comment end]");
        mVisitorIsInsideComment = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 向 StringBuilder 附加一行并根据访问者在文档树中的深度进行缩进。
    /// </summary>
    /// <param name="text"></param>
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++)
        {
            mBuilder.Append("|  ");
        }

        mBuilder.AppendLine(text);
    }

    private bool mVisitorIsInsideComment;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### 也可以看看

* class [DocumentBase](../../documentbase/)
* class [CommentRangeEnd](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
