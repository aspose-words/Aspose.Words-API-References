---
title: LayoutEnumerator.Current
linktitle: Current
articleTitle: Current
second_title: Aspose.Words para .NET
description: Descubra la propiedad actual de LayoutEnumerator para acceder y modificar fácilmente la posición actual en su modelo de diseño de página para una mayor flexibilidad de diseño.
type: docs
weight: 20
url: /es/net/aspose.words.layout/layoutenumerator/current/
---
## LayoutEnumerator.Current property

Obtiene o establece la posición actual en el modelo de diseño de página. Esta propiedad devuelve un objeto opaco que corresponde a la entidad de diseño actual.

```csharp
public object Current { get; set; }
```

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

* class [LayoutEnumerator](../)
* espacio de nombres [Aspose.Words.Layout](../../../aspose.words.layout/)
* asamblea [Aspose.Words](../../../)
