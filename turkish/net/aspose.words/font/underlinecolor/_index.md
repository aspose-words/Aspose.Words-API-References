---
title: Font.UnderlineColor
linktitle: UnderlineColor
articleTitle: UnderlineColor
second_title: .NET için Aspose.Words
description: Gelişmiş metin stili ve görsel çekicilik için yazı tipinizin alt çizgi rengini kolayca özelleştirmek üzere Font UnderlineColor özelliğini keşfedin.
type: docs
weight: 550
url: /tr/net/aspose.words/font/underlinecolor/
---
## Font.UnderlineColor property

Yazı tipine uygulanan alt çizginin rengini alır veya ayarlar.

```csharp
public Color UnderlineColor { get; set; }
```

## Örnekler

Bir metnin altını çizmenin stilini ve rengini nasıl yapılandıracağınızı gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Underline = Underline.Dotted;
builder.Font.UnderlineColor = Color.Red;

builder.Writeln("Underlined text.");

doc.Save(ArtifactsDir + "Font.Underlines.docx");
```

### Ayrıca bakınız

* class [Font](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
