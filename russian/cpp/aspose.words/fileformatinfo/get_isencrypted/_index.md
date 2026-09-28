---
title: "Метод Aspose::Words::FileFormatInfo::get_IsEncrypted"
linktitle: "get_IsEncrypted"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::FileFormatInfo::get_IsEncrypted. Возвращает true, если документ зашифрован и требует пароль для открытия в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words/fileformatinfo/get_isencrypted/
---
## FileFormatInfo::get_IsEncrypted method


Возвращает **true**, если документ зашифрован и требует пароль для открытия.

```cpp
bool Aspose::Words::FileFormatInfo::get_IsEncrypted() const
```

## Примечания


Это свойство существует, чтобы помочь вам различать зашифрованные документы и незашифрованные. Если попытаться загрузить зашифрованный документ с помощью Aspose.Words без указания пароля, будет выброшено исключение. Вы можете использовать это свойство, чтобы определить, требуется ли документу пароль, и выполнить некоторое действие перед загрузкой документа, например, запросить пароль у пользователя.

## Примеры



Показывает, как использовать класс [FileFormatUtil](../../fileformatutil/) для определения формата документа и шифрования.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Настройте объект SaveOptions для шифрования документа
// с паролем при сохранении, а затем сохраните документ.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>(Aspose::Words::SaveFormat::Odt);
saveOptions->set_Password(u"MyPassword");

doc->Save(get_ArtifactsDir() + u"File.DetectDocumentEncryption.odt", saveOptions);

// Проверьте тип файла нашего документа и его статус шифрования.
System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"File.DetectDocumentEncryption.odt");

ASSERT_EQ(u".odt", Aspose::Words::FileFormatUtil::LoadFormatToExtension(info->get_LoadFormat()));
ASSERT_TRUE(info->get_IsEncrypted());
```

## См. также

* Class [FileFormatInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
