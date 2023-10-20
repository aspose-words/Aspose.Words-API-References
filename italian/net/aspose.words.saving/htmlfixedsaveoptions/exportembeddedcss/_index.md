---
title: HtmlFixedSaveOptions.ExportEmbeddedCss
linktitle: ExportEmbeddedCss
articleTitle: ExportEmbeddedCss
second_title: Aspose.Words per .NET
description: HtmlFixedSaveOptions ExportEmbeddedCss proprietà. Specifica se il CSS Cascading Style Sheet deve essere incorporato nel documento Html in C#.
type: docs
weight: 40
url: /it/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedcss/
---
## HtmlFixedSaveOptions.ExportEmbeddedCss property

Specifica se il CSS (Cascading Style Sheet) deve essere incorporato nel documento Html.

```csharp
public bool ExportEmbeddedCss { get; set; }
```

## Esempi

Mostra come determinare dove archiviare i fogli di stile CSS durante l'esportazione di un documento in HTML.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Quando esportiamo un documento in html, Aspose.Words creerà anche un foglio di stile CSS con cui formattare il documento.
// Impostando il flag "ExportEmbeddedCss" su "true" salva il foglio di stile CSS in un file .css,
// e collegarsi al file dal documento html utilizzando un <link> elemento.
// Impostando il flag su "false" incorporerà il foglio di stile CSS all'interno del documento Html,
// che creerà un solo file invece di due.
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    ExportEmbeddedCss = exportEmbeddedCss
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedCss.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedCss.html");

if (exportEmbeddedCss)
{
    Assert.True(Regex.Match(outDocContents, "<style type=\"text/css\">").Success);
    Assert.False(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedCss/styles.css"));
}
else
{
    Assert.True(Regex.Match(outDocContents,
        "<link rel=\"stylesheet\" type=\"text/css\" href=\"HtmlFixedSaveOptions[.]ExportEmbeddedCss/styles[.]css\" media=\"all\" />").Success);
    Assert.True(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedCss/styles.css"));
}
```

### Guarda anche

* class [HtmlFixedSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
