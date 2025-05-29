---
title: TxtExportHeadersFootersMode Enum
linktitle: TxtExportHeadersFootersMode
articleTitle: TxtExportHeadersFootersMode
second_title: Aspose.Words para .NET
description: Descubra cómo la enumeración TxtExportHeadersFootersMode de Aspose.Words mejora las exportaciones de texto simple al personalizar el manejo del encabezado y pie de página para obtener resultados óptimos.
type: docs
weight: 6440
url: /es/net/aspose.words.saving/txtexportheadersfootersmode/
---
## TxtExportHeadersFootersMode enumeration

Especifica la forma en que se exportan los encabezados y pies de página a formato de texto sin formato.

```csharp
public enum TxtExportHeadersFootersMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | `0` | No se exportan encabezados ni pies de página. |
| PrimaryOnly | `1` | Solo se exportan los encabezados y pies de página principales al principio y al final de cada sección. |
| AllAtEnd | `2` | Todos los encabezados y pies de página se colocan después de todos los cuerpos de sección al final de un documento. |

## Ejemplos

Muestra cómo especificar cómo exportar encabezados y pies de página en formato de texto sin formato.

```csharp
Document doc = new Document();

// Insertar encabezados y pies de página pares y primarios en el documento.
// Los encabezados y pies de página principales anularán los encabezados y pies de página pares.
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.HeaderEven));
doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderEven].AppendParagraph("Even header");
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.FooterEven));
doc.FirstSection.HeadersFooters[HeaderFooterType.FooterEven].AppendParagraph("Even footer");
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.HeaderPrimary));
doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].AppendParagraph("Primary header");
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.FooterPrimary));
doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].AppendParagraph("Primary footer");

// Insertar páginas para mostrar estos encabezados y pies de página.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Page 1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2");
builder.InsertBreak(BreakType.PageBreak); 
builder.Write("Page 3");

// Crea un objeto "TxtSaveOptions", que podemos pasar al método "Guardar" del documento
// para modificar la forma en que guardamos el documento en texto plano.
TxtSaveOptions saveOptions = new TxtSaveOptions();

// Establezca la propiedad "ExportHeadersFootersMode" en "TxtExportHeadersFootersMode.None"
// para no exportar ningún encabezado/pie de página.
// Establezca la propiedad "ExportHeadersFootersMode" en "TxtExportHeadersFootersMode.PrimaryOnly"
// para exportar únicamente encabezados y pies de página principales.
// Establezca la propiedad "ExportHeadersFootersMode" en "TxtExportHeadersFootersMode.AllAtEnd"
// para colocar todos los encabezados y pies de página de todos los cuerpos de sección al final del documento.
saveOptions.ExportHeadersFootersMode = txtExportHeadersFootersMode;

doc.Save(ArtifactsDir + "TxtSaveOptions.ExportHeadersFooters.txt", saveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.ExportHeadersFooters.txt");

string newLine = Environment.NewLine;
switch (txtExportHeadersFootersMode)
{
    case TxtExportHeadersFootersMode.AllAtEnd:
        Assert.AreEqual($"Page 1{newLine}" +
                        $"Page 2{newLine}" +
                        $"Page 3{newLine}" +
                        $"Even header{newLine}{newLine}" +
                        $"Primary header{newLine}{newLine}" +
                        $"Even footer{newLine}{newLine}" +
                        $"Primary footer{newLine}{newLine}", docText);
        break;
    case TxtExportHeadersFootersMode.PrimaryOnly:
        Assert.AreEqual($"Primary header{newLine}" +
                        $"Page 1{newLine}" +
                        $"Page 2{newLine}" +
                        $"Page 3{newLine}" +
                        $"Primary footer{newLine}", docText);
        break;
    case TxtExportHeadersFootersMode.None:
        Assert.AreEqual($"Page 1{newLine}" +
                        $"Page 2{newLine}" +
                        $"Page 3{newLine}", docText);
        break;
}
```

### Ver también

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)
