---
title: HtmlFixedSaveOptions.ExportEmbeddedFonts
linktitle: ExportEmbeddedFonts
articleTitle: ExportEmbeddedFonts
second_title: Aspose.Words per .NET
description: Controlla l'incorporamento dei font nel tuo HTML con la proprietà ExportEmbeddedFonts. Migliora la qualità del documento gestendo efficacemente le dimensioni dei file.
type: docs
weight: 50
url: /it/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedfonts/
---
## HtmlFixedSaveOptions.ExportEmbeddedFonts property

Specifica se i font devono essere incorporati nel documento HTML in formato Base64. Nota: l'impostazione di questo flag può aumentare significativamente la dimensione del file HTML di output.

```csharp
public bool ExportEmbeddedFonts { get; set; }
```

## Esempi

Mostra come determinare dove archiviare i font incorporati quando si esporta un documento in formato HTML.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

// Quando esportiamo un documento con font incorporati in .html,
// Aspose.Words può posizionare i font in due possibili posizioni.
// Impostando il flag "ExportEmbeddedFonts" su "true" verranno memorizzati i dati grezzi per i font incorporati nel foglio di stile CSS,
// nella proprietà "url" della regola "@font-face". Questo potrebbe creare un enorme file di foglio di stile CSS.
// e ridurre il numero di file esterni che questa conversione HTML creerà.
// Impostando questo flag su "false" verrà creato un file per ogni font.
// Il foglio di stile CSS creerà un collegamento a ciascun file di font utilizzando la proprietà "url" della regola "@font-face".
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    ExportEmbeddedFonts = exportEmbeddedFonts
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedFonts.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedFonts/styles.css");

if (exportEmbeddedFonts)
{
    Assert.True(Regex.Match(outDocContents,
        "@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], url[(].+[)] format[(]'woff'[)]; }").Success);
    Assert.AreEqual(0, Directory.GetFiles(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedFonts").Count(f => f.EndsWith(".woff")));
}
else
{
    Assert.True(Regex.Match(outDocContents,
        "@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], url[(]'font001[.]woff'[)] format[(]'woff'[)]; }").Success);
    Assert.AreEqual(2, Directory.GetFiles(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedFonts").Count(f => f.EndsWith(".woff")));
}
```

### Guarda anche

* class [HtmlFixedSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
