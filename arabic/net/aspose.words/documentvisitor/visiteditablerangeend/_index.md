---
title: DocumentVisitor.VisitEditableRangeEnd
linktitle: VisitEditableRangeEnd
articleTitle: VisitEditableRangeEnd
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة DocumentVisitor VisitEditableRangeEnd—تعامل بكفاءة مع نهايات النطاق القابلة للتحرير في مستنداتك لتحقيق تحرير سلس ووظائف محسنة.
type: docs
weight: 160
url: /ar/net/aspose.words/documentvisitor/visiteditablerangeend/
---
## DocumentVisitor.VisitEditableRangeEnd method

يتم استدعاؤها عند مواجهة نهاية نطاق قابل للتحرير في المستند.

```csharp
public virtual VisitorAction VisitEditableRangeEnd(EditableRangeEnd editableRangeEnd)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| editableRangeEnd | EditableRangeEnd | الشيء الذي يتم زيارته. |

### قيمة الإرجاع

أ[`VisitorAction`](../../visitoraction/) القيمة التي تحدد كيفية مواصلة التعداد.

## أمثلة

يوضح كيفية طباعة بنية العقدة لكل نطاق قابل للتحرير في مستند.

```csharp
public void EditableRangeToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    EditableRangeStructurePrinter visitor = new EditableRangeStructurePrinter();

    // عندما نحصل على عقدة مركبة لقبول زائر مستند، يقوم الزائر بزيارة العقدة المستقبلة،
    // ثم يمر عبر جميع أبناء العقدة بطريقة العمق أولاً.
    //يمكن للزائر قراءة وتعديل كل عقدة تمت زيارتها.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// يجتاز شجرة العقد غير الثنائية المكونة من عقد فرعية.
/// إنشاء خريطة في شكل سلسلة من جميع عقد EditableRange التي تم مواجهتها وأطفالها.
/// </summary>
public class EditableRangeStructurePrinter : DocumentVisitor
{
    public EditableRangeStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideEditableRange = false;
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
        // نريد طباعة محتويات التشغيلات، ولكن فقط إذا كانت داخل الأشكال، كما هو الحال في حالة مربعات النص
        if (mVisitorIsInsideEditableRange) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها عند مواجهة عقدة EditableRange في المستند.
    /// </summary>
    public override VisitorAction VisitEditableRangeStart(EditableRangeStart editableRangeStart)
    {
        IndentAndAppendLine("[EditableRange start] ID: " + editableRangeStart.Id + " Owner: " +
                            editableRangeStart.EditableRange.SingleUser);
        mDocTraversalDepth++;
        mVisitorIsInsideEditableRange = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها عند انتهاء زيارة عقدة EditableRange.
    /// </summary>
    public override VisitorAction VisitEditableRangeEnd(EditableRangeEnd editableRangeEnd)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[EditableRange end]");
        mVisitorIsInsideEditableRange = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// أضف سطرًا إلى StringBuilder وقم بتدويره وفقًا لمدى عمق الزائر في شجرة المستند.
    /// </summary>
    /// <اسم المعلمة="نص"></param>
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++) mBuilder.Append("|  ");

        mBuilder.AppendLine(text);
    }

    private bool mVisitorIsInsideEditableRange;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### أنظر أيضا

* enum [VisitorAction](../../visitoraction/)
* class [EditableRangeEnd](../../editablerangeend/)
* class [DocumentVisitor](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
