---
title: Footnote.AcceptStart
linktitle: AcceptStart
articleTitle: AcceptStart
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة Footnote AcceptStart، المصممة لتعزيز تفاعل الزائر من خلال توجيه المستخدمين بسلاسة إلى بداية الحاشية السفلية.
type: docs
weight: 100
url: /ar/net/aspose.words.notes/footnote/acceptstart/
---
## Footnote.AcceptStart method

يقبل زائرًا لزيارة بداية الحاشية السفلية.

```csharp
public override VisitorAction AcceptStart(DocumentVisitor visitor)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| visitor | DocumentVisitor | زائر الوثيقة. |

### قيمة الإرجاع

الإجراء الذي يجب على الزائر اتخاذه.

## أمثلة

يوضح كيفية طباعة بنية العقدة لكل حاشية سفلية في مستند.

```csharp
public void FootnoteToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    FootnoteStructurePrinter visitor = new FootnoteStructurePrinter();

    // عندما نحصل على عقدة مركبة لقبول زائر مستند، يقوم الزائر بزيارة العقدة المستقبلة،
    // ثم يمر عبر جميع أبناء العقدة بطريقة العمق أولاً.
    //يمكن للزائر قراءة وتعديل كل عقدة تمت زيارتها.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// يجتاز شجرة العقد غير الثنائية المكونة من عقد فرعية.
/// إنشاء خريطة في شكل سلسلة من جميع عقد الحواشي السفلية التي تم مواجهتها وأطفالها.
/// </summary>
public class FootnoteStructurePrinter : DocumentVisitor
{
    public FootnoteStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideFootnote = false;
    }

    /// <summary>
    /// يحصل على النص العادي للمستند الذي جمعه الزائر.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// يتم استدعاؤها عند مواجهة عقدة الحاشية السفلية في المستند.
    /// </summary>
    public override VisitorAction VisitFootnoteStart(Footnote footnote)
    {
        IndentAndAppendLine("[Footnote start] Type: " + footnote.FootnoteType);
        mDocTraversalDepth++;
        mVisitorIsInsideFootnote = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها بعد زيارة جميع العقد الفرعية لعقدة الحاشية السفلية.
    /// </summary>
    public override VisitorAction VisitFootnoteEnd(Footnote footnote)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Footnote end]");
        mVisitorIsInsideFootnote = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها عند مواجهة عقدة تشغيل في المستند.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideFootnote) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

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

    private bool mVisitorIsInsideFootnote;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### أنظر أيضا

* enum [VisitorAction](../../../aspose.words/visitoraction/)
* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [Footnote](../)
* مساحة الاسم [Aspose.Words.Notes](../../../aspose.words.notes/)
* المجسم [Aspose.Words](../../../)
