---
title: ThemeColor Enum
linktitle: ThemeColor
articleTitle: ThemeColor
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words ThemeColor per personalizzare i temi dei documenti con colori vivaci, migliorando l'aspetto visivo e la professionalità dei tuoi documenti.
type: docs
weight: 7320
url: /it/net/aspose.words.themes/themecolor/
---
## ThemeColor enumeration

Specifica i colori del tema per i temi del documento.

Per saperne di più, visita il[Lavorare con stili e temi](https://docs.aspose.com/words/net/working-with-styles-and-themes/) articolo di documentazione.

```csharp
public enum ThemeColor
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | `-1` | Nessun colore. |
| Dark1 | `0` | Colore principale scuro 1. |
| Light1 | `1` | Colore principale chiaro 1. |
| Dark2 | `2` | Colore principale scuro 2. |
| Light2 | `3` | Colore principale chiaro 2. |
| Accent1 | `4` | Colore accento 1. |
| Accent2 | `5` | Colore accento 2. |
| Accent3 | `6` | Colore accento 3. |
| Accent4 | `7` | Colore accento 4. |
| Accent5 | `8` | Colore accento 5. |
| Accent6 | `9` | Colore accento 6. |
| Hyperlink | `10` | Colore del collegamento ipertestuale. |
| FollowedHyperlink | `11` | Colore del collegamento ipertestuale seguito. |
| Text1 | `12` | Colore del testo 1. |
| Text2 | `13` | Colore del testo 2. |
| Background1 | `14` | Colore di sfondo 1. |
| Background2 | `15` | Colore di sfondo 2. |

## Osservazioni

Il colore del tema specificato è un riferimento a uno dei colori del tema predefiniti, situato nella parte Tema del documento , che consente di impostare le informazioni sul colore centralmente nel documento.

## Esempi

Mostra come creare e utilizzare uno stile a tema.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln();

// Crea uno stile con le proprietà del font del tema.
Style style = doc.Styles.Add(StyleType.Paragraph, "ThemedStyle");
style.Font.ThemeFont = ThemeFont.Major;
style.Font.ThemeColor = ThemeColor.Accent5;
style.Font.TintAndShade = 0.3;

builder.ParagraphFormat.StyleName = "ThemedStyle";
builder.Writeln("Text with themed style");
```

Mostra come lavorare con i font e i colori del tema.

```csharp
Document doc = new Document();

// Definisci i font per le lingue utilizzate di default.
doc.Theme.MinorFonts.Latin = "Algerian";
doc.Theme.MinorFonts.EastAsian = "Aharoni";
doc.Theme.MinorFonts.ComplexScript = "Andalus";

Font font = doc.Styles["Normal"].Font;
Console.WriteLine("Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font.ThemeColor, font.Color);

// Possiamo usare il font e il colore del tema invece dei valori predefiniti.
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

// Esistono diversi modi per reimpostare il font e il colore.
// 1 - Impostando ThemeFont.None/ThemeColor.None:
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

// 2 - Impostando nomi di font/colori non tematici:
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

### Guarda anche

* spazio dei nomi [Aspose.Words.Themes](../../aspose.words.themes/)
* assemblea [Aspose.Words](../../)
