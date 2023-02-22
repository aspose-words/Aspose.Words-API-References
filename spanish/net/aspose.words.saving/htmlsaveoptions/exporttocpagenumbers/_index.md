---
title: HtmlSaveOptions.ExportTocPageNumbers
second_title: Referencia de API de Aspose.Words para .NET
description: HtmlSaveOptions propiedad. Especifica si se escriben números de página en la tabla de contenido al guardar HTML MHTML y EPUB. El valor predeterminado esfalso .
type: docs
weight: 280
url: /es/net/aspose.words.saving/htmlsaveoptions/exporttocpagenumbers/
---
## HtmlSaveOptions.ExportTocPageNumbers property

Especifica si se escriben números de página en la tabla de contenido al guardar HTML, MHTML y EPUB. El valor predeterminado es`falso` .

```csharp
public bool ExportTocPageNumbers { get; set; }
```

### Ejemplos

Muestra cómo mostrar los números de página al guardar un documento con una tabla de contenido en .html.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserte una tabla de contenido y luego complete el documento con párrafos formateados usando un "Título"
// estilo que la tabla de contenido recogerá como entradas. Cada entrada mostrará el párrafo de encabezado a la izquierda,
// y el número de página que contiene el encabezado a la derecha.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

builder.ParagraphFormat.Style = builder.Document.Styles["Heading 1"];
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Entry 1");
builder.Writeln("Entry 2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Entry 3");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Entry 4");
fieldToc.UpdatePageNumbers();
doc.UpdateFields();

// Los documentos HTML no tienen páginas. Si guardamos este documento en HTML,
// los números de página que muestra nuestro TOC no tendrán significado.
// Cuando guardamos el documento en HTML, podemos pasar un objeto SaveOptions para omitir estos números de página del TOC.
// Si establecemos el indicador "ExportTocPageNumbers" en "true",
// cada entrada de TOC mostrará el encabezado, el separador y el número de página, conservando su apariencia en Microsoft Word.
// Si establecemos el indicador "ExportTocPageNumbers" en "falso",
// la operación de guardar omitirá tanto el separador como el número de página y dejará intacto el encabezado de cada entrada.
HtmlSaveOptions options = new HtmlSaveOptions { ExportTocPageNumbers = exportTocPageNumbers };

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportTocPageNumbers.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportTocPageNumbers.html");

if (exportTocPageNumbers)
{
    Assert.True(outDocContents.Contains(
        "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
        "<span>Entry 1</span>" +
        "<span style=\"width:428.14pt; font-family:'Lucida Console'; font-size:10pt; display:inline-block; -aw-font-family:'Times New Roman'; " +
        "-aw-tabstop-align:right; -aw-tabstop-leader:dots; -aw-tabstop-pos:469.8pt\">.......................................................................</span>" +
        "<span>2</span>" +
        "</p>"));
}
else
{
    Assert.True(outDocContents.Contains(
        "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
        "<span>Entry 1</span>" +
        "</p>"));
}
```

### Ver también

* class [HtmlSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../htmlsaveoptions/)
* asamblea [Aspose.Words](../../../)


