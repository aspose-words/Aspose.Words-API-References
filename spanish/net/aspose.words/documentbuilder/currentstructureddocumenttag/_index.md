---
title: DocumentBuilder.CurrentStructuredDocumentTag
linktitle: CurrentStructuredDocumentTag
articleTitle: CurrentStructuredDocumentTag
second_title: Aspose.Words para .NET
description: DocumentBuilder CurrentStructuredDocumentTag propiedad. Obtiene la etiqueta del documento estructurado que está seleccionado actualmente en esteDocumentBuilder  en C#.
type: docs
weight: 80
url: /es/net/aspose.words/documentbuilder/currentstructureddocumenttag/
---
## DocumentBuilder.CurrentStructuredDocumentTag property

Obtiene la etiqueta del documento estructurado que está seleccionado actualmente en este[`DocumentBuilder`](../) .

```csharp
public StructuredDocumentTag CurrentStructuredDocumentTag { get; }
```

## Ejemplos

Muestra cómo mover el cursor de DocumentBuilder dentro de una etiqueta de documento estructurado.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

// Hay varias formas de mover el cursor:
// 1: pasar al primer carácter de la etiqueta del documento estructurado por índice.
builder.MoveToStructuredDocumentTag(1, 1);

// 2 - Pasar al primer carácter de la etiqueta del documento estructurado por objeto.
StructuredDocumentTag tag = (StructuredDocumentTag)doc.GetChild(NodeType.StructuredDocumentTag, 2, true);
builder.MoveToStructuredDocumentTag(tag, 1);
builder.Write(" New text.");

Assert.AreEqual("R New text.ichText", tag.GetText().Trim());

// 3 - Ir al final de la segunda etiqueta del documento estructurado.
builder.MoveToStructuredDocumentTag(1, -1);
Assert.True(builder.IsAtEndOfStructuredDocumentTag);            

// Obtener la etiqueta del documento estructurado seleccionado actualmente.
builder.CurrentStructuredDocumentTag.Color = Color.Green;

doc.Save(ArtifactsDir + "Document.MoveToStructuredDocumentTag.docx");
```

### Ver también

* class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
