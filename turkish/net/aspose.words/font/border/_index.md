---
title: Font.Border
linktitle: Border
articleTitle: Border
second_title: .NET için Aspose.Words
description: Yazı tipi stilinizi ve tasarım esnekliğinizi geliştirmek için özelleştirilebilir bir Kenarlık nesnesi sağlayan Yazı Tipi Kenarlığı özelliğini keşfedin.
type: docs
weight: 60
url: /tr/net/aspose.words/font/border/
---
## Font.Border property

Bir[`Border`](../../border/) yazı tipi için kenarlığı belirten nesne.

```csharp
public Border Border { get; }
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

* class [Border](../../border/)
* class [Font](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
