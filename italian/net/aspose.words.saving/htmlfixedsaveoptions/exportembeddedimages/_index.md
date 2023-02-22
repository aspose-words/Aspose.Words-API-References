---
title: HtmlFixedSaveOptions.ExportEmbeddedImages
second_title: Aspose.Words per .NET API Reference
description: HtmlFixedSaveOptions proprietà. Specifica se le immagini devono essere incorporate nel documento HTML in formato Base64. Nota limpostazione di questo flag può aumentare notevolmente le dimensioni del file HTML di output.
type: docs
weight: 60
url: /it/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedimages/
---
## HtmlFixedSaveOptions.ExportEmbeddedImages property

Specifica se le immagini devono essere incorporate nel documento HTML in formato Base64. Nota l'impostazione di questo flag può aumentare notevolmente le dimensioni del file HTML di output.

```csharp
public bool ExportEmbeddedImages { get; set; }
```

### Esempi

Mostra come determinare dove archiviare le immagini durante l'esportazione di un documento in HTML.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Quando esportiamo un documento con immagini incorporate in .html,
// Aspose.Words può posizionare le immagini in due possibili posizioni.
// L'impostazione del flag "ExportEmbeddedImages" su "true" memorizzerà i dati grezzi
// per tutte le immagini all'interno del documento HTML di output, nell'attributo "src" di <image> tag.
// L'impostazione di questo flag su "false" creerà un file immagine nel file system locale per ogni immagine,
// e archivia tutti questi file in una cartella separata.
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    ExportEmbeddedImages = exportImages
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedImages.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedImages.html");

if (exportImages)
{
    Assert.False(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedImages/image001.jpeg"));
    Assert.True(Regex.Match(outDocContents,
        "<img class=\"awimg\" style=\"left:0pt; top:0pt; width:493.1pt; height:300.55pt;\" src=\".+\" />").Success);
}
else
{
    Assert.True(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedImages/image001.jpeg"));
    Assert.True(Regex.Match(outDocContents,
        "<img class=\"awimg\" style=\"left:0pt; top:0pt; width:493.1pt; height:300.55pt;\" " +
        "src=\"HtmlFixedSaveOptions[.]ExportEmbeddedImages/image001[.]jpeg\" />").Success);
}
```

### Guarda anche

* class [HtmlFixedSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../htmlfixedsaveoptions/)
* assemblea [Aspose.Words](../../../)


