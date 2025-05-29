---
title: Border.LineWidth
linktitle: LineWidth
articleTitle: LineWidth
second_title: .NET için Aspose.Words
description: Tasarımınızın hassasiyetini ve görsel çekiciliğini artırmak için Kenarlık Çizgi Genişliği özelliğini ayarlayarak kenarlık kalınlığını noktalar halinde özelleştirin.
type: docs
weight: 50
url: /tr/net/aspose.words/border/linewidth/
---
## Border.LineWidth property

Sınır genişliğini noktalar halinde alır veya ayarlar.

```csharp
public double LineWidth { get; set; }
```

## Notlar

Satır stili "hiçbiri" olduğunda satır genişliğini sıfırdan büyük ayarlarsanız, satır stili is otomatik olarak tek satıra dönüşür.

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
