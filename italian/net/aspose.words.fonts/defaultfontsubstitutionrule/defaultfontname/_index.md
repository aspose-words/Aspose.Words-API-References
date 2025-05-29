---
title: DefaultFontSubstitutionRule.DefaultFontName
linktitle: DefaultFontName
articleTitle: DefaultFontName
second_title: Aspose.Words per .NET
description: Scopri come gestire facilmente DefaultFontSubstitutionRule e personalizzare il nome del tuo font predefinito per una maggiore flessibilità di progettazione.
type: docs
weight: 10
url: /it/net/aspose.words.fonts/defaultfontsubstitutionrule/defaultfontname/
---
## DefaultFontSubstitutionRule.DefaultFontName property

Ottiene o imposta il nome del font predefinito.

```csharp
public string DefaultFontName { get; set; }
```

## Osservazioni

Il valore predefinito è 'Times New Roman'.

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

Mostra come specificare un font predefinito.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Arvo";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

FontSourceBase[] fontSources = FontSettings.DefaultInstance.GetFontsSources();

// Le fonti dei font utilizzate dal documento contengono il font "Arial", ma non "Arvo".
Assert.AreEqual(1, fontSources.Length);
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

// Imposta la proprietà "DefaultFontName" su "Courier New" per,
// durante il rendering del documento, applica quel font in tutti i casi in cui un altro font non è disponibile.
FontSettings.DefaultInstance.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Courier New";

Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Courier New"));

// Aspose.Words utilizzerà ora il font predefinito al posto di eventuali font mancanti durante qualsiasi chiamata di rendering.
doc.Save(ArtifactsDir + "FontSettings.DefaultFontName.pdf");
```

### Guarda anche

* class [DefaultFontSubstitutionRule](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)
