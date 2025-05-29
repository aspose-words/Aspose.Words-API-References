---
title: NodeType Enum
linktitle: NodeType
articleTitle: NodeType
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.NodeType para identificar y administrar fácilmente diferentes tipos de nodos de documentos de Word para un procesamiento perfecto de documentos.
type: docs
weight: 4920
url: /es/net/aspose.words/nodetype/
---
## NodeType enumeration

Especifica el tipo de un nodo de documento de Word.

```csharp
public enum NodeType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Any | `0` | Indica todos los tipos de nodos. Permite seleccionar todos los hijos. |
| Document | `1` | A[`Document`](../document/) objeto que, como raíz del árbol del documento, proporciona acceso a todo el documento de Word. |
| Section | `2` | A[`Section`](../section/) objeto que corresponde a una sección de un documento de Word. |
| Body | `3` | A[`Body`](../body/) objeto que contiene el texto principal de una sección (historia del texto principal). |
| HeaderFooter | `4` | A[`HeaderFooter`](../headerfooter/) objeto que contiene el texto de un encabezado o pie de página particular dentro de una sección. |
| Table | `5` | A[`Table`](../../aspose.words.tables/table/) objeto que representa una tabla en un documento de Word. |
| Row | `6` | Una fila de una mesa. |
| Cell | `7` | Una celda de una fila de la tabla. |
| Paragraph | `8` | Un párrafo de texto. |
| BookmarkStart | `9` | Un comienzo de un marcador de página. |
| BookmarkEnd | `10` | Un extremo de un marcador de página. |
| EditableRangeStart | `11` | Un comienzo de una gama editable. |
| EditableRangeEnd | `12` | Un final de un rango editable. |
| MoveFromRangeStart | `13` | Un comienzo de un rango MoveFrom. |
| MoveFromRangeEnd | `14` | Un final de un rango MoveFrom. |
| MoveToRangeStart | `15` | Un comienzo de una gama MoveTo. |
| MoveToRangeEnd | `16` | Un final de un rango MoveTo. |
| GroupShape | `17` | Un grupo de formas, imágenes, objetos OLE u otras formas de grupo. |
| Shape | `18` | Un objeto de dibujo, como una forma de OfficeArt, una imagen o un objeto OLE. |
| Comment | `19` | Un comentario en un documento de Word. |
| Footnote | `20` | Una nota al pie o nota final en un documento de Word. |
| Run | `21` | Una serie de textos. |
| FieldStart | `22` | Un carácter especial que designa el inicio de un campo de Word. |
| FieldSeparator | `23` | Un carácter especial que separa el código de campo del resultado del campo. |
| FieldEnd | `24` | Un carácter especial que designa el final de un campo de Word. |
| FormField | `25` | Un campo de formulario. |
| SpecialChar | `26` | Un carácter especial que no es uno de los tipos de caracteres especiales más específicos. |
| SmartTag | `27` | Una etiqueta inteligente alrededor de una o más estructuras en línea (ejecuciones, imágenes, campos, etc.) dentro de un párrafo |
| StructuredDocumentTag | `28` | Permite definir información específica del cliente y su medio de presentación. |
| StructuredDocumentTagRangeStart | `29` | Un comienzo de**a distancia** Etiqueta de documento estructurado que acepta contenido de varias secciones. |
| StructuredDocumentTagRangeEnd | `30` | Un fin de**a distancia** Etiqueta de documento estructurado que acepta contenido de varias secciones. |
| GlossaryDocument | `31` | Un documento de glosario dentro del documento principal. |
| BuildingBlock | `32` | Un bloque de construcción dentro de un documento de glosario (por ejemplo, una entrada de documento de glosario). |
| CommentRangeStart | `33` | Un nodo marcador que representa el inicio de un rango comentado. |
| CommentRangeEnd | `34` | Un nodo marcador que representa el final de un rango comentado. |
| OfficeMath | `35` | Un objeto de Office Math. Puede ser una ecuación, una función, una matriz o cualquier otro objeto matemático. Puede ser una colección de objetos matemáticos y también contener objetos no matemáticos, como secuencias de texto. |
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
// Tenga en cuenta que 'CustomNodeId' no se guarda en un archivo de salida y solo existe durante la vida útil del nodo.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// Iterar a través de la colección de hijos inmediatos del párrafo,
// e imprimir cualquier recorrido o forma que encontremos dentro.
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
