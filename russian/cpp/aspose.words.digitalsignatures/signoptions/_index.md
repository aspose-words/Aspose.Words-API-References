---
title: "Класс Aspose::Words::DigitalSignatures::SignOptions"
linktitle: "SignOptions"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::DigitalSignatures::SignOptions. Позволяет задавать параметры подписи документа. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.digitalsignatures/signoptions/
---
## SignOptions class


Позволяет задавать параметры подписи документа. Чтобы узнать больше, посетите статью документации [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/).

```cpp
class SignOptions : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_ApplicationVersion](./get_applicationversion/)() const | Получает или задает версию приложения для цифровой подписи. Значение по умолчанию — "12.0". |
| [get_ColorDepth](./get_colordepth/)() const | Получает или задает глубину цвета для цифровой подписи. Значение по умолчанию — 32. |
| [get_Comments](./get_comments/)() const | Указывает комментарии к цифровой подписи. Значение по умолчанию — **empty string**. |
| [get_DecryptionPassword](./get_decryptionpassword/)() const | Пароль для расшифровки исходного документа. Значение по умолчанию — **empty string**. |
| [get_HorizontalResolution](./get_horizontalresolution/)() const | Получает или задает горизонтальное разрешение для цифровой подписи. Значение по умолчанию — 1920. |
| [get_OfficeVersion](./get_officeversion/)() const | Получает или задает версию Office для цифровой подписи. Значение по умолчанию — "12.0". |
| [get_ProviderId](./get_providerid/)() const | Указывает идентификатор класса поставщика подписи. Значение по умолчанию — **Empty (all zeroes) Guid**. |
| [get_SignatureLineId](./get_signaturelineid/)() const | Идентификатор строки подписи. Значение по умолчанию — **Empty (all zeroes) Guid**. |
| [get_SignatureLineImage](./get_signaturelineimage/)() const | Изображение, которое будет отображаться в связанной [SignatureLine](../../aspose.words.drawing/signatureline/). Значение по умолчанию — **null**. |
| [get_SignTime](./get_signtime/)() const | Дата подписи. Значение по умолчанию — **current time** (**Now**) |
| [get_VerticalResolution](./get_verticalresolution/)() const | Получает или задает вертикальное разрешение для цифровой подписи. Значение по умолчанию — 1200. |
| [get_WindowsVersion](./get_windowsversion/)() const | Получает или задает версию Windows для цифровой подписи. Значение по умолчанию — "6.1". |
| [get_XmlDsigLevel](./get_xmldsiglevel/)() const | Указывает уровень цифровой подписи на основе стандарта XML-DSig. Значение по умолчанию — [XmlDSig](../xmldsiglevel/). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ApplicationVersion](./set_applicationversion/)(const System::String\&) | Сеттер для [Aspose::Words::DigitalSignatures::SignOptions::get_ApplicationVersion](./get_applicationversion/). |
| [set_ColorDepth](./set_colordepth/)(int32_t) | Сеттер для [Aspose::Words::DigitalSignatures::SignOptions::get_ColorDepth](./get_colordepth/). |
| [set_Comments](./set_comments/)(const System::String\&) | Сеттер для [Aspose::Words::DigitalSignatures::SignOptions::get_Comments](./get_comments/). |
| [set_DecryptionPassword](./set_decryptionpassword/)(const System::String\&) | Сеттер для [Aspose::Words::DigitalSignatures::SignOptions::get_DecryptionPassword](./get_decryptionpassword/). |
| [set_HorizontalResolution](./set_horizontalresolution/)(int32_t) | Сеттер для [Aspose::Words::DigitalSignatures::SignOptions::get_HorizontalResolution](./get_horizontalresolution/). |
| [set_OfficeVersion](./set_officeversion/)(const System::String\&) | Сеттер для [Aspose::Words::DigitalSignatures::SignOptions::get_OfficeVersion](./get_officeversion/). |
| [set_ProviderId](./set_providerid/)(System::Guid) | Сеттер для [Aspose::Words::DigitalSignatures::SignOptions::get_ProviderId](./get_providerid/). |
| [set_SignatureLineId](./set_signaturelineid/)(System::Guid) | Идентификатор строки подписи. Значение по умолчанию — **Empty (all zeroes) Guid**. |
| [set_SignatureLineImage](./set_signaturelineimage/)(const System::ArrayPtr\<uint8_t\>\&) | Изображение, которое будет отображаться в связанной [SignatureLine](../../aspose.words.drawing/signatureline/). Значение по умолчанию — **null**. |
| [set_SignTime](./set_signtime/)(System::DateTime) | Сеттер для [Aspose::Words::DigitalSignatures::SignOptions::get_SignTime](./get_signtime/). |
| [set_VerticalResolution](./set_verticalresolution/)(int32_t) | Сеттер для [Aspose::Words::DigitalSignatures::SignOptions::get_VerticalResolution](./get_verticalresolution/). |
| [set_WindowsVersion](./set_windowsversion/)(const System::String\&) | Сеттер для [Aspose::Words::DigitalSignatures::SignOptions::get_WindowsVersion](./get_windowsversion/). |
| [set_XmlDsigLevel](./set_xmldsiglevel/)(Aspose::Words::DigitalSignatures::XmlDsigLevel) | Сеттер для [Aspose::Words::DigitalSignatures::SignOptions::get_XmlDsigLevel](./get_xmldsiglevel/). |
| [SignOptions](./signoptions/)() |  |
| static [Type](./type/)() |  |

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

## См. также

* Namespace [Aspose::Words::DigitalSignatures](../)
* Library [Aspose.Words for C++](../../)
