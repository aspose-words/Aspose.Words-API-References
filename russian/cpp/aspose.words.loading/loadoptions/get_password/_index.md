---
title: "метод Aspose::Words::Loading::LoadOptions::get_Password"
linktitle: "get_Password"
second_title: "Справочник API Aspose.Words для C++"
description: "метод Aspose::Words::Loading::LoadOptions::get_Password. Получает или задает пароль для открытия зашифрованного документа. Может быть null или пустой строкой. По умолчанию null в C++."
type: docs
weight: 12000
url: /ru/cpp/aspose.words.loading/loadoptions/get_password/
---
## LoadOptions::get_Password method


Получает или задает пароль для открытия зашифрованного документа. Может быть **null** или пустой строкой. По умолчанию — **null**.

```cpp
System::String Aspose::Words::Loading::LoadOptions::get_Password() const
```

## Примечания


Вам необходимо знать пароль для открытия зашифрованного документа. Если документ не зашифрован, установите значение **null** или пустую строку.

## Примеры



Показывает, как подписать зашифрованный файл документа.
```cpp
// Создайте сертификат X.509 из хранилища PKCS#12, которое должно содержать закрытый ключ.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

// Создайте комментарий, дату и пароль расшифровки, которые будут применены с нашей новой цифровой подписью.
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_Comments(u"Comment");
signOptions->set_SignTime(System::DateTime::get_Now());
signOptions->set_DecryptionPassword(u"docPassword");

// Установите локальное системное имя файла для неподписанного входного документа и имя файла вывода для его новой цифрово подписанной копии.
System::String inputFileName = get_MyDir() + u"Encrypted.docx";
System::String outputFileName = get_ArtifactsDir() + u"DigitalSignatureUtil.DecryptionPassword.docx";

Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

## См. также

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
