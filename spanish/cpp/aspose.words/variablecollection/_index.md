---
title: "Clase Aspose::Words::VariableCollection"
linktitle: "VariableCollection"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::VariableCollection. Una colección de variables del documento. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 73000
url: /es/cpp/aspose.words/variablecollection/
---
## VariableCollection class


Una colección de variables del documento. Para obtener más información, visite el artículo de documentación [Work with Document Properties](https://docs.aspose.com/words/cpp/work-with-document-properties/).

```cpp
class VariableCollection : public System::Collections::Generic::IEnumerable<System::Collections::Generic::KeyValuePair<System::String, System::String>>
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Add](./add/)(const System::String\&, const System::String\&) | Agrega una variable de documento a la colección. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Elimina todos los elementos de la colección. |
| [Contains](./contains/)(const System::String\&) | Determina si la colección contiene una variable de documento con el nombre dado. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Obtiene el número de elementos contenidos en la colección. |
| [GetEnumerator](./getenumerator/)() override | Devuelve un objeto enumerador que puede usarse para iterar sobre todas las variables en la colección. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | Obtiene o establece una variable de documento por su nombre sin distinción de mayúsculas/minúsculas. Los valores **null** no están permitidos como lado derecho de la asignación y serán reemplazados por una cadena vacía. |
| [idx_get](./idx_get/)(int32_t) | Obtiene o establece una variable de documento en el índice especificado. Los valores **null** no están permitidos como lado derecho de la asignación y serán reemplazados por una cadena vacía. |
| [idx_set](./idx_set/)(const System::String\&, const System::String\&) | Obtiene o establece una variable de documento por su nombre sin distinción de mayúsculas/minúsculas. Los valores **null** no están permitidos como lado derecho de la asignación y serán reemplazados por una cadena vacía. |
| [idx_set](./idx_set/)(int32_t, const System::String\&) | Obtiene o establece una variable de documento en el índice especificado. Los valores **null** no están permitidos como lado derecho de la asignación y serán reemplazados por una cadena vacía. |
| [IndexOfKey](./indexofkey/)(const System::String\&) | Devuelve el índice basado en cero de la variable de documento especificada en la colección. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | Elimina una variable de documento con el nombre especificado de la colección. |
| [RemoveAt](./removeat/)(int32_t) | Elimina una variable de documento en el índice especificado. |
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
## Observaciones


Los nombres y valores de las variables son cadenas.

Los nombres de las variables no distinguen entre mayúsculas y minúsculas.

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
