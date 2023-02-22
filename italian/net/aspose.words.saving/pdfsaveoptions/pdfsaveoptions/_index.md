---
title: PdfSaveOptions.PdfSaveOptions
second_title: Aspose.Words per .NET API Reference
description: PdfSaveOptions costruttore. Inizializza una nuova istanza di questa classe che può essere utilizzata per salvare un documento in Pdf formato.
type: docs
weight: 10
url: /it/net/aspose.words.saving/pdfsaveoptions/pdfsaveoptions/
---
## PdfSaveOptions constructor

Inizializza una nuova istanza di questa classe che può essere utilizzata per salvare un documento in Pdf formato.

```csharp
public PdfSaveOptions()
```

### Esempi

Mostra come abilitare o disabilitare i sottoinsiemi quando si incorporano i caratteri durante il rendering di un documento in PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Arvo";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Configura le nostre fonti di font per assicurarci di avere accesso a entrambi i font in questo documento.
FontSourceBase[] originalFontsSources = FontSettings.DefaultInstance.GetFontsSources();
Aspose.Words.Fonts.FolderFontSource folderFontSource = new Aspose.Words.Fonts.FolderFontSource(FontsDir, true);
FontSettings.DefaultInstance.SetFontsSources(new[] { originalFontsSources[0], folderFontSource });

FontSourceBase[] fontSources = FontSettings.DefaultInstance.GetFontsSources();
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(fontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

// Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Poiché il nostro documento contiene un carattere personalizzato, potrebbe essere desiderabile incorporarlo nel documento di output.
// Imposta la proprietà "EmbedFullFonts" su "true" per incorporare ogni glifo di ogni carattere incorporato nel PDF di output.
// Le dimensioni del documento possono diventare molto grandi, ma avremo il pieno utilizzo di tutti i caratteri se modifichiamo il PDF.
// Imposta la proprietà "EmbedFullFonts" su "false" per applicare il sottoinsieme ai caratteri, salvando solo i glifi
// che il documento sta utilizzando. Il file sarà notevolmente più piccolo,
// ma potremmo aver bisogno di accedere a qualsiasi carattere personalizzato se modifichiamo il documento.
options.EmbedFullFonts = embedFullFonts;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmbedFullFonts.pdf", options);

if (embedFullFonts)
    Assert.That(500000, Is.LessThan(new FileInfo(ArtifactsDir + "PdfSaveOptions.EmbedFullFonts.pdf").Length));
else
    Assert.That(25000, Is.AtLeast(new FileInfo(ArtifactsDir + "PdfSaveOptions.EmbedFullFonts.pdf").Length));

// Ripristina le origini dei caratteri originali.
FontSettings.DefaultInstance.SetFontsSources(originalFontsSources);
```

### Guarda anche

* class [PdfSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../pdfsaveoptions/)
* assemblea [Aspose.Words](../../../)


