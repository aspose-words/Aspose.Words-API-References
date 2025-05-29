---
title: HeaderFooterCollection.ToArray
linktitle: ToArray
articleTitle: ToArray
second_title: Aspose.Words لـ .NET
description: حوّل مجموعة HeaderFooter إلى مصفوفة جديدة بسهولة باستخدام طريقة ToArray. بسّط إدارة بياناتك اليوم!
type: docs
weight: 30
url: /ar/net/aspose.words/headerfootercollection/toarray/
---
## HeaderFooterCollection.ToArray method

نسخ الكل`رأس وتذييل` من المجموعة إلى مجموعة جديدة من`رأس وتذييل` س.

```csharp
public HeaderFooter[] ToArray()
```

### قيمة الإرجاع

مجموعة من`رأس وتذييل`س.

## أمثلة

يوضح كيفية طباعة بنية العقدة لكل رأس وتذييل في المستند.

```csharp
public void HeaderFooterToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    HeaderFooterStructurePrinter visitor = new HeaderFooterStructurePrinter();

    // عندما نحصل على عقدة مركبة لقبول زائر مستند، يقوم الزائر بزيارة العقدة المستقبلة،
    // ثم يمر عبر جميع أبناء العقدة بطريقة العمق أولاً.
    //يمكن للزائر قراءة وتعديل كل عقدة تمت زيارتها.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());

    // الطريقة البديلة للوصول إلى قسم رأس/تذييل المستند قسمًا تلو الآخر هي عن طريق الوصول إلى المجموعة.
    HeaderFooter[] headerFooters = doc.FirstSection.HeadersFooters.ToArray();
    Assert.AreEqual(3, headerFooters.Length);
}

/// <summary>
/// يجتاز شجرة العقد غير الثنائية المكونة من عقد فرعية.
/// إنشاء خريطة في شكل سلسلة من جميع عقد HeaderFooter التي تم مواجهتها وأطفالها.
/// </summary>
public class HeaderFooterStructurePrinter : DocumentVisitor
{
    public HeaderFooterStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideHeaderFooter = false;
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
        if (mVisitorIsInsideHeaderFooter) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها عند مواجهة عقدة HeaderFooter في المستند.
    /// </summary>
    public override VisitorAction VisitHeaderFooterStart(HeaderFooter headerFooter)
    {
        IndentAndAppendLine("[HeaderFooter start] HeaderFooterType: " + headerFooter.HeaderFooterType);
        mDocTraversalDepth++;
        mVisitorIsInsideHeaderFooter = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها بعد زيارة جميع العقد الفرعية لعقدة HeaderFooter.
    /// </summary>
    public override VisitorAction VisitHeaderFooterEnd(HeaderFooter headerFooter)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[HeaderFooter end]");
        mVisitorIsInsideHeaderFooter = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// أضف سطرًا إلى StringBuilder، وقم بتدويره وفقًا لمدى عمق الزائر في شجرة المستند.
    /// </summary>
    /// <اسم المعلمة="نص"></param>
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++) mBuilder.Append("|  ");

        mBuilder.AppendLine(text);
    }

    private bool mVisitorIsInsideHeaderFooter;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### أنظر أيضا

* class [HeaderFooter](../../headerfooter/)
* class [HeaderFooterCollection](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
