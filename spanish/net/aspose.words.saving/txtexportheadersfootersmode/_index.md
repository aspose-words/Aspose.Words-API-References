---
title: Enum TxtExportHeadersFootersMode
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Saving.TxtExportHeadersFootersMode enumeración. Especifica la forma en que se exportan los encabezados y pies de página a formato de texto sin formato.
type: docs
weight: 5640
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
| PrimaryOnly | `1` | Solo se exportan encabezados y pies de página principales al principio y al final de cada sección. |
| AllAtEnd | `2` | Todos los encabezados y pies de página se colocan después de todos los cuerpos de las secciones al final de un documento. |

### Ejemplos

Muestra cómo especificar cómo exportar encabezados y pies de página a formato de texto sin formato.

```csharp
Document doc = new Document();

// Insertar encabezados/pies de página pares y primarios en el documento.
// Los encabezados/pies de página principales anularán los encabezados/pies de página pares.
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

// Crea un objeto "TxtSaveOptions", que podemos pasar al método "Guardar" del documento.
// para modificar cómo guardamos el documento en texto plano.
TxtSaveOptions saveOptions = new TxtSaveOptions();

// Establece la propiedad "ExportHeadersFootersMode" en "TxtExportHeadersFootersMode.None"
// para no exportar ningún encabezado/pie de página.
// Establece la propiedad "ExportHeadersFootersMode" en "TxtExportHeadersFootersMode.PrimaryOnly"
// para exportar solo encabezados/pies de página principales.
// Establece la propiedad "ExportHeadersFootersMode" en "TxtExportHeadersFootersMode.AllAtEnd"
// para colocar todos los encabezados y pies de página de todos los cuerpos de las secciones al final del documento.
saveOptions.ExportHeadersFootersMode = txtExportHeadersFootersMode;

doc.Save(ArtifactsDir + "TxtSaveOptions.ExportHeadersFooters.txt", saveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.ExportHeadersFooters.txt");

switch (txtExportHeadersFootersMode)
{
    case TxtExportHeadersFootersMode.AllAtEnd:
        Assert.AreEqual("Page 1\r\n" +
                        "Page 2\r\n" +
                        "Page 3\r\n" +
                        "Even header\r\n\r\n" +
                        "Primary header\r\n\r\n" +
                        "Even footer\r\n\r\n" +
                        "Primary footer\r\n\r\n", docText);
        break;
    case TxtExportHeadersFootersMode.PrimaryOnly:
        Assert.AreEqual("Primary header\r\n" +
                        "Page 1\r\n" +
                        "Page 2\r\n" +
                        "Page 3\r\n" +
                        "Primary footer\r\n", docText);
        break;
    case TxtExportHeadersFootersMode.None:
        Assert.AreEqual("Page 1\r\n" +
                        "Page 2\r\n" +
                        "Page 3\r\n", docText);
        break;
}
```

### Ver también

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)


