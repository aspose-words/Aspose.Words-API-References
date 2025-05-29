---
title: Border.Equals
linktitle: Equals
articleTitle: Equals
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة "تساوي الحدود" لمقارنة قيم الحدود بسهولة وتحسين دقة تصميمك. حقق نتائج متسقة دون عناء!
type: docs
weight: 100
url: /ar/net/aspose.words/border/equals/
---
## Equals(*[Border](../)*) {#equals}

يحدد ما إذا كانت الحدود المحددة مساوية في القيمة للحد الحالي.

```csharp
public bool Equals(Border rhs)
```

## أمثلة

يُظهر كيف يمكن لمجموعات الحدود مشاركة العناصر.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Paragraph 1.");
builder.Write("Paragraph 2.");

// نظرًا لأننا استخدمنا نفس تكوين الحدود أثناء الإنشاء
// هذه الفقرات، مجموعات حدودها تشترك في نفس العناصر.
BorderCollection firstParagraphBorders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;
BorderCollection secondParagraphBorders = builder.CurrentParagraph.ParagraphFormat.Borders;
for (int i = 0; i < firstParagraphBorders.Count; i++)
{
    Assert.IsTrue(firstParagraphBorders[i].Equals(secondParagraphBorders[i]));
    Assert.AreEqual(firstParagraphBorders[i].GetHashCode(), secondParagraphBorders[i].GetHashCode());
    Assert.False(firstParagraphBorders[i].IsVisible);
}

foreach (Border border in secondParagraphBorders)
    border.LineStyle = LineStyle.DotDash;

// بعد تغيير نمط خط الحدود في الفقرة الثانية فقط،
// لم تعد مجموعات الحدود تشترك في نفس العناصر.
for (int i = 0; i < firstParagraphBorders.Count; i++)
{
    Assert.IsFalse(firstParagraphBorders[i].Equals(secondParagraphBorders[i]));
    Assert.AreNotEqual(firstParagraphBorders[i].GetHashCode(), secondParagraphBorders[i].GetHashCode());

    // يؤدي تغيير مظهر الحدود الفارغة إلى جعلها مرئية.
    Assert.True(secondParagraphBorders[i].IsVisible);
}

doc.Save(ArtifactsDir + "Border.SharedElements.docx");
```

### أنظر أيضا

* class [Border](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## Equals(*object*) {#equals_1}

يحدد ما إذا كان الكائن المحدد يساوي في القيمة الكائن الحالي.

```csharp
public override bool Equals(object obj)
```

## أمثلة

يُظهر كيف يمكن لمجموعات الحدود مشاركة العناصر.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Paragraph 1.");
builder.Write("Paragraph 2.");

// نظرًا لأننا استخدمنا نفس تكوين الحدود أثناء الإنشاء
// هذه الفقرات، مجموعات حدودها تشترك في نفس العناصر.
BorderCollection firstParagraphBorders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;
BorderCollection secondParagraphBorders = builder.CurrentParagraph.ParagraphFormat.Borders;
for (int i = 0; i < firstParagraphBorders.Count; i++)
{
    Assert.IsTrue(firstParagraphBorders[i].Equals(secondParagraphBorders[i]));
    Assert.AreEqual(firstParagraphBorders[i].GetHashCode(), secondParagraphBorders[i].GetHashCode());
    Assert.False(firstParagraphBorders[i].IsVisible);
}

foreach (Border border in secondParagraphBorders)
    border.LineStyle = LineStyle.DotDash;

// بعد تغيير نمط خط الحدود في الفقرة الثانية فقط،
// لم تعد مجموعات الحدود تشترك في نفس العناصر.
for (int i = 0; i < firstParagraphBorders.Count; i++)
{
    Assert.IsFalse(firstParagraphBorders[i].Equals(secondParagraphBorders[i]));
    Assert.AreNotEqual(firstParagraphBorders[i].GetHashCode(), secondParagraphBorders[i].GetHashCode());

    // يؤدي تغيير مظهر الحدود الفارغة إلى جعلها مرئية.
    Assert.True(secondParagraphBorders[i].IsVisible);
}

doc.Save(ArtifactsDir + "Border.SharedElements.docx");
```

### أنظر أيضا

* class [Border](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
