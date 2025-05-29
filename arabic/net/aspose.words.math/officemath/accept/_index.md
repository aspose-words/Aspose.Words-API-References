---
title: OfficeMath.Accept
linktitle: Accept
articleTitle: Accept
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة OfficeMath Accept لإدارة الزوار بسلاسة. حسّن سير عملك من خلال التكامل السهل والكفاءة المُحسّنة!
type: docs
weight: 60
url: /ar/net/aspose.words.math/officemath/accept/
---
## OfficeMath.Accept method

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

مكالمات [`VisitOfficeMathStart`](../../../aspose.words/documentvisitor/visitofficemathstart/) ، ثم يدعو[`Accept`](../../../aspose.words/node/accept/) لجميع العقد الفرعية لبرنامج Office Math والمكالمات[`VisitOfficeMathEnd`](../../../aspose.words/documentvisitor/visitofficemathend/) في النهاية.

## أمثلة

يوضح كيفية طباعة بنية العقدة لكل عقدة رياضيات مكتبية في مستند.

```csharp
public void OfficeMathToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    OfficeMathStructurePrinter visitor = new OfficeMathStructurePrinter();

    // عندما نحصل على عقدة مركبة لقبول زائر مستند، يقوم الزائر بزيارة العقدة المستقبلة،
    // ثم يمر عبر جميع أبناء العقدة بطريقة العمق أولاً.
    //يمكن للزائر قراءة وتعديل كل عقدة تمت زيارتها.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// يجتاز شجرة العقد غير الثنائية المكونة من عقد فرعية.
/// إنشاء خريطة في شكل سلسلة من جميع عقد OfficeMath التي تمت مواجهتها وأطفالها.
/// </summary>
public class OfficeMathStructurePrinter : DocumentVisitor
{
    public OfficeMathStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideOfficeMath = false;
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
        if (mVisitorIsInsideOfficeMath) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها عند مواجهة عقدة OfficeMath في المستند.
    /// </summary>
    public override VisitorAction VisitOfficeMathStart(OfficeMath officeMath)
    {
        IndentAndAppendLine("[OfficeMath start] Math object type: " + officeMath.MathObjectType);
        mDocTraversalDepth++;
        mVisitorIsInsideOfficeMath = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها بعد زيارة جميع العقد الفرعية لعقدة OfficeMath.
    /// </summary>
    public override VisitorAction VisitOfficeMathEnd(OfficeMath officeMath)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[OfficeMath end]");
        mVisitorIsInsideOfficeMath = false;

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

    private bool mVisitorIsInsideOfficeMath;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### أنظر أيضا

* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [OfficeMath](../)
* مساحة الاسم [Aspose.Words.Math](../../../aspose.words.math/)
* المجسم [Aspose.Words](../../../)
