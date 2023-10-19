---
title: Font.TextEffect
linktitle: TextEffect
articleTitle: TextEffect
second_title: Aspose.Words for .NET
description: Font TextEffect mülk. Yazı tipi animasyon efektini alır veya ayarlar C#'da.
type: docs
weight: 450
url: /tr/net/aspose.words/font/texteffect/
---
## Font.TextEffect property

Yazı tipi animasyon efektini alır veya ayarlar.

```csharp
public TextEffect TextEffect { get; set; }
```

## Örnekler

Bir koşuya görsel efektin nasıl uygulanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 36;
builder.Font.TextEffect = TextEffect.SparkleText;

builder.Writeln("Text with a sparkle effect.");

// Microsoft Word'ün eski sürümleri yalnızca yazı tipi animasyon efektlerini destekler.
doc.Save(ArtifactsDir + "Font.SparklingText.doc");
```

### Ayrıca bakınız

* enum [TextEffect](../../texteffect/)
* class [Font](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
