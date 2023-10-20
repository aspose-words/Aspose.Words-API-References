---
title: Node.ParentNode
linktitle: ParentNode
articleTitle: ParentNode
second_title: Aspose.Words para .NET
description: Node ParentNode propiedad. Obtiene el padre inmediato de este nodo en C#.
type: docs
weight: 60
url: /es/net/aspose.words/node/parentnode/
---
## Node.ParentNode property

Obtiene el padre inmediato de este nodo.

```csharp
public CompositeNode ParentNode { get; }
```

## Observaciones

Si se acaba de crear un nodo y aún no se ha agregado al árbol, o si se ha eliminado del árbol, el padre es`nulo`.

## Ejemplos

Muestra cómo acceder al nodo principal de un nodo.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Agrega un nodo Ejecutar secundario al primer párrafo del documento.
Run run = new Run(doc, "Hello world!");
para.AppendChild(run);

// El párrafo es el nodo padre del nodo de ejecución. Podemos rastrear este linaje.
// hasta llegar al nodo del documento, que es la raíz del árbol de nodos del documento.
Assert.AreEqual(para, run.ParentNode);
Assert.AreEqual(doc.FirstSection.Body, para.ParentNode);
Assert.AreEqual(doc.FirstSection, doc.FirstSection.Body.ParentNode);
Assert.AreEqual(doc, doc.FirstSection.ParentNode);
```

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

* class [CompositeNode](../../compositenode/)
* class [Node](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
