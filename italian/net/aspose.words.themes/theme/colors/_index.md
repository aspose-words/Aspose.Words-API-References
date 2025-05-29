---
title: Theme.Colors
linktitle: Colors
articleTitle: Colors
second_title: Aspose.Words per .NET
description: Personalizza l'aspetto del tuo documento con la proprietà Colori tema, che consente di ottenere un set esclusivo di colori vivaci per un risultato sorprendente.
type: docs
weight: 20
url: /it/net/aspose.words.themes/theme/colors/
---
## Theme.Colors property

Consente di specificare l'insieme dei colori del tema per il documento.

```csharp
public ThemeColors Colors { get; }
```

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

* class [ThemeColors](../../themecolors/)
* class [Theme](../)
* spazio dei nomi [Aspose.Words.Themes](../../../aspose.words.themes/)
* assemblea [Aspose.Words](../../../)
