---
title: "Aspose::Words::Saving::OdtSaveOptions::OdtSaveOptions constructor"
linktitle: "OdtSaveOptions"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::OdtSaveOptions::OdtSaveOptions constructor. Инициализирует новый экземпляр этого класса, который может использоваться для сохранения документа в формате Odt в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.saving/odtsaveoptions/odtsaveoptions/
---
## OdtSaveOptions::OdtSaveOptions() constructor


Инициализирует новый экземпляр этого класса, который может использоваться для сохранения документа в формате [Odt](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::Saving::OdtSaveOptions::OdtSaveOptions()
```


## Примеры



Показывает, как сделать сохранённый документ соответствующим более старой схеме ODT.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>();
saveOptions->set_MeasureUnit(Aspose::Words::Saving::OdtSaveMeasureUnit::Centimeters);
saveOptions->set_IsStrictSchema11(exportToOdt11Specs);

doc->Save(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt", saveOptions);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt");
ASSERT_EQ(Aspose::Words::MeasurementUnits::Centimeters, doc->get_LayoutOptions()->get_RevisionOptions()->get_MeasurementUnit());
```

## См. также

* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## OdtSaveOptions::OdtSaveOptions(Aspose::Words::SaveFormat) constructor


Инициализирует новый экземпляр этого класса, который может использоваться для сохранения документа в формате [Odt](../../../aspose.words/saveformat/) или [Ott](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::Saving::OdtSaveOptions::OdtSaveOptions(Aspose::Words::SaveFormat saveFormat)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| saveFormat | Aspose::Words::SaveFormat | Может быть [Odt](../../../aspose.words/saveformat/) или [Ott](../../../aspose.words/saveformat/). |

## Примеры



Показывает, как зашифровать сохранённый документ ODT/OTT паролем, а затем загрузить его с помощью Aspose.Words.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Создайте новый OdtSaveOptions и передайте либо "SaveFormat.Odt",
// или "SaveFormat.Ott" в качестве формата для сохранения документа.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>(saveFormat);
saveOptions->set_Password(u"@sposeEncrypted_1145");

System::String extensionString = Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat);

// Если открыть этот документ в подходящем редакторе,
// он запросит у нас пароль, указанный в объекте SaveOptions.
doc->Save(get_ArtifactsDir() + u"OdtSaveOptions.Encrypt" + extensionString, saveOptions);

System::SharedPtr<Aspose::Words::FileFormatInfo> docInfo = Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"OdtSaveOptions.Encrypt" + extensionString);

ASSERT_TRUE(docInfo->get_IsEncrypted());

// Если мы захотим открыть или отредактировать этот документ снова с помощью Aspose.Words,
// нам потребуется предоставить объект LoadOptions с правильным паролем в конструктор загрузки.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OdtSaveOptions.Encrypt" + extensionString, System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"@sposeEncrypted_1145"));

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## См. также

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## OdtSaveOptions::OdtSaveOptions(const System::String\&) constructor


Инициализирует новый экземпляр этого класса, который может использоваться для сохранения документа в формате [Odt](../../../aspose.words/saveformat/), зашифрованного паролем.

```cpp
Aspose::Words::Saving::OdtSaveOptions::OdtSaveOptions(const System::String &password)
```

## См. также

* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
