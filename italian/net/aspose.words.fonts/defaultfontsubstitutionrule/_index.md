---
title: DefaultFontSubstitutionRule Class
linktitle: DefaultFontSubstitutionRule
articleTitle: DefaultFontSubstitutionRule
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Fonts.DefaultFontSubstitutionRule per una gestione fluida dei font e una formattazione avanzata dei documenti. Ottimizza il tuo flusso di lavoro oggi stesso!
type: docs
weight: 3250
url: /it/net/aspose.words.fonts/defaultfontsubstitutionrule/
---
## DefaultFontSubstitutionRule class

Regola predefinita per la sostituzione dei font.

Per saperne di più, visita il[Lavorare con i font](https://docs.aspose.com/words/net/working-with-fonts/) articolo di documentazione.

```csharp
public class DefaultFontSubstitutionRule : FontSubstitutionRule
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [DefaultFontName](../../aspose.words.fonts/defaultfontsubstitutionrule/defaultfontname/) { get; set; } | Ottiene o imposta il nome del font predefinito. |
| virtual [Enabled](../../aspose.words.fonts/fontsubstitutionrule/enabled/) { get; set; } | Specifica se la regola è abilitata o meno. |

## Osservazioni

Questa regola definisce il nome del font predefinito da utilizzare per la sostituzione se il font originale non è disponibile.

## Esempi

Mostra come impostare la regola predefinita per la sostituzione dei font.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// Ottieni la regola di sostituzione predefinita in FontSettings.
// Questa regola sostituirà tutti i font mancanti con "Times New Roman".
DefaultFontSubstitutionRule defaultFontSubstitutionRule =
    fontSettings.SubstitutionSettings.DefaultFontSubstitution;
Assert.True(defaultFontSubstitutionRule.Enabled);
Assert.AreEqual("Times New Roman", defaultFontSubstitutionRule.DefaultFontName);

// Imposta il sostituto del font predefinito su "Courier New".
defaultFontSubstitutionRule.DefaultFontName = "Courier New";

// Utilizzando un generatore di documenti, aggiungi del testo in un font di cui non abbiamo bisogno per vedere la sostituzione avvenire,
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
