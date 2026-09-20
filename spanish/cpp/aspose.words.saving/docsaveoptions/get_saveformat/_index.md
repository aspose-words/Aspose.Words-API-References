---
title: "Aspose::Words::Saving::DocSaveOptions::get_SaveFormat método"
linktitle: "get_SaveFormat"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::DocSaveOptions::get_SaveFormat método. Especifica el formato en el que se guardará el documento si se utiliza este objeto de opciones de guardado. Puede ser Doc o Dot en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.saving/docsaveoptions/get_saveformat/
---
## DocSaveOptions::get_SaveFormat method


Especifica el formato en el que se guardará el documento si se utiliza este objeto de opciones de guardado. Puede ser [Doc](../../../aspose.words/saveformat/) o [Dot](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::DocSaveOptions::get_SaveFormat() override
```


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

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [DocSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
