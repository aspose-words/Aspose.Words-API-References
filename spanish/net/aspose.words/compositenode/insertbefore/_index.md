---
title: CompositeNode.InsertBefore
linktitle: InsertBefore
articleTitle: InsertBefore
second_title: Aspose.Words para .NET
description: Descubra cómo utilizar el método InsertBefore de CompositeNode para insertar sin problemas nodos antes de los nodos de referencia, mejorando así la gestión de su estructura de datos.
type: docs
weight: 160
url: /es/net/aspose.words/compositenode/insertbefore/
---
## CompositeNode.InsertBefore&lt;T&gt; method

Inserta el nodo especificado inmediatamente antes del nodo de referencia especificado.

```csharp
public T InsertBefore<T>(T newChild, Node refChild)
    where T : Node
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| newChild | T | El[`Node`](../../node/) Insertar. |
| refChild | Node | El[`Node`](../../node/) Ese es el nodo de referencia. El*newChild* se coloca antes de este nodo. |

### Valor_devuelto

El nodo insertado.

## Observaciones

Si*refChild* es`nulo` , insertos*newChild* al final de la lista de nodos secundarios.

Si el*newChild* Ya está en el árbol, primero se elimina.

Si el nodo que se está insertando se creó a partir de otro documento, debe utilizar [`ImportNode`](../../documentbase/importnode/) para importar el nodo al documento actual. Luego, el nodo importado se puede insertar en el documento actual.

## Ejemplos

Muestra cómo agregar, actualizar y eliminar nodos secundarios en la colección de secundarios de un CompositeNode.

```csharp
Document doc = new Document();

// Un documento vacío, por defecto, tiene un párrafo.
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

// Los nodos compuestos, como nuestro párrafo, pueden contener otros nodos compuestos y en línea como hijos.
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
Run paragraphText = new Run(doc, "Initial text. ");
paragraph.AppendChild(paragraphText);

// Crea tres nodos de ejecución más.
Run run1 = new Run(doc, "Run 1. ");
Run run2 = new Run(doc, "Run 2. ");
Run run3 = new Run(doc, "Run 3. ");

// El cuerpo del documento no mostrará estas ejecuciones hasta que las insertemos en un nodo compuesto
// que en sí mismo es una parte del árbol de nodos del documento, como hicimos con la primera ejecución.
//Podemos determinar dónde se encuentra el contenido de texto de los nodos que insertamos
// aparece en el documento al especificar una ubicación de inserción relativa a otro nodo en el párrafo.
Assert.AreEqual("Initial text.", paragraph.GetText().Trim());

// Inserte la segunda ejecución en el párrafo delante de la ejecución inicial.
paragraph.InsertBefore(run2, paragraphText);

Assert.AreEqual("Run 2. Initial text.", paragraph.GetText().Trim());

// Insertar la tercera ejecución después de la ejecución inicial.
paragraph.InsertAfter(run3, paragraphText);

Assert.AreEqual("Run 2. Initial text. Run 3.", paragraph.GetText().Trim());

// Inserta la primera ejecución al inicio de la colección de nodos secundarios del párrafo.
paragraph.PrependChild(run1);

Assert.AreEqual("Run 1. Run 2. Initial text. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(4, paragraph.GetChildNodes(NodeType.Any, true).Count);

//Podemos modificar el contenido de la ejecución editando y eliminando nodos secundarios existentes.
((Run)paragraph.GetChildNodes(NodeType.Run, true)[1]).Text = "Updated run 2. ";
paragraph.GetChildNodes(NodeType.Run, true).Remove(paragraphText);

Assert.AreEqual("Run 1. Updated run 2. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, true).Count);
```

### Ver también

* class [Node](../../node/)
* class [CompositeNode](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
