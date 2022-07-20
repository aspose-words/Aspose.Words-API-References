---
title: VisitCommentStart
second_title: Aspose.Words لمراجع .NET API
description: يتم الاستدعاء عند بدء تعداد نص التعليق.
type: docs
weight: 130
url: /ar/net/aspose.words/documentvisitor/visitcommentstart/
---
## DocumentVisitor.VisitCommentStart method

يتم الاستدعاء عند بدء تعداد نص التعليق.

```csharp
public virtual VisitorAction VisitCommentStart(Comment comment)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| comment | Comment | الكائن الذي تتم زيارته. |

### قيمة الإرجاع

أ[`VisitorAction`](../../visitoraction) القيمة التي تحدد كيفية متابعة التعداد.

### أمثلة

يوضح كيفية طباعة بنية العقدة لكل تعليق ونطاق تعليق في مستند.

```csharp
public void CommentsToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    CommentStructurePrinter visitor = new CommentStructurePrinter();

    // عندما نحصل على عقدة مركبة لقبول زائر المستند ، يزور الزائر عقدة القبول ،
    // ثم يعبر جميع أبناء العقدة بطريقة العمق أولاً.
    // يمكن للزائر قراءة كل عقدة تمت زيارتها وتعديلها.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// يتجاوز الشجرة غير الثنائية للعقد الفرعية للعقد.
/// ينشئ خريطة في شكل سلسلة من جميع العقد Comment / CommentRange التي تمت مواجهتها وأطفالها.
/// </summary>
public class CommentStructurePrinter : DocumentVisitor
{
    public CommentStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideComment = false;
    }

    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// يتم الاستدعاء عند مواجهة عقدة تشغيل في المستند.
    /// يتم تسجيل Run فقط إذا كان تابعًا لعقدة Comment أو CommentRange.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideComment) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

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
        IndentAndAppendLine("[Comment range end]");
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
    /// يتم استدعاؤها بعد زيارة جميع العقد الفرعية لعقدة التعليق.
    /// </summary>
    public override VisitorAction VisitCommentEnd(Comment comment)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Comment end]");
        mVisitorIsInsideComment = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// قم بإلحاق سطر بـ StringBuilder ، وقم بعمل مسافة بادئة له اعتمادًا على مدى عمق الزائر
    /// في شجرة نطاق تعليق / تعليق للعقد الفرعية.
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

يوضح كيفية استخدام تطبيق DocumentVisitor لإزالة كل المحتوى المخفي من المستند.

```csharp
{
    Document doc = new Document(MyDir + "Hidden content.docx");

    RemoveHiddenContentVisitor hiddenContentRemover = new RemoveHiddenContentVisitor();

    // فيما يلي ثلاثة أنواع من الحقول التي يمكن أن تقبل زائر المستند ،
    // مما سيسمح له بزيارة عقدة القبول ، ثم اجتياز العقد الفرعية بطريقة العمق أولاً.
    // 1 - عقدة فقرة:
    Paragraph para = (Paragraph) doc.GetChild(NodeType.Paragraph, 4, true);
    para.Accept(hiddenContentRemover);

    // 2 - عقدة الجدول:
    Table table = doc.FirstSection.Body.Tables[0];
    table.Accept(hiddenContentRemover);

    // 3 - عقدة المستند:
    doc.Accept(hiddenContentRemover);

    doc.Save(ArtifactsDir + "Font.RemoveHiddenContentFromDocument.docx");

/// <summary>
/// يزيل جميع العقد التي تمت زيارتها والتي تم وضع علامة عليها على أنها "محتوى مخفي".
/// </summary>
public class RemoveHiddenContentVisitor : DocumentVisitor
{
    /// <summary>
    /// يتم الاستدعاء عند مواجهة عقدة FieldStart في المستند.
    /// </summary>
    public override VisitorAction VisitFieldStart(FieldStart fieldStart)
    {
        if (fieldStart.Font.Hidden)
            fieldStart.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم الاستدعاء عند مواجهة عقدة FieldEnd في المستند.
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        if (fieldEnd.Font.Hidden)
            fieldEnd.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم الاستدعاء عند مواجهة عقدة FieldSeparator في المستند.
    /// </summary>
    public override VisitorAction VisitFieldSeparator(FieldSeparator fieldSeparator)
    {
        if (fieldSeparator.Font.Hidden)
            fieldSeparator.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم الاستدعاء عند مواجهة عقدة تشغيل في المستند.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (run.Font.Hidden)
            run.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها عند مواجهة عقدة فقرة في المستند.
    /// </summary>
    public override VisitorAction VisitParagraphStart(Paragraph paragraph)
    {
        if (paragraph.ParagraphBreakFont.Hidden)
            paragraph.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم الاستدعاء عند مواجهة FormField في المستند.
    /// </summary>
    public override VisitorAction VisitFormField(FormField formField)
    {
        if (formField.Font.Hidden)
            formField.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤه عند مواجهة GroupShape في المستند.
    /// </summary>
    public override VisitorAction VisitGroupShapeStart(GroupShape groupShape)
    {
        if (groupShape.Font.Hidden)
            groupShape.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤه عند مواجهة شكل في المستند.
    /// </summary>
    public override VisitorAction VisitShapeStart(Shape shape)
    {
        if (shape.Font.Hidden)
            shape.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤه عند مواجهة أحد التعليقات في المستند.
    /// </summary>
    public override VisitorAction VisitCommentStart(Comment comment)
    {
        if (comment.Font.Hidden)
            comment.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها عند مواجهة حاشية سفلية في المستند.
    /// </summary>
    public override VisitorAction VisitFootnoteStart(Footnote footnote)
    {
        if (footnote.Font.Hidden)
            footnote.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها عند مواجهة حرف خاص في المستند.
    /// </summary>
    public override VisitorAction VisitSpecialChar(SpecialChar specialChar)
    {
        if (specialChar.Font.Hidden)
            specialChar.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها عند زيارة عقدة جدول تنتهي في المستند.
    /// </summary>
    public override VisitorAction VisitTableEnd(Table table)
    {
        // قد يحتوي المحتوى الموجود داخل خلايا الجدول على علامة المحتوى المخفية ، ولكن لا يمكن للجداول نفسها.
        // إذا كان هذا الجدول لا يحتوي إلا على محتوى مخفي ، لكان هذا الزائر قد أزاله بالكامل ،
        // ولن تكون هناك عقد فرعية متبقية.
        // وبالتالي ، يمكننا أيضًا التعامل مع الجدول نفسه كمحتوى مخفي وإزالته.
        // ستحتوي الجداول الفارغة ولكن ليس بها محتوى مخفي على خلايا بها فقرات فارغة بداخلها ،
        // التي لن يزيلها هذا الزائر.
        if (!table.HasChildNodes)
            table.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم الاستدعاء عند زيارة عقدة خلية في المستند.
    /// </summary>
    public override VisitorAction VisitCellEnd(Cell cell)
    {
        if (!cell.HasChildNodes && cell.ParentNode != null)
            cell.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها عند زيارة عقدة صف منتهية في المستند.
    /// </summary>
    public override VisitorAction VisitRowEnd(Row row)
    {
        if (!row.HasChildNodes && row.ParentNode != null)
            row.Remove();

        return VisitorAction.Continue;
    }
}
```

### أنظر أيضا

* enum [VisitorAction](../../visitoraction)
* class [Comment](../../comment)
* class [DocumentVisitor](../../documentvisitor)
* مساحة الاسم [Aspose.Words](../../documentvisitor)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
