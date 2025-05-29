---
title: StructuredDocumentTag.Accept
linktitle: Accept
articleTitle: Accept
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة قبول StructuredDocumentTag—دمج تفاعلات الزائر بسلاسة لتحسين وظائف المستند وإشراك المستخدم.
type: docs
weight: 330
url: /ar/net/aspose.words.markup/structureddocumenttag/accept/
---
## StructuredDocumentTag.Accept method

يقبل زائرًا.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| visitor | DocumentVisitor | الزائر الذي سيقوم بزيارة العقد. |

### قيمة الإرجاع

صحيح إذا تمت زيارة جميع العقد؛ خطأ إذا[`DocumentVisitor`](../../../aspose.words/documentvisitor/) تم إيقاف العملية قبل زيارة كافة العقد.

## ملاحظات

يُحصي هذه العقدة وجميع أبنائها. تستدعي كل عقدة طريقة مقابلة على[`DocumentVisitor`](../../../aspose.words/documentvisitor/).

لمزيد من المعلومات راجع نمط تصميم الزائر.

مكالمات [`VisitStructuredDocumentTagStart`](../../../aspose.words/documentvisitor/visitstructureddocumenttagstart/) ، ثم يدعو[`Accept`](../../../aspose.words/node/accept/) لجميع العقد الفرعية x000d_ للعلامة الذكية والمكالمات[`VisitStructuredDocumentTagEnd`](../../../aspose.words/documentvisitor/visitstructureddocumenttagend/) في النهاية.

## أمثلة

يوضح كيفية طباعة بنية العقدة لكل علامة مستند منظمة في مستند.

```csharp
public void StructuredDocumentTagToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    StructuredDocumentTagNodePrinter visitor = new StructuredDocumentTagNodePrinter();

    // عندما نحصل على عقدة مركبة لقبول زائر مستند، يقوم الزائر بزيارة العقدة المستقبلة،
    // ثم يمر عبر جميع أبناء العقدة بطريقة العمق أولاً.
    //يمكن للزائر قراءة وتعديل كل عقدة تمت زيارتها.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// يجتاز شجرة العقد غير الثنائية المكونة من عقد فرعية.
/// إنشاء خريطة في شكل سلسلة من جميع عقد StructuredDocumentTag التي تم مواجهتها وأطفالها.
/// </summary>
public class StructuredDocumentTagNodePrinter : DocumentVisitor
{
    public StructuredDocumentTagNodePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideStructuredDocumentTag = false;
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
        if (mVisitorIsInsideStructuredDocumentTag) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها عند مواجهة عقدة StructuredDocumentTag في المستند.
    /// </summary>
    public override VisitorAction VisitStructuredDocumentTagStart(StructuredDocumentTag sdt)
    {
        IndentAndAppendLine("[StructuredDocumentTag start] Title: " + sdt.Title);
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها بعد زيارة جميع العقد الفرعية لعقدة StructuredDocumentTag.
    /// </summary>
    public override VisitorAction VisitStructuredDocumentTagEnd(StructuredDocumentTag sdt)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[StructuredDocumentTag end]");

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

    private readonly bool mVisitorIsInsideStructuredDocumentTag;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### أنظر أيضا

* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [StructuredDocumentTag](../)
* مساحة الاسم [Aspose.Words.Markup](../../../aspose.words.markup/)
* المجسم [Aspose.Words](../../../)
