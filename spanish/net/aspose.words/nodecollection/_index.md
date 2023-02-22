---
title: Class NodeCollection
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.NodeCollection clase. Representa una colección de nodos de un tipo específico.
type: docs
weight: 3960
url: /es/net/aspose.words/nodecollection/
---
## NodeCollection class

Representa una colección de nodos de un tipo específico.

```csharp
public class NodeCollection : IEnumerable<Node>
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Obtiene el número de nodos de la colección. |
| [Item](../../aspose.words/nodecollection/item/) { get; } | Recupera un nodo en el índice dado. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(Node) | Agrega un nodo al final de la colección. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Elimina todos los nodos de esta colección y del documento. |
| [Contains](../../aspose.words/nodecollection/contains/)(Node) | Determina si un nodo está en la colección. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Proporciona una iteración de estilo "foreach" simple sobre la colección de nodos. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(Node) | Devuelve el índice de base cero del nodo especificado. |
| [Insert](../../aspose.words/nodecollection/insert/)(int, Node) | Inserta un nodo en la colección en el índice especificado. |
| [Remove](../../aspose.words/nodecollection/remove/)(Node) | Elimina el nodo de la colección y del documento. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(int) | Elimina el nodo en el índice especificado de la colección y del documento. |
| [ToArray](../../aspose.words/nodecollection/toarray/)() | Copia todos los nodos de la colección a una nueva matriz de nodos. |

### Observaciones

**Colección de nodos** no posee los nodos que contiene, sino que es solo una selección de nodes del tipo especificado, pero los nodos se almacenan en el árbol bajo sus respectivos nodos principales.

**Colección de nodos**admite el acceso indexado, la iteración y proporciona métodos para agregar y eliminar.

los **Colección de nodos** la colección está "viva", es decir, los cambios en los elementos secundarios del nodo object a partir del cual se creó se reflejan inmediatamente en los nodos devueltos por el **Colección de nodos** propiedades y métodos.

**Colección de nodos** es devuelto por[`GetChildNodes`](../compositenode/getchildnodes/) y también sirve como clase base para colecciones de nodos tipificados como[`SectionCollection`](../sectioncollection/) , [`ParagraphCollection`](../paragraphcollection/) etc.

**Colección de nodos** puede ser "plano" y contener solo elementos secundarios inmediatos del nodo desde el que se creó , o puede ser "profundo" y contener todos los elementos secundarios descendientes.

### Ejemplos

Muestra cómo reemplazar todas las formas de cuadro de texto con formas de imagen.

```csharp
Document doc = new Document(MyDir + "Textboxes in drawing canvas.docx");

Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(3, shapes.Count(s => s.ShapeType == ShapeType.TextBox));
Assert.AreEqual(1, shapes.Count(s => s.ShapeType == ShapeType.Image));

foreach (Shape shape in shapes)
{
    if (shape.ShapeType == ShapeType.TextBox)
    {
        Shape replacementShape = new Shape(doc, ShapeType.Image);
        replacementShape.ImageData.SetImage(ImageDir + "Logo.jpg");
        replacementShape.Left = shape.Left;
        replacementShape.Top = shape.Top;
        replacementShape.Width = shape.Width;
        replacementShape.Height = shape.Height;
        replacementShape.RelativeHorizontalPosition = shape.RelativeHorizontalPosition;
        replacementShape.RelativeVerticalPosition = shape.RelativeVerticalPosition;
        replacementShape.HorizontalAlignment = shape.HorizontalAlignment;
        replacementShape.VerticalAlignment = shape.VerticalAlignment;
        replacementShape.WrapType = shape.WrapType;
        replacementShape.WrapSide = shape.WrapSide;

        shape.ParentNode.InsertAfter(replacementShape, shape);
        shape.Remove();
    }
}

shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(0, shapes.Count(s => s.ShapeType == ShapeType.TextBox));
Assert.AreEqual(4, shapes.Count(s => s.ShapeType == ShapeType.Image));

doc.Save(ArtifactsDir + "Shape.ReplaceTextboxesWithImages.docx");
```

### Ver también

* class [Node](../node/)
* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)


