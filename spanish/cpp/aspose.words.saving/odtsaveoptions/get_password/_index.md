---
title: "Aspose::Words::Saving::OdtSaveOptions::get_Password método"
linktitle: "get_Password"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::OdtSaveOptions::get_Password método. Obtiene o establece una contraseña para cifrar el documento en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.saving/odtsaveoptions/get_password/
---
## OdtSaveOptions::get_Password method


Obtiene o establece una contraseña para cifrar el documento.

```cpp
System::String Aspose::Words::Saving::OdtSaveOptions::get_Password() const
```

## Observaciones


Para guardar el documento sin cifrado, esta propiedad debe ser **null** o una cadena vacía.

## Ejemplos



Muestra cómo cifrar un documento ODT/OTT guardado con una contraseña y luego cargarlo usando Aspose.Words.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Cree una nueva OdtSaveOptions, y pase cualquiera de "SaveFormat.Odt",
// o "SaveFormat.Ott" como el formato en el que guardar el documento.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>(saveFormat);
saveOptions->set_Password(u"@sposeEncrypted_1145");

System::String extensionString = Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat);

// Si abrimos este documento con un editor apropiado,
// nos pedirá la contraseña que especificamos en el objeto SaveOptions.
doc->Save(get_ArtifactsDir() + u"OdtSaveOptions.Encrypt" + extensionString, saveOptions);

System::SharedPtr<Aspose::Words::FileFormatInfo> docInfo = Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"OdtSaveOptions.Encrypt" + extensionString);

ASSERT_TRUE(docInfo->get_IsEncrypted());

// Si deseamos abrir o editar este documento nuevamente usando Aspose.Words,
// tendremos que proporcionar un objeto LoadOptions con la contraseña correcta al constructor de carga.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OdtSaveOptions.Encrypt" + extensionString, System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"@sposeEncrypted_1145"));

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## Ver también

* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
