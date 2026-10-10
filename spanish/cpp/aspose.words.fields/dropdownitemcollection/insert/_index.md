---
title: "Aspose::Words::Fields::DropDownItemCollection::Insert método"
linktitle: "Insert"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::DropDownItemCollection::Insert método. Inserta una cadena en la colección en el índice especificado en C++."
type: docs
weight: 15000
url: /es/cpp/aspose.words.fields/dropdownitemcollection/insert/
---
## DropDownItemCollection::Insert method


Inserta una cadena en la colección en el índice especificado.

```cpp
void Aspose::Words::Fields::DropDownItemCollection::Insert(int32_t index, const System::String &value)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| index | int32_t | El índice basado en cero en el que se inserta el valor. |
| value | const System::String\& | La cadena a insertar. |

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

* Class [DropDownItemCollection](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
