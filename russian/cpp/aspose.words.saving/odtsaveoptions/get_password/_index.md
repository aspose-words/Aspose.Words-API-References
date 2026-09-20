---
title: "Aspose::Words::Saving::OdtSaveOptions::get_Password method"
linktitle: "get_Password"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::OdtSaveOptions::get_Password method. Получает или задает пароль для шифрования документа в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.saving/odtsaveoptions/get_password/
---
## OdtSaveOptions::get_Password method


Получает или задает пароль для шифрования документа.

```cpp
System::String Aspose::Words::Saving::OdtSaveOptions::get_Password() const
```

## Примечания


Чтобы сохранить документ без шифрования, это свойство должно быть **null** или пустой строкой.

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

* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
