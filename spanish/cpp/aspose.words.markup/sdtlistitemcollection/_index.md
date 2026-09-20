---
title: "Aspose::Words::Markup::SdtListItemCollection class"
linktitle: "SdtListItemCollection"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Markup::SdtListItemCollection class. Proporciona acceso a los elementos SdtListItem de una etiqueta de documento estructurado. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 9000
url: /es/cpp/aspose.words.markup/sdtlistitemcollection/
---
## SdtListItemCollection class


Proporciona acceso a los elementos [SdtListItem](../sdtlistitem/) de una etiqueta de documento estructurado. Para obtener más información, visite el artículo de documentación [Etiquetas de documento estructurado o control de contenido](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class SdtListItemCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Markup::SdtListItem>>
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Markup::SdtListItem\>\&) | Agrega un elemento a esta colección. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Elimina todos los elementos de esta colección. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Obtiene el número de elementos en la colección. |
| [get_SelectedValue](./get_selectedvalue/)() | Especifica el valor seleccionado actualmente en esta lista. Se permite un valor nulo, lo que significa que no hay ninguna entrada seleccionada asociada con esta colección de elementos de lista. |
| [GetEnumerator](./getenumerator/)() override | Devuelve un objeto enumerador que puede usarse para iterar sobre todos los elementos de la colección. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Devuelve un objeto [SdtListItem](../sdtlistitem/) dado su índice basado en cero en la colección. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [RemoveAt](./removeat/)(int32_t) | Elimina un elemento de la lista en el índice especificado. |
| [set_SelectedValue](./set_selectedvalue/)(const System::SharedPtr\<Aspose::Words::Markup::SdtListItem\>\&) | Método set para [Aspose::Words::Markup::SdtListItemCollection::get_SelectedValue](./get_selectedvalue/). |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| Typedef | Descripción |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |

## Ejemplos



Muestra cómo trabajar con etiquetas de documento estructurado de lista desplegable.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::DropDownList, Aspose::Words::Markup::MarkupLevel::Block);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(tag);

// Una etiqueta de documento estructurado de lista desplegable es un formulario que permite al usuario
// seleccionar una opción de una lista haciendo clic izquierdo y abriendo el formulario en Microsoft Word.
// La propiedad "ListItems" contiene todos los elementos de lista, y cada elemento de lista es un "SdtListItem".
System::SharedPtr<Aspose::Words::Markup::SdtListItemCollection> listItems = tag->get_ListItems();
listItems->Add(System::MakeObject<Aspose::Words::Markup::SdtListItem>(u"Value 1"));

ASSERT_EQ(listItems->idx_get(0)->get_DisplayText(), listItems->idx_get(0)->get_Value());

// Agregue 3 elementos de lista más. Inicialice estos elementos usando un constructor diferente al del primer elemento
// para mostrar cadenas que sean diferentes de sus valores.
listItems->Add(System::MakeObject<Aspose::Words::Markup::SdtListItem>(u"Item 2", u"Value 2"));
listItems->Add(System::MakeObject<Aspose::Words::Markup::SdtListItem>(u"Item 3", u"Value 3"));
listItems->Add(System::MakeObject<Aspose::Words::Markup::SdtListItem>(u"Item 4", u"Value 4"));

ASSERT_EQ(4, listItems->get_Count());

// La lista desplegable está mostrando el primer elemento. Asigne un elemento de lista diferente a "SelectedValue" para mostrarlo.
listItems->set_SelectedValue(listItems->idx_get(3));

ASSERT_EQ(u"Value 4", listItems->get_SelectedValue()->get_Value());

// Recorra la colección e imprima cada elemento.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Markup::SdtListItem>>> enumerator = listItems->GetEnumerator();
    while (enumerator->MoveNext())
    {
        if (enumerator->get_Current() != nullptr)
        {
            std::cout << System::String::Format(u"List item: {0}, value: {1}", enumerator->get_Current()->get_DisplayText(), enumerator->get_Current()->get_Value()) << std::endl;
        }
    }
}

// Elimine el último elemento de la lista.
listItems->RemoveAt(3);

ASSERT_EQ(3, listItems->get_Count());

// Dado que nuestro control desplegable está configurado para mostrar el elemento eliminado por defecto, proporciónele un elemento que exista para mostrar.
listItems->set_SelectedValue(listItems->idx_get(1));

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.ListItemCollection.docx");

// Utilice el método "Clear" para vaciar toda la colección de elementos del desplegable de una vez.
listItems->Clear();

ASSERT_EQ(0, listItems->get_Count());
```

## Ver también

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
