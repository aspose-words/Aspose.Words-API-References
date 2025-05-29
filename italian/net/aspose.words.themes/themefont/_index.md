---
title: ThemeFont Enum
linktitle: ThemeFont
articleTitle: ThemeFont
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words ThemeFont per gestire facilmente i font dei temi dei documenti e migliorarne l'aspetto visivo con stili personalizzati.
type: docs
weight: 7340
url: /it/net/aspose.words.themes/themefont/
---
## ThemeFont enumeration

Specifica i tipi di nomi di font del tema per i temi dei documenti.

```csharp
public enum ThemeFont
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | `0` | Nessun font del tema. |
| Major | `1` | Carattere tema principale. |
| Minor | `2` | Carattere tematico minore. |

## Osservazioni

Specifica un tipo di font tematico a cui è possibile fare riferimento come font tematico all'interno delle proprietà dell'oggetto padre. Questo font tematico è un riferimento a uno dei font tematici predefiniti, situato nella parte Tema del documento , che consente di impostare le informazioni sul font centralmente nel documento.

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
