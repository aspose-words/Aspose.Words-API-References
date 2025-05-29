---
title: Font.TextEffect
linktitle: TextEffect
articleTitle: TextEffect
second_title: .NET için Aspose.Words
description: Font TextEffect özelliğini kullanarak font animasyonlarını kolayca özelleştirebilir, tasarımlarınızı dinamik metin efektleriyle zenginleştirerek etkileyici bir kullanıcı deneyimi yaşayabilirsiniz.
type: docs
weight: 460
url: /tr/net/aspose.words/font/texteffect/
---
## Font.TextEffect property

Yazı tipi animasyon efektini alır veya ayarlar.

```csharp
public TextEffect TextEffect { get; set; }
```

## Örnekler

Koşuya görsel efektin nasıl uygulanacağını gösterir.

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
