---
title: FieldRD.IsPathRelative
linktitle: IsPathRelative
articleTitle: IsPathRelative
second_title: Aspose.Words para .NET
description: Descubra la propiedad IsPathRelative de FieldRD para gestionar fácilmente las rutas de los documentos. Simplifique su codificación con configuraciones de rutas flexibles para una mayor eficiencia.
type: docs
weight: 30
url: /es/net/aspose.words.fields/fieldrd/ispathrelative/
---
## FieldRD.IsPathRelative property

Obtiene o establece si la ruta es relativa al documento actual.

```csharp
public bool IsPathRelative { get; set; }
```

## Ejemplos

Muestra cómo utilizar el campo RD para crear entradas de tabla de contenido a partir de encabezados en otros documentos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Utilice un generador de documentos para insertar una tabla de contenido,
// y luego agregue una entrada para la tabla de contenidos en la página siguiente.
builder.InsertField(FieldType.FieldTOC, true);
builder.InsertBreak(BreakType.PageBreak);
builder.CurrentParagraph.ParagraphFormat.StyleName = "Heading 1";
builder.Writeln("TOC entry from within this document");

// Inserte un campo RD, que hace referencia a otro documento del sistema de archivos local en su propiedad FileName.
// La tabla de contenidos ahora también aceptará todos los encabezados del documento referenciado como entradas para su tabla.
FieldRD field = (FieldRD)builder.InsertField(FieldType.FieldRefDoc, true);
field.FileName = ArtifactsDir + "ReferencedDocument.docx";

Assert.AreEqual($" RD  {ArtifactsDir.Replace(@"\",@"\\")}ReferencedDocument.docx", field.GetFieldCode());

 // Cree el documento al que hace referencia el campo RD e inserte un encabezado.
//Este encabezado aparecerá como una entrada en el campo TOC en nuestro primer documento.
Document referencedDoc = new Document();
DocumentBuilder refDocBuilder = new DocumentBuilder(referencedDoc);
refDocBuilder.CurrentParagraph.ParagraphFormat.StyleName = "Heading 1";
refDocBuilder.Writeln("TOC entry from referenced document");
referencedDoc.Save(ArtifactsDir + "ReferencedDocument.docx");

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.RD.docx");
```

### Ver también

* class [FieldRD](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
