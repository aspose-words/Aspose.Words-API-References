---
title: HtmlFixedSaveOptions.ExportEmbeddedSvg
linktitle: ExportEmbeddedSvg
articleTitle: ExportEmbeddedSvg
second_title: Aspose.Words per .NET
description: Scopri la proprietà ExportEmbeddedSvg di HtmlFixedSaveOptions e incorpora facilmente risorse SVG nei tuoi documenti HTML per ottenere effetti visivi migliori. Valore predefinito: true.
type: docs
weight: 70
url: /it/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedsvg/
---
## HtmlFixedSaveOptions.ExportEmbeddedSvg property

Specifica se le risorse SVG devono essere incorporate nel documento HTML. Il valore predefinito è`VERO` .

```csharp
public bool ExportEmbeddedSvg { get; set; }
```

## Esempi

Mostra come determinare dove memorizzare gli oggetti SVG quando si esporta un documento in formato HTML.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Quando esportiamo un documento con oggetti SVG in .html,
// Aspose.Words può posizionare questi oggetti in due possibili posizioni.
// Impostando il flag "ExportEmbeddedSvg" su "true" verranno incorporati tutti i dati grezzi dell'oggetto SVG
// all'interno dell'HTML di output, all'interno dei tag <image>.
// Impostando questo flag su "false" verrà creato un file nel file system locale per ciascun oggetto SVG.
// L'HTML si collegherà a ciascun file utilizzando l'attributo "data" di un tag <object>.
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
