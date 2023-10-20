---
title: LayoutCollector.GetEntity
linktitle: GetEntity
articleTitle: GetEntity
second_title: Aspose.Words para .NET
description: LayoutCollector GetEntity método. Devuelve una posición opaca delLayoutEnumerator que corresponde al nodo especificado. Puede utilizar el valor devuelto como argumento paraCurrent dado que el documento que se está enumerando y el documento del nodo son el mismo en C#.
type: docs
weight: 50
url: /es/net/aspose.words.layout/layoutcollector/getentity/
---
## LayoutCollector.GetEntity method

Devuelve una posición opaca del[`LayoutEnumerator`](../../layoutenumerator/) que corresponde al nodo especificado. Puede utilizar el valor devuelto como argumento para[`Current`](../../layoutenumerator/current/) dado que el documento que se está enumerando y el documento del nodo son el mismo.

```csharp
public object GetEntity(Node node)
```

## Observaciones

Este método funciona sólo para[`Paragraph`](../../../aspose.words/paragraph/) nodos, así como nodos en línea indivisibles, por ejemplo[`BookmarkStart`](../../../aspose.words/bookmarkstart/) o[`Shape`](../../../aspose.words.drawing/shape/) . No funciona para[`Run`](../../../aspose.words/run/) ,[`Cell`](../../../aspose.words.tables/cell/)[`Row`](../../../aspose.words.tables/row/) o[`Table`](../../../aspose.words.tables/table/) nodos y nodos dentro del encabezado/pie de página.

Tenga en cuenta que la entidad regresó por un[`Paragraph`](../../../aspose.words/paragraph/) El nodo es un intervalo de salto de párrafo. Utilice el método apropiado para ascender a la línea principal.

Si necesita navegar a un[`Run`](../../../aspose.words/run/) de texto, puede insertar un marcador justo antes de it y luego navegar hasta el marcador.

Si necesita navegar a un[`Cell`](../../../aspose.words.tables/cell/) nodo entonces puedes moverte a un[`Paragraph`](../../../aspose.words/paragraph/) nodo en esta celda y luego ascender a una entidad principal. El mismo enfoque se puede utilizar para[`Row`](../../../aspose.words.tables/row/) y[`Table`](../../../aspose.words.tables/table/) nodos.

## Ejemplos

Muestra cómo ver los rangos de páginas que abarca un nodo.

```csharp
Document doc = new Document();
LayoutCollector layoutCollector = new LayoutCollector(doc);

// Llama al método "GetNumPagesSpanned" para contar cuántas páginas abarca el contenido de nuestro documento.
// Dado que el documento está vacío, ese número de páginas actualmente es cero.
Assert.AreEqual(doc, layoutCollector.Document);
Assert.AreEqual(0, layoutCollector.GetNumPagesSpanned(doc));

// Complete el documento con 5 páginas de contenido.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Section 1");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.SectionBreakEvenPage);
builder.Write("Section 2");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.PageBreak);

// Antes del recopilador de diseño, debemos llamar al método "UpdatePageLayout" para obtener
// una cifra precisa para cualquier métrica relacionada con el diseño, como el recuento de páginas.
Assert.AreEqual(0, layoutCollector.GetNumPagesSpanned(doc));

layoutCollector.Clear();
doc.UpdatePageLayout();

Assert.AreEqual(5, layoutCollector.GetNumPagesSpanned(doc));

// Podemos ver los números de las páginas inicial y final de cualquier nodo y su extensión total de páginas.
NodeCollection nodes = doc.GetChildNodes(NodeType.Any, true);
foreach (Node node in nodes)
{
    Console.WriteLine($"->  NodeType.{node.NodeType}: ");
    Console.WriteLine(
        $"\tStarts on page {layoutCollector.GetStartPageIndex(node)}, ends on page {layoutCollector.GetEndPageIndex(node)}," +
        $" spanning {layoutCollector.GetNumPagesSpanned(node)} pages.");
}

// Podemos iterar sobre las entidades de diseño usando un LayoutEnumerator.
LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

Assert.AreEqual(LayoutEntityType.Page, layoutEnumerator.Type);

// LayoutEnumerator puede atravesar la colección de entidades de diseño como un árbol.
// También podemos aplicarlo a la entidad de diseño correspondiente de cualquier nodo.
layoutEnumerator.Current = layoutCollector.GetEntity(doc.GetChild(NodeType.Paragraph, 1, true));

Assert.AreEqual(LayoutEntityType.Span, layoutEnumerator.Type);
Assert.AreEqual("¶", layoutEnumerator.Text);
```

### Ver también

* class [Node](../../../aspose.words/node/)
* class [LayoutCollector](../)
* espacio de nombres [Aspose.Words.Layout](../../../aspose.words.layout/)
* asamblea [Aspose.Words](../../../)
