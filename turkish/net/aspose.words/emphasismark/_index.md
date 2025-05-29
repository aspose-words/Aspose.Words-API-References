---
title: EmphasisMark Enum
linktitle: EmphasisMark
articleTitle: EmphasisMark
second_title: .NET için Aspose.Words
description: Belgenizin biçimlendirmesini geliştirmek için çeşitli vurgulama türleri sunan Aspose.Words.EmphasisMark enum'unu keşfedin. Metninizin etkisini bugün yükseltin!
type: docs
weight: 1870
url: /tr/net/aspose.words/emphasismark/
---
## EmphasisMark enumeration

Olası vurgu işareti türlerini belirtir.

```csharp
public enum EmphasisMark
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Vurgu işareti yok. |
| OverSolidCircle | `1` | Vurgu işareti metnin üstünde gösterilen dolu siyah dairedir. |
| OverComma | `2` | Vurgu işareti metnin üstünde gösterilen bir virgül karakteridir. |
| OverWhiteCircle | `3` | Vurgu işareti metnin üstünde gösterilen boş beyaz dairedir. |
| UnderSolidCircle | `4` | Vurgu işareti metnin altında gösterilen dolu siyah dairedir. |

## Örnekler

Glif karakterinin üstüne/altına ek karakterin nasıl ekleneceğini gösterir.

```csharp
DocumentBuilder builder = new DocumentBuilder();

// Vurgu işaretlerinin olası türleri:
// https://apireference.aspose.com/words/net/aspose.words/emphasismark
builder.Font.EmphasisMark = emphasisMark; 

builder.Write("Emphasis text");
builder.Writeln();
builder.Font.ClearFormatting();
builder.Write("Simple text");

builder.Document.Save(ArtifactsDir + "Fonts.SetEmphasisMark.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
