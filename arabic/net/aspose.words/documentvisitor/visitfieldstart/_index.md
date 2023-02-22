---
title: DocumentVisitor.VisitFieldStart
second_title: Aspose.Words لمراجع .NET API
description: DocumentVisitor طريقة. يتم استدعاؤها عندما يبدأ أحد الحقول في المستند.
type: docs
weight: 200
url: /ar/net/aspose.words/documentvisitor/visitfieldstart/
---
## DocumentVisitor.VisitFieldStart method

يتم استدعاؤها عندما يبدأ أحد الحقول في المستند.

```csharp
public virtual VisitorAction VisitFieldStart(FieldStart fieldStart)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fieldStart | FieldStart | الكائن الذي تتم زيارته. |

### قيمة الإرجاع

أ[`VisitorAction`](../../visitoraction/) القيمة التي تحدد كيفية متابعة التعداد.

### ملاحظات

يتكون الحقل في مستند Word من رمز الحقل وقيمة الحقل.

على سبيل المثال ، يمكن تمثيل الحقل الذي يعرض رقم الصفحة على النحو التالي:

[FieldStart] الصفحة [FieldSeparator] 98 [FieldEnd]

يفصل فاصل الحقل رمز الحقل عن قيمة الحقل في المستند. لاحظ أن بعض حقول لها رمز حقل فقط ولا تحتوي على فاصل حقل وقيمة حقل.

يمكن أن تتداخل الحقول.

### أمثلة

يوضح كيفية طباعة بنية العقدة لكل حقل في المستند.

```csharp
public void FieldToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    FieldStructurePrinter visitor = new FieldStructurePrinter();

    // عندما نحصل على عقدة مركبة لقبول زائر المستند ، يزور الزائر عقدة القبول ،
    // ثم يعبر جميع أبناء العقدة بطريقة العمق أولاً.
    // يمكن للزائر قراءة كل عقدة تمت زيارتها وتعديلها.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// يتجاوز الشجرة غير الثنائية للعقد الفرعية للعقد.
/// ينشئ خريطة في شكل سلسلة من جميع العقد الميدانية التي تمت مواجهتها وأطفالها.
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
    /// يتم الاستدعاء عند مواجهة عقدة تشغيل في المستند.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideField) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم الاستدعاء عند مواجهة عقدة FieldStart في المستند.
    /// </summary>
    public override VisitorAction VisitFieldStart(FieldStart fieldStart)
    {
        IndentAndAppendLine("[Field start] FieldType: " + fieldStart.FieldType);
        mDocTraversalDepth++;
        mVisitorIsInsideField = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم الاستدعاء عند مواجهة عقدة FieldEnd في المستند.
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Field end]");
        mVisitorIsInsideField = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم الاستدعاء عند مواجهة عقدة FieldSeparator في المستند.
    /// </summary>
    public override VisitorAction VisitFieldSeparator(FieldSeparator fieldSeparator)
    {
        IndentAndAppendLine("[FieldSeparator]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// قم بإلحاق سطر بـ StringBuilder ، وقم بعمل مسافة بادئة له اعتمادًا على مدى عمق الزائر
    /// في شجرة الحقل للعقد الفرعية.
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

    private bool mVisitorIsInsideField;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### أنظر أيضا

* enum [VisitorAction](../../visitoraction/)
* class [FieldStart](../../../aspose.words.fields/fieldstart/)
* class [DocumentVisitor](../)
* مساحة الاسم [Aspose.Words](../../documentvisitor/)
* المجسم [Aspose.Words](../../../)


