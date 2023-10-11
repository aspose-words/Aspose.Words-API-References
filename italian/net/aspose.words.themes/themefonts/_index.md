---
title: Class ThemeFonts
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Themes.ThemeFonts classe. Rappresenta una raccolta di caratteri nello schema dei caratteri consentendo di specificare caratteri diversi per lingue diverseLatin EastAsian EComplexScript .
type: docs
weight: 6500
url: /it/net/aspose.words.themes/themefonts/
---
## ThemeFonts class

Rappresenta una raccolta di caratteri nello schema dei caratteri, consentendo di specificare caratteri diversi per lingue diverse[`Latin`](./latin/) ,[`EastAsian`](./eastasian/) E[`ComplexScript`](./complexscript/) .

Per saperne di più, visita il[Lavorare con stili e temi](https://docs.aspose.com/words/net/working-with-styles-and-themes/) articolo di documentazione.

```csharp
public class ThemeFonts
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [ComplexScript](../../aspose.words.themes/themefonts/complexscript/) { get; set; } | Specifica il nome del carattere per i caratteri ComplexScript. |
| [EastAsian](../../aspose.words.themes/themefonts/eastasian/) { get; set; } | Specifica il nome del carattere per i caratteri dell'Asia orientale. |
| [Latin](../../aspose.words.themes/themefonts/latin/) { get; set; } | Specifica il nome del carattere per i caratteri latini. |

### Esempi

Mostra come impostare colori e caratteri personalizzati per i temi.

```csharp
Document doc = new Document(MyDir + "Theme colors.docx");

// L'oggetto "Tema" ci dà accesso al tema del documento, una fonte di caratteri e colori predefiniti.
Theme theme = doc.Theme;

// Alcuni stili, come "Intestazione 1" e "Sottotitolo", erediteranno questi caratteri.
theme.MajorFonts.Latin = "Courier New";
theme.MinorFonts.Latin = "Agency FB";

// Anche altre lingue potrebbero avere i propri caratteri personalizzati in questo tema.
Assert.AreEqual(string.Empty, theme.MajorFonts.ComplexScript);
Assert.AreEqual(string.Empty, theme.MajorFonts.EastAsian);
Assert.AreEqual(string.Empty, theme.MinorFonts.ComplexScript);
Assert.AreEqual(string.Empty, theme.MinorFonts.EastAsian);

// La proprietà "Colori" contiene la tavolozza dei colori di Microsoft Word,
// che appare quando si cambia l'ombreggiatura o il colore del carattere.
// Applica colori personalizzati alla tavolozza dei colori in modo da potervi accedere facilmente in Microsoft Word
// quando, ad esempio, modifichiamo il colore del carattere tramite "Home" -> "Carattere" -> "Colore del carattere",
// oppure inserisci una forma e quindi impostane un colore tramite "Formato forma" -> "Stili di forma".
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

// Applica colori personalizzati ai collegamenti ipertestuali negli stati cliccati e non cliccati.
colors.Hyperlink = Color.Black;
colors.FollowedHyperlink = Color.Gray;

doc.Save(ArtifactsDir + "Themes.CustomColorsAndFonts.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Themes](../../aspose.words.themes/)
* assemblea [Aspose.Words](../../)


