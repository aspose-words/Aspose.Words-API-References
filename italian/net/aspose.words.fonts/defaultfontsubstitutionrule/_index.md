---
title: DefaultFontSubstitutionRule Class
linktitle: DefaultFontSubstitutionRule
articleTitle: DefaultFontSubstitutionRule
second_title: Aspose.Words per .NET
description: Aspose.Words.Fonts.DefaultFontSubstitutionRule classe. Regola di sostituzione dei caratteri predefinita in C#.
type: docs
weight: 2840
url: /it/net/aspose.words.fonts/defaultfontsubstitutionrule/
---
## DefaultFontSubstitutionRule class

Regola di sostituzione dei caratteri predefinita.

Per saperne di più, visita il[Lavorare con i caratteri](https://docs.aspose.com/words/net/working-with-fonts/) articolo di documentazione.

```csharp
public class DefaultFontSubstitutionRule : FontSubstitutionRule
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [DefaultFontName](../../aspose.words.fonts/defaultfontsubstitutionrule/defaultfontname/) { get; set; } | Ottiene o imposta il nome del carattere predefinito. |
| virtual [Enabled](../../aspose.words.fonts/fontsubstitutionrule/enabled/) { get; set; } | Specifica se la regola è abilitata o meno. |

## Osservazioni

Questa regola definisce il nome del carattere predefinito singolo da utilizzare per la sostituzione se il carattere originale non è disponibile.

## Esempi

Mostra come impostare la regola di sostituzione dei caratteri predefinita.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// Ottieni la regola di sostituzione predefinita in FontSettings.
// Questa regola sostituirà tutti i caratteri mancanti con "Times New Roman".
DefaultFontSubstitutionRule defaultFontSubstitutionRule =
    fontSettings.SubstitutionSettings.DefaultFontSubstitution;
Assert.True(defaultFontSubstitutionRule.Enabled);
Assert.AreEqual("Times New Roman", defaultFontSubstitutionRule.DefaultFontName);

// Imposta il carattere sostitutivo predefinito su "Courier New".
defaultFontSubstitutionRule.DefaultFontName = "Courier New";

// Usando un generatore di documenti, aggiungi del testo in un carattere che non è necessario per vedere avvenire la sostituzione,
// e quindi visualizzare il risultato in un PDF.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Missing Font";
builder.Writeln("Line written in a missing font, which will be substituted with Courier New.");

doc.Save(ArtifactsDir + "FontSettings.DefaultFontSubstitutionRule.pdf");
```

### Guarda anche

* class [FontSubstitutionRule](../fontsubstitutionrule/)
* spazio dei nomi [Aspose.Words.Fonts](../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../)
