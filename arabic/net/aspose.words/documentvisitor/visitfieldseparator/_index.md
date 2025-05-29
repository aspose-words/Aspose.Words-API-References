---
title: DocumentVisitor.VisitFieldSeparator
linktitle: VisitFieldSeparator
articleTitle: VisitFieldSeparator
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة VisitFieldSeparator في DocumentVisitor. استخدم فواصل الحقول بكفاءة في مستنداتك لتسهيل المعالجة.
type: docs
weight: 190
url: /ar/net/aspose.words/documentvisitor/visitfieldseparator/
---
## DocumentVisitor.VisitFieldSeparator method

يتم استدعاؤها عند مواجهة فاصل حقل في المستند.

```csharp
public virtual VisitorAction VisitFieldSeparator(FieldSeparator fieldSeparator)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fieldSeparator | FieldSeparator | الشيء الذي يتم زيارته. |

### قيمة الإرجاع

أ[`VisitorAction`](../../visitoraction/) القيمة التي تحدد كيفية مواصلة التعداد.

## ملاحظات

يفصل فاصل الحقول رمز الحقل عن قيمته في المستند. يُرجى ملاحظة أن بعض حقول تحتوي على رمز الحقل فقط، ولا تحتوي على فاصل أو قيمة حقل.

لمزيد من المعلومات انظر[`VisitFieldStart`](../visitfieldstart/)

## أمثلة

يوضح كيفية طباعة بنية العقدة لكل حقل في المستند.

```csharp
public void FieldToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    FieldStructurePrinter visitor = new FieldStructurePrinter();

    // عندما نحصل على عقدة مركبة لقبول زائر مستند، يقوم الزائر بزيارة العقدة المستقبلة،
    // ثم يمر عبر جميع أبناء العقدة بطريقة العمق أولاً.
    //يمكن للزائر قراءة وتعديل كل عقدة تمت زيارتها.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// يجتاز شجرة العقد غير الثنائية المكونة من عقد فرعية.
/// إنشاء خريطة في شكل سلسلة من جميع عقد الحقل التي تم مواجهتها وأطفالها.
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
    /// يتم استدعاؤها عند مواجهة عقدة تشغيل في المستند.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideField) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها عند مواجهة عقدة FieldStart في المستند.
    /// </summary>
    public override VisitorAction VisitFieldStart(FieldStart fieldStart)
    {
        IndentAndAppendLine("[Field start] FieldType: " + fieldStart.FieldType);
        mDocTraversalDepth++;
        mVisitorIsInsideField = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها عند مواجهة عقدة FieldEnd في المستند.
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Field end]");
        mVisitorIsInsideField = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها عند مواجهة عقدة FieldSeparator في المستند.
    /// </summary>
    public override VisitorAction VisitFieldSeparator(FieldSeparator fieldSeparator)
    {
        IndentAndAppendLine("[FieldSeparator]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// أضف سطرًا إلى StringBuilder، وقم بتدويره حسب عمق الزائر
    /// في شجرة الحقل الخاصة بالعقد الفرعية.
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

    private bool mVisitorIsInsideField;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### أنظر أيضا

* enum [VisitorAction](../../visitoraction/)
* class [FieldSeparator](../../../aspose.words.fields/fieldseparator/)
* class [DocumentVisitor](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
