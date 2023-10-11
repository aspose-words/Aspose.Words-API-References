---
title: Class LayoutCollector
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Layout.LayoutCollector clase. Esta clase permite calcular números de página de nodos de documentos.
type: docs
weight: 3320
url: /es/net/aspose.words.layout/layoutcollector/
---
## LayoutCollector class

Esta clase permite calcular números de página de nodos de documentos.

Para obtener más información, visite el[Conversión a formato de página fija](https://docs.aspose.com/words/net/converting-to-fixed-page-format/) artículo de documentación.

```csharp
public class LayoutCollector
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [LayoutCollector](layoutcollector/)(Document) | Inicializa una instancia de esta clase. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Document](../../aspose.words.layout/layoutcollector/document/) { get; set; } | Obtiene o establece el documento al que está adjunta esta instancia de recopilador. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Clear](../../aspose.words.layout/layoutcollector/clear/)() | Borra todos los datos de diseño recopilados. Llame a este método después de que el documento se haya actualizado manualmente o se haya reconstruido el diseño. |
| [GetEndPageIndex](../../aspose.words.layout/layoutcollector/getendpageindex/)(Node) | Obtiene el índice basado en 1 de la página donde termina el nodo. Devuelve 0 si el nodo no se puede asignar a una página. |
| [GetEntity](../../aspose.words.layout/layoutcollector/getentity/)(Node) | Devuelve una posición opaca del[`LayoutEnumerator`](../layoutenumerator/) que corresponde al nodo especificado. Puede utilizar el valor devuelto como argumento para[`Current`](../layoutenumerator/current/) dado que el documento que se está enumerando y el documento del nodo son el mismo. |
| [GetNumPagesSpanned](../../aspose.words.layout/layoutcollector/getnumpagesspanned/)(Node) | Obtiene el número de páginas que abarca el nodo especificado. 0 si el nodo está dentro de una sola página. Esto es lo mismo que[`GetEndPageIndex`](./getendpageindex/) -[`GetStartPageIndex`](./getstartpageindex/) . |
| [GetStartPageIndex](../../aspose.words.layout/layoutcollector/getstartpageindex/)(Node) | Obtiene el índice basado en 1 de la página donde comienza el nodo. Devuelve 0 si el nodo no se puede asignar a una página. |

### Observaciones

Cuando creas un`LayoutCollector` y especificar un[`Document`](../../aspose.words/document/) objeto de documento al que adjuntar, el recopilador registrará la asignación de nodos de documento a objetos de diseño cuando el documento se formatee en páginas.

Podrá averiguar en qué página se encuentra un nodo de documento en particular (por ejemplo, ejecución, párrafo o celda de tabla) utilizando el[`GetStartPageIndex`](./getstartpageindex/) ,[`GetEndPageIndex`](./getendpageindex/) y[`GetNumPagesSpanned`](./getnumpagesspanned/)métodos. Estos métodos crean automáticamente un modelo de diseño de página del documento y actualizan los campos si es necesario.

Cuando ya no necesite recopilar información de diseño, es mejor configurar el[`Document`](./document/) propiedad a`nulo` para evitar la recopilación innecesaria de más asignaciones de diseño.

### Ejemplos

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

* espacio de nombres [Aspose.Words.Layout](../../aspose.words.layout/)
* asamblea [Aspose.Words](../../)


