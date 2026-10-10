---
title: "Método Aspose::Words::Loading::LoadOptions::get_UpdateDirtyFields"
linktitle: "get_UpdateDirtyFields"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Loading::LoadOptions::get_UpdateDirtyFields. Especifica si se deben actualizar los campos con el atributo dirty en C++."
type: docs
weight: 17000
url: /es/cpp/aspose.words.loading/loadoptions/get_updatedirtyfields/
---
## LoadOptions::get_UpdateDirtyFields method


Especifica si se deben actualizar los campos con el atributo **dirty**.

```cpp
bool Aspose::Words::Loading::LoadOptions::get_UpdateDirtyFields() const
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

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
