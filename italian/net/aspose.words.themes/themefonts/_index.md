---
title: ThemeFonts Class
linktitle: ThemeFonts
articleTitle: ThemeFonts
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words ThemeFonts, un potente strumento per gestire schemi di font multilingue, migliorando lo stile e la leggibilità dei tuoi documenti.
type: docs
weight: 7350
url: /it/net/aspose.words.themes/themefonts/
---
## ThemeFonts class

Rappresenta una raccolta di font nello schema dei font, consentendo di specificare font diversi per lingue diverse[`Latin`](./latin/) ,[`EastAsian`](./eastasian/) E[`ComplexScript`](./complexscript/) .

Per saperne di più, visita il[Lavorare con stili e temi](https://docs.aspose.com/words/net/working-with-styles-and-themes/) articolo di documentazione.

```csharp
public class ThemeFonts
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [ComplexScript](../../aspose.words.themes/themefonts/complexscript/) { get; set; } | Specifica il nome del font per i caratteri ComplexScript. |
| [EastAsian](../../aspose.words.themes/themefonts/eastasian/) { get; set; } | Specifica il nome del font per i caratteri dell'Asia orientale. |
| [Latin](../../aspose.words.themes/themefonts/latin/) { get; set; } | Specifica il nome del font per i caratteri latini. |

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
