---
title: "Aspose::Words::Markup::SdtListItem class"
linktitle: "SdtListItem"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Markup::SdtListItem class. Este elemento especifica un único elemento de lista dentro de una etiqueta de documento estructurado ComboBox o DropDownList padre. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 8000
url: /es/cpp/aspose.words.markup/sdtlistitem/
---
## SdtListItem class


Este elemento especifica un único elemento de lista dentro de una etiqueta de documento estructurado padre [ComboBox](../sdttype/) o [DropDownList](../sdttype/). Para obtener más información, visite el artículo de documentación [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class SdtListItem : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_DisplayText](./get_displaytext/)() const | Obtiene el texto que se mostrará en el contenido de ejecución en lugar del contenido del atributo [Value](./get_value/) para este elemento de lista. |
| [get_Value](./get_value/)() const | Obtiene el valor de este elemento de lista. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [SdtListItem](./sdtlistitem/)(const System::String\&, const System::String\&) | Inicializa una nueva instancia de esta clase. |
| [SdtListItem](./sdtlistitem/)(const System::String\&) | Inicializa una nueva instancia de esta clase. |
| static [Type](./type/)() |  |

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
