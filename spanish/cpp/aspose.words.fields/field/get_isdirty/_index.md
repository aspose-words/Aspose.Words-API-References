---
title: "Aspose::Words::Fields::Field::get_IsDirty método"
linktitle: "get_IsDirty"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Fields::Field::get_IsDirty. Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento en C++."
type: docs
weight: 7000
url: /es/cpp/aspose.words.fields/field/get_isdirty/
---
## Field::get_IsDirty method


Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento.

```cpp
bool Aspose::Words::Fields::Field::get_IsDirty()
```


## Ejemplos



Muestra cómo usar la propiedad especial para actualizar el resultado del campo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Asigne el valor de la propiedad incorporada "Author" del documento y luego muéstrelo con un campo.
doc->get_BuiltInDocumentProperties()->set_Author(u"John Doe");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldAuthor>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true));

ASSERT_FALSE(field->get_IsDirty());
ASSERT_EQ(u"John Doe", field->get_Result());

// Actualice la propiedad. El campo sigue mostrando el valor antiguo.
doc->get_BuiltInDocumentProperties()->set_Author(u"John & Jane Doe");

ASSERT_EQ(u"John Doe", field->get_Result());

// Dado que el valor del campo está desactualizado, podemos marcarlo como "dirty".
// Este valor permanecerá desactualizado hasta que actualicemos el campo manualmente con el método Field.Update().
field->set_IsDirty(true);

{
    auto docStream = System::MakeObject<System::IO::MemoryStream>();
    // Si guardamos sin llamar a un método de actualización,
    // el campo seguirá mostrando el valor desactualizado en el documento de salida.
    doc->Save(docStream, Aspose::Words::SaveFormat::Docx);

    // El objeto LoadOptions tiene una opción para actualizar todos los campos
    // marcados como "dirty" al cargar el documento.
    auto options = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
    options->set_UpdateDirtyFields(updateDirtyFields);
    doc = System::MakeObject<Aspose::Words::Document>(docStream, options);

    ASSERT_EQ(u"John & Jane Doe", doc->get_BuiltInDocumentProperties()->get_Author());

    field = System::ExplicitCast<Aspose::Words::Fields::FieldAuthor>(doc->get_Range()->get_Fields()->idx_get(0));

    // Actualizar campos dirty de esta manera establece automáticamente su bandera "IsDirty" a false.
    if (updateDirtyFields)
    {
        ASSERT_EQ(u"John & Jane Doe", field->get_Result());
        ASSERT_FALSE(field->get_IsDirty());
    }
    else
    {
        ASSERT_EQ(u"John Doe", field->get_Result());
        ASSERT_TRUE(field->get_IsDirty());
    }
}
```

## Ver también

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
