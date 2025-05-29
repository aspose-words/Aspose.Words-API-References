---
title: Document.FontSettings
linktitle: FontSettings
articleTitle: FontSettings
second_title: Aspose.Words per .NET
description: Scopri come personalizzare facilmente le impostazioni dei font dei documenti. Migliora i tuoi documenti con opzioni di font personalizzate per una migliore leggibilità e uno stile impeccabile.
type: docs
weight: 150
url: /it/net/aspose.words/document/fontsettings/
---
## Document.FontSettings property

Ottiene o imposta le impostazioni del font del documento.

```csharp
public FontSettings FontSettings { get; set; }
```

## Osservazioni

Questa proprietà consente di specificare le impostazioni del font per ogni documento. Se impostata su`null` , impostazioni predefinite del font statico [`DefaultInstance`](../../../aspose.words.fonts/fontsettings/defaultinstance/) verrà utilizzato.

Il valore predefinito è`null`.

## Esempi

Mostra come impostare le regole di sostituzione dei font.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

FontSourceBase[] fontSources = FontSettings.DefaultInstance.GetFontsSources();

// Le origini font predefinite contengono il primo font utilizzato dal documento.
Assert.AreEqual(1, fontSources.Length);
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// Il secondo font, "Amethysta", non è disponibile.
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// Possiamo configurare una tabella di sostituzione dei font che determina
// quali font verranno utilizzati da Aspose.Words come sostituti dei font non disponibili.
// Imposta due font sostitutivi per "Amethysta": "Arvo" e "Courier New".
// Se il primo sostituto non è disponibile, Aspose.Words tenta di utilizzare il secondo sostituto e così via.
doc.FontSettings = new FontSettings();
doc.FontSettings.SubstitutionSettings.TableSubstitution.SetSubstitutes(
    "Amethysta", new[] {"Arvo", "Courier New"});

 // "Amethysta" non è disponibile e la regola di sostituzione stabilisce che il primo font da utilizzare come sostituto è "Arvo".
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

 // Anche "Arvo" non è disponibile, ma "Courier New" sì.
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Courier New"));

// Il documento di output visualizzerà il testo che utilizza il font "Amethysta" formattato con "Courier New".
doc.Save(ArtifactsDir + "FontSettings.TableSubstitution.pdf");
```

### Guarda anche

* class [FontSettings](../../../aspose.words.fonts/fontsettings/)
* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
