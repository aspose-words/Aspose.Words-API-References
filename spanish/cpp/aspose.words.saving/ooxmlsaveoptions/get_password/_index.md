---
title: "Aspose::Words::Saving::OoxmlSaveOptions::get_Password método"
linktitle: "get_Password"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::OoxmlSaveOptions::get_Password método. Obtiene/establece una contraseña para cifrar el documento usando el algoritmo de cifrado estándar ECMA376 en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words.saving/ooxmlsaveoptions/get_password/
---
## OoxmlSaveOptions::get_Password method


Obtiene/establece una contraseña para cifrar el documento usando el algoritmo de cifrado ECMA376 Standard.

```cpp
System::String Aspose::Words::Saving::OoxmlSaveOptions::get_Password() const
```

## Observaciones


Para guardar el documento sin cifrado, esta propiedad debe ser **null** o una cadena vacía.

## Ejemplos



Muestra cómo crear un documento Office Open XML cifrado con contraseña.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Password(u"MyPassword");

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.Password.docx", saveOptions);

// No podremos abrir este documento con Microsoft Word o
// Aspose.Words sin proporcionar la contraseña correcta.
ASSERT_THROW(static_cast<std::function<void()>>([&doc]() -> void
{
    doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.Password.docx");
})(), Aspose::Words::IncorrectPasswordException);

// Abra el documento cifrado pasando la contraseña correcta en un objeto LoadOptions.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.Password.docx", System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"MyPassword"));

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## Ver también

* Class [OoxmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
