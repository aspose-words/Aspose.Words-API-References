---
title: SpecialChar Class
linktitle: SpecialChar
articleTitle: SpecialChar
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.SpecialChar، أداتك الأساسية لإدارة الأحرف الخاصة في المستندات. حسّن معالجة مستنداتك اليوم!
type: docs
weight: 6950
url: /ar/net/aspose.words/specialchar/
---
## SpecialChar class

الفئة الأساسية للأحرف الخاصة في المستند.

لمعرفة المزيد، قم بزيارة[نموذج كائن المستند (DOM) في Aspose.Words](https://docs.aspose.com/words/net/aspose-words-document-object-model/) مقالة توثيقية.

```csharp
public class SpecialChar : Inline
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | يحدد معرف العقدة المخصص. |
| virtual [Document](../../aspose.words/node/document/) { get; } | يحصل على المستند الذي تنتمي إليه هذه العقدة. |
| [Font](../../aspose.words/inline/font/) { get; } | يوفر الوصول إلى تنسيق الخط لهذا الكائن. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | إرجاع`حقيقي` إذا كانت هذه العقدة قادرة على احتواء عقد أخرى. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | يعود صحيحًا إذا تم حذف هذا الكائن في Microsoft Word أثناء تمكين تتبع التغييرات. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | يعود صحيحًا إذا تم تغيير تنسيق الكائن في Microsoft Word أثناء تمكين تتبع التغييرات. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | يعود صحيحًا إذا تم إدراج هذا الكائن في Microsoft Word أثناء تمكين تتبع التغييرات. |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | إرجاع`حقيقي` إذا تم نقل هذا الكائن (حذفه) في Microsoft Word أثناء تمكين تتبع التغييرات. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | إرجاع`حقيقي` إذا تم نقل هذا الكائن (إدراجه) في Microsoft Word أثناء تمكين تتبع التغييرات. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| override [NodeType](../../aspose.words/specialchar/nodetype/) { get; } | إرجاعSpecialChar . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | يحصل على الوالد المباشر لهذه العقدة. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | يسترد الأصل[`Paragraph`](../paragraph/) من هذه العقدة. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرةً. |
| [Range](../../aspose.words/node/range/) { get; } | يعيد[`Range`](../range/)الكائن الذي يمثل الجزء من المستند الموجود في هذه العقدة. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Accept](../../aspose.words/specialchar/accept/)(*[DocumentVisitor](../documentvisitor/)*) | يقبل زائرًا. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | ينشئ نسخة مكررة من العقدة. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | يحصل على السلف الأول للعنصر المحدد[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | يحصل على السلف الأول لنوع الكائن المحدد. |
| override [GetText](../../aspose.words/specialchar/gettext/)() | يحصل على الحرف الخاص الذي تمثله هذه العقدة. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | يحصل على العقدة التالية وفقًا لخوارزمية عبور شجرة الترتيب المسبق. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | يحصل على العقدة السابقة وفقًا لخوارزمية عبور شجرة الترتيب المسبق. |
| [Remove](../../aspose.words/node/remove/)() | يزيل نفسه من الأصل. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | يصدر محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | يقوم بتصدير محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |

## ملاحظات

يمكن أن يتضمن مستند Microsoft Word عددًا من الأحرف الخاصة التي تمثل الحقول وحقول النماذج والأشكال وكائنات OLE والحواشي السفلية وما إلى ذلك. بالنسبة لقائمة للأحرف الخاصة، راجع[`ControlChar`](../controlchar/).

`SpecialChar` هي عقدة مضمنة ولا يمكن أن تكون إلا طفلة لـ[`Paragraph`](../paragraph/).

`SpecialChar` يتم استخدام char كفئة أساسية لفئات أكثر تحديدًا التي تمثل الأحرف الخاصة التي يوفر Aspose.Words إمكانية الوصول البرمجي لها. `SpecialChar`تُستخدم الفئة أيضًا لتمثيل الأحرف الخاصة التي ولا يوفر Aspose.Words وصولاً برمجيًا تفصيليًا.

## أمثلة

يوضح كيفية استخدام تنفيذ DocumentVisitor لإزالة كل المحتوى المخفي من المستند.

```csharp
public void RemoveHiddenContentFromDocument()
{
    Document doc = new Document(MyDir + "Hidden content.docx");
    RemoveHiddenContentVisitor hiddenContentRemover = new RemoveHiddenContentVisitor();

    // فيما يلي ثلاثة أنواع من الحقول التي يمكنها قبول زائر المستند،
    // مما سيسمح لها بزيارة العقدة المستقبلة، ثم عبور العقد الفرعية الخاصة بها بطريقة العمق أولاً.
    // 1 - عقدة الفقرة:
    Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 4, true);
    para.Accept(hiddenContentRemover);

    // 2 - عقدة الجدول:
    Table table = doc.FirstSection.Body.Tables[0];
    table.Accept(hiddenContentRemover);

    // 3 - عقدة المستند:
    doc.Accept(hiddenContentRemover);

    doc.Save(ArtifactsDir + "Font.RemoveHiddenContentFromDocument.docx");
}

/// <summary>
/// يقوم بإزالة جميع العقد التي تمت زيارتها والتي تم وضع علامة "المحتوى المخفي" عليها.
/// </summary>
public class RemoveHiddenContentVisitor : DocumentVisitor
{
    /// <summary>
    /// يتم استدعاؤها عند مواجهة عقدة FieldStart في المستند.
    /// </summary>
    public override VisitorAction VisitFieldStart(FieldStart fieldStart)
    {
        if (fieldStart.Font.Hidden)
            fieldStart.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها عند مواجهة عقدة FieldEnd في المستند.
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        if (fieldEnd.Font.Hidden)
            fieldEnd.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها عند مواجهة عقدة FieldSeparator في المستند.
    /// </summary>
    public override VisitorAction VisitFieldSeparator(FieldSeparator fieldSeparator)
    {
        if (fieldSeparator.Font.Hidden)
            fieldSeparator.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها عند مواجهة عقدة تشغيل في المستند.
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
    /// يتم استدعاؤها عند العثور على FormField في المستند.
    /// </summary>
    public override VisitorAction VisitFormField(FormField formField)
    {
        if (formField.Font.Hidden)
            formField.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها عند مواجهة GroupShape في المستند.
    /// </summary>
    public override VisitorAction VisitGroupShapeStart(GroupShape groupShape)
    {
        if (groupShape.Font.Hidden)
            groupShape.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها عند العثور على شكل في المستند.
    /// </summary>
    public override VisitorAction VisitShapeStart(Shape shape)
    {
        if (shape.Font.Hidden)
            shape.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها عند العثور على تعليق في المستند.
    /// </summary>
    public override VisitorAction VisitCommentStart(Comment comment)
    {
        if (comment.Font.Hidden)
            comment.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها عند العثور على حاشية سفلية في المستند.
    /// </summary>
    public override VisitorAction VisitFootnoteStart(Footnote footnote)
    {
        if (footnote.Font.Hidden)
            footnote.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها عند مواجهة SpecialCharacter في المستند.
    /// </summary>
    public override VisitorAction VisitSpecialChar(SpecialChar specialChar)
    {
        Console.WriteLine(specialChar.GetText());

        if (specialChar.Font.Hidden)
            specialChar.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها عند انتهاء زيارة عقدة الجدول في المستند.
    /// </summary>
    public override VisitorAction VisitTableEnd(Table table)
    {
        // قد يكون المحتوى الموجود داخل خلايا الجدول يحتوي على علامة المحتوى المخفي، ولكن الجداول نفسها لا يمكن أن يكون لديها هذه العلامة.
        // إذا لم يكن في هذا الجدول سوى محتوى مخفي، فإن هذا الزائر كان سيحذفه بالكامل،
        //ولن يتبقى أي عقدة فرعية.
        // وبالتالي، يمكننا أيضًا التعامل مع الجدول نفسه كمحتوى مخفي وإزالته.
        // ستحتوي الجداول الفارغة التي لا تحتوي على محتوى مخفي على خلايا تحتوي على فقرات فارغة بداخلها،
        // والتي لن يقوم هذا الزائر بإزالتها.
        if (!table.HasChildNodes)
            table.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها عند انتهاء زيارة عقدة الخلية في المستند.
    /// </summary>
    public override VisitorAction VisitCellEnd(Cell cell)
    {
        if (!cell.HasChildNodes && cell.ParentNode != null)
            cell.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها عند انتهاء زيارة عقدة الصف في المستند.
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

* class [Inline](../inline/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
