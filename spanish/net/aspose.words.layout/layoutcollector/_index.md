---
title: LayoutCollector Class
linktitle: LayoutCollector
articleTitle: LayoutCollector
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Layout.LayoutCollector para calcular de manera eficiente los números de página de los nodos del documento, mejorando su experiencia de administración de documentos.
type: docs
weight: 3770
url: /es/net/aspose.words.layout/layoutcollector/
---
## LayoutCollector class

Esta clase permite calcular los números de página de los nodos del documento.

Para obtener más información, visite el[Conversión a formato de página fija](https://docs.aspose.com/words/net/converting-to-fixed-page-format/) Artículo de documentación.

```csharp
public class LayoutCollector
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [LayoutCollector](layoutcollector/)(*[Document](../../aspose.words/document/)*) | Inicializa una instancia de esta clase. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Document](../../aspose.words.layout/layoutcollector/document/) { get; set; } | Obtiene o establece el documento al que está adjunta esta instancia de recopilador. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Clear](../../aspose.words.layout/layoutcollector/clear/)() | Borra todos los datos de diseño recopilados. Llama a este método después de actualizar manualmente el documento o reconstruir el diseño. |
| [GetEndPageIndex](../../aspose.words.layout/layoutcollector/getendpageindex/)(*[Node](../../aspose.words/node/)*) | Obtiene el índice basado en 1 de la página donde termina el nodo. Devuelve 0 si el nodo no se puede asignar a una página. |
| [GetEntity](../../aspose.words.layout/layoutcollector/getentity/)(*[Node](../../aspose.words/node/)*) | Devuelve una posición opaca del[`LayoutEnumerator`](../layoutenumerator/) que corresponde al nodo especificado. Puede usar el valor devuelto como argumento para[`Current`](../layoutenumerator/current/) Dado que el documento que se está enumerando y el documento del nodo son los mismos, |
| [GetNumPagesSpanned](../../aspose.words.layout/layoutcollector/getnumpagesspanned/)(*[Node](../../aspose.words/node/)*) | Obtiene el número de páginas que abarca el nodo especificado. 0 si el nodo está dentro de una sola página. Esto es lo mismo que[`GetEndPageIndex`](./getendpageindex/) -[`GetStartPageIndex`](./getstartpageindex/) . |
| [GetStartPageIndex](../../aspose.words.layout/layoutcollector/getstartpageindex/)(*[Node](../../aspose.words/node/)*) | Obtiene el índice basado en 1 de la página donde comienza el nodo. Devuelve 0 si el nodo no se puede asignar a una página. |

## Observaciones

Cuando creas un`LayoutCollector` y especificar una[`Document`](../../aspose.words/document/)objeto de documento al que adjuntar, el recopilador registrará la asignación de nodos de documento a objetos de diseño cuando el documento se formatee en páginas.

Podrás averiguar en qué página se encuentra un nodo de documento en particular (por ejemplo, una ejecución, un párrafo o una celda de tabla) utilizando el[`GetStartPageIndex`](./getstartpageindex/) ,[`GetEndPageIndex`](./getendpageindex/) y[`GetNumPagesSpanned`](./getnumpagesspanned/) métodos. Estos métodos crean automáticamente el modelo de diseño de página del documento y actualizan los campos si es necesario.

Cuando ya no necesite recopilar información de diseño, es mejor configurar el[`Document`](./document/) propiedad a`nulo` para evitar la recopilación innecesaria de más asignaciones de diseño.

## Ejemplos

Muestra cómo ver los rangos de páginas que abarca un nodo.

```csharp
Document doc = new Document();
LayoutCollector layoutCollector = new LayoutCollector(doc);

// Llame al método "GetNumPagesSpanned" para contar cuántas páginas abarca el contenido de nuestro documento.
//Como el documento está vacío, ese número de páginas actualmente es cero.
Assert.AreEqual(doc, layoutCollector.Document);
Assert.AreEqual(0, layoutCollector.GetNumPagesSpanned(doc));

// Rellene el documento con 5 páginas de contenido.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Section 1");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.SectionBreakEvenPage);
builder.Write("Section 2");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.PageBreak);

// Antes del recopilador de diseño, necesitamos llamar al método "UpdatePageLayout" para obtener
// una cifra precisa para cualquier métrica relacionada con el diseño, como el número de páginas.
Assert.AreEqual(0, layoutCollector.GetNumPagesSpanned(doc));

layoutCollector.Clear();
doc.UpdatePageLayout();

Assert.AreEqual(5, layoutCollector.GetNumPagesSpanned(doc));

//Podemos ver los números de las páginas de inicio y final de cualquier nodo y sus extensiones de página generales.
NodeCollection nodes = doc.GetChildNodes(NodeType.Any, true);
foreach (Node node in nodes)
{
    Console.WriteLine($"->  NodeType.{node.NodeType}: ");
    Console.WriteLine(
        $"\tStarts on page {layoutCollector.GetStartPageIndex(node)}, ends on page {layoutCollector.GetEndPageIndex(node)}," +
        $" spanning {layoutCollector.GetNumPagesSpanned(node)} pages.");
}

// Podemos iterar sobre las entidades de diseño utilizando un LayoutEnumerator.
LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

Assert.AreEqual(LayoutEntityType.Page, layoutEnumerator.Type);

// LayoutEnumerator puede recorrer la colección de entidades de diseño como un árbol.
// También podemos aplicarlo a la entidad de diseño correspondiente de cualquier nodo.
layoutEnumerator.Current = layoutCollector.GetEntity(doc.GetChild(NodeType.Paragraph, 1, true));

Assert.AreEqual(LayoutEntityType.Span, layoutEnumerator.Type);
Assert.AreEqual("¶", layoutEnumerator.Text);
```

### Ver también

* espacio de nombres [Aspose.Words.Layout](../../aspose.words.layout/)
* asamblea [Aspose.Words](../../)
