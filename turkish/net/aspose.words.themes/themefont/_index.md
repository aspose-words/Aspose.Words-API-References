---
title: ThemeFont Enum
linktitle: ThemeFont
articleTitle: ThemeFont
second_title: .NET için Aspose.Words
description: Belge tema yazı tiplerini kolayca yönetmek ve belgelerinizin görsel çekiciliğini özel stillerle artırmak için Aspose.Words ThemeFont enum'unu keşfedin.
type: docs
weight: 7340
url: /tr/net/aspose.words.themes/themefont/
---
## ThemeFont enumeration

Belge temaları için tema yazı tipi adlarının türlerini belirtir.

```csharp
public enum ThemeFont
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Tema yazı tipi yok. |
| Major | `1` | Ana tema yazı tipi. |
| Minor | `2` | Küçük tema yazı tipi. |

## Notlar

Üst nesne özellikleri içinde tema yazı tipi olarak başvurulabilen bir tema yazı tipi türünü belirtir. Bu tema yazı tipi, belgenin Tema bölümünde bulunan önceden tanımlanmış tema yazı tiplerinden birine başvurudur ve bu, yazı tipi bilgilerinin belgede merkezi olarak ayarlanmasına olanak tanır.

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
