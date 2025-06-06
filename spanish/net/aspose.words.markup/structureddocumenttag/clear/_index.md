---
title: StructuredDocumentTag.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words para .NET
description: Limpie sin esfuerzo el contenido de la etiqueta de su documento estructurado con el método Borrar y muestre un marcador de posición definido para una mejor gestión de documentos.
type: docs
weight: 360
url: /es/net/aspose.words.markup/structureddocumenttag/clear/
---
## StructuredDocumentTag.Clear method

Borra el contenido de esta etiqueta de documento estructurado y muestra un marcador de posición si está definido.

```csharp
public void Clear()
```

## Observaciones

No es posible borrar el contenido de una etiqueta de documento estructurado si tiene revisiones.

Si esta etiqueta de documento estructurado se asigna a XML personalizado (con el uso de la[`XmlMapping`](../xmlmapping/) propiedad), se borra el nodo XML referenciado.

## Ejemplos

Muestra cómo eliminar el contenido de los elementos de etiquetas de documentos estructurados.

```csharp
Document doc = new Document();

// Cree una etiqueta de documento estructurada de texto simple y luego añádala al documento.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);
doc.FirstSection.Body.AppendChild(tag);

// Esta etiqueta de documento estructurado, que tiene la forma de un cuadro de texto, ya muestra texto de marcador de posición.
Assert.AreEqual("Click here to enter text.", tag.GetText().Trim());
Assert.True(tag.IsShowingPlaceholderText);

// Crea un bloque de construcción con contenido de texto.
GlossaryDocument glossaryDoc = doc.GlossaryDocument;
BuildingBlock substituteBlock = new BuildingBlock(glossaryDoc);
substituteBlock.Name = "My placeholder";
substituteBlock.AppendChild(new Section(glossaryDoc));
substituteBlock.FirstSection.EnsureMinimum();
substituteBlock.FirstSection.Body.FirstParagraph.AppendChild(new Run(glossaryDoc, "Custom placeholder text."));
glossaryDoc.AppendChild(substituteBlock);

// Establezca la propiedad "PlaceholderName" de la etiqueta del documento estructurado en el nombre de nuestro bloque de construcción para obtener
// la etiqueta de documento estructurado para mostrar el contenido del bloque de construcción en lugar del texto predeterminado original.
tag.PlaceholderName = "My placeholder";

Assert.AreEqual("Custom placeholder text.", tag.GetText().Trim());
Assert.True(tag.IsShowingPlaceholderText);

// Edite el texto de la etiqueta del documento estructurado y oculte el texto del marcador de posición.
Run run = (Run)tag.GetChild(NodeType.Run, 0, true);
run.Text = "New text.";
tag.IsShowingPlaceholderText = false;

Assert.AreEqual("New text.", tag.GetText().Trim());

// Utilice el método "Borrar" para borrar el contenido de esta etiqueta de documento estructurado y mostrar el marcador de posición nuevamente.
tag.Clear();

Assert.True(tag.IsShowingPlaceholderText);
Assert.AreEqual("Custom placeholder text.", tag.GetText().Trim());
```

### Ver también

* class [StructuredDocumentTag](../)
* espacio de nombres [Aspose.Words.Markup](../../../aspose.words.markup/)
* asamblea [Aspose.Words](../../../)
