---
title: "Aspose::Words::Saving::OdtSaveOptions::OdtSaveOptions constructor"
linktitle: "OdtSaveOptions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::OdtSaveOptions::OdtSaveOptions constructor. Inicializa una nueva instancia de esta clase que puede usarse para guardar un documento en formato Odt en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.saving/odtsaveoptions/odtsaveoptions/
---
## OdtSaveOptions::OdtSaveOptions() constructor


Inicializa una nueva instancia de esta clase que puede usarse para guardar un documento en el formato [Odt](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::Saving::OdtSaveOptions::OdtSaveOptions()
```


## Ejemplos



Muestra cómo hacer que un documento guardado cumpla con un esquema ODT más antiguo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>();
saveOptions->set_MeasureUnit(Aspose::Words::Saving::OdtSaveMeasureUnit::Centimeters);
saveOptions->set_IsStrictSchema11(exportToOdt11Specs);

doc->Save(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt", saveOptions);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt");
ASSERT_EQ(Aspose::Words::MeasurementUnits::Centimeters, doc->get_LayoutOptions()->get_RevisionOptions()->get_MeasurementUnit());
```

## Ver también

* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## OdtSaveOptions::OdtSaveOptions(Aspose::Words::SaveFormat) constructor


Inicializa una nueva instancia de esta clase que puede usarse para guardar un documento en el formato [Odt](../../../aspose.words/saveformat/) o [Ott](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::Saving::OdtSaveOptions::OdtSaveOptions(Aspose::Words::SaveFormat saveFormat)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| saveFormat | Aspose::Words::SaveFormat | Puede ser [Odt](../../../aspose.words/saveformat/) o [Ott](../../../aspose.words/saveformat/). |

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

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## OdtSaveOptions::OdtSaveOptions(const System::String\&) constructor


Inicializa una nueva instancia de esta clase que puede usarse para guardar un documento en el formato [Odt](../../../aspose.words/saveformat/) cifrado con una contraseña.

```cpp
Aspose::Words::Saving::OdtSaveOptions::OdtSaveOptions(const System::String &password)
```

## Ver también

* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
