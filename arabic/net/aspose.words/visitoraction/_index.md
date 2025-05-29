---
title: VisitorAction Enum
linktitle: VisitorAction
articleTitle: VisitorAction
second_title: Aspose.Words لـ .NET
description: استكشف Aspose.Words.VisitorAction enum لإدارة تعداد العقد بسهولة، مما يعزز كفاءة معالجة المستندات والتحكم فيها.
type: docs
weight: 7470
url: /ar/net/aspose.words/visitoraction/
---
## VisitorAction enumeration

يسمح للزائر بالتحكم في تعداد العقد.

```csharp
public enum VisitorAction
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Continue | `0` | يطلب الزائر استمرار التعداد. |
| SkipThisNode | `1` | يطلب الزائر تخطي العقدة الحالية ومواصلة التعداد. |
| Stop | `2` | يطلب الزائر إيقاف تعداد العقد. |

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

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
