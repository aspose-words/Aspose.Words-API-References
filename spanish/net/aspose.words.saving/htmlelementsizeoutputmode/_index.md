---
title: HtmlElementSizeOutputMode Enum
linktitle: HtmlElementSizeOutputMode
articleTitle: HtmlElementSizeOutputMode
second_title: Aspose.Words para .NET
description: Aspose.Words.Saving.HtmlElementSizeOutputMode enumeración. Especifica cómo Aspose.Words exporta anchos y altos de elementos a HTML MHTML y EPUB en C#.
type: docs
weight: 5060
url: /es/net/aspose.words.saving/htmlelementsizeoutputmode/
---
## HtmlElementSizeOutputMode enumeration

Especifica cómo Aspose.Words exporta anchos y altos de elementos a HTML, MHTML y EPUB.

```csharp
public enum HtmlElementSizeOutputMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| All | `0` | Se exportan todos los tamaños de elementos, tanto en unidades absolutas como relativas, especificados en el documento. |
| RelativeOnly | `1` | Los tamaños de los elementos se exportan solo si se especifican en unidades relativas en el documento. Los tamaños fijos no se exportan en este modo. Los agentes visuales calcularán los tamaños faltantes para hacer que el diseño del documento sea más natural. |
| None | `2` | Los tamaños de los elementos no se exportan. Los agentes visuales crearán el diseño automáticamente según la relación entre los elementos. |

## Ejemplos

Muestra cómo conservar sangrías negativas en el archivo .html de salida.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserta una tabla con sangría negativa, lo que la empujará hacia la izquierda más allá del límite izquierdo de la página.
Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1");
builder.InsertCell();
builder.Write("Row 1, Cell 2");
builder.EndTable();
table.LeftIndent = -36;
table.PreferredWidth = PreferredWidth.FromPoints(144);

builder.InsertBreak(BreakType.ParagraphBreak);

// Inserta una tabla con una sangría positiva, lo que empujará la tabla hacia la derecha.
table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1");
builder.InsertCell();
builder.Write("Row 1, Cell 2");
builder.EndTable();
table.LeftIndent = 36;
table.PreferredWidth = PreferredWidth.FromPoints(144);

// Cuando guardamos un documento en HTML, Aspose.Words solo conservará las sangrías negativas
// como el que hemos aplicado a la primera tabla si configuramos el indicador "AllowNegativeIndent"
// en un objeto SaveOptions que pasaremos a "true".
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    AllowNegativeIndent = allowNegativeIndent,
    TableWidthOutputMode = HtmlElementSizeOutputMode.RelativeOnly
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.NegativeIndent.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.NegativeIndent.html");

if (allowNegativeIndent)
{
    Assert.True(outDocContents.Contains(
        "<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:-41.65pt; border:0.75pt solid #000000; -aw-border:0.5pt single; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
    Assert.True(outDocContents.Contains(
        "<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:30.35pt; border:0.75pt solid #000000; -aw-border:0.5pt single; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
}
else
{
    Assert.True(outDocContents.Contains(
        "<table cellspacing=\"0\" cellpadding=\"0\" style=\"border:0.75pt solid #000000; -aw-border:0.5pt single; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
    Assert.True(outDocContents.Contains(
        "<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:30.35pt; border:0.75pt solid #000000; -aw-border:0.5pt single; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
}
```

### Ver también

* property [TableWidthOutputMode](../htmlsaveoptions/tablewidthoutputmode/)
* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)
