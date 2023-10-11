---
title: Node.Document
second_title: Referencia de API de Aspose.Words para .NET
description: Node propiedad. Obtiene el documento al que pertenece este nodo.
type: docs
weight: 20
url: /es/net/aspose.words/node/document/
---
## Node.Document property

Obtiene el documento al que pertenece este nodo.

```csharp
public virtual DocumentBase Document { get; }
```

### Observaciones

El nodo siempre pertenece a un documento incluso si acaba de crearse y aún no se ha agregado al árbol, o si se ha eliminado del árbol.

### Ejemplos

Muestra cómo crear un nodo y configurar su documento propietario.

```csharp
Document doc = new Document();
Paragraph para = new Paragraph(doc);
para.AppendChild(new Run(doc, "Hello world!"));

// Todavía no hemos agregado este párrafo como hijo a ningún nodo compuesto.
Assert.IsNull(para.ParentNode);

// Si un nodo es un tipo de nodo secundario apropiado de otro nodo compuesto,
// podemos adjuntarlo como hijo solo si ambos nodos tienen el mismo documento de propietario.
// El documento propietario es el documento que pasamos al constructor del nodo.
// No hemos adjuntado este párrafo al documento, por lo que el documento no contiene su texto.
Assert.AreEqual(para.Document, doc);
Assert.AreEqual(string.Empty, doc.GetText().Trim());

// Dado que el documento es propietario de este párrafo, podemos aplicar uno de sus estilos al contenido del párrafo.
para.ParagraphFormat.Style = doc.Styles["Heading 1"];

// Agregue este nodo al documento y luego verifique su contenido.
doc.FirstSection.Body.AppendChild(para);

Assert.AreEqual(doc.FirstSection.Body, para.ParentNode);
Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Ver también

* class [DocumentBase](../../documentbase/)
* class [Node](../)
* espacio de nombres [Aspose.Words](../../node/)
* asamblea [Aspose.Words](../../../)


