---
title: "Aspose::Words::VariableCollection::GetEnumerator método"
linktitle: "GetEnumerator"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::VariableCollection::GetEnumerator método. Devuelve un objeto enumerador que puede usarse para iterar sobre todas las variables en la colección en C++."
type: docs
weight: 10000
url: /es/cpp/aspose.words/variablecollection/getenumerator/
---
## VariableCollection::GetEnumerator method


Devuelve un objeto enumerador que puede usarse para iterar sobre todas las variables en la colección.

```cpp
System::SharedPtr<System::Collections::Generic::IEnumerator<System::Collections::Generic::KeyValuePair<System::String, System::String>>> Aspose::Words::VariableCollection::GetEnumerator() override
```


## Ejemplos



Muestra cómo trabajar con la colección de variables de un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::VariableCollection> variables = doc->get_Variables();

// Cada documento tiene una colección de variables de pares clave/valor, a la que podemos agregar elementos.
variables->Add(u"Home address", u"123 Main St.");
variables->Add(u"City", u"London");
variables->Add(u"Bedrooms", u"3");

ASSERT_EQ(3, variables->get_Count());

// Podemos mostrar los valores de las variables en el cuerpo del documento usando campos DOCVARIABLE.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDocVariable>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDocVariable, true));
field->set_VariableName(u"Home address");
field->Update();

ASSERT_EQ(u"123 Main St.", field->get_Result());

// Asignar valores a claves existentes los actualizará.
variables->Add(u"Home address", u"456 Queen St.");

// Luego tendremos que actualizar los campos DOCVARIABLE para asegurar que muestren un valor actualizado.
ASSERT_EQ(u"123 Main St.", field->get_Result());

field->Update();

ASSERT_EQ(u"456 Queen St.", field->get_Result());

// Verifique que existan variables de documento con un determinado nombre o valor.
ASSERT_TRUE(variables->Contains(u"City"));
ASSERT_TRUE(variables->LINQ_Any(static_cast<System::Func<System::Collections::Generic::KeyValuePair<System::String, System::String>, bool>>(static_cast<std::function<bool(System::Collections::Generic::KeyValuePair<System::String, System::String> v)>>([](System::Collections::Generic::KeyValuePair<System::String, System::String> v) -> bool
{
    return v.get_Value() == u"London";
}))));

// La colección de variables ordena automáticamente las variables alfabéticamente por nombre.
ASSERT_EQ(0, variables->IndexOfKey(u"Bedrooms"));
ASSERT_EQ(1, variables->IndexOfKey(u"City"));
ASSERT_EQ(2, variables->IndexOfKey(u"Home address"));

ASSERT_EQ(u"3", variables->idx_get(0));
ASSERT_EQ(u"London", variables->idx_get(u"City"));

// Enumere la colección de variables.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::Collections::Generic::KeyValuePair<System::String, System::String>>> enumerator = doc->get_Variables()->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Name: {0}, Value: {1}", enumerator->get_Current().get_Key(), enumerator->get_Current().get_Value()) << std::endl;
    }
}

// A continuación se presentan tres formas de eliminar variables de documento de una colección.
// 1 -  Por nombre:
variables->Remove(u"City");

ASSERT_FALSE(variables->Contains(u"City"));

// 2 -  Por índice:
variables->RemoveAt(1);

ASSERT_FALSE(variables->Contains(u"Home address"));

// 3 -  Borrar toda la colección de una vez:
variables->Clear();

ASSERT_EQ(0, variables->get_Count());
```

## Ver también

* Class [VariableCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
