---
title: "Aspose::Words::FileFormatInfo класс"
linktitle: "FileFormatInfo"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::FileFormatInfo класс. Содержит данные, возвращаемые методами обнаружения формата документа FileFormatUtil. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 27000
url: /ru/cpp/aspose.words/fileformatinfo/
---
## FileFormatInfo class


Содержит данные, возвращаемые методами обнаружения формата документа [FileFormatUtil](../fileformatutil/). Чтобы узнать больше, посетите статью документации [Detect File Format and Check Format Compatibility](https://docs.aspose.com/words/cpp/detect-file-format-and-check-format-compatibility/).

```cpp
class FileFormatInfo : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_Encoding](./get_encoding/)() const | Получает обнаруженную кодировку, если она применима к текущему формату документа. В данный момент кодировка определяется только для HTML‑документов. |
| [get_HasDigitalSignature](./get_hasdigitalsignature/)() const | Возвращает **true**, если документ содержит цифровую подпись. Это свойство лишь информирует о наличии цифровой подписи в документе, но не указывает, действительна она или нет. |
| [get_HasMacros](./get_hasmacros/)() const | Возвращает **true**, если документ содержит макросы VBA. |
| [get_IsEncrypted](./get_isencrypted/)() const | Возвращает **true**, если документ зашифрован и требует пароль для открытия. |
| [get_LoadFormat](./get_loadformat/)() const | Получает обнаруженный формат документа. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Примечания


Вы не создаёте экземпляры этого класса напрямую. Объекты этого класса возвращаются методами [DetectFileFormat()](../).

## Примеры



Показывает, как использовать класс [FileFormatUtil](../fileformatutil/) для обнаружения формата документа и шифрования.
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


Показывает, как использовать класс [FileFormatUtil](../fileformatutil/) для обнаружения формата документа и наличия цифровых подписей.
```cpp
// Используйте экземпляр FileFormatInfo, чтобы проверить, что документ не имеет цифровой подписи.
System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Document.docx");

ASSERT_EQ(u".docx", Aspose::Words::FileFormatUtil::LoadFormatToExtension(info->get_LoadFormat()));
ASSERT_FALSE(info->get_HasDigitalSignature());

System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw", nullptr);
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_SignTime(System::DateTime::get_Now());
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(get_MyDir() + u"Document.docx", get_ArtifactsDir() + u"File.DetectDigitalSignatures.docx", certificateHolder, signOptions);

// Используйте новый FileFormatInstance, чтобы подтвердить, что он подписан.
info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"File.DetectDigitalSignatures.docx");

ASSERT_TRUE(info->get_HasDigitalSignature());

// Мы можем загрузить и получить доступ к подписям подписанного документа в коллекции, как показано ниже.
ASSERT_EQ(1, Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(get_ArtifactsDir() + u"File.DetectDigitalSignatures.docx")->get_Count());
```

## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
