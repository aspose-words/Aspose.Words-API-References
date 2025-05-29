---
title: TextEffect Enum
linktitle: TextEffect
articleTitle: TextEffect
second_title: .NET için Aspose.Words
description: Dinamik metin animasyonları için Aspose.Words.TextEffect enum'unu keşfedin. Etkileyici bir kullanıcı deneyimi için belgelerinizi ilgi çekici efektlerle geliştirin.
type: docs
weight: 7270
url: /tr/net/aspose.words/texteffect/
---
## TextEffect enumeration

Metin çalışmaları için animasyon efekti.

```csharp
public enum TextEffect
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` |  |
| LasVegasLights | `1` |  |
| BlinkingBackground | `2` |  |
| SparkleText | `3` |  |
| MarchingBlackAnts | `4` |  |
| MarchingRedAnts | `5` |  |
| Shimmer | `6` |  |

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

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
