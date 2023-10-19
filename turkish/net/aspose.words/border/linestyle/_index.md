---
title: Border.LineStyle
linktitle: LineStyle
articleTitle: LineStyle
second_title: Aspose.Words for .NET
description: Border LineStyle mülk. Kenarlık stilini alır veya ayarlar C#'da.
type: docs
weight: 40
url: /tr/net/aspose.words/border/linestyle/
---
## Border.LineStyle property

Kenarlık stilini alır veya ayarlar.

```csharp
public LineStyle LineStyle { get; set; }
```

## Notlar

Çizgi stilini yok olarak ayarlarsanız çizgi genişliği otomatik olarak sıfıra değiştirilir.

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

* enum [LineStyle](../../linestyle/)
* class [Border](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
