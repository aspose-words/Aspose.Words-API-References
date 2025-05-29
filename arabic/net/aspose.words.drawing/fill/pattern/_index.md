---
title: Fill.Pattern
linktitle: Pattern
articleTitle: Pattern
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية نمط التعبئة للوصول بسهولة إلى نمط الطباعة وتخصيصه لتصاميمك. حسّن مشاريعك بخيارات تعبئة فريدة!
type: docs
weight: 160
url: /ar/net/aspose.words.drawing/fill/pattern/
---
## Fill.Pattern property

يحصل على[`PatternType`](../../patterntype/) للتعبئة.

```csharp
public PatternType Pattern { get; }
```

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
