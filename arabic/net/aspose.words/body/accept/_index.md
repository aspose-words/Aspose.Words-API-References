---
title: Body.Accept
linktitle: Accept
articleTitle: Accept
second_title: Aspose.Words لـ .NET
description: اكتشف أسلوب Body Accept لتفاعل سلس مع الزوار. حسّن تجربة المستخدم وعزز معدلات التحويل من خلال نهجنا الفريد!
type: docs
weight: 40
url: /ar/net/aspose.words/body/accept/
---
## Body.Accept method

يقبل زائرًا.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| visitor | DocumentVisitor | الزائر الذي سيقوم بزيارة العقد. |

### قيمة الإرجاع

صحيح إذا تمت زيارة جميع العقد؛ خطأ إذا[`DocumentVisitor`](../../documentvisitor/) تم إيقاف العملية قبل زيارة كافة العقد.

## ملاحظات

يُحصي هذه العقدة وجميع أبنائها. تستدعي كل عقدة طريقة مقابلة على[`DocumentVisitor`](../../documentvisitor/).

لمزيد من المعلومات راجع نمط تصميم الزائر.

مكالمات [`VisitBodyStart`](../../documentvisitor/visitbodystart/) ، ثم يدعو[`Accept`](../../node/accept/) لجميع العقد الفرعية لقسم والمكالمات[`VisitBodyEnd`](../../documentvisitor/visitbodyend/) في النهاية.

## أمثلة

يوضح كيفية معالجة أحرف علامة التبويب الخاصة بالموضع المطلق باستخدام زائر المستند.

```csharp
public void DocumentToTxt()
{
    Document doc = new Document(MyDir + "Absolute position tab.docx");

    // استخراج محتويات النص من مستندنا عن طريق قبول زائر المستند المخصص هذا.
    DocTextExtractor myDocTextExtractor = new DocTextExtractor();
    Section fisrtSection = doc.FirstSection;
    fisrtSection.Body.Accept(myDocTextExtractor);
    // قم بزيارة بداية نص المستند فقط.
    fisrtSection.Body.AcceptStart(myDocTextExtractor);
    // قم بزيارة نهاية نص المستند فقط.
    fisrtSection.Body.AcceptEnd(myDocTextExtractor);

    // تم تحويل الموضع المطلق لعلامة التبويب، والتي ليس لها معادل في شكل سلسلة، صراحةً إلى حرف علامة تبويب.
    Assert.AreEqual("Before AbsolutePositionTab\tAfter AbsolutePositionTab", myDocTextExtractor.GetText());

    // يمكن لـ AbsolutePositionTab قبول DocumentVisitor أيضًا.
    AbsolutePositionTab absPositionTab = (AbsolutePositionTab)doc.FirstSection.Body.FirstParagraph.GetChild(NodeType.SpecialChar, 0, true);

    myDocTextExtractor = new DocTextExtractor();
    absPositionTab.Accept(myDocTextExtractor);

    Assert.AreEqual("\t", myDocTextExtractor.GetText());
}

/// <summary>
/// يجمع محتوى النص لجميع عمليات التشغيل في المستند الذي تمت زيارته. يستبدل جميع علامات التبويب المطلقة بعلامات تبويب عادية.
/// </summary>
public class DocTextExtractor : DocumentVisitor
{
    public DocTextExtractor()
    {
        mBuilder = new StringBuilder();
    }

    /// <summary>
    /// يتم استدعاؤها عند مواجهة عقدة تشغيل في المستند.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        AppendText(run.Text);
        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها عند مواجهة عقدة AbsolutePositionTab في المستند.
    /// </summary>
    public override VisitorAction VisitAbsolutePositionTab(AbsolutePositionTab tab)
    {
        mBuilder.Append("\t");
        return VisitorAction.Continue;
    }

    /// <summary>
    /// يُضيف نصًا إلى المخرجات الحالية. يُراعي علامة المخرجات المُفعّلة/المعطّلة.
    /// </summary>
    private void AppendText(string text)
    {
        mBuilder.Append(text);
    }

    /// <summary>
    /// نص عادي للمستند الذي جمعه الزائر.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    private readonly StringBuilder mBuilder;
}
```

### أنظر أيضا

* class [DocumentVisitor](../../documentvisitor/)
* class [Body](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
