---
title: HtmlFixedSaveOptions.ExportEmbeddedSvg
linktitle: ExportEmbeddedSvg
articleTitle: ExportEmbeddedSvg
second_title: Aspose.Words per .NET
description: HtmlFixedSaveOptions ExportEmbeddedSvg proprietà. Specifica se le risorse SVG devono essere incorporate nel documento Html. Il valore predefinito èVERO  in C#.
type: docs
weight: 70
url: /it/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedsvg/
---
## HtmlFixedSaveOptions.ExportEmbeddedSvg property

Specifica se le risorse SVG devono essere incorporate nel documento Html. Il valore predefinito è`VERO` .

```csharp
public bool ExportEmbeddedSvg { get; set; }
```

## Esempi

Mostra come determinare dove archiviare gli oggetti SVG durante l'esportazione di un documento in Html.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Quando esportiamo un documento con oggetti SVG in .html,
// Aspose.Words può posizionare questi oggetti in due possibili posizioni.
// Impostando il flag "ExportEmbeddedSvg" su "true" verranno incorporati tutti i dati grezzi dell'oggetto SVG
// all'interno dell'HTML di output, all'interno di <image> tag.
// Impostando questo flag su "false" verrà creato un file nel file system locale per ciascun oggetto SVG.
// L'HTML si collegherà a ciascun file utilizzando l'attributo "data" di un <oggetto> etichetta.
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    ExportEmbeddedSvg = exportSvgs
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedSvgs.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedSvgs.html");

if (exportSvgs)
{
    Assert.False(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001.svg"));
    Assert.True(Regex.Match(outDocContents,
        "<image id=\"image004\" xlink:href=.+/>").Success);
}
else
{
    Assert.True(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001.svg"));
    Assert.True(Regex.Match(outDocContents,
        "<object type=\"image/svg[+]xml\" data=\"HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001[.]svg\"></object>").Success);
}
```

### Guarda anche

* class [HtmlFixedSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
