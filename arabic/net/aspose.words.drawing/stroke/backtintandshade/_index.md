---
title: Stroke.BackTintAndShade
linktitle: BackTintAndShade
articleTitle: BackTintAndShade
second_title: Aspose.Words لـ .NET
description: اضبط لون خلفية خطك بسهولة باستخدام Stroke BackTintAndShade. تحكم في السطوع والظلال للحصول على تصميم مثالي.
type: docs
weight: 30
url: /ar/net/aspose.words.drawing/stroke/backtintandshade/
---
## Stroke.BackTintAndShade property

يحصل على أو يعين قيمة مزدوجة لتفتيح أو تعتيم لون خلفية الخط.

```csharp
public double BackTintAndShade { get; set; }
```

## ملاحظات

القيم المسموح بها لهذه الخاصية تتراوح بين -1 (الأغمق) و1 (الأفتح). صفر (0) محايد. محاولة ضبط هذه الخاصية على قيمة أقل من -1 أو أكثر من 1 تؤدي إلى:ArgumentOutOfRangeException.

## أمثلة

يوضح كيفية ضبط لون السمة والصبغة والظل.

```csharp
Document doc = new Document(MyDir + "Stroke gradient outline.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Stroke stroke = shape.Stroke;
stroke.BackThemeColor = ThemeColor.Dark2;
stroke.BackTintAndShade = 0.2d;

doc.Save(ArtifactsDir + "Shape.StrokeBackThemeColors.docx");
```

### أنظر أيضا

* class [Stroke](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
