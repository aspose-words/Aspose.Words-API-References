---
title: Footnote.Accept
second_title: Aspose.Words لمراجع .NET API
description: Footnote طريقة. يقبل الزائر.
type: docs
weight: 70
url: /ar/net/aspose.words.notes/footnote/accept/
---
## Footnote.Accept method

يقبل الزائر.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| visitor | DocumentVisitor | الزائر الذي سيزور العقد. |

### قيمة الإرجاع

صحيح إذا تمت زيارة جميع العقد؛ كاذبة إذا[`DocumentVisitor`](../../../aspose.words/documentvisitor/) أوقفت العملية قبل زيارة كافة العقد.

### ملاحظات

يعدد هذه العقدة وجميع أبنائها. تستدعي كل عقدة الطريقة المقابلة لها[`DocumentVisitor`](../../../aspose.words/documentvisitor/).

لمزيد من المعلومات، راجع نمط تصميم الزائر.

يستدعي DocumentVisitor.VisitFootnoteStart، ثم يستدعي قبول لكافة العقد التابعة للحاشية السفلية ويستدعي DocumentVisitor.VisitFootnoteEnd في النهاية.

### أمثلة

يوضح كيفية طباعة بنية العقدة لكل حاشية سفلية في المستند.

```csharp
public void FootnoteToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    FootnoteStructurePrinter visitor = new FootnoteStructurePrinter();

    // عندما نحصل على عقدة مركبة لقبول زائر المستند، يقوم الزائر بزيارة العقدة المقبولة،
    // ثم يجتاز جميع أبناء العقدة بطريقة العمق الأول.
    // يمكن للزائر قراءة وتعديل كل عقدة تمت زيارتها.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// يجتاز الشجرة غير الثنائية للعقدة التابعة.
/// ينشئ خريطة على شكل سلسلة تحتوي على جميع عقد الحواشي السفلية وأبناءها.
/// </summary>
public class FootnoteStructurePrinter : DocumentVisitor
{
    public FootnoteStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideFootnote = false;
    }

    /// <summary>
    /// يحصل على النص العادي للمستند الذي قام الزائر بتجميعه.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// يتم استدعاؤه عند مواجهة عقدة حاشية سفلية في المستند.
    /// </summary>
    public override VisitorAction VisitFootnoteStart(Footnote footnote)
    {
        IndentAndAppendLine("[Footnote start] Type: " + footnote.FootnoteType);
        mDocTraversalDepth++;
        mVisitorIsInsideFootnote = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم الاتصال به بعد زيارة جميع العقد التابعة لعقدة الحاشية السفلية.
    /// </summary>
    public override VisitorAction VisitFootnoteEnd(Footnote footnote)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Footnote end]");
        mVisitorIsInsideFootnote = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم الاتصال به عند مواجهة عقدة التشغيل في المستند.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideFootnote) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// ألحق سطرًا بـ StringBuilder وقم بوضع مسافة بادئة له اعتمادًا على مدى عمق الزائر في شجرة المستندات.
    /// </summary>
    /// <param name="text"></param>
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

* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [Footnote](../)
* مساحة الاسم [Aspose.Words.Notes](../../footnote/)
* المجسم [Aspose.Words](../../../)


