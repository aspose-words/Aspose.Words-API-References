---
title: NodeType Enum
linktitle: NodeType
articleTitle: NodeType
second_title: Aspose.Words para .NET
description: Aspose.Words.NodeType enumeración. Especifica el tipo de nodo de un documento de Word en C#.
type: docs
weight: 4230
url: /es/net/aspose.words/nodetype/
---
## NodeType enumeration

Especifica el tipo de nodo de un documento de Word.

```csharp
public enum NodeType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Any | `0` | Indica todos los tipos de nodos. Permite seleccionar todos los niños. |
| Document | `1` | A[`Document`](../document/) objeto que, como raíz del árbol del documento, proporciona acceso a todo el documento de Word. |
| Section | `2` | A[`Section`](../section/) objeto que corresponde a una sección de un documento de Word. |
| Body | `3` | A[`Body`](../body/) Objeto que contiene el texto principal de una sección (artículo del texto principal). |
| HeaderFooter | `4` | A[`HeaderFooter`](../headerfooter/) objeto que contiene texto de un encabezado o pie de página particular dentro de una sección. |
| Table | `5` | A[`Table`](../../aspose.words.tables/table/) Objeto que representa una tabla en un documento de Word. |
| Row | `6` | Una fila de una mesa. |
| Cell | `7` | Una celda de una fila de la tabla. |
| Paragraph | `8` | Un párrafo de texto. |
| BookmarkStart | `9` | El comienzo de un marcador de libros. |
| BookmarkEnd | `10` | El final de un marcador de libros. |
| EditableRangeStart | `11` | Un comienzo de un rango editable. |
| EditableRangeEnd | `12` | Un final de un rango editable. |
| MoveFromRangeStart | `13` | Un comienzo de un rango MoveFrom. |
| MoveFromRangeEnd | `14` | El final de un rango MoveFrom. |
| MoveToRangeStart | `15` | Un comienzo de un rango MoveTo. |
| MoveToRangeEnd | `16` | El final de un rango MoveTo. |
| GroupShape | `17` | Un grupo de formas, imágenes, objetos OLE u otras formas grupales. |
| Shape | `18` | Un objeto de dibujo, como una forma, imagen o un objeto OLE de OfficeArt. |
| Comment | `19` | Un comentario en un documento de Word. |
| Footnote | `20` | Una nota al pie o al final de un documento de Word. |
| Run | `21` | Una serie de texto. |
| FieldStart | `22` | Carácter especial que designa el inicio de un campo de Word. |
| FieldSeparator | `23` | Un carácter especial que separa el código de campo del resultado del campo. |
| FieldEnd | `24` | Carácter especial que designa el final de un campo de Word. |
| FormField | `25` | Un campo de formulario. |
| SpecialChar | `26` | Un carácter especial que no es uno de los tipos de caracteres especiales más específicos. |
| SmartTag | `27` | Una etiqueta inteligente alrededor de una o más estructuras en línea (ejecuciones, imágenes, campos, etc.) dentro de un párrafo |
| StructuredDocumentTag | `28` | Permite definir información específica del cliente y sus medios de presentación. |
| StructuredDocumentTagRangeStart | `29` | un comienzo de**a distancia** Etiqueta de documento estructurado que acepta contenido de varias secciones. |
| StructuredDocumentTagRangeEnd | `30` | un fin de**a distancia** Etiqueta de documento estructurado que acepta contenido de varias secciones. |
| GlossaryDocument | `31` | Un documento de glosario dentro del documento principal. |
| BuildingBlock | `32` | Un bloque de construcción dentro de un documento de glosario (por ejemplo, entrada de documento de glosario). |
| CommentRangeStart | `33` | Un nodo marcador que representa el inicio de un rango comentado. |
| CommentRangeEnd | `34` | Un nodo marcador que representa el final de un rango comentado. |
| OfficeMath | `35` | Un objeto de Office Math. Puede ser una ecuación, función, matriz u otro objeto matemático. Puede ser una colección de objetos matemáticos y también puede contener algunos objetos no matemáticos, como series de texto. |
| SubDocument | `36` | Un nodo de subdocumento que es un enlace a otro documento. |
| System | `37` | Reservado para uso interno de Aspose.Words. |
| Null | `38` | Reservado para uso interno de Aspose.Words. |

## Ejemplos

Muestra cómo recorrer la colección de nodos secundarios de un nodo compuesto.

```csharp
Document doc = new Document();

// Agregue dos ejecuciones y una forma como nodos secundarios al primer párrafo de este documento.
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// Tenga en cuenta que 'CustomNodeId' no se guarda en un archivo de salida y existe solo durante la vida útil del nodo.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// Iterar a través de la colección de hijos inmediatos del párrafo,
// e imprimir cualquier corrida o forma que encontremos dentro.
NodeCollection children = paragraph.GetChildNodes(NodeType.Any, false);

Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, false).Count);

foreach (Node child in children)
    switch (child.NodeType)
    {
        case NodeType.Run:
            Console.WriteLine("Run contents:");
            Console.WriteLine($"\t\"{child.GetText().Trim()}\"");
            break;
        case NodeType.Shape:
            Shape childShape = (Shape)child;
            Console.WriteLine("Shape:");
            Console.WriteLine($"\t{childShape.ShapeType}, {childShape.Width}x{childShape.Height}");
            break;
    }
```

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
