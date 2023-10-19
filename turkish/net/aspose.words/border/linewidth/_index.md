---
title: Border.LineWidth
linktitle: LineWidth
articleTitle: LineWidth
second_title: Aspose.Words for .NET
description: Border LineWidth mülk. Kenarlık genişliğini nokta cinsinden alır veya ayarlar C#'da.
type: docs
weight: 50
url: /tr/net/aspose.words/border/linewidth/
---
## Border.LineWidth property

Kenarlık genişliğini nokta cinsinden alır veya ayarlar.

```csharp
public double LineWidth { get; set; }
```

## Notlar

Çizgi stili yokken çizgi genişliğini sıfırdan büyük ayarlarsanız çizgi stili is otomatik olarak tek satıra değiştirilir.

## Örnekler

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
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
