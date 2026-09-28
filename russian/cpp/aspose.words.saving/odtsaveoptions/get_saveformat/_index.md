---
title: "Метод Aspose::Words::Saving::OdtSaveOptions::get_SaveFormat"
linktitle: "get_SaveFormat"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::OdtSaveOptions::get_SaveFormat. Указывает формат, в котором будет сохранён документ, если используется этот объект параметров сохранения. Может быть Odt или Ott в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words.saving/odtsaveoptions/get_saveformat/
---
## OdtSaveOptions::get_SaveFormat method


Указывает формат, в котором будет сохранён документ, если используется этот объект параметров сохранения. Может быть [Odt](../../../aspose.words/saveformat/) или [Ott](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::OdtSaveOptions::get_SaveFormat() override
```


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
