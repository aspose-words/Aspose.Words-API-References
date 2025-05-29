---
title: HtmlSaveOptions.ExportShapesAsSvg
linktitle: ExportShapesAsSvg
articleTitle: ExportShapesAsSvg
second_title: Aspose.Words para .NET
description: Descubra cómo utilizar HtmlSaveOptions ExportShapesAsSvg para convertir nodos de forma en imágenes SVG al guardar en formatos HTML, MHTML, EPUB o AZW3.
type: docs
weight: 250
url: /es/net/aspose.words.saving/htmlsaveoptions/exportshapesassvg/
---
## HtmlSaveOptions.ExportShapesAsSvg property

Controla si[`Shape`](../../../aspose.words.drawing/shape/)Los nodos se convierten en imágenes SVG al guardar en HTML, MHTML, EPUB o AZW3. El valor predeterminado es`FALSO` .

```csharp
public bool ExportShapesAsSvg { get; set; }
```

## Observaciones

Si esta opción está configurada en`verdadero` ,[`Shape`](../../../aspose.words.drawing/shape/) Los nodos se exportan como elementos &lt;svg&gt;. De lo contrario, se representan en mapas de bits y se exportan como elementos &lt;img&gt;.

## Ejemplos

Muestra cómo exportar formas como gráficos vectoriales escalables.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBox = builder.InsertShape(ShapeType.TextBox, 100.0, 60.0);
builder.MoveTo(textBox.FirstParagraph);
builder.Write("My text box");

// Cuando guardamos el documento en HTML, podemos pasar un objeto SaveOptions
// para determinar cómo la operación de guardado exportará las formas del cuadro de texto.
// Si establecemos el indicador "ExportTextBoxAsSvg" en "verdadero",
// La operación de guardar convertirá las formas con texto en objetos SVG.
// Si establecemos el indicador "ExportTextBoxAsSvg" en "falso",
// La operación de guardar convertirá las formas con texto en imágenes.
HtmlSaveOptions options = new HtmlSaveOptions { ExportShapesAsSvg = exportShapesAsSvg };

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportTextBox.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportTextBox.html");

if (exportShapesAsSvg)
{
    Assert.True(outDocContents.Contains(
        "<span style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\">" +
        "<svg xmlns=\"http://www.w3.org/2000/svg\" xmlns:xlink=\"http://www.w3.org/1999/xlink\" versión=\"1.1\" ancho=\"133\" alto=\"80\">"));
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
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
