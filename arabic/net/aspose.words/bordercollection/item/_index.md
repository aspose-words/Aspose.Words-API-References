---
title: BorderCollection.Item
second_title: Aspose.Words لمراجع .NET API
description: BorderCollection ملكية. يسترد أBorder الكائن حسب نوع الحدود.
type: docs
weight: 60
url: /ar/net/aspose.words/bordercollection/item/
---
## BorderCollection indexer (1 of 2)

يسترد أ[`Border`](../../border/) الكائن حسب نوع الحدود.

```csharp
public Border this[BorderType borderType] { get; }
```

| معامل | وصف |
| --- | --- |
| borderType | أ[`BorderType`](../../bordertype/) value الذي يحدد نوع الحد المطلوب استرداده. |

### ملاحظات

لاحظ أنه ليست كل الحدود موجودة لعناصر وثيقة مختلفة. تطرح هذه الطريقة استثناءً إذا طلبت حدًا لا ينطبق على الكائن الحالي.

### أمثلة

يوضح كيفية تزيين النص بالحدود والتظليل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

BorderCollection borders = builder.ParagraphFormat.Borders;
borders.DistanceFromText = 20;
borders[BorderType.Left].LineStyle = LineStyle.Double;
borders[BorderType.Right].LineStyle = LineStyle.Double;
borders[BorderType.Top].LineStyle = LineStyle.Double;
borders[BorderType.Bottom].LineStyle = LineStyle.Double;

Shading shading = builder.ParagraphFormat.Shading;
shading.Texture = TextureIndex.TextureDiagonalCross;
shading.BackgroundPatternColor = Color.LightCoral;
shading.ForegroundPatternColor = Color.LightSalmon;

builder.Write("This paragraph is formatted with a double border and shading.");
doc.Save(ArtifactsDir + "DocumentBuilder.ApplyBordersAndShading.docx");
```

### أنظر أيضا

* class [Border](../../border/)
* enum [BorderType](../../bordertype/)
* class [BorderCollection](../)
* مساحة الاسم [Aspose.Words](../../bordercollection/)
* المجسم [Aspose.Words](../../../)

---

## BorderCollection indexer (2 of 2)

يسترد أ[`Border`](../../border/) كائن حسب الفهرس.

```csharp
public Border this[int index] { get; }
```

| معامل | وصف |
| --- | --- |
| index | الفهرس القائم على الصفر من الحدود لاسترداد. |

### أمثلة

يوضح كيف يمكن لمجموعات الحدود مشاركة العناصر.

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

    // تغيير مظهر الحدود الفارغة يجعلها مرئية.
    Assert.True(secondParagraphBorders[i].IsVisible);
}

doc.Save(ArtifactsDir + "Border.SharedElements.docx");
```

### أنظر أيضا

* class [Border](../../border/)
* class [BorderCollection](../)
* مساحة الاسم [Aspose.Words](../../bordercollection/)
* المجسم [Aspose.Words](../../../)


