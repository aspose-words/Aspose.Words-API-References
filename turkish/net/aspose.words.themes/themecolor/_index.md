---
title: ThemeColor Enum
linktitle: ThemeColor
articleTitle: ThemeColor
second_title: .NET için Aspose.Words
description: Belge temalarınızı canlı renklerle özelleştirmek, belgenizin görsel çekiciliğini ve profesyonelliğini artırmak için Aspose.Words ThemeColor numaralandırmasını keşfedin.
type: docs
weight: 7320
url: /tr/net/aspose.words.themes/themecolor/
---
## ThemeColor enumeration

Belge temaları için tema renklerini belirtir.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Stiller ve Temalarla Çalışma](https://docs.aspose.com/words/net/working-with-styles-and-themes/) belgeleme makalesi.

```csharp
public enum ThemeColor
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `-1` | Renk yok. |
| Dark1 | `0` | Koyu ana renk 1. |
| Light1 | `1` | Açık ana renk 1. |
| Dark2 | `2` | Koyu ana renk 2. |
| Light2 | `3` | Açık ana renk 2. |
| Accent1 | `4` | Vurgu rengi 1. |
| Accent2 | `5` | Vurgu rengi 2. |
| Accent3 | `6` | Vurgu rengi 3. |
| Accent4 | `7` | Vurgu rengi 4. |
| Accent5 | `8` | Vurgu rengi 5. |
| Accent6 | `9` | Vurgu rengi 6. |
| Hyperlink | `10` | Köprü rengi. |
| FollowedHyperlink | `11` | Köprü metni rengini takip etti. |
| Text1 | `12` | Metin rengi 1. |
| Text2 | `13` | Metin rengi 2. |
| Background1 | `14` | Arkaplan rengi 1. |
| Background2 | `15` | Arkaplan rengi 2. |

## Notlar

Belirtilen tema rengi, belgesinin Tema bölümünde bulunan önceden tanımlanmış tema renklerinden birine referanstır ve renk bilgilerinin belgede merkezi olarak ayarlanmasına olanak tanır.

## Örnekler

Temalı stilin nasıl oluşturulacağını ve kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln();

// Tema yazı tipi özellikleriyle biraz stil yaratın.
Style style = doc.Styles.Add(StyleType.Paragraph, "ThemedStyle");
style.Font.ThemeFont = ThemeFont.Major;
style.Font.ThemeColor = ThemeColor.Accent5;
style.Font.TintAndShade = 0.3;

builder.ParagraphFormat.StyleName = "ThemedStyle";
builder.Writeln("Text with themed style");
```

Tema yazı tipleri ve renkleriyle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();

// Varsayılan olarak kullanılan diller için yazı tiplerini tanımla.
doc.Theme.MinorFonts.Latin = "Algerian";
doc.Theme.MinorFonts.EastAsian = "Aharoni";
doc.Theme.MinorFonts.ComplexScript = "Andalus";

Font font = doc.Styles["Normal"].Font;
Console.WriteLine("Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font.ThemeColor, font.Color);

// Varsayılan değerler yerine temanın yazı tipini ve rengini kullanabiliriz.
font.ThemeFont = ThemeFont.Minor;
font.ThemeColor = ThemeColor.Accent2;

Assert.AreEqual(ThemeFont.Minor, font.ThemeFont);
Assert.AreEqual("Algerian", font.Name);

Assert.AreEqual(ThemeFont.Minor, font.ThemeFontAscii);
Assert.AreEqual("Algerian", font.NameAscii);

Assert.AreEqual(ThemeFont.Minor, font.ThemeFontBi);
Assert.AreEqual("Andalus", font.NameBi);

Assert.AreEqual(ThemeFont.Minor, font.ThemeFontFarEast);
Assert.AreEqual("Aharoni", font.NameFarEast);

Assert.AreEqual(ThemeFont.Minor, font.ThemeFontOther);
Assert.AreEqual("Algerian", font.NameOther);

Assert.AreEqual(ThemeColor.Accent2, font.ThemeColor);
Assert.AreEqual(Color.Empty, font.Color);

// Yazı tipini ve rengini sıfırlamanın birkaç yolu vardır.
// 1 - ThemeFont.None/ThemeColor.None ayarlanarak:
font.ThemeFont = ThemeFont.None;
font.ThemeColor = ThemeColor.None;

Assert.AreEqual(ThemeFont.None, font.ThemeFont);
Assert.AreEqual("Algerian", font.Name);

Assert.AreEqual(ThemeFont.None, font.ThemeFontAscii);
Assert.AreEqual("Algerian", font.NameAscii);

Assert.AreEqual(ThemeFont.None, font.ThemeFontBi);
Assert.AreEqual("Andalus", font.NameBi);

Assert.AreEqual(ThemeFont.None, font.ThemeFontFarEast);
Assert.AreEqual("Aharoni", font.NameFarEast);

Assert.AreEqual(ThemeFont.None, font.ThemeFontOther);
Assert.AreEqual("Algerian", font.NameOther);

Assert.AreEqual(ThemeColor.None, font.ThemeColor);
Assert.AreEqual(Color.Empty, font.Color);

// 2 - Tema dışı yazı tipi/renk adlarını ayarlayarak:
font.Name = "Arial";
font.Color = Color.Blue;

Assert.AreEqual(ThemeFont.None, font.ThemeFont);
Assert.AreEqual("Arial", font.Name);

Assert.AreEqual(ThemeFont.None, font.ThemeFontAscii);
Assert.AreEqual("Arial", font.NameAscii);

Assert.AreEqual(ThemeFont.None, font.ThemeFontBi);
Assert.AreEqual("Arial", font.NameBi);

Assert.AreEqual(ThemeFont.None, font.ThemeFontFarEast);
Assert.AreEqual("Arial", font.NameFarEast);

Assert.AreEqual(ThemeFont.None, font.ThemeFontOther);
Assert.AreEqual("Arial", font.NameOther);

Assert.AreEqual(ThemeColor.None, font.ThemeColor);
Assert.AreEqual(Color.Blue.ToArgb(), font.Color.ToArgb());
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Themes](../../aspose.words.themes/)
* toplantı [Aspose.Words](../../)
