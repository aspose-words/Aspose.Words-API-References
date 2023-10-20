---
title: FontSubstitutionSettings.DefaultFontSubstitution
linktitle: DefaultFontSubstitution
articleTitle: DefaultFontSubstitution
second_title: Aspose.Words per .NET
description: FontSubstitutionSettings DefaultFontSubstitution proprietà. Impostazioni relative alla regola di sostituzione dei caratteri predefinita in C#.
type: docs
weight: 10
url: /it/net/aspose.words.fonts/fontsubstitutionsettings/defaultfontsubstitution/
---
## FontSubstitutionSettings.DefaultFontSubstitution property

Impostazioni relative alla regola di sostituzione dei caratteri predefinita.

```csharp
public DefaultFontSubstitutionRule DefaultFontSubstitution { get; }
```

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

* class [DefaultFontSubstitutionRule](../../defaultfontsubstitutionrule/)
* class [FontSubstitutionSettings](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)
