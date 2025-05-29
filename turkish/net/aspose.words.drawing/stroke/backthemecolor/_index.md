---
title: Stroke.BackThemeColor
linktitle: BackThemeColor
articleTitle: BackThemeColor
second_title: .NET için Aspose.Words
description: Stroke BackThemeColor özelliğiyle tasarımınızı özelleştirin. Görsel çekiciliği artırmak için vuruş arka planınız için kolayca bir ThemeColor ayarlayın.
type: docs
weight: 20
url: /tr/net/aspose.words.drawing/stroke/backthemecolor/
---
## Stroke.BackThemeColor property

Kontur arka plan rengini temsil eden bir ThemeColor nesnesi alır veya ayarlar.

```csharp
public ThemeColor BackThemeColor { get; set; }
```

## Örnekler

Tema renginin, tonunun ve gölgesinin nasıl geri ayarlanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Stroke gradient outline.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Stroke stroke = shape.Stroke;
stroke.BackThemeColor = ThemeColor.Dark2;
stroke.BackTintAndShade = 0.2d;

doc.Save(ArtifactsDir + "Shape.StrokeBackThemeColors.docx");
```

### Ayrıca bakınız

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Stroke](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
