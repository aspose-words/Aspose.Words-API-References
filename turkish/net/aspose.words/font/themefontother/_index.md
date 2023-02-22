---
title: Font.ThemeFontOther
second_title: Aspose.Words for .NET API Referansı
description: Font mülk. Bu Font nesnesiyle ilişkilendirilmiş uygulanan font şemasında 128  255 arasında karakter kodlarına sahip karakterler için kullanılan tema fontunu alır veya ayarlar.
type: docs
weight: 510
url: /tr/net/aspose.words/font/themefontother/
---
## Font.ThemeFontOther property

Bu Font nesnesiyle ilişkilendirilmiş uygulanan font şemasında 128 - 255 arasında karakter kodlarına sahip karakterler için kullanılan tema fontunu alır veya ayarlar.

```csharp
public ThemeFont ThemeFontOther { get; set; }
```

### Örnekler

Tema yazı tipleri ve renkleri ile nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();

// Varsayılan olarak kullanılan diller için yazı tiplerini tanımlayın.
doc.Theme.MinorFonts.Latin = "Algerian";
doc.Theme.MinorFonts.EastAsian = "Aharoni";
doc.Theme.MinorFonts.ComplexScript = "Andalus";

Font font = doc.Styles["Normal"].Font;
Console.WriteLine("Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font.ThemeColor, font.Color);

// Varsayılan değerler yerine tema yazı tipi ve rengini kullanabiliriz.
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
// 1 - ThemeFont.None/ThemeColor.None ayarını yaparak:
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

// 2 - Tema dışı yazı tipi/renk adları ayarlayarak:
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

* enum [ThemeFont](../../../aspose.words.themes/themefont/)
* class [Font](../)
* ad alanı [Aspose.Words](../../font/)
* toplantı [Aspose.Words](../../../)


