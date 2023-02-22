---
title: Border.LineWidth
second_title: Aspose.Words for .NET API Referansı
description: Border mülk. Kenarlık genişliğini nokta olarak alır veya ayarlar.
type: docs
weight: 50
url: /tr/net/aspose.words/border/linewidth/
---
## Border.LineWidth property

Kenarlık genişliğini nokta olarak alır veya ayarlar.

```csharp
public double LineWidth { get; set; }
```

### Notlar

Çizgi stili yokken çizgi genişliğini sıfırdan büyük ayarlarsanız, çizgi stili is otomatik olarak tek satıra değiştirilir.

### Örnekler

Kenarlıkla çevrili bir dizenin belgeye nasıl ekleneceğini gösterir.

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


