---
title: DocumentBuilder.CurrentStory
linktitle: CurrentStory
articleTitle: CurrentStory
second_title: Aspose.Words para .NET
description: Descubra la propiedad CurrentStory de DocumentBuilder para acceder y administrar la historia seleccionada de manera eficiente, mejorando su experiencia de edición de documentos.
type: docs
weight: 70
url: /es/net/aspose.words/documentbuilder/currentstory/
---
## DocumentBuilder.CurrentStory property

Obtiene la historia que está seleccionada actualmente en este[`DocumentBuilder`](../) .

```csharp
public Story CurrentStory { get; }
```

## Ejemplos

Muestra cómo trabajar con la historia actual de un generador de documentos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Una historia es un tipo de nodo que tiene nodos de párrafo secundarios, como un cuerpo.
Assert.AreEqual(builder.CurrentStory, doc.FirstSection.Body);
Assert.AreEqual(builder.CurrentStory, builder.CurrentParagraph.ParentNode);
Assert.AreEqual(StoryType.MainText, builder.CurrentStory.StoryType);

builder.CurrentStory.AppendParagraph("Text added to current Story.");

//Una historia también puede contener tablas.
Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1");
builder.InsertCell();
builder.Write("Row 1, cell 2");
builder.EndTable();

Assert.IsTrue(builder.CurrentStory.Tables.Contains(table));
```

### Ver también

* class [Story](../../story/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
