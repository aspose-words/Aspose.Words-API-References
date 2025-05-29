---
title: Font.ThemeFontFarEast
linktitle: ThemeFontFarEast
articleTitle: ThemeFontFarEast
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie mit Font ThemeFontFarEast ostasiatische Schriftarten in Ihren Designs anpassen können. Werten Sie Ihre Projekte mit einzigartiger, maßgeschneiderter Typografie auf!
type: docs
weight: 510
url: /de/net/aspose.words/font/themefontfareast/
---
## Font.ThemeFontFarEast property

Ruft die Schriftart des ostasiatischen Designs im angewendeten Schriftartenschema ab oder legt sie fest, die mit diesem verknüpft ist.[`Font`](../) Objekt.

```csharp
public ThemeFont ThemeFontFarEast { get; set; }
```

## Beispiele

Zeigt, wie mit Designschriftarten und -farben gearbeitet wird.

```csharp
Document doc = new Document();

// Definieren Sie Schriftarten für die standardmäßig verwendeten Sprachen.
doc.Theme.MinorFonts.Latin = "Algerian";
doc.Theme.MinorFonts.EastAsian = "Aharoni";
doc.Theme.MinorFonts.ComplexScript = "Andalus";

Font font = doc.Styles["Normal"].Font;
Console.WriteLine("Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font.ThemeColor, font.Color);

// Wir können die Schriftart und Farbe des Designs anstelle der Standardwerte verwenden.
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

// Es gibt mehrere Möglichkeiten, Schriftart und Farbe zurückzusetzen.
// 1 – Durch Festlegen von ThemeFont.None/ThemeColor.None:
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

// 2 – Durch Festlegen von Schriftart-/Farbnamen, die nicht zum Design gehören:
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

### Siehe auch

* enum [ThemeFont](../../../aspose.words.themes/themefont/)
* class [Font](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
