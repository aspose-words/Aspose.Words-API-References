---
title: DocumentVisitor.VisitFieldEnd
second_title: Aspose.Words لمراجع .NET API
description: DocumentVisitor طريقة. يتم استدعاؤه عندما ينتهي الحقل في المستند.
type: docs
weight: 180
url: /ar/net/aspose.words/documentvisitor/visitfieldend/
---
## DocumentVisitor.VisitFieldEnd method

يتم استدعاؤه عندما ينتهي الحقل في المستند.

```csharp
public virtual VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fieldEnd | FieldEnd | الكائن الذي تتم زيارته. |

### قيمة الإرجاع

أ[`VisitorAction`](../../visitoraction/) القيمة التي تحدد كيفية متابعة التعداد.

### ملاحظات

لمزيد من المعلومات انظر[`VisitFieldStart`](../visitfieldstart/)

### أمثلة

يوضح كيفية طباعة بنية العقدة لكل حقل في المستند.

```csharp
public void FieldToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    FieldStructurePrinter visitor = new FieldStructurePrinter();

    // عندما نحصل على عقدة مركبة لقبول زائر المستند، يقوم الزائر بزيارة العقدة المقبولة،
    // ثم يجتاز جميع أبناء العقدة بطريقة العمق الأول.
    // يمكن للزائر قراءة وتعديل كل عقدة تمت زيارتها.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// يجتاز الشجرة غير الثنائية للعقدة التابعة.
/// ينشئ خريطة على شكل سلسلة من جميع العقد الميدانية التي تمت مواجهتها وأبناءها.
/// </summary>
public class FieldStructurePrinter : DocumentVisitor
{
    public FieldStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideField = false;
    }

    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// يتم الاتصال به عند مواجهة عقدة التشغيل في المستند.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideField) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم الاتصال به عند مواجهة عقدة FieldStart في المستند.
    /// </summary>
    public override VisitorAction VisitFieldStart(FieldStart fieldStart)
    {
        IndentAndAppendLine("[Field start] FieldType: " + fieldStart.FieldType);
        mDocTraversalDepth++;
        mVisitorIsInsideField = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم الاتصال به عند مواجهة عقدة FieldEnd في المستند.
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Field end]");
        mVisitorIsInsideField = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم الاتصال به عند مواجهة عقدة FieldSeparator في المستند.
    /// </summary>
    public override VisitorAction VisitFieldSeparator(FieldSeparator fieldSeparator)
    {
        IndentAndAppendLine("[FieldSeparator]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// ألحق سطرًا بـ StringBuilder، ثم ضع مسافة بادئة له اعتمادًا على مدى عمق الزائر
    /// في شجرة العقد التابعة للحقل.
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

    private bool mVisitorIsInsideField;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### أنظر أيضا

* enum [VisitorAction](../../visitoraction/)
* class [FieldEnd](../../../aspose.words.fields/fieldend/)
* class [DocumentVisitor](../)
* مساحة الاسم [Aspose.Words](../../documentvisitor/)
* المجسم [Aspose.Words](../../../)


