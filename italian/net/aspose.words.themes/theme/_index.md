---
title: Theme Class
linktitle: Theme
articleTitle: Theme
second_title: Aspose.Words per .NET
description: Esplora la classe Aspose.Words.Theme per arricchire i tuoi documenti con temi personalizzabili, tra cui MajorFonts, MinorFonts e colori vivaci.
type: docs
weight: 7310
url: /it/net/aspose.words.themes/theme/
---
## Theme class

Rappresenta il tema del documento e fornisce l'accesso alle parti principali del tema, tra cui[`MajorFonts`](./majorfonts/) ,[`MinorFonts`](./minorfonts/) E[`Colors`](./colors/)

Per saperne di più, visita il[Lavorare con stili e temi](https://docs.aspose.com/words/net/working-with-styles-and-themes/) articolo di documentazione.

```csharp
public class Theme
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [Theme](theme/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Colors](../../aspose.words.themes/theme/colors/) { get; } | Consente di specificare l'insieme dei colori del tema per il documento. |
| [MajorFonts](../../aspose.words.themes/theme/majorfonts/) { get; } | Consente di specificare l'insieme dei caratteri principali per le diverse lingue. |
| [MinorFonts](../../aspose.words.themes/theme/minorfonts/) { get; } | Consente di specificare l'insieme dei font secondari per le diverse lingue. |

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
