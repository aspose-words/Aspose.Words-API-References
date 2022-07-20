---
title: SpecialChar
second_title: Aspose.Words لمراجع .NET API
description: الفئة الأساسية للأحرف الخاصة في المستند.
type: docs
weight: 5800
url: /ar/net/aspose.words/specialchar/
---
## SpecialChar class

الفئة الأساسية للأحرف الخاصة في المستند.

```csharp
public class SpecialChar : Inline
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | يحدد معرف العقدة المخصص ._ x000d_ |
| virtual [Document](../../aspose.words/node/document) { get; } | الحصول على المستند الذي تنتمي إليه هذه العقدة . |
| [Font](../../aspose.words/inline/font) { get; } | يوفر الوصول إلى تنسيق خط هذا الكائن. |
| virtual [IsComposite](../../aspose.words/node/iscomposite) { get; } | إرجاع صحيح إذا كانت هذه العقدة يمكن أن تحتوي على عقد أخرى. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision) { get; } | إرجاع صحيح إذا تم حذف هذا الكائن في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision) { get; } | إرجاع صحيح إذا تم تغيير تنسيق الكائن في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision) { get; } | إرجاع صحيح إذا تم إدراج هذا الكائن في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision) { get; } | عوائد **حقيقي** إذا تم نقل (حذف) هذا الكائن في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision) { get; } | عوائد **حقيقي** إذا تم نقل هذا الكائن (إدراجه) في Microsoft Word أثناء تمكين تعقب التغيير. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| override [NodeType](../../aspose.words/specialchar/nodetype) { get; } | عوائد **NodeType.SpecialChar** . |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | الحصول على الأصل المباشر لهذه العقدة. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph) { get; } | استرداد الأصل[`Paragraph`](../paragraph) من هذه العقدة. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرة. |
| [Range](../../aspose.words/node/range) { get; } | إرجاع أ **نطاق** الكائن الذي يمثل جزء المستند الموجود في هذه العقدة. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Accept](../../aspose.words/specialchar/accept)(DocumentVisitor) | يقبل الزائر . |
| [Clone](../../aspose.words/node/clone)(bool) | لإنشاء نسخة مكررة من العقدة . |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | يحصل على أول سلف محدد[`NodeType`](../nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | الحصول على الأصل الأول لنوع الكائن المحدد. |
| override [GetText](../../aspose.words/specialchar/gettext)() | يحصل على الحرف الخاص الذي تمثله هذه العقدة . |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | الحصول على العقدة التالية وفقًا لخوارزمية اجتياز الشجرة بالطلب المسبق. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | الحصول على العقدة السابقة وفقًا لخوارزمية اجتياز الشجرة بالطلب المسبق. |
| [Remove](../../aspose.words/node/remove)() | يزيل نفسه من الأصل. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | يصدر محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | يصدر محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |

### ملاحظات

يمكن أن يتضمن مستند Microsoft Word عددًا من الأحرف الخاصة_ x000d_ التي تمثل الحقول ، وحقول النموذج ، والأشكال ، وكائنات OLE ، والحواشي السفلية ، إلخ.[`ControlChar`](../controlchar).

**SpecialChar** هي عقدة مضمنة ويمكن أن تكون تابعة فقط لـ **فقرة**.

**SpecialChar** يتم استخدام char كفئة أساسية للفئات الأكثر تحديدًا التي تمثل الأحرف الخاصة التي توفرها Aspose.Words وصول برمجي لـ . The **SpecialChar** تُستخدم الفئة نفسها أيضًا لتمثيل الحرف الخاص الذي لا يوفر له Aspose.Words وصول برمجي مفصل.

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

* class [Inline](../inline)
* مساحة الاسم [Aspose.Words](../../aspose.words)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
