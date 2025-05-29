---
title: Comment
linktitle: Comment
articleTitle: Comment
second_title: Aspose.Words لـ .NET
description: أنشئ تعليقات جذابة بسهولة باستخدام مُنشئ التعليقات لدينا. أنشئ نسخة جديدة من فئة التعليقات وحسّن تفاعل المستخدم بسلاسة!
type: docs
weight: 10
url: /ar/net/aspose.words/comment/comment/
---
## Comment(*[DocumentBase](../../documentbase/)*) {#constructor}

يقوم بتهيئة مثيل جديد لـ[`Comment`](../) الصف.

```csharp
public Comment(DocumentBase doc)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| doc | DocumentBase | وثيقة المالك. |

## ملاحظات

متى[`Comment`](../) يتم إنشاؤه، فهو ينتمي إلى المستند المحدد، ولكنه ليس جزءًا من المستند بعد[`ParentNode`](../../node/parentnode/) يكون`باطل`.

لإضافة[`Comment`](../) لاستخدام المستند[`InsertAfter`](../../compositenode/insertafter/) أو[`InsertBefore`](../../compositenode/insertbefore/) على الفقرة التي تريد إدراج التعليق فيها.

بعد إنشاء تعليق، لا تنس تعيينه[`Author`](../author/) ، [`Initial`](../initial/) و[`DateTime`](../datetime/) ملكيات.

## أمثلة

يوضح كيفية طباعة محتويات كافة التعليقات ونطاقات تعليقاتها باستخدام زائر المستند.

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

    // أضف نصًا إلى المستند، ثم قم بتحريف النص داخل نطاق التعليقات، ثم أضف تعليقك.
    Paragraph para = doc.FirstSection.Body.FirstParagraph;
    para.AppendChild(new CommentRangeStart(doc, newComment.Id));
    para.AppendChild(new Run(doc, "Commented text."));
    para.AppendChild(new CommentRangeEnd(doc, newComment.Id));
    para.AppendChild(newComment); 

    //أضف ردين على التعليق.
    newComment.AddReply("John Doe", "JD", DateTime.Now, "New reply.");
    newComment.AddReply("John Doe", "JD", DateTime.Now, "Another reply.");

    PrintAllCommentInfo(doc.GetChildNodes(NodeType.Comment, true));
}

/// <summary>
/// يتكرر كل تعليق على المستوى الأعلى ويطبع نطاق التعليق ومحتوياته وردوده.
/// </summary>
private static void PrintAllCommentInfo(NodeCollection comments)
{
    CommentInfoPrinter commentVisitor = new CommentInfoPrinter();

    // كرر جميع التعليقات الرئيسية. بخلاف تعليقات الرد، لا يوجد للتعليقات الرئيسية أي سلف.
    foreach (Comment comment in comments.Where(c => ((Comment)c).Ancestor == null).ToList())
    {
        // أولاً، قم بزيارة بداية نطاق التعليق.
        CommentRangeStart commentRangeStart = (CommentRangeStart)comment.PreviousSibling.PreviousSibling.PreviousSibling;
        commentRangeStart.Accept(commentVisitor);

        // ثم قم بزيارة التعليق، وأي ردود قد تكون لديه.
        comment.Accept(commentVisitor);
        // قم بزيارة بداية التعليق فقط.
        comment.AcceptStart(commentVisitor);
        // قم بزيارة نهاية التعليق فقط.
        comment.AcceptEnd(commentVisitor);

        foreach (Comment reply in comment.Replies)
            reply.Accept(commentVisitor);

        // وأخيرًا، قم بزيارة نهاية نطاق التعليق، ثم قم بطباعة محتويات النص الخاصة بالزائر.
        CommentRangeEnd commentRangeEnd = (CommentRangeEnd)comment.PreviousSibling;
        commentRangeEnd.Accept(commentVisitor);

        Console.WriteLine(commentVisitor.GetText());
    }
}

/// <summary>
/// طباعة المعلومات ومحتويات جميع التعليقات ونطاقات التعليقات الموجودة في المستند.
/// </summary>
public class CommentInfoPrinter : DocumentVisitor
{
    public CommentInfoPrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideComment = false;
    }

    /// <summary>
    /// يحصل على النص العادي للمستند الذي جمعه الزائر.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// يتم استدعاؤها عند مواجهة عقدة تشغيل في المستند.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideComment) IndentAndAppendLine("[Run] \"" + run.Text + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها عند مواجهة عقدة CommentRangeStart في المستند.
    /// </summary>
    public override VisitorAction VisitCommentRangeStart(CommentRangeStart commentRangeStart)
    {
        IndentAndAppendLine("[Comment range start] ID: " + commentRangeStart.Id);
        mDocTraversalDepth++;
        mVisitorIsInsideComment = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها عند مواجهة عقدة CommentRangeEnd في المستند.
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
    /// يتم استدعاؤها عند انتهاء زيارة عقدة التعليق في المستند.
    /// </summary>
    public override VisitorAction VisitCommentEnd(Comment comment)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Comment end]");
        mVisitorIsInsideComment = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// أضف سطرًا إلى StringBuilder وقم بتدويره وفقًا لمدى عمق الزائر في شجرة المستند.
    /// </summary>
    /// <اسم المعلمة="نص"></param>
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

* class [DocumentBase](../../documentbase/)
* class [Comment](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## Comment(*[DocumentBase](../../documentbase/), string, string, DateTime*) {#constructor_1}

يقوم بتهيئة مثيل جديد لـ[`Comment`](../) الصف.

```csharp
public Comment(DocumentBase doc, string author, string initial, DateTime dateTime)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| doc | DocumentBase | وثيقة المالك. |
| author | String | اسم مؤلف التعليق. لا يمكن`باطل`. |
| initial | String | الأحرف الأولى من اسم المؤلف للتعليق. لا يمكن`باطل`. |
| dateTime | DateTime | التاريخ والوقت للتعليق. |

## أمثلة

يوضح كيفية إضافة تعليق إلى فقرة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

Comment comment = new Comment(doc, "John Doe", "JD", DateTime.Today);
builder.CurrentParagraph.AppendChild(comment);
builder.MoveTo(comment.AppendChild(new Paragraph(doc)));
builder.Write("Comment text.");

Assert.AreEqual(DateTime.Today, comment.DateTime);

 // في Microsoft Word، يمكننا النقر بزر الماوس الأيمن فوق هذا التعليق في نص المستند لتحريره أو الرد عليه.
doc.Save(ArtifactsDir + "InlineStory.AddComment.docx");
```

### أنظر أيضا

* class [DocumentBase](../../documentbase/)
* class [Comment](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
