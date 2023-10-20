---
title: StructuredDocumentTag.Accept
linktitle: Accept
articleTitle: Accept
second_title: Aspose.Words لـ .NET
description: StructuredDocumentTag Accept طريقة. يقبل الزائر في C#.
type: docs
weight: 330
url: /ar/net/aspose.words.markup/structureddocumenttag/accept/
---
## StructuredDocumentTag.Accept method

يقبل الزائر.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| visitor | DocumentVisitor | الزائر الذي سيزور العقد. |

### قيمة الإرجاع

صحيح إذا تمت زيارة جميع العقد؛ كاذبة إذا[`DocumentVisitor`](../../../aspose.words/documentvisitor/) أوقفت العملية قبل زيارة كافة العقد.

## ملاحظات

يعدد هذه العقدة وجميع أبنائها. تستدعي كل عقدة الطريقة المقابلة لها[`DocumentVisitor`](../../../aspose.words/documentvisitor/).

لمزيد من المعلومات، راجع نمط تصميم الزائر.

المكالمات[`VisitStructuredDocumentTagStart`](../../../aspose.words/documentvisitor/visitstructureddocumenttagstart/) ، ثم يتصل[`Accept`](../../../aspose.words/node/accept/) لجميع العقد الفرعية للعلامة الذكية والمكالمات[`VisitStructuredDocumentTagEnd`](../../../aspose.words/documentvisitor/visitstructureddocumenttagend/) في النهاية.

## أمثلة

يوضح كيفية طباعة بنية العقدة لكل علامة مستند منظمة في المستند.

```csharp
public void StructuredDocumentTagToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    StructuredDocumentTagNodePrinter visitor = new StructuredDocumentTagNodePrinter();

    // عندما نحصل على عقدة مركبة لقبول زائر المستند، يقوم الزائر بزيارة العقدة المقبولة،
    // ثم يجتاز جميع أبناء العقدة بطريقة العمق الأول.
    // يمكن للزائر قراءة وتعديل كل عقدة تمت زيارتها.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// يجتاز الشجرة غير الثنائية للعقدة التابعة.
/// ينشئ خريطة في شكل سلسلة من جميع العقد StructuredDocumentTag التي تمت مواجهتها وأبناءها.
/// </summary>
public class StructuredDocumentTagNodePrinter : DocumentVisitor
{
    public StructuredDocumentTagNodePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideStructuredDocumentTag = false;
    }

    /// <summary>
    /// يحصل على النص العادي للمستند الذي قام الزائر بتجميعه.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// يتم الاتصال به عند مواجهة عقدة التشغيل في المستند.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideStructuredDocumentTag) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤه عند مواجهة عقدة StructuredDocumentTag في المستند.
    /// </summary>
    public override VisitorAction VisitStructuredDocumentTagStart(StructuredDocumentTag sdt)
    {
        IndentAndAppendLine("[StructuredDocumentTag start] Title: " + sdt.Title);
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم الاتصال به بعد زيارة جميع العقد التابعة لعقدة StructuredDocumentTag.
    /// </summary>
    public override VisitorAction VisitStructuredDocumentTagEnd(StructuredDocumentTag sdt)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[StructuredDocumentTag end]");

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
