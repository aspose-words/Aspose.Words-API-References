---
title: DocumentVisitor.VisitAbsolutePositionTab
linktitle: VisitAbsolutePositionTab
articleTitle: VisitAbsolutePositionTab
second_title: Aspose.Words لـ .NET
description: DocumentVisitor VisitAbsolutePositionTab طريقة. تم الاتصال به عندما أAbsolutePositionTab تمت مصادفة عقدة في المستند في C#.
type: docs
weight: 10
url: /ar/net/aspose.words/documentvisitor/visitabsolutepositiontab/
---
## DocumentVisitor.VisitAbsolutePositionTab method

تم الاتصال به عندما أ[`AbsolutePositionTab`](../../absolutepositiontab/) تمت مصادفة عقدة في المستند.

```csharp
public virtual VisitorAction VisitAbsolutePositionTab(AbsolutePositionTab tab)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| tab | AbsolutePositionTab | الكائن الذي تتم زيارته. |

### قيمة الإرجاع

أ[`VisitorAction`](../../visitoraction/) القيمة التي تحدد كيفية متابعة التعداد.

## أمثلة

يوضح كيفية معالجة أحرف علامة تبويب الموضع المطلق مع زائر المستند.

```csharp
public void DocumentToTxt()
{
    Document doc = new Document(MyDir + "Absolute position tab.docx");

    // استخرج محتويات النص من وثيقتنا عن طريق قبول زائر المستند المخصص هذا.
    DocTextExtractor myDocTextExtractor = new DocTextExtractor();
    doc.FirstSection.Body.Accept(myDocTextExtractor);

    // تم تحويل علامة تبويب الموضع المطلق، التي ليس لها ما يعادلها في شكل سلسلة، بشكل صريح إلى حرف جدولة.
    Assert.AreEqual("Before AbsolutePositionTab\tAfter AbsolutePositionTab", myDocTextExtractor.GetText());

    // يمكن لـAbsolutePositionTab قبول DocumentVisitor بمفرده أيضًا.
    AbsolutePositionTab absPositionTab = (AbsolutePositionTab)doc.FirstSection.Body.FirstParagraph.GetChild(NodeType.SpecialChar, 0, true);

    myDocTextExtractor = new DocTextExtractor();
    absPositionTab.Accept(myDocTextExtractor);

    Assert.AreEqual("\t", myDocTextExtractor.GetText());
}

/// <summary>
/// يجمع محتويات النص لجميع عمليات التشغيل في المستند الذي تمت زيارته. يستبدل كافة أحرف علامات التبويب المطلقة بعلامات تبويب عادية.
/// </summary>
public class DocTextExtractor : DocumentVisitor
{
    public DocTextExtractor()
    {
        mBuilder = new StringBuilder();
    }

    /// <summary>
    /// يتم الاتصال به عند مواجهة عقدة التشغيل في المستند.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        AppendText(run.Text);
        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم الاتصال به عند مواجهة عقدةAbsolutePositionTab في المستند.
    /// </summary>
    public override VisitorAction VisitAbsolutePositionTab(AbsolutePositionTab tab)
    {
        mBuilder.Append("\t");
        return VisitorAction.Continue;
    }

    /// <summary>
    /// يضيف نصًا إلى الإخراج الحالي. يكرم علامة الإخراج الممكنة/المعطلة.
    /// </summary>
    private void AppendText(string text)
    {
        mBuilder.Append(text);
    }

    /// <summary>
    /// نص عادي للوثيقة التي جمعها الزائر.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    private readonly StringBuilder mBuilder;
}
```

### أنظر أيضا

* enum [VisitorAction](../../visitoraction/)
* class [AbsolutePositionTab](../../absolutepositiontab/)
* class [DocumentVisitor](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
