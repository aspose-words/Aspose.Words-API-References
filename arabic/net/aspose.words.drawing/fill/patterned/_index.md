---
title: Fill.Patterned
linktitle: Patterned
articleTitle: Patterned
second_title: Aspose.Words لـ .NET
description: Fill Patterned طريقة. يضبط التعبئة المحددة على النمط في C#.
type: docs
weight: 220
url: /ar/net/aspose.words.drawing/fill/patterned/
---
## Patterned(*[PatternType](../../patterntype/)*) {#patterned}

يضبط التعبئة المحددة على النمط.

```csharp
public void Patterned(PatternType patternType)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| patternType | PatternType | [`PatternType`](../../patterntype/) |

## أمثلة

يوضح كيفية تعيين نمط للشكل.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Fill fill = shape.Fill;

Console.WriteLine("Pattern value is: {0}", fill.Pattern);

// هناك عدة طرق محددة لملء النمط.
// 1 - تطبيق النمط على تعبئة الشكل:
fill.Patterned(PatternType.DiagonalBrick);

// 2 - قم بتطبيق النمط بألوان المقدمة والخلفية على تعبئة الشكل:
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

يضبط التعبئة المحددة على النمط.

```csharp
public void Patterned(PatternType patternType, Color foreColor, Color backColor)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| patternType | PatternType | [`PatternType`](../../patterntype/) |
| foreColor | Color | لون تعبئة المقدمة. |
| backColor | Color | لون تعبئة الخلفية. |

## أمثلة

يوضح كيفية تعيين نمط للشكل.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Fill fill = shape.Fill;

Console.WriteLine("Pattern value is: {0}", fill.Pattern);

// هناك عدة طرق محددة لملء النمط.
// 1 - تطبيق النمط على تعبئة الشكل:
fill.Patterned(PatternType.DiagonalBrick);

// 2 - قم بتطبيق النمط بألوان المقدمة والخلفية على تعبئة الشكل:
fill.Patterned(PatternType.DiagonalBrick, Color.Aqua, Color.Bisque);

doc.Save(ArtifactsDir + "Shape.FillPattern.docx");
```

### أنظر أيضا

* enum [PatternType](../../patterntype/)
* class [Fill](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
