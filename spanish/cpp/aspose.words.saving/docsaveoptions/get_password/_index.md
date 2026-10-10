---
title: "Método Aspose::Words::Saving::DocSaveOptions::get_Password"
linktitle: "get_Password"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::DocSaveOptions::get_Password. Obtiene/establece una contraseña para cifrar el documento usando el método de cifrado RC4 en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.saving/docsaveoptions/get_password/
---
## DocSaveOptions::get_Password method


Obtiene/establece una contraseña para cifrar el documento usando el método de cifrado RC4.

```cpp
System::String Aspose::Words::Saving::DocSaveOptions::get_Password() const
```

## Observaciones


Para guardar el documento sin cifrado, esta propiedad debe ser **null** o una cadena vacía.

## Ejemplos



Muestra cómo establecer opciones de guardado para formatos antiguos de Microsoft Word.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Hello world!");

auto options = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>(Aspose::Words::SaveFormat::Doc);

// Establezca una contraseña que protegerá la carga del documento por Microsoft Word o Aspose.Words.
// Tenga en cuenta que esto no cifra el contenido del documento de ninguna manera.
options->set_Password(u"MyPassword");

// Si el documento contiene una hoja de ruta, podemos preservarla al guardar estableciendo esta bandera en true.
options->set_SaveRoutingSlip(true);

doc->Save(get_ArtifactsDir() + u"DocSaveOptions.SaveAsDoc.doc", options);

// Para poder cargar el documento,
// necesitaremos aplicar la contraseña que especificamos en el objeto DocSaveOptions en un objeto LoadOptions.
ASSERT_THROW(static_cast<std::function<void()>>([&doc]() -> void
{
    doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocSaveOptions.SaveAsDoc.doc");
})(), Aspose::Words::IncorrectPasswordException);

auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"MyPassword");
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocSaveOptions.SaveAsDoc.doc", loadOptions);

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## Ver también

* Class [DocSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
