---
title: "Метод Aspose::Words::FileFormatInfo::get_HasDigitalSignature"
linktitle: "get_HasDigitalSignature"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::FileFormatInfo::get_HasDigitalSignature. Возвращает true, если данный документ содержит цифровую подпись. Это свойство лишь информирует о наличии цифровой подписи в документе, но не указывает, действительна она или нет в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words/fileformatinfo/get_hasdigitalsignature/
---
## FileFormatInfo::get_HasDigitalSignature method


Возвращает **true**, если документ содержит цифровую подпись. Это свойство лишь информирует о наличии цифровой подписи в документе, но не указывает, действительна она или нет.

```cpp
bool Aspose::Words::FileFormatInfo::get_HasDigitalSignature() const
```

## Примечания


Это свойство существует, чтобы помочь вам различать документы с цифровой подписью и без неё. Если вы используете Aspose.Words для изменения и сохранения документа, подписанного цифровой подписью, подпись будет потеряна. Это задумано так, потому что цифровая подпись предназначена для защиты подлинности документа. Используя это свойство, вы можете обнаружить цифрово подписанные документы перед их обработкой так же, как обычные документы, и предпринять действия, чтобы избежать потери цифровой подписи, например, уведомить пользователя.

## Примеры



Показывает, как использовать класс [FileFormatUtil](../../fileformatutil/) для определения формата документа и наличия цифровых подписей.
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

* Class [FileFormatInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
