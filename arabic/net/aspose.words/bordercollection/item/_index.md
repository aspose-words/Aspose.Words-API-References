---
title: BorderCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية BorderCollection Item للوصول بسهولة إلى كائنات Border حسب النوع. بسّط تصميمك مع إدارة فعّالة للحدود!
type: docs
weight: 60
url: /ar/net/aspose.words/bordercollection/item/
---
## BorderCollection indexer (1 of 2)

يسترجع[`Border`](../../border/) الكائن حسب نوع الحدود.

```csharp
public Border this[BorderType borderType] { get; }
```

| معامل | وصف |
| --- | --- |
| borderType | أ[`BorderType`](../../bordertype/) value التي تحدد نوع الحدود التي سيتم استردادها. |

## ملاحظات

لاحظ أنه ليست كل الحدود موجودة لعناصر المستند المختلفة. تطرح هذه الطريقة استثناءً إذا طلبت حدودًا غير قابلة للتطبيق على الكائن الحالي.

## أمثلة

يوضح كيفية تزيين النص باستخدام الحدود والتظليل.

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
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## BorderCollection indexer (2 of 2)

يسترجع[`Border`](../../border/) الكائن حسب index.

```csharp
public Border this[int index] { get; }
```

| معامل | وصف |
| --- | --- |
| index | فهرس الحدود الذي يبدأ من الصفر لاسترجاعه. |

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

* class [Border](../../border/)
* class [BorderCollection](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
