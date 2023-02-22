---
title: XpsSaveOptions.OutlineOptions
second_title: Referencia de API de Aspose.Words para .NET
description: XpsSaveOptions propiedad. Permite especificar opciones de contorno.
type: docs
weight: 20
url: /es/net/aspose.words.saving/xpssaveoptions/outlineoptions/
---
## XpsSaveOptions.OutlineOptions property

Permite especificar opciones de contorno.

```csharp
public OutlineOptions OutlineOptions { get; }
```

### Observaciones

Tenga en cuenta que la opción ExpandedOutlineLevels no funcionará al guardar en XPS.

### Ejemplos

Muestra cómo limitar el nivel de los encabezados que aparecerán en el esquema de un documento XPS guardado.

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

// Crea un objeto "XpsSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar cómo ese método convierte el documento a .XPS.
XpsSaveOptions saveOptions = new XpsSaveOptions();

Assert.AreEqual(SaveFormat.Xps, saveOptions.SaveFormat);

// El documento XPS de salida contendrá un esquema, una tabla de contenido que enumera los encabezados en el cuerpo del documento.
// Al hacer clic en una entrada de este esquema, nos llevará a la ubicación de su respectivo encabezado.
// Establezca la propiedad "HeadingsOutlineLevels" en "2" para excluir todos los encabezados cuyos niveles estén por encima de 2 del esquema.
// Los dos últimos encabezados que hemos insertado arriba no aparecerán.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "XpsSaveOptions.OutlineLevels.xps", saveOptions);
```

### Ver también

* class [OutlineOptions](../../outlineoptions/)
* class [XpsSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../xpssaveoptions/)
* asamblea [Aspose.Words](../../../)


