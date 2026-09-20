---
title: "Clase Aspose::Words::NodeCollection"
linktitle: "NodeCollection"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::NodeCollection. Representa una colección de nodos de un tipo específico. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 43000
url: /es/cpp/aspose.words/nodecollection/
---
## NodeCollection class


Representa una colección de nodos de un tipo específico. Para obtener más información, visite el artículo de documentación [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class NodeCollection : public Aspose::Words::INodeCollection,
                       public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Node>>
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Agrega un nodo al final de la colección. |
| [Clear](./clear/)() | Elimina todos los nodos de esta colección y del documento. |
| [Contains](./contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Determina si un nodo está en la colección. |
| [get_Count](./get_count/)() | Obtiene el número de nodos en la colección. |
| [GetEnumerator](./getenumerator/)() override | Proporciona una iteración simple al estilo "foreach" sobre la colección de nodos. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Recupera un nodo en el índice dado. |
| [IndexOf](./indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Devuelve el índice basado en cero del nodo especificado. |
| [Insert](./insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Inserta un nodo en la colección en el índice especificado. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Elimina el nodo de la colección y del documento. |
| [RemoveAt](./removeat/)(int32_t) | Elimina el nodo en el índice especificado de la colección y del documento. |
| [ToArray](./toarray/)() | Copia todos los nodos de la colección a una nueva matriz de nodos. |
| static [Type](./type/)() |  |
## Observaciones


[NodeCollection](./) does not own the nodes it contains, rather, is just a selection of nodes of the specified type, but the nodes are stored in the tree under their respective parent nodes.

[NodeCollection](./) supports indexed access, iteration and provides add and remove methods.

La colección [NodeCollection](./) es "en vivo", es decir, los cambios en los hijos del objeto nodo del que se creó se reflejan inmediatamente en los nodos devueltos por las propiedades y métodos de [NodeCollection](./).

[NodeCollection](./) is returned by [GetChildNodes()](../compositenode/getchildnodes/) and also serves as a base class for typed node collections such as [SectionCollection](../sectioncollection/), [ParagraphCollection](../paragraphcollection/) etc.

[NodeCollection](./) can be "flat" and contain only immediate children of the node it was created from, or it can be "deep" and contain all descendant children.

## Ejemplos



Muestra cómo reemplazar todas las formas de cuadro de texto por formas de imagen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Textboxes in drawing canvas.docx");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(3, shapes->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Shape>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Shape> s)>>([](System::SharedPtr<Aspose::Words::Drawing::Shape> s) -> bool
{
    return s->get_ShapeType() == Aspose::Words::Drawing::ShapeType::TextBox;
}))));
ASSERT_EQ(1, shapes->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Shape>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Shape> s)>>([](System::SharedPtr<Aspose::Words::Drawing::Shape> s) -> bool
{
    return s->get_ShapeType() == Aspose::Words::Drawing::ShapeType::Image;
}))));

for (System::SharedPtr<Aspose::Words::Drawing::Shape> shape : shapes)
{
    if (shape->get_ShapeType() == Aspose::Words::Drawing::ShapeType::TextBox)
    {
        auto replacementShape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Image);
        replacementShape->get_ImageData()->SetImage(get_ImageDir() + u"Logo.jpg");
        replacementShape->set_Left(shape->get_Left());
        replacementShape->set_Top(shape->get_Top());
        replacementShape->set_Width(shape->get_Width());
        replacementShape->set_Height(shape->get_Height());
        replacementShape->set_RelativeHorizontalPosition(shape->get_RelativeHorizontalPosition());
        replacementShape->set_RelativeVerticalPosition(shape->get_RelativeVerticalPosition());
        replacementShape->set_HorizontalAlignment(shape->get_HorizontalAlignment());
        replacementShape->set_VerticalAlignment(shape->get_VerticalAlignment());
        replacementShape->set_WrapType(shape->get_WrapType());
        replacementShape->set_WrapSide(shape->get_WrapSide());

        shape->get_ParentNode()->InsertAfter<System::SharedPtr<Aspose::Words::Drawing::Shape>>(replacementShape, shape);
        shape->Remove();
    }
}

shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(0, shapes->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Shape>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Shape> s)>>([](System::SharedPtr<Aspose::Words::Drawing::Shape> s) -> bool
{
    return s->get_ShapeType() == Aspose::Words::Drawing::ShapeType::TextBox;
}))));
ASSERT_EQ(4, shapes->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Shape>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Shape> s)>>([](System::SharedPtr<Aspose::Words::Drawing::Shape> s) -> bool
{
    return s->get_ShapeType() == Aspose::Words::Drawing::ShapeType::Image;
}))));

doc->Save(get_ArtifactsDir() + u"Shape.ReplaceTextboxesWithImages.docx");
```

## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
