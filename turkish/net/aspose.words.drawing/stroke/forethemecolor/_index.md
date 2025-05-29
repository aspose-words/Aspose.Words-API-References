---
title: Stroke.ForeThemeColor
linktitle: ForeThemeColor
articleTitle: ForeThemeColor
second_title: .NET için Aspose.Words
description: Stroke ForeThemeColor özelliğiyle vuruşunuzun ön plan rengini zahmetsizce yönetin. Tasarımlarınızı canlı tema renkleriyle özelleştirin!
type: docs
weight: 140
url: /tr/net/aspose.words.drawing/stroke/forethemecolor/
---
## Stroke.ForeThemeColor property

Vuruş ön plan rengini temsil eden bir ThemeColor nesnesi alır veya ayarlar.

```csharp
public ThemeColor ForeThemeColor { get; set; }
```

## Örnekler

Ön tema renginin, tonunun ve gölgesinin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.TextBox, 100, 40);
Stroke stroke = shape.Stroke;
stroke.ForeThemeColor = ThemeColor.Dark1;
stroke.ForeTintAndShade = 0.5;

doc.Save(ArtifactsDir + "Shape.StrokeForeThemeColors.docx");
```

### Ayrıca bakınız

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Stroke](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
