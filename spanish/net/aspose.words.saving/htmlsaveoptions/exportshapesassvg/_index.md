---
title: HtmlSaveOptions.ExportShapesAsSvg
second_title: Referencia de API de Aspose.Words para .NET
description: HtmlSaveOptions propiedad. Controla siShape los nodos se convierten en imágenes SVG cuando se guardan en HTML MHTML o EPUB. El valor predeterminado esfalso .
type: docs
weight: 260
url: /es/net/aspose.words.saving/htmlsaveoptions/exportshapesassvg/
---
## HtmlSaveOptions.ExportShapesAsSvg property

Controla si[`Shape`](../../../aspose.words.drawing/shape/) los nodos se convierten en imágenes SVG cuando se guardan en HTML, MHTML o EPUB. El valor predeterminado es`falso` .

```csharp
public bool ExportShapesAsSvg { get; set; }
```

### Observaciones

Si esta opción se establece en`verdadero` ,[`Shape`](../../../aspose.words.drawing/shape/) los nodos se exportan como elementos &lt;svg&gt;. De lo contrario, se representan en mapas de bits y se exportan como elementos &lt;img&gt;.

Tenga en cuenta que esta opción también afecta a los cuadros de texto, ya que están representados por[`Shape`](../../../aspose.words.drawing/shape/) nodes. Como resultado, si esta opción se establece en`verdadero` , anula elExportTextBoxAsSvgproperty value y hace que los cuadros de texto se conviertan a SVG.

### Ejemplos

Muestra cómo exportar formas como gráficos vectoriales escalables.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBox = builder.InsertShape(ShapeType.TextBox, 100.0, 60.0);
builder.MoveTo(textBox.FirstParagraph);
builder.Write("My text box");

// Cuando guardamos el documento en HTML, podemos pasar un objeto SaveOptions
// para determinar cómo la operación de guardado exportará las formas de los cuadros de texto.
// Si establecemos el indicador "ExportTextBoxAsSvg" en "verdadero",
// la operación de guardar convertirá formas con texto en objetos SVG.
// Si establecemos el indicador "ExportTextBoxAsSvg" en "falso",
// la operación de guardar convertirá formas con texto en imágenes.
HtmlSaveOptions options = new HtmlSaveOptions { ExportShapesAsSvg = exportShapesAsSvg };

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportTextBox.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportTextBox.html");

if (exportShapesAsSvg)
{
    Assert.True(outDocContents.Contains(
        "<span style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\">" +
        "<svg xmlns=\"http://www.w3.org/2000/svg\" xmlns:xlink=\"http://www.w3.org/1999/xlink\" version=\"1.1\" width=\"133\" height= \"80\">"));
}
else
{
    Assert.True(outDocContents.Contains(
        "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
            "<img src=\"HtmlSaveOptions.ExportTextBox.001.png\" width=\"136\" height=\"83\" alt=\"\" " +
            "style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" +
        "</p>"));
}
```

### Ver también

* class [HtmlSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../htmlsaveoptions/)
* asamblea [Aspose.Words](../../../)


