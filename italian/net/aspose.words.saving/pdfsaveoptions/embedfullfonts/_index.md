---
title: PdfSaveOptions.EmbedFullFonts
linktitle: EmbedFullFonts
articleTitle: EmbedFullFonts
second_title: Aspose.Words per .NET
description: Scopri come la funzionalità EmbedFullFonts di PdfSaveOptions migliora i tuoi documenti PDF garantendo l'incorporamento completo dei font per una formattazione perfetta.
type: docs
weight: 120
url: /it/net/aspose.words.saving/pdfsaveoptions/embedfullfonts/
---
## PdfSaveOptions.EmbedFullFonts property

Controlla come i font vengono incorporati nei documenti PDF risultanti.

```csharp
public bool EmbedFullFonts { get; set; }
```

## Osservazioni

Il valore predefinito è`falso`, il che significa che i font vengono suddivisi in sottoinsiemi prima dell'incorporamento. Il sottoinsieme è utile se si desidera ridurre le dimensioni del file di output. Il sottoinsieme rimuove tutti i glifi inutilizzati da un font.

Quando questo valore è impostato su`VERO`, un file di font completo viene incorporato nel PDF senza sottoinsiemi. Questo si tradurrà in file di output più grandi, ma può essere un'opzione utile quando si desidera modificare il PDF risultante in un secondo momento (ad esempio, aggiungere altro testo).

Alcuni font sono di grandi dimensioni (diversi megabyte) e incorporarli senza subsetting darà luogo a documenti di output di grandi dimensioni.

## Esempi

Mostra come abilitare o disabilitare il sottoinsieme quando si incorporano font durante il rendering di un documento in PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Arvo";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Configuriamo le nostre fonti di font per assicurarci di avere accesso a entrambi i font presenti in questo documento.
FontSourceBase[] originalFontsSources = FontSettings.DefaultInstance.GetFontsSources();
Aspose.Words.Fonts.FolderFontSource folderFontSource =
    new Aspose.Words.Fonts.FolderFontSource(FontsDir, true);
FontSettings.DefaultInstance.SetFontsSources(new[] { originalFontsSources[0], folderFontSource });

FontSourceBase[] fontSources = FontSettings.DefaultInstance.GetFontsSources();
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(fontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

// Creiamo un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Poiché il nostro documento contiene un font personalizzato, potrebbe essere opportuno incorporarlo nel documento di output.
// Impostare la proprietà "EmbedFullFonts" su "true" per incorporare ogni glifo di ogni font incorporato nel PDF di output.
// Le dimensioni del documento potrebbero aumentare notevolmente, ma se modifichiamo il PDF potremo utilizzare appieno tutti i font.
// Imposta la proprietà "EmbedFullFonts" su "false" per applicare il sottoinsieme ai font, salvando solo i glifi
// che il documento sta utilizzando. Il file sarà considerevolmente più piccolo,
// ma potremmo aver bisogno di accedere a font personalizzati se modifichiamo il documento.
options.EmbedFullFonts = embedFullFonts;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmbedFullFonts.pdf", options);

// Ripristina le sorgenti dei font originali.
FontSettings.DefaultInstance.SetFontsSources(originalFontsSources);
```

### Guarda anche

* class [PdfSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
