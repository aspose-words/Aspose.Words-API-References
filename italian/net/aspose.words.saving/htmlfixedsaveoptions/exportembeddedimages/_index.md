---
title: HtmlFixedSaveOptions.ExportEmbeddedImages
linktitle: ExportEmbeddedImages
articleTitle: ExportEmbeddedImages
second_title: Aspose.Words per .NET
description: Scopri come la proprietà ExportEmbeddedImages in HtmlFixedSaveOptions migliora i tuoi documenti HTML incorporando immagini in formato Base64, ottimizzando la qualità visiva e gestendo al contempo le dimensioni dei file.
type: docs
weight: 60
url: /it/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedimages/
---
## HtmlFixedSaveOptions.ExportEmbeddedImages property

Specifica se le immagini devono essere incorporate nel documento HTML in formato Base64. Nota: l'impostazione di questo flag può aumentare significativamente la dimensione del file HTML di output.

```csharp
public bool ExportEmbeddedImages { get; set; }
```

## Esempi

Mostra come determinare dove archiviare le immagini quando si esporta un documento in formato HTML.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Quando esportiamo un documento con immagini incorporate in .html,
// Aspose.Words può posizionare le immagini in due possibili posizioni.
// Impostando il flag "ExportEmbeddedImages" su "true" verranno memorizzati i dati grezzi
// per tutte le immagini presenti nel documento HTML di output, nell'attributo "src" dei tag <image>.
// Impostando questo flag su "false" verrà creato un file immagine nel file system locale per ogni immagine,
// e memorizzare tutti questi file in una cartella separata.
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
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
