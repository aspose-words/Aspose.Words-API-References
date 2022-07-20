---
title: CommentRangeStart
second_title: Aspose.Words for .NET API 参考
description: 表示具有关联注释的文本区域的开始
type: docs
weight: 250
url: /zh/net/aspose.words/commentrangestart/
---
## CommentRangeStart class

表示具有关联注释的文本区域的开始。

```csharp
public sealed class CommentRangeStart : Node
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [CommentRangeStart](commentrangestart)(DocumentBase, int) | 初始化这个类的一个新实例。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | 指定自定义节点标识符。 |
| virtual [Document](../../aspose.words/node/document) { get; } | 获取该节点所属的文档。 |
| [Id](../../aspose.words/commentrangestart/id) { get; set; } | 指定该区域链接到的注释的标识符。 |
| virtual [IsComposite](../../aspose.words/node/iscomposite) { get; } | 如果此节点可以包含其他节点，则返回 true。 |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | 获取紧跟此节点的节点。 |
| override [NodeType](../../aspose.words/commentrangestart/nodetype) { get; } | 返回CommentRangeStart. |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | 获取此节点的直接父节点。 |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | 获取紧接在此节点之前的节点。 |
| [Range](../../aspose.words/node/range) { get; } | 返回一个 **范围**表示此节点中包含的文档部分的对象。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| override [Accept](../../aspose.words/commentrangestart/accept)(DocumentVisitor) | 接受访客。 |
| [Clone](../../aspose.words/node/clone)(bool) | 创建节点的副本。 |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | 获取指定的第一个祖先[`NodeType`](../nodetype). |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | 获取指定对象类型的第一个祖先。 |
| virtual [GetText](../../aspose.words/node/gettext)() | 获取该节点及其所有子节点的文本。 |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | 根据前序树遍历算法获取下一个节点。 |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | 根据前序树遍历算法获取上一个节点。 |
| [Remove](../../aspose.words/node/remove)() | 从父级中移除自身。 |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | 将节点的内容导出为指定格式的字符串。 |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | 使用指定的保存选项将节点的内容导出为字符串。 |

### 评论

要创建锚定到文本区域的注释，您需要创建一个[`Comment`](../comment)and 然后创建[`CommentRangeStart`](../commentrangestart)和[`CommentRangeEnd`](../commentrangeend)并将它们的标识符 设置为相同[`Id`](../comment/id)价值。

[`CommentRangeStart`](../commentrangestart)是一个内联级节点，只能是[`Paragraph`](../paragraph).

### 例子

显示如何使用文档访问者打印所有评论的内容及其评论范围。

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

    // 向文档中添加文本，在评论范围内对其进行变形，然后添加您的评论。
    Paragraph para = doc.FirstSection.Body.FirstParagraph;
    para.AppendChild(new CommentRangeStart(doc, newComment.Id));
    para.AppendChild(new Run(doc, "Commented text."));
    para.AppendChild(new CommentRangeEnd(doc, newComment.Id));
    para.AppendChild(newComment); 

    // 在评论中添加两个回复。
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

    // 遍历所有顶级注释。与回复类型的评论不同，顶级评论没有祖先。
    foreach (Comment comment in comments.Where(c => ((Comment)c).Ancestor == null))
    {
        // 首先，访问评论范围的开头。
        CommentRangeStart commentRangeStart = (CommentRangeStart)comment.PreviousSibling.PreviousSibling.PreviousSibling;
        commentRangeStart.Accept(commentVisitor);

        // 然后，访问评论，以及它可能有的任何回复。
        comment.Accept(commentVisitor);

        foreach (Comment reply in comment.Replies)
            reply.Accept(commentVisitor);

        // 最后，访问评论范围的末尾，然后打印访问者的文本内容。
        CommentRangeEnd commentRangeEnd = (CommentRangeEnd)comment.PreviousSibling;
        commentRangeEnd.Accept(commentVisitor);

        Console.WriteLine(commentVisitor.GetText());
    }
}

/// <summary>
/// 打印文档中遇到的所有评论和评论范围的信息和内容。
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
    /// 在文档中遇到评论节点时调用。
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
    /// 在文档中结束对 Comment 节点的访问时调用。
    /// </summary>
    public override VisitorAction VisitCommentEnd(Comment comment)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Comment end]");
        mVisitorIsInsideComment = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// 将一行添加到 StringBuilder 并根据访问者在文档树中的深度缩进。
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

* class [Node](../node)
* 命名空间 [Aspose.Words](../../aspose.words)
* 部件 [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
