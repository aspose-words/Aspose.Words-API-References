---
title: XpsSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words para .NET
description: Descubra la propiedad SaveFormat de XpsSaveOptions, que define cómo se guarda su documento. ¡Asegure un formato XPS óptimo para una gestión fluida de documentos!
type: docs
weight: 40
url: /es/net/aspose.words.saving/xpssaveoptions/saveformat/
---
## XpsSaveOptions.SaveFormat property

Especifica el formato en el que se guardará el documento si se utiliza este objeto de opciones de guardado. Solo se puedeXps .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## Ejemplos

Muestra cómo limitar el nivel de encabezados que aparecerán en el esquema de un documento XPS guardado.

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

// Crea un objeto "XpsSaveOptions" que podamos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento a .XPS.
XpsSaveOptions saveOptions = new XpsSaveOptions();

Assert.AreEqual(SaveFormat.Xps, saveOptions.SaveFormat);

// El documento XPS de salida contendrá un esquema, una tabla de contenidos que enumera los encabezados en el cuerpo del documento.
// Al hacer clic en una entrada de este esquema accederemos a la ubicación de su encabezado respectivo.
// Establezca la propiedad "HeadingsOutlineLevels" en "2" para excluir del esquema todos los encabezados cuyos niveles sean superiores a 2.
//Los dos últimos encabezados que hemos insertado arriba no aparecerán.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "XpsSaveOptions.OutlineLevels.xps", saveOptions);
```

### Ver también

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [XpsSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
