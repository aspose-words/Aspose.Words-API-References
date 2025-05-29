---
title: Border.Color
linktitle: Color
articleTitle: Color
second_title: .NET için Aspose.Words
description: Çarpıcı bir görsel etki için kenarlık renklerini ayarlamanıza ve değiştirmenize olanak tanıyan Kenarlık Rengi özelliğiyle tasarımlarınızı zahmetsizce özelleştirin.
type: docs
weight: 10
url: /tr/net/aspose.words/border/color/
---
## Border.Color property

Sınır rengini alır veya ayarlar.

```csharp
public Color Color { get; set; }
```

## Örnekler

Bir belgeye kenarlıkla çevrili bir dizenin nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Write("Text surrounded by green border.");

doc.Save(ArtifactsDir + "Border.FontBorder.docx");
```

### Ayrıca bakınız

* class [Border](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
