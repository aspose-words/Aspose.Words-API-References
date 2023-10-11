---
title: HtmlFixedSaveOptions.SaveFontFaceCssSeparately
second_title: Referencia de API de Aspose.Words para .NET
description: HtmlFixedSaveOptions propiedad. El indicador indica si las reglas CSS fontface deben colocarse en un archivo separado fontFaces.css cuando un documento se guarda con una hoja de estilo externa es decir cuandoExportEmbeddedCss esFALSO . El valor predeterminado esFALSO  todas las reglas CSS se escriben en un único archivo styles.css.
type: docs
weight: 160
url: /es/net/aspose.words.saving/htmlfixedsaveoptions/savefontfacecssseparately/
---
## HtmlFixedSaveOptions.SaveFontFaceCssSeparately property

El indicador indica si las reglas CSS "@font-face" deben colocarse en un archivo separado "fontFaces.css" cuando un documento se guarda con una hoja de estilo externa (es decir, cuando[`ExportEmbeddedCss`](../exportembeddedcss/) es`FALSO` ). El valor predeterminado es`FALSO` , todas las reglas CSS se escriben en un único archivo "styles.css".

```csharp
public bool SaveFontFaceCssSeparately { get; set; }
```

### Observaciones

Establecer esta propiedad en`verdadero` restaura el comportamiento anterior (archivos separados) para compatibilidad con el código heredado.

### Ejemplos

Muestra cómo colocar CSS en un archivo separado y agregar un prefijo a todos sus nombres de clases CSS.

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
* espacio de nombres [Aspose.Words.Saving](../../htmlfixedsaveoptions/)
* asamblea [Aspose.Words](../../../)


