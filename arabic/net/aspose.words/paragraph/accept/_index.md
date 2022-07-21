---
title: Accept
second_title: Aspose.Words لمراجع .NET API
description: يقبل الزائر .
type: docs
weight: 230
url: /ar/net/aspose.words/paragraph/accept/
---
## Paragraph.Accept method

يقبل الزائر .

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| visitor | DocumentVisitor | الزائر الذي سيزور العقد. |

### قيمة الإرجاع

صحيح إذا تمت زيارة جميع العقد ؛ خطأ إذا أوقف برنامج DocumentVisitor العملية قبل زيارة جميع العقد.

### ملاحظات

يعدّ فوق هذه العقدة وجميع توابعها. تستدعي كل عقدة طريقة مقابلة في DocumentVisitor.

لمزيد من المعلومات ، راجع نمط تصميم الزائر.

يستدعي DocumentVisitor.VisitParagraphStart ، ثم يستدعي Accept لجميع العقد الفرعية من الفقرة ويستدعي DocumentVisitor.VisitParagraphEnd في النهاية.

### أمثلة

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

* class [DocumentVisitor](../../documentvisitor)
* class [Paragraph](../../paragraph)
* مساحة الاسم [Aspose.Words](../../paragraph)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
