---
title: Document.LastSection
linktitle: LastSection
articleTitle: LastSection
second_title: Aspose.Words para .NET
description: Descubra la propiedad LastSection para acceder fácilmente a la sección final de su documento, mejorando la navegación y la eficiencia de la gestión de contenido.
type: docs
weight: 250
url: /es/net/aspose.words/document/lastsection/
---
## Document.LastSection property

Obtiene la última sección del documento.

```csharp
public Section LastSection { get; }
```

## Observaciones

Devuelve`nulo`si no hay secciones.

## Ejemplos

Muestra cómo crear una nueva sección con un generador de documentos.

```csharp
Document doc = new Document();

// Un documento en blanco contiene una sección por defecto,
// que contiene nodos secundarios que podemos editar.
Assert.AreEqual(1, doc.Sections.Count);

// Utilice un generador de documentos para agregar texto a la primera sección.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Crea una segunda sección insertando un salto de sección.
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.AreEqual(2, doc.Sections.Count);

//Cada sección tiene su propia configuración de página.
//Podemos dividir el texto de la segunda sección en dos columnas.
// Esto no afectará el texto de la primera sección.
doc.LastSection.PageSetup.TextColumns.SetCount(2);
builder.Writeln("Column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Column 2.");

Assert.AreEqual(1, doc.FirstSection.PageSetup.TextColumns.Count);
Assert.AreEqual(2, doc.LastSection.PageSetup.TextColumns.Count);

doc.Save(ArtifactsDir + "Section.Create.docx");
```

### Ver también

* class [Section](../../section/)
* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
