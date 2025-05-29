---
title: Fill.Patterned
linktitle: Patterned
articleTitle: Patterned
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة Fill Patterned لتطبيق أنماط فريدة على تصميماتك بسهولة، مما يعزز الإبداع والجاذبية البصرية في مشاريعك.
type: docs
weight: 230
url: /ar/net/aspose.words.drawing/fill/patterned/
---
## Patterned(*[PatternType](../../patterntype/)*) {#patterned}

يضبط التعبئة المحددة إلى نمط.

```csharp
public void Patterned(PatternType patternType)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| patternType | PatternType | [`PatternType`](../../patterntype/) |

## أمثلة

يوضح كيفية تعيين نمط لشكل ما.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Fill fill = shape.Fill;

Console.WriteLine("Pattern value is: {0}", fill.Pattern);

// هناك عدة طرق محددة لتعبئة النمط.
// 1 - تطبيق النمط على تعبئة الشكل:
fill.Patterned(PatternType.DiagonalBrick);

// 2 - تطبيق النمط بألوان المقدمة والخلفية على تعبئة الشكل:
fill.Patterned(PatternType.DiagonalBrick, Color.Aqua, Color.Bisque);

doc.Save(ArtifactsDir + "Shape.FillPattern.docx");
```

### أنظر أيضا

* enum [PatternType](../../patterntype/)
* class [Fill](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)

---

## Patterned(*[PatternType](../../patterntype/), Color, Color*) {#patterned_1}

يضبط التعبئة المحددة إلى نمط.

```csharp
public void Patterned(PatternType patternType, Color foreColor, Color backColor)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| patternType | PatternType | [`PatternType`](../../patterntype/) |
| foreColor | Color | لون تعبئة المقدمة. |
| backColor | Color | لون تعبئة الخلفية. |

## أمثلة

يوضح كيفية تعيين نمط لشكل ما.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Fill fill = shape.Fill;

Console.WriteLine("Pattern value is: {0}", fill.Pattern);

// هناك عدة طرق محددة لتعبئة النمط.
// 1 - تطبيق النمط على تعبئة الشكل:
fill.Patterned(PatternType.DiagonalBrick);

// 2 - تطبيق النمط بألوان المقدمة والخلفية على تعبئة الشكل:
fill.Patterned(PatternType.DiagonalBrick, Color.Aqua, Color.Bisque);

doc.Save(ArtifactsDir + "Shape.FillPattern.docx");
```

### أنظر أيضا

* enum [PatternType](../../patterntype/)
* class [Fill](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
