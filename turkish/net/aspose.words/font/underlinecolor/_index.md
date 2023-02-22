---
title: Font.UnderlineColor
second_title: Aspose.Words for .NET API Referansı
description: Font mülk. Yazı tipine uygulanan alt çizginin rengini alır veya ayarlar.
type: docs
weight: 540
url: /tr/net/aspose.words/font/underlinecolor/
---
## Font.UnderlineColor property

Yazı tipine uygulanan alt çizginin rengini alır veya ayarlar.

```csharp
public Color UnderlineColor { get; set; }
```

### Örnekler

Metnin altı çizili stilinin ve renginin nasıl yapılandırılacağını gösterir.

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
* ad alanı [Aspose.Words](../../font/)
* toplantı [Aspose.Words](../../../)


