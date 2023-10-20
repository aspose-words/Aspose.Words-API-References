---
title: Font.Border
linktitle: Border
articleTitle: Border
second_title: Aspose.Words for .NET
description: Font Border mülk. Bir değeri döndürürBorder yazı tipinin kenarlığını belirten nesne C#'da.
type: docs
weight: 60
url: /tr/net/aspose.words/font/border/
---
## Font.Border property

Bir değeri döndürür[`Border`](../../border/) yazı tipinin kenarlığını belirten nesne.

```csharp
public Border Border { get; }
```

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

* class [Border](../../border/)
* class [Font](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
