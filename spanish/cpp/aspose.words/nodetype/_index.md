---
title: "Aspose::Words::NodeType enumeración"
linktitle: "NodeType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::NodeType enum. Especifica el tipo de un nodo de documento Word en C++."
type: docs
weight: 102000
url: /es/cpp/aspose.words/nodetype/
---
## NodeType enum


Especifica el tipo de un nodo de documento Word.

```cpp
enum class NodeType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Cualquiera | 0 | Indica todos los tipos de nodo. Permite seleccionar todos los hijos. |
| Document | 1 | Un objeto [Document](../document/) que, como la raíz del árbol del documento, proporciona acceso a todo el documento Word. Un nodo [Document](../document/) puede tener nodos [Section](../section/). |
| Section | 2 | Un objeto [Section](../section/) que corresponde a una sección en un documento Word. Un nodo [Section](../section/) puede tener nodos [Body](../body/) y [HeaderFooter](../headerfooter/). |
| Body | 3 | Un objeto [Body](../body/) que contiene el texto principal de una sección (historia de texto principal). Un nodo [Body](../body/) puede tener nodos [Paragraph](../paragraph/) y [Table](../../aspose.words.tables/table/). |
| HeaderFooter | 4 | Un objeto [HeaderFooter](../headerfooter/) que contiene el texto de un encabezado o pie de página particular dentro de una sección. Un nodo [HeaderFooter](../headerfooter/) puede tener nodos [Paragraph](../paragraph/) y [Table](../../aspose.words.tables/table/). |
| Table | 5 | Un objeto [Table](../../aspose.words.tables/table/) que representa una tabla en un documento Word. Un nodo [Table](../../aspose.words.tables/table/) puede tener nodos [Row](../../aspose.words.tables/row/). |
| Row | 6 | Una fila de una tabla. Un nodo [Row](../../aspose.words.tables/row/) puede tener nodos [Cell](../../aspose.words.tables/cell/). |
| Cell | 7 | Una celda de una fila de tabla. Un nodo [Cell](../../aspose.words.tables/cell/) puede tener nodos [Paragraph](../paragraph/) y [Table](../../aspose.words.tables/table/). |
| Paragraph | 8 | Un párrafo de texto. Un nodo [Paragraph](../paragraph/) es un contenedor para elementos de nivel en línea [Run](../run/), [FieldStart](../../aspose.words.fields/fieldstart/), [FieldSeparator](../../aspose.words.fields/fieldseparator/), [FieldEnd](../../aspose.words.fields/fieldend/), [FormField](../../aspose.words.fields/formfield/), [Shape](../../aspose.words.drawing/shape/), [GroupShape](../../aspose.words.drawing/groupshape/), [Footnote](../../aspose.words.notes/footnote/), [Comment](../comment/), [SpecialChar](../specialchar/), así como [BookmarkStart](../bookmarkstart/) y [BookmarkEnd](../bookmarkend/). |
| BookmarkStart | 9 | Un inicio de un marcador. |
| BookmarkEnd | 10 | Un final de un marcador. |
| EditableRangeStart | 11 | Un inicio de un rango editable. |
| EditableRangeEnd | 12 | Un final de un rango editable. |
| MoveFromRangeStart | 13 | Un comienzo de un rango MoveFrom. |
| MoveFromRangeEnd | 14 | Un final de un rango MoveFrom. |
| MoveToRangeStart | 15 | Un comienzo de un rango MoveTo. |
| MoveToRangeEnd | 16 | Un final de un rango MoveTo. |
| GroupShape | 17 | Un grupo de formas, imágenes, objetos OLE u otras formas de grupo. Un nodo [GroupShape](../../aspose.words.drawing/groupshape/) puede contener otros nodos [Shape](../../aspose.words.drawing/shape/) y [GroupShape](../../aspose.words.drawing/groupshape/). |
| Shape | 18 | Un objeto de dibujo, como una forma OfficeArt, una imagen o un objeto OLE. Un nodo [Shape](../../aspose.words.drawing/shape/) puede contener nodos [Paragraph](../paragraph/) y [Table](../../aspose.words.tables/table/). |
| Comment | 19 | Un comentario en un documento Word. Un nodo [Comment](../comment/) puede tener nodos [Paragraph](../paragraph/) y [Table](../../aspose.words.tables/table/). |
| Footnote | 20 | Una nota al pie o nota final en un documento Word. Un nodo [Footnote](../../aspose.words.notes/footnote/) puede tener nodos [Paragraph](../paragraph/) y [Table](../../aspose.words.tables/table/). |
| Run | 21 | Una secuencia de texto. |
| FieldStart | 22 | Un carácter especial que designa el inicio de un campo Word. |
| FieldSeparator | 23 | Un carácter especial que separa el código del campo del resultado del campo. |
| FieldEnd | 24 | Un carácter especial que designa el final de un campo Word. |
| FormField | 25 | Un campo de formulario. |
| SpecialChar | 26 | Un carácter especial que no es uno de los tipos de caracteres especiales más específicos. |
| SmartTag | 27 | Una etiqueta inteligente alrededor de una o más estructuras en línea (secuencias, imágenes, campos, etc.) dentro de un párrafo. |
| StructuredDocumentTag | 28 | Permite definir información específica del cliente y sus medios de presentación. |
| StructuredDocumentTagRangeStart | 29 | Un inicio de una etiqueta de documento estructurado **ranged** que acepta contenido de múltiples secciones. |
| StructuredDocumentTagRangeEnd | 30 | Un final de una etiqueta de documento estructurado **ranged** que acepta contenido de múltiples secciones. |
| GlossaryDocument | 31 | Un documento de glosario dentro del documento principal. |
| BuildingBlock | 32 | Un bloque de construcción dentro de un documento de glosario (p. ej., entrada del documento de glosario). |
| CommentRangeStart | 33 | Un nodo marcador que representa el inicio de un rango comentado. |
| CommentRangeEnd | 34 | Un nodo marcador que representa el final de un rango comentado. |
| OfficeMath | 35 | Un objeto Office [Math](../../aspose.words.math/). Puede ser una ecuación, una función, una matriz u otro de los objetos matemáticos. Puede ser una colección de objetos matemáticos y también puede contener algunos objetos no matemáticos, como fragmentos de texto. |
| SubDocument | 36 | Un nodo subdocumento que es un enlace a otro documento. |
| System | 37 | Reservado para uso interno por [Aspose.Words](../). |
| Null | 38 | Reservado para uso interno por [Aspose.Words](../). |


## Ejemplos



Muestra cómo recorrer la colección de nodos hijos de un nodo compuesto.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Agregue dos ejecuciones y una forma como nodos hijos al primer párrafo de este documento.
auto paragraph = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world! "));

auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(200);
shape->set_Height(200);
// Tenga en cuenta que el 'CustomNodeId' no se guarda en un archivo de salida y solo existe durante la vida del nodo.
shape->set_CustomNodeId(100);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello again!"));

// Itere a través de la colección de hijos inmediatos del párrafo,
// y muestre cualquier ejecución o forma que encontremos dentro.
System::SharedPtr<Aspose::Words::NodeCollection> children = paragraph->GetChildNodes(Aspose::Words::NodeType::Any, false);

ASSERT_EQ(3, paragraph->GetChildNodes(Aspose::Words::NodeType::Any, false)->get_Count());

for (auto&& child : System::IterateOver(children))
{
    switch (child->get_NodeType())
    {
        case Aspose::Words::NodeType::Run:
            std::cout << "Run contents:" << std::endl;
            std::cout << System::String::Format(u"\t\"{0}\"", child->GetText().Trim()) << std::endl;
            break;

        case Aspose::Words::NodeType::Shape:
        {
            auto childShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(child);
            std::cout << "Shape:" << std::endl;
            std::cout << System::String::Format(u"\t{0}, {1}x{2}", childShape->get_ShapeType(), childShape->get_Width(), childShape->get_Height()) << std::endl;
            ASSERT_EQ(100, shape->get_CustomNodeId());
            break;
        }

        default:
            break;
    }
}
```

## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
