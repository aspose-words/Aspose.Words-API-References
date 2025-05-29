---
title: DocumentBuilder.MoveToStructuredDocumentTag
linktitle: MoveToStructuredDocumentTag
articleTitle: MoveToStructuredDocumentTag
second_title: Aspose.Words para .NET
description: Navegue sin esfuerzo a las etiquetas de documentos estructurados con el método MoveToStructuredDocumentTag de DocumentBuilder, mejorando la eficiencia de la edición de sus documentos.
type: docs
weight: 620
url: /es/net/aspose.words/documentbuilder/movetostructureddocumenttag/
---
## MoveToStructuredDocumentTag(*int, int*) {#movetostructureddocumenttag_1}

Mueve el cursor a una etiqueta de documento estructurado en la sección actual.

```csharp
public void MoveToStructuredDocumentTag(int structuredDocumentTagIndex, int characterIndex)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| structuredDocumentTagIndex | Int32 | El índice de la etiqueta del documento estructurado al que se desea mover. |
| characterIndex | Int32 | Índice del carácter dentro de la etiqueta del documento estructurado. Un valor negativo permite especificar una posición desde el final de la etiqueta. Use -1 para ir al final de la etiqueta. Si la etiqueta está a nivel de bloque y desea mover el cursor al final de su último párrafo, especifique -2. |

## Observaciones

La navegación se realiza dentro de la historia actual de la sección actual. Es decir, si movió el cursor al encabezado principal de la primera sección, entonces*structuredDocumentTagIndex* especificó el índice de la etiqueta del documento estructurado dentro del encabezado de esa sección.

Cuando*structuredDocumentTagIndex* es mayor o igual a 0, especifica un índice desde el inicio de la sección, siendo 0 la primera etiqueta de documento estructurado. Cuando *structuredDocumentTagIndex*es menor que 0, especifica un índice desde el final de la sección donde -1 es la última etiqueta del documento estructurado.

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

* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## MoveToStructuredDocumentTag(*[StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/), int*) {#movetostructureddocumenttag}

Mueve el cursor a la etiqueta del documento estructurado.

```csharp
public void MoveToStructuredDocumentTag(StructuredDocumentTag structuredDocumentTag, 
    int characterIndex)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| structuredDocumentTag | StructuredDocumentTag | La etiqueta del documento estructurado a la que moverse. |
| characterIndex | Int32 | Índice del carácter dentro de la etiqueta del documento estructurado. Un valor negativo permite especificar una posición desde el final de la etiqueta. Use -1 para ir al final de la etiqueta. Si la etiqueta está a nivel de bloque y desea mover el cursor al final de su último párrafo, especifique -2. |

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
