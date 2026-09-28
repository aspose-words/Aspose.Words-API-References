---
title: "Aspose::Words::DigitalSignatures::CertificateHolder class"
linktitle: "CertificateHolder"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::DigitalSignatures::CertificateHolder class. Представляет держателя экземпляра X509Certificate2. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 1000
url: /ru/cpp/aspose.words.digitalsignatures/certificateholder/
---
## CertificateHolder class


Представляет держатель экземпляра **X509Certificate2**. Чтобы узнать больше, посетите статью документации [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/).

```cpp
class CertificateHolder : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| static [Create](./create/)(const System::ArrayPtr\<uint8_t\>\&, const System::SharedPtr\<System::Security::SecureString\>\&) | Создаёт объект [CertificateHolder](./) используя массив байтов хранилища PKCS12 и его пароль. |
| static [Create](./create/)(const System::ArrayPtr\<uint8_t\>\&, const System::String\&) | Создаёт объект [CertificateHolder](./) используя массив байтов хранилища PKCS12 и его пароль. |
| static [Create](./create/)(const System::String\&, const System::String\&) | Создаёт объект [CertificateHolder](./) используя путь к хранилищу PKCS12 и его пароль. |
| static [Create](./create/)(const System::String\&, const System::String\&, const System::String\&) | Создаёт объект [CertificateHolder](./) используя путь к хранилищу PKCS12, его пароль и псевдоним, с помощью которого будет найден закрытый ключ и сертификат. |
| [get_Certificate](./get_certificate/)() | Возвращает экземпляр **X509Certificate2**, который содержит закрытый и открытый ключи и цепочку сертификатов. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Примечания


[CertificateHolder](./) can be created by static factory methods only. It contains an instance of **X509Certificate2** which is used to introduce private, public keys and certificate chains into the system. This class is applied in [DigitalSignatureUtil](../digitalsignatureutil/) and [PdfDigitalSignatureDetails](../../aspose.words.saving/pdfdigitalsignaturedetails/) instead of obsolete methods with **X509Certificate2** as parameters.

## Примеры



Показывает, как цифрово подписывать документы.
```cpp
// Создайте сертификат X.509 из хранилища PKCS#12, которое должно содержать закрытый ключ.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

// Создайте комментарий и дату, которые будут применены с нашей новой цифровой подписью.
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_Comments(u"My comment");
signOptions->set_SignTime(System::DateTime::get_Now());

// Возьмите неподписанный документ из локальной файловой системы через файловый поток,
// затем создайте подписанную копию, определяемую именем файла выходного файлового потока.
{
    System::SharedPtr<System::IO::Stream> streamIn = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Document.docx", System::IO::FileMode::Open);
    {
        System::SharedPtr<System::IO::Stream> streamOut = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"DigitalSignatureUtil.SignDocument.docx", System::IO::FileMode::OpenOrCreate);
        Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```


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

* Namespace [Aspose::Words::DigitalSignatures](../)
* Library [Aspose.Words for C++](../../)
