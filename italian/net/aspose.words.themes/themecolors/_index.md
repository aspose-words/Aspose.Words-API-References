---
title: ThemeColors Class
linktitle: ThemeColors
articleTitle: ThemeColors
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.ThemeColors, caratterizzata da una versatile combinazione di 12 colori per migliorare l'aspetto visivo e la coerenza del tuo documento.
type: docs
weight: 7330
url: /it/net/aspose.words.themes/themecolors/
---
## ThemeColors class

Rappresenta lo schema dei colori del tema del documento che contiene dodici colori.

`ThemeColors` L'oggetto contiene sei colori di accento, due colori scuri, due colori chiari e un colore per ciascuno dei collegamenti ipertestuali e dei collegamenti ipertestuali seguiti.

```csharp
public class ThemeColors
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Accent1](../../aspose.words.themes/themecolors/accent1/) { get; set; } | Specifica il colore Accento 1. |
| [Accent2](../../aspose.words.themes/themecolors/accent2/) { get; set; } | Specifica il colore Accento 2. |
| [Accent3](../../aspose.words.themes/themecolors/accent3/) { get; set; } | Specifica il colore Accento 3. |
| [Accent4](../../aspose.words.themes/themecolors/accent4/) { get; set; } | Specifica il colore Accento 4. |
| [Accent5](../../aspose.words.themes/themecolors/accent5/) { get; set; } | Specifica il colore Accento 5. |
| [Accent6](../../aspose.words.themes/themecolors/accent6/) { get; set; } | Specifica il colore Accento 6. |
| [Dark1](../../aspose.words.themes/themecolors/dark1/) { get; set; } | Specifica il colore Scuro 1. |
| [Dark2](../../aspose.words.themes/themecolors/dark2/) { get; set; } | Specifica il colore Scuro 2. |
| [FollowedHyperlink](../../aspose.words.themes/themecolors/followedhyperlink/) { get; set; } | Specifica il colore per un collegamento ipertestuale cliccato. |
| [Hyperlink](../../aspose.words.themes/themecolors/hyperlink/) { get; set; } | Specifica il colore per un collegamento ipertestuale. |
| [Light1](../../aspose.words.themes/themecolors/light1/) { get; set; } | Specifica il colore Luce 1. |
| [Light2](../../aspose.words.themes/themecolors/light2/) { get; set; } | Specifica il colore Luce 2. |

## Esempi

Mostra come impostare colori e caratteri personalizzati per i temi.

```csharp
Document doc = new Document(MyDir + "Theme colors.docx");

// L'oggetto "Theme" ci dà accesso al tema del documento, una fonte di font e colori predefiniti.
Theme theme = doc.Theme;

// Alcuni stili, come "Titolo 1" e "Sottotitolo", erediteranno questi font.
theme.MajorFonts.Latin = "Courier New";
theme.MinorFonts.Latin = "Agency FB";

// Anche altre lingue potrebbero avere i loro font personalizzati in questo tema.
Assert.AreEqual(string.Empty, theme.MajorFonts.ComplexScript);
Assert.AreEqual(string.Empty, theme.MajorFonts.EastAsian);
Assert.AreEqual(string.Empty, theme.MinorFonts.ComplexScript);
Assert.AreEqual(string.Empty, theme.MinorFonts.EastAsian);

// La proprietà "Colori" contiene la tavolozza dei colori di Microsoft Word,
// che appare quando si cambia l'ombreggiatura o il colore del carattere.
// Applica colori personalizzati alla tavolozza dei colori in modo da potervi accedere facilmente in Microsoft Word
// quando, ad esempio, cambiamo il colore del carattere tramite "Home" -> "Carattere" -> "Colore carattere",
// oppure inserisci una forma e poi impostane un colore tramite "Formato forma" -> "Stili forma".
ThemeColors colors = theme.Colors;
colors.Dark1 = Color.MidnightBlue;
colors.Light1 = Color.PaleGreen;
colors.Dark2 = Color.Indigo;
colors.Light2 = Color.Khaki;

colors.Accent1 = Color.OrangeRed;
colors.Accent2 = Color.LightSalmon;
colors.Accent3 = Color.Yellow;
colors.Accent4 = Color.Gold;
colors.Accent5 = Color.BlueViolet;
colors.Accent6 = Color.DarkViolet;

// Applica colori personalizzati ai collegamenti ipertestuali quando sono cliccati o non cliccati.
colors.Hyperlink = Color.Black;
colors.FollowedHyperlink = Color.Gray;

doc.Save(ArtifactsDir + "Themes.CustomColorsAndFonts.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Themes](../../aspose.words.themes/)
* assemblea [Aspose.Words](../../)
