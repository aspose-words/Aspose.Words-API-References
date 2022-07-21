---
title: ExportRoundtripInformation
second_title: Referencia de API de Aspose.Words para .NET
description: Especifica si se escribe la información de ida y vuelta al guardar en HTML MHTML o EPUB. El valor predeterminado esverdadero para HTML yfalso para MHTML y EPUB.
type: docs
weight: 250
url: /es/net/aspose.words.saving/htmlsaveoptions/exportroundtripinformation/
---
## HtmlSaveOptions.ExportRoundtripInformation property

Especifica si se escribe la información de ida y vuelta al guardar en HTML, MHTML o EPUB. El valor predeterminado es`verdadero` para HTML y`falso` para MHTML y EPUB.

```csharp
public bool ExportRoundtripInformation { get; set; }
```

### Observaciones

Guardar la información de ida y vuelta permite restaurar las propiedades del documento, como las tabulaciones, los comentarios , los encabezados y los pies de página durante la carga de los documentos HTML en un[`Document`](../../../aspose.words/document) objeto.

Cuando`verdadero`, la información de ida y vuelta se exporta como -aw-* CSS properties de los elementos HTML correspondientes.

Cuando`falso`, no genera información de ida y vuelta en los archivos producidos.

### Ejemplos

Muestra cómo conservar elementos ocultos al convertir a .html.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Al convertir un documento a .html, algunos elementos como marcadores ocultos, posiciones de formas originales,
// o las notas al pie se eliminarán o se convertirán en texto sin formato y se perderán efectivamente.
// Guardar con un objeto HtmlSaveOptions con ExportRoundtripInformation establecido en verdadero conservará estos elementos.

// Cuando guardamos el documento en HTML, podemos pasar un objeto SaveOptions para determinar
// cómo la operación de guardado exportará elementos del documento que HTML no admite o no utiliza,
// como marcadores ocultos y posiciones de formas originales.
// Si establecemos el indicador "ExportRoundtripInformation" en "true", la operación de guardado conservará estos elementos.
// Si establecemos el indicador "ExportRoundTripInformation" en "falso", la operación de guardar descartará estos elementos.
// Querremos conservar dichos elementos si tenemos la intención de cargar el HTML guardado usando Aspose.Words,
// ya que podrían ser útiles una vez más.
HtmlSaveOptions options = new HtmlSaveOptions { ExportRoundtripInformation = exportRoundtripInformation };

doc.Save(ArtifactsDir + "HtmlSaveOptions.RoundTripInformation.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.RoundTripInformation.html");
doc = new Document(ArtifactsDir + "HtmlSaveOptions.RoundTripInformation.html");

if (exportRoundtripInformation)
{
    Assert.True(outDocContents.Contains("<div style=\"-aw-headerfooter-type:header-primary; clear:both\">"));
    Assert.True(outDocContents.Contains("<span style=\"-aw-import:ignore\">&#xa0;</span>"));

    Assert.True(outDocContents.Contains(
        "td colspan=\"2\" style=\"width:210.6pt; border-style:solid; border-width:0.75pt 6pt 0.75pt 0.75pt; " +
        "padding-right:2.4pt; padding-left:5.03pt; vertical-align:top; " +
        "-aw-border-bottom:0.5pt single; -aw-border-left:0.5pt single; -aw-border-top:0.5pt single\">"));

    Assert.True(outDocContents.Contains(
        "<li style=\"margin-left:30.2pt; padding-left:5.8pt; -aw-font-family:'Courier New'; -aw-font-weight:normal; -aw-number-format:'o'\">"));

    Assert.True(outDocContents.Contains(
        "<img src=\"HtmlSaveOptions.RoundTripInformation.003.jpeg\" width=\"350\" height=\"180\" alt=\"\" " +
        "style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />"));

    Assert.True(outDocContents.Contains(
        "<span>Page number </span>" +
        "<span style=\"-aw-field-start:true\"></span>" +
        "<span style=\"-aw-field-code:' PAGE   \\\\* MERGEFORMAT '\"></span>" +
        "<span style=\"-aw-field-separator:true\"></span>" +
        "<span>1</span>" +
        "<span style=\"-aw-field-end:true\"></span>"));

    Assert.AreEqual(1, doc.Range.Fields.Count(f => f.Type == FieldType.FieldPage));
}
else
{
    Assert.True(outDocContents.Contains("<div style=\"clear:both\">"));
    Assert.True(outDocContents.Contains("<span>&#xa0;</span>"));

    Assert.True(outDocContents.Contains(
        "<td colspan=\"2\" style=\"width:210.6pt; border-style:solid; border-width:0.75pt 6pt 0.75pt 0.75pt; " +
        "padding-right:2.4pt; padding-left:5.03pt; vertical-align:top\">"));

    Assert.True(outDocContents.Contains(
        "<li style=\"margin-left:30.2pt; padding-left:5.8pt\">"));

    Assert.True(outDocContents.Contains(
        "<img src=\"HtmlSaveOptions.RoundTripInformation.003.jpeg\" width=\"350\" height=\"180\" alt=\"\" />"));

    Assert.True(outDocContents.Contains(
        "<span>Page number 1</span>"));

    Assert.AreEqual(0, doc.Range.Fields.Count(f => f.Type == FieldType.FieldPage));
}
```

### Ver también

* class [HtmlSaveOptions](../../htmlsaveoptions)
* espacio de nombres [Aspose.Words.Saving](../../htmlsaveoptions)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
