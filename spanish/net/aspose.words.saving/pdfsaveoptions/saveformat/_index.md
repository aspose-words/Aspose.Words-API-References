---
title: PdfSaveOptions.SaveFormat
second_title: Referencia de API de Aspose.Words para .NET
description: PdfSaveOptions propiedad. Especifica el formato en el que se guardará el documento si se utiliza este objeto de opciones de guardado. Solo se puedePdf .
type: docs
weight: 250
url: /es/net/aspose.words.saving/pdfsaveoptions/saveformat/
---
## PdfSaveOptions.SaveFormat property

Especifica el formato en el que se guardará el documento si se utiliza este objeto de opciones de guardado. Solo se puedePdf .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

### Ejemplos

Muestra cómo limitar el nivel de los encabezados que aparecerán en el esquema de un documento PDF guardado.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insertar encabezados que puedan servir como entradas de TOC de los niveles 1, 2 y luego 3.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

// Crea un objeto "PdfSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar cómo ese método convierte el documento a .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.SaveFormat = SaveFormat.Pdf;

// El documento PDF de salida contendrá un esquema, que es una tabla de contenido que enumera los encabezados en el cuerpo del documento.
// Al hacer clic en una entrada de este esquema, nos llevará a la ubicación de su respectivo encabezado.
// Establezca la propiedad "HeadingsOutlineLevels" en "2" para excluir todos los encabezados cuyos niveles estén por encima de 2 del esquema.
// Los dos últimos encabezados que hemos insertado arriba no aparecerán.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.HeadingsOutlineLevels.pdf", saveOptions);
```

### Ver también

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [PdfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../pdfsaveoptions/)
* asamblea [Aspose.Words](../../../)


