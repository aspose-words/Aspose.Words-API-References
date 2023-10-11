---
title: Class ThemeColors
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Themes.ThemeColors classe. Rappresenta la combinazione di colori del tema del documento che contiene dodici colori.
type: docs
weight: 6480
url: /it/net/aspose.words.themes/themecolors/
---
## ThemeColors class

Rappresenta la combinazione di colori del tema del documento che contiene dodici colori.

`ThemeColors` l'oggetto contiene sei colori accentati, due colori scuri, due colori chiari e un colore per ciascuno dei collegamenti ipertestuali e dei collegamenti ipertestuali seguiti.

```csharp
public class ThemeColors
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Accent1](../../aspose.words.themes/themecolors/accent1/) { get; set; } | Specifica l'accento colore 1. |
| [Accent2](../../aspose.words.themes/themecolors/accent2/) { get; set; } | Specifica l'accento colore 2. |
| [Accent3](../../aspose.words.themes/themecolors/accent3/) { get; set; } | Specifica l'accento colore 3. |
| [Accent4](../../aspose.words.themes/themecolors/accent4/) { get; set; } | Specifica l'accento colore 4. |
| [Accent5](../../aspose.words.themes/themecolors/accent5/) { get; set; } | Specifica l'accento colore 5. |
| [Accent6](../../aspose.words.themes/themecolors/accent6/) { get; set; } | Specifica l'accento colore 6. |
| [Dark1](../../aspose.words.themes/themecolors/dark1/) { get; set; } | Specifica il colore Scuro 1. |
| [Dark2](../../aspose.words.themes/themecolors/dark2/) { get; set; } | Specifica il colore Scuro 2. |
| [FollowedHyperlink](../../aspose.words.themes/themecolors/followedhyperlink/) { get; set; } | Specifica il colore per un collegamento ipertestuale su cui si è fatto clic. |
| [Hyperlink](../../aspose.words.themes/themecolors/hyperlink/) { get; set; } | Specifica il colore per un collegamento ipertestuale. |
| [Light1](../../aspose.words.themes/themecolors/light1/) { get; set; } | Specifica il colore della luce 1. |
| [Light2](../../aspose.words.themes/themecolors/light2/) { get; set; } | Specifica il colore della luce 2. |

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


