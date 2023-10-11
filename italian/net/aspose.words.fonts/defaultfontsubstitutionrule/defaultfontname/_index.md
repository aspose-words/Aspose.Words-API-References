---
title: DefaultFontSubstitutionRule.DefaultFontName
second_title: Aspose.Words per .NET API Reference
description: DefaultFontSubstitutionRule proprietà. Ottiene o imposta il nome del carattere predefinito.
type: docs
weight: 10
url: /it/net/aspose.words.fonts/defaultfontsubstitutionrule/defaultfontname/
---
## DefaultFontSubstitutionRule.DefaultFontName property

Ottiene o imposta il nome del carattere predefinito.

```csharp
public string DefaultFontName { get; set; }
```

### Osservazioni

Il valore predefinito è "Times New Roman".

### Esempi

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

Mostra come specificare un carattere predefinito.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Arvo";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

FontSourceBase[] fontSources = FontSettings.DefaultInstance.GetFontsSources();

// Le origini dei caratteri utilizzati dal documento contengono il carattere "Arial", ma non "Arvo".
Assert.AreEqual(1, fontSources.Length);
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

// Imposta la proprietà "DefaultFontName" su "Courier New" su,
 // durante il rendering del documento, applica quel carattere in tutti i casi in cui un altro carattere non è disponibile.
FontSettings.DefaultInstance.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Courier New";

Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Courier New"));

// Aspose.Words ora utilizzerà il carattere predefinito al posto di eventuali caratteri mancanti durante qualsiasi chiamata di rendering.
doc.Save(ArtifactsDir + "FontSettings.DefaultFontName.pdf");
```

### Guarda anche

* class [DefaultFontSubstitutionRule](../)
* spazio dei nomi [Aspose.Words.Fonts](../../defaultfontsubstitutionrule/)
* assemblea [Aspose.Words](../../../)


