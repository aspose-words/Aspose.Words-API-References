---
title: HtmlFixedSaveOptions.CssClassNamesPrefix
linktitle: CssClassNamesPrefix
articleTitle: CssClassNamesPrefix
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad HtmlFixedSaveOptions CssClassNamesPrefix mejora su estilo al agregar un prefijo personalizable a todos los nombres de clase en su style.css.
type: docs
weight: 20
url: /es/net/aspose.words.saving/htmlfixedsaveoptions/cssclassnamesprefix/
---
## HtmlFixedSaveOptions.CssClassNamesPrefix property

Especifica el prefijo que se agrega a todos los nombres de clase en el archivo style.css. El valor predeterminado es`"aw"` .

```csharp
public string CssClassNamesPrefix { get; set; }
```

## Ejemplos

Muestra cómo colocar CSS en un archivo separado y agregar un prefijo a todos sus nombres de clase CSS.

```csharp
Document doc = new Document(MyDir + "Bookmarks.docx");

HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    CssClassNamesPrefix = "myprefix",
    SaveFontFaceCssSeparately = true
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.AddCssClassNamesPrefix.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.AddCssClassNamesPrefix.html");

Assert.True(Regex.Match(outDocContents,
    "<div class=\"myprefixdiv myprefixpage\" style=\"width:595[.]3pt; height:841[.]9pt;\">" +
    "<div class=\"myprefixdiv\" style=\"left:85[.]05pt; top:36pt; clip:rect[(]0pt,510[.]25pt,74[.]95pt,-85.05pt[)];\">" +
    "<span class=\"myprefixspan myprefixtext001\" style=\"font-size:11pt; left:294[.]73pt; top:0[.]36pt; line-height:12[.]29pt;\">").Success);

outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.AddCssClassNamesPrefix/styles.css");

Assert.True(Regex.Match(outDocContents,
    ".myprefixdiv { position:absolute; } " +
    ".myprefixspan { position:absolute; white-space:pre; color:#000000; font-size:12pt; }").Success);
```

### Ver también

* class [HtmlFixedSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
