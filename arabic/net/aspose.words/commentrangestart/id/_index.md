---
title: Id
second_title: Aspose.Words لمراجع .NET API
description: يحدد معرف التعليق الذي ترتبط به هذه المنطقة.
type: docs
weight: 20
url: /ar/net/aspose.words/commentrangestart/id/
---
## CommentRangeStart.Id property

يحدد معرف التعليق الذي ترتبط به هذه المنطقة.

```csharp
public int Id { get; set; }
```

### أمثلة

يُظهر كيفية طباعة محتويات جميع التعليقات ونطاقات التعليقات الخاصة بها باستخدام زائر المستند.

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

    // أضف نصًا إلى المستند ، وقم بإجراء التواء له في نطاق تعليق ، ثم أضف تعليقك.
    Paragraph para = doc.FirstSection.Body.FirstParagraph;
    para.AppendChild(new CommentRangeStart(doc, newComment.Id));
    para.AppendChild(new Run(doc, "Commented text."));
    para.AppendChild(new CommentRangeEnd(doc, newComment.Id));
    para.AppendChild(newComment); 

    // أضف ردين على التعليق.
    newComment.AddReply("John Doe", "JD", DateTime.Now, "New reply.");
    newComment.AddReply("John Doe", "JD", DateTime.Now, "Another reply.");

    PrintAllCommentInfo(doc.GetChildNodes(NodeType.Comment, true));
}

/// <summary>
/// يتكرر عبر كل تعليق من المستوى الأعلى ويطبع نطاق التعليقات والمحتويات والردود الخاصة به.
/// </summary>
private static void PrintAllCommentInfo(NodeCollection comments)
{
    CommentInfoPrinter commentVisitor = new CommentInfoPrinter();

    // كرر عبر جميع تعليقات المستوى الأعلى. بخلاف تعليقات نوع الرد ، ليس لتعليقات المستوى الأعلى أصل.
    foreach (Comment comment in comments.Where(c => ((Comment)c).Ancestor == null))
    {
        // أولاً ، قم بزيارة بداية نطاق التعليقات.
        CommentRangeStart commentRangeStart = (CommentRangeStart)comment.PreviousSibling.PreviousSibling.PreviousSibling;
        commentRangeStart.Accept(commentVisitor);

        // ثم قم بزيارة التعليق وأية ردود قد تكون عليه.
        comment.Accept(commentVisitor);

        foreach (Comment reply in comment.Replies)
            reply.Accept(commentVisitor);

        // أخيرًا ، قم بزيارة نهاية نطاق التعليقات ، ثم اطبع محتويات نص الزائر.
        CommentRangeEnd commentRangeEnd = (CommentRangeEnd)comment.PreviousSibling;
        commentRangeEnd.Accept(commentVisitor);

        Console.WriteLine(commentVisitor.GetText());
    }
}

/// <summary>
/// يطبع معلومات ومحتويات كافة التعليقات ونطاقات التعليقات التي تمت مواجهتها في المستند.
/// </summary>
public class CommentInfoPrinter : DocumentVisitor
{
    public CommentInfoPrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideComment = false;
    }

    /// <summary>
    /// يحصل على النص العادي للمستند الذي قام الزائر بتجميعه.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// يتم الاستدعاء عند مواجهة عقدة تشغيل في المستند.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideComment) IndentAndAppendLine("[Run] \"" + run.Text + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤه عند مصادفة عقدة CommentRangeStart في المستند.
    /// </summary>
    public override VisitorAction VisitCommentRangeStart(CommentRangeStart commentRangeStart)
    {
        IndentAndAppendLine("[Comment range start] ID: " + commentRangeStart.Id);
        mDocTraversalDepth++;
        mVisitorIsInsideComment = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤه عند مواجهة عقدة CommentRangeEnd في المستند.
    /// </summary>
    public override VisitorAction VisitCommentRangeEnd(CommentRangeEnd commentRangeEnd)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Comment range end] ID: " + commentRangeEnd.Id + "\n");
        mVisitorIsInsideComment = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها عند مواجهة عقدة تعليق في المستند.
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
    /// يتم الاستدعاء عند انتهاء زيارة عقدة التعليق في المستند.
    /// </summary>
    public override VisitorAction VisitCommentEnd(Comment comment)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Comment end]");
        mVisitorIsInsideComment = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// قم بإلحاق سطر بـ StringBuilder وقم بعمل مسافة بادئة له اعتمادًا على مدى عمق الزائر في شجرة المستند.
    /// </summary>
    /// < param name = "text" > < / param >
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

### أنظر أيضا

* class [CommentRangeStart](../../commentrangestart)
* مساحة الاسم [Aspose.Words](../../commentrangestart)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
