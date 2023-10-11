---
title: Border.Color
second_title: Aspose.Words for .NET API Referansı
description: Border mülk. Kenarlık rengini alır veya ayarlar.
type: docs
weight: 10
url: /tr/net/aspose.words/border/color/
---
## Border.Color property

Kenarlık rengini alır veya ayarlar.

```csharp
public Color Color { get; set; }
```

### Örnekler

Kenarlıkla çevrelenmiş bir dizenin belgeye nasıl ekleneceğini gösterir.

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
* ad alanı [Aspose.Words](../../border/)
* toplantı [Aspose.Words](../../../)


