---
title: Document.Theme
linktitle: Theme
articleTitle: Theme
second_title: Aspose.Words per .NET
description: Accedi alla proprietà Tema del documento per recuperare senza sforzo l'oggetto Tema, migliorando così il design e l'aspetto visivo del tuo documento.
type: docs
weight: 440
url: /it/net/aspose.words/document/theme/
---
## Document.Theme property

Ottiene il`Theme` oggetto per questo documento.

```csharp
public Theme Theme { get; }
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

* class [Theme](../../../aspose.words.themes/theme/)
* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
