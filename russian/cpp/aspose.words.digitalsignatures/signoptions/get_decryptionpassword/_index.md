---
title: "Метод Aspose::Words::DigitalSignatures::SignOptions::get_DecryptionPassword"
linktitle: "get_DecryptionPassword"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::DigitalSignatures::SignOptions::get_DecryptionPassword метод. Пароль для расшифровки исходного документа. Значение по умолчанию — пустая строка в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.digitalsignatures/signoptions/get_decryptionpassword/
---
## SignOptions::get_DecryptionPassword method


Пароль для расшифровки исходного документа. Значение по умолчанию — **empty string**.

```cpp
System::String Aspose::Words::DigitalSignatures::SignOptions::get_DecryptionPassword() const
```


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

* Class [SignOptions](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
