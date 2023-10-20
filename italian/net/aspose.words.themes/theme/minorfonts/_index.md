---
title: Theme.MinorFonts
linktitle: MinorFonts
articleTitle: MinorFonts
second_title: Aspose.Words per .NET
description: Theme MinorFonts proprietà. Permette di specificare il set di caratteri minori per diverse lingue in C#.
type: docs
weight: 40
url: /it/net/aspose.words.themes/theme/minorfonts/
---
## Theme.MinorFonts property

Permette di specificare il set di caratteri minori per diverse lingue.

```csharp
public ThemeFonts MinorFonts { get; }
```

## Esempi

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

* class [ThemeFonts](../../themefonts/)
* class [Theme](../)
* spazio dei nomi [Aspose.Words.Themes](../../../aspose.words.themes/)
* assemblea [Aspose.Words](../../../)
