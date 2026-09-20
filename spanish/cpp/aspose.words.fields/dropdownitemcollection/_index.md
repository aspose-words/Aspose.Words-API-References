---
title: "Aspose::Words::Fields::DropDownItemCollection clase"
linktitle: "DropDownItemCollection"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::DropDownItemCollection clase. Una colección de cadenas que representan todos los elementos en un campo de formulario desplegable. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.fields/dropdownitemcollection/
---
## DropDownItemCollection class


Una colección de cadenas que representan todos los elementos en un campo de formulario desplegable. Para obtener más información, visite el artículo de documentación [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class DropDownItemCollection : public System::Collections::Generic::IEnumerable<System::String>,
                               public Aspose::Words::IComplexAttr
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Add](./add/)(const System::String\&) | Agrega una cadena al final de la colección. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Elimina todos los elementos de la colección. |
| [Contains](./contains/)(const System::String\&) | Determina si la colección contiene el valor especificado. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Obtiene el número de elementos contenidos en la colección. |
| [GetEnumerator](./getenumerator/)() override | Devuelve un objeto enumerador que puede usarse para iterar sobre todos los elementos de la colección. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Obtiene o establece el elemento en el índice especificado. |
| [idx_set](./idx_set/)(int32_t, const System::String\&) | Obtiene o establece el elemento en el índice especificado. |
| [IndexOf](./indexof/)(const System::String\&) | Devuelve el índice basado en cero del valor especificado en la colección. |
| [Insert](./insert/)(int32_t, const System::String\&) | Inserta una cadena en la colección en el índice especificado. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | Elimina el valor especificado de la colección. |
| [RemoveAt](./removeat/)(int32_t) | Elimina un valor en el índice especificado. |
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



Muestra cómo insertar un campo de cuadro combinado y editar los elementos en su colección de ítems.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserte un cuadro combinado y luego verifique su colección de elementos desplegables.
// En Microsoft Word, el usuario hará clic en el cuadro combinado,
// y luego elegirá uno de los textos de los ítems en la colección para mostrar.
System::ArrayPtr<System::String> items = System::MakeArray<System::String>({u"One", u"Two", u"Three"});
System::SharedPtr<Aspose::Words::Fields::FormField> comboBoxField = builder->InsertComboBox(u"DropDown", items, 0);
System::SharedPtr<Aspose::Words::Fields::DropDownItemCollection> dropDownItems = comboBoxField->get_DropDownItems();

ASSERT_EQ(3, dropDownItems->get_Count());
ASSERT_EQ(u"One", dropDownItems->idx_get(0));
ASSERT_EQ(1, dropDownItems->IndexOf(u"Two"));
ASSERT_TRUE(dropDownItems->Contains(u"Three"));

// Hay dos formas de agregar un nuevo ítem a una colección existente de ítems de cuadro desplegable.
// 1 -  Añadir un ítem al final de la colección:
dropDownItems->Add(u"Four");

// 2 -  Insertar un ítem antes de otro ítem en un índice especificado:
dropDownItems->Insert(3, u"Three and a half");

ASSERT_EQ(5, dropDownItems->get_Count());

// Itere sobre la colección e imprima cada elemento.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::String>> dropDownCollectionEnumerator = dropDownItems->GetEnumerator();
    while (dropDownCollectionEnumerator->MoveNext())
    {
        std::cout << dropDownCollectionEnumerator->get_Current() << std::endl;
    }
}

// Hay dos formas de eliminar elementos de una colección de ítems desplegables.
// 1 -  Eliminar un ítem cuyo contenido sea igual a la cadena pasada:
dropDownItems->Remove(u"Four");

// 2 -  Eliminar un ítem en un índice:
dropDownItems->RemoveAt(3);

ASSERT_EQ(3, dropDownItems->get_Count());
ASSERT_FALSE(dropDownItems->Contains(u"Three and a half"));
ASSERT_FALSE(dropDownItems->Contains(u"Four"));

doc->Save(get_ArtifactsDir() + u"FormFields.DropDownItemCollection.html");

// Vaciar toda la colección de ítems desplegables.
dropDownItems->Clear();
```

## Ver también

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
