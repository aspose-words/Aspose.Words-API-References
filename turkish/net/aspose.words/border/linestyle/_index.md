---
title: Border.LineStyle
linktitle: LineStyle
articleTitle: LineStyle
second_title: .NET için Aspose.Words
description: Border LineStyle özelliğiyle tasarımınızı özelleştirerek, gelişmiş görsel çekicilik için benzersiz kenarlık stilleri kolayca alabilir veya ayarlayabilirsiniz.
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

Eğer çizgi stilini hiçbiri olarak ayarlarsanız, çizgi genişliği otomatik olarak sıfıra değişir.

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

* enum [LineStyle](../../linestyle/)
* class [Border](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
