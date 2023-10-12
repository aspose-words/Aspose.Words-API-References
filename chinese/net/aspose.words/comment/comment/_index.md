---
title: Comment.Comment
second_title: Aspose.Words for .NET API 参考
description: Comment 构造函数. 初始化一个新实例Comment类.
type: docs
weight: 10
url: /zh/net/aspose.words/comment/comment/
---
## Comment(DocumentBase) {#constructor}

初始化一个新实例[`Comment`](../)类.

```csharp
public Comment(DocumentBase doc)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| doc | DocumentBase | 所有者文件。 |

### 评论

什么时候[`Comment`](../)创建后，它属于指定文档，但还不是 文档的一部分并且[`ParentNode`](../../node/parentnode/)是`无效的`。

追加[`Comment`](../)到文档使用Node)或者Node) 在您想要插入评论的段落上。

创建评论后，不要忘记设置它[`Author`](../author/), [`Initial`](../initial/)和[`DateTime`](../datetime/)特性。

### 例子

展示如何使用文档访问者打印所有注释的内容及其注释范围。

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

    // 将文本添加到文档中，将其扭曲到注释范围内，然后添加您的注释。
    Paragraph para = doc.FirstSection.Body.FirstParagraph;
    para.AppendChild(new CommentRangeStart(doc, newComment.Id));
    para.AppendChild(new Run(doc, "Commented text."));
    para.AppendChild(new CommentRangeEnd(doc, newComment.Id));
    para.AppendChild(newComment); 

    // 添加两条对评论的回复。
    newComment.AddReply("John Doe", "JD", DateTime.Now, "New reply.");
    newComment.AddReply("John Doe", "JD", DateTime.Now, "Another reply.");

    PrintAllCommentInfo(doc.GetChildNodes(NodeType.Comment, true));
}

/// <summary>
/// 迭代每个顶级评论并打印其评论范围、内容和回复。
/// </summary>
private static void PrintAllCommentInfo(NodeCollection comments)
{
    CommentInfoPrinter commentVisitor = new CommentInfoPrinter();

    // 迭代所有顶级注释。与回复类型评论不同，顶级评论没有祖先。
    foreach (Comment comment in comments.Where(c => ((Comment)c).Ancestor == null))
    {
        // 首先，访问评论范围的开头。
        CommentRangeStart commentRangeStart = (CommentRangeStart)comment.PreviousSibling.PreviousSibling.PreviousSibling;
        commentRangeStart.Accept(commentVisitor);

        // 然后，访问评论及其可能有的任何回复。
        comment.Accept(commentVisitor);

        foreach (Comment reply in comment.Replies)
            reply.Accept(commentVisitor);

        // 最后访问评论范围末尾，然后打印访问者的文本内容。
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
    /// 在文档中遇到 CommentRangeStart 节点时调用。
    /// </summary>
    public override VisitorAction VisitCommentRangeStart(CommentRangeStart commentRangeStart)
    {
        IndentAndAppendLine("[Comment range start] ID: " + commentRangeStart.Id);
        mDocTraversalDepth++;
        mVisitorIsInsideComment = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 在文档中遇到 CommentRangeEnd 节点时调用。
    /// </summary>
    public override VisitorAction VisitCommentRangeEnd(CommentRangeEnd commentRangeEnd)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Comment range end] ID: " + commentRangeEnd.Id + "\n");
        mVisitorIsInsideComment = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 在文档中遇到 Comment 节点时调用。
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
    /// 当文档中Comment节点的访问结束时调用。
    /// </summary>
    public override VisitorAction VisitCommentEnd(Comment comment)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Comment end]");
        mVisitorIsInsideComment = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 将一行追加到 StringBuilder 并根据访问者在文档树中的深度对其进行缩进。
    /// </summary>
    /// <param name="text"></param>;
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
* class [Comment](../)
* 命名空间 [Aspose.Words](../../comment/)
* 部件 [Aspose.Words](../../../)

---

## Comment(DocumentBase, string, string, DateTime) {#constructor_1}

初始化一个新实例[`Comment`](../)类.

```csharp
public Comment(DocumentBase doc, string author, string initial, DateTime dateTime)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| doc | DocumentBase | 所有者文件。 |
| author | String | 评论的作者姓名。不可能是`无效的`。 |
| initial | String | 评论的作者姓名缩写。不可能是`无效的`。 |
| dateTime | DateTime | 发表评论的日期和时间。 |

### 例子

演示如何向段落添加注释。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

Comment comment = new Comment(doc, "John Doe", "JD", DateTime.Today);
builder.CurrentParagraph.AppendChild(comment);
builder.MoveTo(comment.AppendChild(new Paragraph(doc)));
builder.Write("Comment text.");

Assert.AreEqual(DateTime.Today, comment.DateTime);

 // 在Microsoft Word中，我们可以在文档正文中右键单击该注释进行编辑，或者回复。
doc.Save(ArtifactsDir + "InlineStory.AddComment.docx");
```

### 也可以看看

* class [DocumentBase](../../documentbase/)
* class [Comment](../)
* 命名空间 [Aspose.Words](../../comment/)
* 部件 [Aspose.Words](../../../)


