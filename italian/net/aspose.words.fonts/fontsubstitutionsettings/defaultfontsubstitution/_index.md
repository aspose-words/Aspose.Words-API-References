---
title: FontSubstitutionSettings.DefaultFontSubstitution
linktitle: DefaultFontSubstitution
articleTitle: DefaultFontSubstitution
second_title: Aspose.Words per .NET
description: Scopri come la proprietà DefaultFontSubstitution ottimizza le impostazioni dei font per una tipografia impeccabile. Migliora il tuo design con efficaci regole di sostituzione dei font.
type: docs
weight: 10
url: /it/net/aspose.words.fonts/fontsubstitutionsettings/defaultfontsubstitution/
---
## FontSubstitutionSettings.DefaultFontSubstitution property

Impostazioni relative alla regola di sostituzione del font predefinito.

```csharp
public DefaultFontSubstitutionRule DefaultFontSubstitution { get; }
```

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

* class [DefaultFontSubstitutionRule](../../defaultfontsubstitutionrule/)
* class [FontSubstitutionSettings](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)
