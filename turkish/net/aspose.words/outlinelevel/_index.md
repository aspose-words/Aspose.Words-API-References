---
title: OutlineLevel Enum
linktitle: OutlineLevel
articleTitle: OutlineLevel
second_title: .NET için Aspose.Words
description: Belgelerinizdeki paragraf anahat düzeylerini gelişmiş organizasyon ve netlik için kolayca yönetmek üzere Aspose.Words.OutlineLevel enum'unu keşfedin.
type: docs
weight: 5060
url: /tr/net/aspose.words/outlinelevel/
---
## OutlineLevel enumeration

Belgedeki bir paragrafın ana hat düzeyini belirtir.

```csharp
public enum OutlineLevel
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Level1 | `0` | Paragraf anahat seviyesi 1'de (en üst seviye). |
| Level2 | `1` | Paragraf ana hat seviyesi 2'dedir. |
| Level3 | `2` | Paragraf ana hat düzeyi 3'tedir. |
| Level4 | `3` | Paragraf ana hat düzeyinde 4. |
| Level5 | `4` | Paragraf ana hat düzeyinde 5. |
| Level6 | `5` | Paragraf ana hat düzeyinde 6. |
| Level7 | `6` | Paragraf ana hat düzeyinde 7. |
| Level8 | `7` | Paragraf ana hat düzeyinde 8. |
| Level9 | `8` | Paragraf ana hat düzeyinde 9. |
| BodyText | `9` | Paragraf ana metin düzeyindedir. |

## Örnekler

Daraltılabilir metin oluşturmak için paragraf anahat düzeylerinin nasıl yapılandırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Her paragrafın bir OutlineLevel değeri vardır. Bu değer 1 ile 9 arasında herhangi bir sayı veya varsayılan "BodyText" değeri olabilir.
// Özelliği numaralandırılmış değerlerden birine ayarlamak sola doğru bir ok gösterecektir
// paragrafın başlangıcı.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level1;
builder.Writeln("Paragraph outline level 1.");

// Seviye 1 en üst seviyedir. Daha yüksek seviyedeki bir paragrafın altında daha düşük seviyedeki bir paragraf varsa,
// üst düzey paragrafı daraltmak alt düzey paragrafı da daraltacaktır.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level2;
builder.Writeln("Paragraph outline level 2.");

// Aynı seviyedeki iki paragraf birbirini daraltmaz,
// ve oklar işaret ettikleri paragrafları daraltmaz.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level3;
builder.Writeln("Paragraph outline level 3.");
builder.Writeln("Paragraph outline level 3.");

// Varsayılan "BodyText" değeri, herhangi bir düzeydeki bir paragrafın daraltabileceği en düşük değerdir.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.BodyText;
builder.Writeln("Paragraph at main text level.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphOutlineLevel.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
