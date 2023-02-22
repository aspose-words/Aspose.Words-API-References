---
title: HtmlSaveOptions.TableWidthOutputMode
second_title: Referencia de API de Aspose.Words para .NET
description: HtmlSaveOptions propiedad. Controla cómo se exportan los anchos de tabla fila y celda a HTML MHTML o EPUB. El valor predeterminado esAll .
type: docs
weight: 460
url: /es/net/aspose.words.saving/htmlsaveoptions/tablewidthoutputmode/
---
## HtmlSaveOptions.TableWidthOutputMode property

Controla cómo se exportan los anchos de tabla, fila y celda a HTML, MHTML o EPUB. El valor predeterminado esAll .

```csharp
public HtmlElementSizeOutputMode TableWidthOutputMode { get; set; }
```

### Observaciones

En el formato HTML, los elementos de tabla, fila y celda ( **&lt;tabla&gt;** , **&lt;tr&gt;** , **&lt;th&gt;** , **&lt;td&gt;**) pueden tener sus anchos especificados en unidades relativas (porcentaje) o absolutas. En un documento en Aspose.Words, tablas, filas y celdas pueden tener sus anchos especificados usando unidades relativas o absolutas también.

Cuando convierte un documento a HTML usando Aspose.Words, es posible que desee controlar cómo se exportan los anchos de tabla, fila y celda para afectar cómo se muestra el documento resultante en el agente visual (por ejemplo, un navegador o visor).

Utilice esta propiedad como filtro para especificar qué valores de ancho de tabla se exportan al documento de destino. Por ejemplo, si está convirtiendo un documento a EPUB y tiene la intención de verlo en un dispositivo de lectura móvil, , entonces probablemente desee evitar exportar valores de ancho absolutos. Para hacer esto, debe especificar el modo de salidaRelativeOnly oNone para que el espectador en el dispositivo móvil pueda diseñar la tabla para que se ajuste al ancho de la pantalla lo mejor que pueda.

### Ejemplos

Muestra cómo conservar las sangrías negativas en el .html de salida.

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
// como el que hemos aplicado a la primera tabla si ponemos el flag "AllowNegativeIndent"
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

* enum [HtmlElementSizeOutputMode](../../htmlelementsizeoutputmode/)
* class [HtmlSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../htmlsaveoptions/)
* asamblea [Aspose.Words](../../../)


