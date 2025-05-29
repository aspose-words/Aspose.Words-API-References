---
title: NodeCollection Class
linktitle: NodeCollection
articleTitle: NodeCollection
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.NodeCollection, su solución ideal para gestionar diversos tipos de nodos de forma eficiente en el procesamiento de documentos. ¡Mejore su flujo de trabajo hoy mismo!
type: docs
weight: 4890
url: /es/net/aspose.words/nodecollection/
---
## NodeCollection class

Representa una colección de nodos de un tipo específico.

Para obtener más información, visite el[Modelo de objetos de documento (DOM) de Aspose.Words](https://docs.aspose.com/words/net/aspose-words-document-object-model/) Artículo de documentación.

```csharp
public class NodeCollection : IEnumerable<Node>
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Obtiene el número de nodos en la colección. |
| [Item](../../aspose.words/nodecollection/item/) { get; } | Recupera un nodo en el índice dado. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../node/)*) | Agrega un nodo al final de la colección. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Elimina todos los nodos de esta colección y del documento. |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../node/)*) | Determina si un nodo está en la colección. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Proporciona una iteración simple al estilo "foreach" sobre la colección de nodos. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../node/)*) | Devuelve el índice basado en cero del nodo especificado. |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../node/)*) | Inserta un nodo en la colección en el índice especificado. |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../node/)*) | Elimina el nodo de la colección y del documento. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | Elimina el nodo en el índice especificado de la colección y del documento. |
| [ToArray](../../aspose.words/nodecollection/toarray/)() | Copia todos los nodos de la colección a una nueva matriz de nodos. |

## Observaciones

`NodeCollection` no posee los nodos que contiene, sino que es solo una selección de nodes del tipo especificado, pero los nodos se almacenan en el árbol bajo sus respectivos nodos padres.

`NodeCollection` Admite acceso indexado, iteración y proporciona métodos de agregar y eliminar.

El`NodeCollection` La colección está "activa", es decir, los cambios en los hijos del nodo object desde el que se creó se reflejan inmediatamente en los nodos devueltos por la colección.`NodeCollection` Propiedades y métodos de .

`NodeCollection` es devuelto por[`GetChildNodes`](../compositenode/getchildnodes/) y también sirve como clase base para colecciones de nodos tipificados como[`SectionCollection`](../sectioncollection/) , [`ParagraphCollection`](../paragraphcollection/) etc.

`NodeCollection`puede ser "plano" y contener sólo los hijos inmediatos del nodo desde el cual fue creado , o puede ser "profundo" y contener todos los hijos descendientes.

## Ejemplos

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
