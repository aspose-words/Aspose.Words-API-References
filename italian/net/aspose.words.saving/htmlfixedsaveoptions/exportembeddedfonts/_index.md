---
title: HtmlFixedSaveOptions.ExportEmbeddedFonts
second_title: Aspose.Words per .NET API Reference
description: HtmlFixedSaveOptions proprietà. Specifica se i caratteri devono essere incorporati nel documento Html in formato Base64. Nota che limpostazione di questo flag può aumentare significativamente la dimensione del file Html di output.
type: docs
weight: 50
url: /it/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedfonts/
---
## HtmlFixedSaveOptions.ExportEmbeddedFonts property

Specifica se i caratteri devono essere incorporati nel documento Html in formato Base64. Nota che l'impostazione di questo flag può aumentare significativamente la dimensione del file Html di output.

```csharp
public bool ExportEmbeddedFonts { get; set; }
```

### Esempi

Mostra come determinare dove archiviare i caratteri incorporati durante l'esportazione di un documento in HTML.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

// Quando esportiamo un documento con caratteri incorporati in .html,
// Aspose.Words può posizionare i caratteri in due possibili posizioni.
// Impostando il flag "ExportEmbeddedFonts" su "true" verranno memorizzati i dati grezzi per i caratteri incorporati nel foglio di stile CSS,
// nella proprietà "url" della regola "@font-face". Ciò potrebbe creare un enorme file di fogli di stile CSS
// e riduci il numero di file esterni creati da questa conversione HTML.
// Impostando questo flag su "false" verrà creato un file per ciascun carattere.
// Il foglio di stile CSS si collegherà a ciascun file di font utilizzando la proprietà "url" della regola "@font-face".
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
* spazio dei nomi [Aspose.Words.Saving](../../htmlfixedsaveoptions/)
* assemblea [Aspose.Words](../../../)


