---
title: Fill.Patterned
second_title: Aspose.Words لمراجع .NET API
description: Fill طريقة. يضبط التعبئة المحددة على النمط.
type: docs
weight: 230
url: /ar/net/aspose.words.drawing/fill/patterned/
---
## Patterned(PatternType) {#patterned}

يضبط التعبئة المحددة على النمط.

```csharp
public void Patterned(PatternType patternType)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| patternType | PatternType | [`PatternType`](../../patterntype/) |

### أمثلة

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
* مساحة الاسم [Aspose.Words.Drawing](../../fill/)
* المجسم [Aspose.Words](../../../)

---

## Patterned(PatternType, Color, Color) {#patterned_1}

يضبط التعبئة المحددة على النمط.

```csharp
public void Patterned(PatternType patternType, Color foreColor, Color backColor)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| patternType | PatternType | [`PatternType`](../../patterntype/) |
| foreColor | Color | لون تعبئة المقدمة. |
| backColor | Color | لون تعبئة الخلفية. |

### أمثلة

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
* مساحة الاسم [Aspose.Words.Drawing](../../fill/)
* المجسم [Aspose.Words](../../../)


