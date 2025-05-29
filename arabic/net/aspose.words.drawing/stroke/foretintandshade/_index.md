---
title: Stroke.ForeTintAndShade
linktitle: ForeTintAndShade
articleTitle: ForeTintAndShade
second_title: Aspose.Words لـ .NET
description: قم بضبط خاصية Stroke ForeTintAndShade لتفتيح أو تعتيم لون المقدمة في ضربتك بسهولة لتحسين التأثير البصري.
type: docs
weight: 150
url: /ar/net/aspose.words.drawing/stroke/foretintandshade/
---
## Stroke.ForeTintAndShade property

يحصل على أو يعين قيمة مزدوجة لتفتيح أو تغميق لون مقدمة الخط.

```csharp
public double ForeTintAndShade { get; set; }
```

## ملاحظات

القيم المسموح بها لهذه الخاصية تتراوح بين -1 (الأغمق) و1 (الأفتح). صفر (0) محايد. محاولة ضبط هذه الخاصية على قيمة أقل من -1 أو أكثر من 1 تؤدي إلى:ArgumentOutOfRangeException.

## أمثلة

يوضح كيفية تعيين لون السمة والصبغة والظل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.TextBox, 100, 40);
Stroke stroke = shape.Stroke;
stroke.ForeThemeColor = ThemeColor.Dark1;
stroke.ForeTintAndShade = 0.5;

doc.Save(ArtifactsDir + "Shape.StrokeForeThemeColors.docx");
```

### أنظر أيضا

* class [Stroke](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
