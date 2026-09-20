---
title: "Método Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField"
linktitle: "get_PreserveIncludePictureField"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField. Obtiene o establece si se debe preservar el campo INCLUDEPICTURE al leer formatos de Microsoft Word. El valor predeterminado es false en C++."
type: docs
weight: 13000
url: /es/cpp/aspose.words.loading/loadoptions/get_preserveincludepicturefield/
---
## LoadOptions::get_PreserveIncludePictureField method


Obtiene o establece si se debe conservar el campo INCLUDEPICTURE al leer formatos de Microsoft Word. El valor predeterminado es **false**.

```cpp
bool Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField() const
```

## Observaciones


Por defecto, el campo INCLUDEPICTURE se convierte en un objeto de forma. Puedes sobrescribirlo si necesitas que el campo se preserve, por ejemplo, si deseas actualizarlo programáticamente. Ten en cuenta, sin embargo, que este enfoque no es común para Aspose.Words. Úsalo bajo tu propio riesgo.

Uno de los posibles casos de uso puede ser usar un MERGEFIELD como campo hijo para cambiar dinámicamente la ruta de origen de la imagen. En este caso necesitas que el INCLUDEPICTURE se preserve en el modelo.

## Ejemplos



Muestra cómo preservar o descartar campos INCLUDEPICTURE al cargar un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto includePicture = System::ExplicitCast<Aspose::Words::Fields::FieldIncludePicture>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIncludePicture, true));
includePicture->set_SourceFullName(get_ImageDir() + u"Transparent background logo.png");
includePicture->Update(true);

{
    auto docStream = System::MakeObject<System::IO::MemoryStream>();
    doc->Save(docStream, System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx));

    // Podemos establecer una bandera en un objeto LoadOptions para decidir si convertir todos los campos INCLUDEPICTURE
    // en formas de imagen al cargar un documento que los contiene.
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
    loadOptions->set_PreserveIncludePictureField(preserveIncludePictureField);

    doc = System::MakeObject<Aspose::Words::Document>(docStream, loadOptions);

    if (preserveIncludePictureField)
    {
        ASSERT_TRUE(doc->get_Range()->get_Fields()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fields::Field>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fields::Field> f)>>([](System::SharedPtr<Aspose::Words::Fields::Field> f) -> bool
        {
            return f->get_Type() == Aspose::Words::Fields::FieldType::FieldIncludePicture;
        }))));

        doc->UpdateFields();
        doc->Save(get_ArtifactsDir() + u"Field.PreserveIncludePicture.docx");
    }
    else
    {
        ASSERT_FALSE(doc->get_Range()->get_Fields()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fields::Field>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fields::Field> f)>>([](System::SharedPtr<Aspose::Words::Fields::Field> f) -> bool
        {
            return f->get_Type() == Aspose::Words::Fields::FieldType::FieldIncludePicture;
        }))));
    }
}
```

## Ver también

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
