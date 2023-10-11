---
title: Enum BorderType
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.BorderType Sıralama. Kenarlığın kenarlarını belirtir.
type: docs
weight: 100
url: /tr/net/aspose.words/bordertype/
---
## BorderType enumeration

Kenarlığın kenarlarını belirtir.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Belgelerle Programlama](https://docs.aspose.com/words/net/programming-with-documents/) dokümantasyon makalesi.

```csharp
public enum BorderType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `-1` | Varsayılan değer. |
| Bottom | `0` | Bir paragrafın veya tablo hücresinin alt kenarlığını belirtir. |
| Left | `1` | Bir paragrafın veya tablo hücresinin sol kenarlığını belirtir. |
| Right | `2` | Bir paragrafın veya tablo hücresinin sağ kenarlığını belirtir. |
| Top | `3` | Bir paragrafın veya tablo hücresinin üst kenarlığını belirtir. |
| Horizontal | `4` | Tablodaki hücreler arasındaki veya uyumlu paragraflar arasındaki yatay kenarlığı belirtir. |
| Vertical | `5` | Tablodaki hücreler arasındaki dikey sınırı belirtir. |
| DiagonalDown | `6` | Bir tablo hücresindeki çapraz kenarlığı belirtir. |
| DiagonalUp | `7` | Bir tablo hücresindeki çapraz kenarlığı belirtir. |

### Örnekler

Üst kenarlığı olan bir paragrafın nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Border topBorder = builder.ParagraphFormat.Borders.Top;
topBorder.LineWidth = 4.0d;
topBorder.LineStyle = LineStyle.DashSmallGap;
// ThemeColor'ı yalnızca LineWidth veya LineStyle ayarlandığında ayarlayın.
topBorder.ThemeColor = ThemeColor.Accent1;
topBorder.TintAndShade = 0.25d;

builder.Writeln("Text with a top border.");

doc.Save(ArtifactsDir + "Border.ParagraphTopBorder.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)


