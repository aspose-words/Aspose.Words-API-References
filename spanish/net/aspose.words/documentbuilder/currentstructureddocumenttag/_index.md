---
title: DocumentBuilder.CurrentStructuredDocumentTag
linktitle: CurrentStructuredDocumentTag
articleTitle: CurrentStructuredDocumentTag
second_title: Aspose.Words para .NET
description: Descubra la propiedad CurrentStructuredDocumentTag en DocumentBuilder. Acceda fácilmente a la etiqueta del documento estructurado seleccionado para una gestión eficiente de documentos.
type: docs
weight: 80
url: /es/net/aspose.words/documentbuilder/currentstructureddocumenttag/
---
## DocumentBuilder.CurrentStructuredDocumentTag property

Obtiene la etiqueta del documento estructurado que está seleccionada actualmente en este[`DocumentBuilder`](../) .

```csharp
public StructuredDocumentTag CurrentStructuredDocumentTag { get; }
```

## Ejemplos

Muestra cómo mover el cursor de DocumentBuilder dentro de una etiqueta de documento estructurado.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

// Hay varias formas de mover el cursor:
// 1 - Moverse al primer carácter de la etiqueta del documento estructurado por índice.
builder.MoveToStructuredDocumentTag(1, 1);

// 2 - Moverse al primer carácter de la etiqueta del documento estructurado por objeto.
StructuredDocumentTag tag = (StructuredDocumentTag)doc.GetChild(NodeType.StructuredDocumentTag, 2, true);
builder.MoveToStructuredDocumentTag(tag, 1);
builder.Write(" New text.");

Assert.AreEqual("R New text.ichText", tag.GetText().Trim());

// 3 - Moverse al final de la segunda etiqueta del documento estructurado.
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
