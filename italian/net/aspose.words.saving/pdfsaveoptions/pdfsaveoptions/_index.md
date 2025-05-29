---
title: PdfSaveOptions
linktitle: PdfSaveOptions
articleTitle: PdfSaveOptions
second_title: Aspose.Words per .NET
description: Scopri il costruttore PdfSaveOptions, progettato per inizializzare e salvare senza problemi i tuoi documenti in formato PDF di alta qualità. Semplifica il tuo flusso di lavoro oggi stesso!
type: docs
weight: 10
url: /it/net/aspose.words.saving/pdfsaveoptions/pdfsaveoptions/
---
## PdfSaveOptions constructor

Inizializza una nuova istanza di questa classe che può essere utilizzata per salvare un documento in Pdf formato.

```csharp
public PdfSaveOptions()
```

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
