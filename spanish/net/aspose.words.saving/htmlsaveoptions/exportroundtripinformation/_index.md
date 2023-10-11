---
title: HtmlSaveOptions.ExportRoundtripInformation
second_title: Referencia de API de Aspose.Words para .NET
description: HtmlSaveOptions propiedad. Especifica si se escribe la información de ida y vuelta al guardar en HTML MHTML o EPUB. El valor predeterminado esverdadero para HTML yFALSO para MHTML y EPUB.
type: docs
weight: 240
url: /es/net/aspose.words.saving/htmlsaveoptions/exportroundtripinformation/
---
## HtmlSaveOptions.ExportRoundtripInformation property

Especifica si se escribe la información de ida y vuelta al guardar en HTML, MHTML o EPUB. El valor predeterminado es`verdadero` para HTML y`FALSO` para MHTML y EPUB.

```csharp
public bool ExportRoundtripInformation { get; set; }
```

### Observaciones

Guardar la información de ida y vuelta permite restaurar propiedades del documento, como tabulaciones, comentarios , encabezados y pies de página durante la carga de documentos HTML nuevamente en un[`Document`](../../../aspose.words/document/) objeto.

Cuando`verdadero`, la información de ida y vuelta se exporta como -aw-* CSS properties de los elementos HTML correspondientes.

Cuando`FALSO`, hace que no se envíe información de ida y vuelta a los archivos producidos.

### Ejemplos

Muestra cómo conservar elementos ocultos al convertir a .html.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Al convertir un documento a .html, algunos elementos como marcadores ocultos, posiciones de formas originales,
// o las notas a pie de página se eliminarán o se convertirán a texto sin formato y, efectivamente, se perderán.
// Guardar con un objeto HtmlSaveOptions con ExportRoundtripInformation establecido en verdadero preservará estos elementos.

// Cuando guardamos el documento en HTML, podemos pasar un objeto SaveOptions para determinar
// cómo la operación de guardar exportará elementos del documento que HTML no admite ni utiliza,
// como marcadores ocultos y posiciones de formas originales.
// Si configuramos el indicador "ExportRoundtripInformation" en "verdadero", la operación de guardar preservará estos elementos.
// Si configuramos el indicador "ExportRoundTripInformation" en "falso", la operación de guardar descartará estos elementos.
// Querremos conservar dichos elementos si pretendemos cargar el HTML guardado usando Aspose.Words,
// ya que podrían ser de utilidad una vez más.
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

* class [HtmlSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../htmlsaveoptions/)
* asamblea [Aspose.Words](../../../)


