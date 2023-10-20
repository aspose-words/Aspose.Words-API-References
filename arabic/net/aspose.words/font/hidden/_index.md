---
title: Font.Hidden
linktitle: Hidden
articleTitle: Hidden
second_title: Aspose.Words لـ .NET
description: Font Hidden ملكية. صحيح إذا تم تنسيق الخط كنص مخفي في C#.
type: docs
weight: 140
url: /ar/net/aspose.words/font/hidden/
---
## Font.Hidden property

صحيح إذا تم تنسيق الخط كنص مخفي.

```csharp
public bool Hidden { get; set; }
```

## أمثلة

يوضح كيفية إنشاء مجموعة من النص المخفي.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// مع تعيين العلامة المخفية على "صحيح"، سيكون أي نص نقوم بإنشائه باستخدام كائن الخط هذا غير مرئي في المستند.
// لن نرى أو نبرز النص المخفي إلا إذا قمنا بتمكين خيار "النص المخفي".
// موجود في Microsoft Word عبر "ملف" -> "الخيارات" -> "عرض". سيظل النص موجودا
// وسنتمكن من الوصول إلى هذا النص برمجياً.
// لا ينصح باستخدام هذه الطريقة لإخفاء المعلومات الحساسة.
builder.Font.Hidden = true;
builder.Font.Size = 36;

builder.Writeln("This text will not be visible in the document.");

doc.Save(ArtifactsDir + "Font.Hidden.docx");
```

يوضح كيفية استخدام تطبيق DocumentVisitor لإزالة كل المحتوى المخفي من المستند.

```csharp
public void RemoveHiddenContentFromDocument()
{
    Document doc = new Document(MyDir + "Hidden content.docx");
    RemoveHiddenContentVisitor hiddenContentRemover = new RemoveHiddenContentVisitor();

    // فيما يلي ثلاثة أنواع من الحقول التي يمكنها قبول زائر المستند،
    // والذي سيسمح لها بزيارة العقدة المقبولة، ثم اجتياز العقد الفرعية الخاصة بها بطريقة العمق أولاً.
    // 1 - عقدة الفقرة:
    Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 4, true);
    para.Accept(hiddenContentRemover);

    // 2 - عقدة الجدول:
    Table table = doc.FirstSection.Body.Tables[0];
    table.Accept(hiddenContentRemover);

    // 3 - عقدة الوثيقة:
    doc.Accept(hiddenContentRemover);

    doc.Save(ArtifactsDir + "Font.RemoveHiddenContentFromDocument.docx");
}

/// <summary>
/// يزيل جميع العقد التي تمت زيارتها والتي تم وضع علامة "المحتوى المخفي" عليها.
/// </summary>
public class RemoveHiddenContentVisitor : DocumentVisitor
{
    /// <summary>
    /// يتم الاتصال به عند مواجهة عقدة FieldStart في المستند.
    /// </summary>
    public override VisitorAction VisitFieldStart(FieldStart fieldStart)
    {
        if (fieldStart.Font.Hidden)
            fieldStart.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم الاتصال به عند مواجهة عقدة FieldEnd في المستند.
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        if (fieldEnd.Font.Hidden)
            fieldEnd.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم الاتصال به عند مواجهة عقدة FieldSeparator في المستند.
    /// </summary>
    public override VisitorAction VisitFieldSeparator(FieldSeparator fieldSeparator)
    {
        if (fieldSeparator.Font.Hidden)
            fieldSeparator.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم الاتصال به عند مواجهة عقدة التشغيل في المستند.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (run.Font.Hidden)
            run.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤه عند مواجهة عقدة فقرة في المستند.
    /// </summary>
    public override VisitorAction VisitParagraphStart(Paragraph paragraph)
    {
        if (paragraph.ParagraphBreakFont.Hidden)
            paragraph.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم الاتصال به عند مواجهة FormField في المستند.
    /// </summary>
    public override VisitorAction VisitFormField(FormField formField)
    {
        if (formField.Font.Hidden)
            formField.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم الاتصال به عند مواجهة شكل مجموعة في المستند.
    /// </summary>
    public override VisitorAction VisitGroupShapeStart(GroupShape groupShape)
    {
        if (groupShape.Font.Hidden)
            groupShape.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤه عند مواجهة شكل ما في المستند.
    /// </summary>
    public override VisitorAction VisitShapeStart(Shape shape)
    {
        if (shape.Font.Hidden)
            shape.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤه عند مواجهة تعليق في المستند.
    /// </summary>
    public override VisitorAction VisitCommentStart(Comment comment)
    {
        if (comment.Font.Hidden)
            comment.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤه عند وجود حاشية سفلية في المستند.
    /// </summary>
    public override VisitorAction VisitFootnoteStart(Footnote footnote)
    {
        if (footnote.Font.Hidden)
            footnote.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم الاتصال به عند مواجهة حرف خاص في المستند.
    /// </summary>
    public override VisitorAction VisitSpecialChar(SpecialChar specialChar)
    {
        if (specialChar.Font.Hidden)
            specialChar.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم الاتصال به عند انتهاء زيارة عقدة الجدول في المستند.
    /// </summary>
    public override VisitorAction VisitTableEnd(Table table)
    {
        // قد يحتوي المحتوى الموجود داخل خلايا الجدول على علامة محتوى مخفية، لكن لا يمكن أن تحتوي الجداول نفسها على علامة محتوى مخفية.
        // لو لم يكن هذا الجدول سوى محتوى مخفي، لكان هذا الزائر قد أزاله كله،
        // ولن تكون هناك عقد فرعية متبقية.
        // وبالتالي، يمكننا أيضًا التعامل مع الجدول نفسه كمحتوى مخفي وإزالته.
        // الجداول الفارغة ولكن لا تحتوي على محتوى مخفي ستحتوي على خلايا تحتوي على فقرات فارغة بداخلها،
        // الذي لن يقوم هذا الزائر بإزالته.
        if (!table.HasChildNodes)
            table.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم الاتصال به عند انتهاء زيارة عقدة الخلية في المستند.
    /// </summary>
    public override VisitorAction VisitCellEnd(Cell cell)
    {
        if (!cell.HasChildNodes && cell.ParentNode != null)
            cell.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم الاتصال به عند انتهاء زيارة عقدة الصف في المستند.
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

* class [Font](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
