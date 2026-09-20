---
title: "Класс Aspose::Words::DigitalSignatures::DigitalSignature"
linktitle: "DigitalSignature"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::DigitalSignatures::DigitalSignature. Представляет цифровую подпись документа и результат её проверки. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.digitalsignatures/digitalsignature/
---
## DigitalSignature class


Представляет цифровую подпись в документе и результат её проверки. Чтобы узнать больше, посетите статью документации [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/).

```cpp
class DigitalSignature : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_ApplicationVersion](./get_applicationversion/)() | Получает версию приложения для цифровой подписи. |
| [get_CertificateHolder](./get_certificateholder/)() const | Возвращает объект держателя сертификата, содержащий сертификат, использованный для подписи документа. |
| [get_ColorDepth](./get_colordepth/)() | Получает глубину цвета для цифровой подписи. |
| [get_Comments](./get_comments/)() | Получает комментарий цели подписи. |
| [get_HorizontalResolution](./get_horizontalresolution/)() | Получает горизонтальное разрешение для цифровой подписи. |
| [get_IssuerName](./get_issuername/)() | Возвращает отличительное имя субъекта сертификата издателя. |
| [get_IsValid](./get_isvalid/)() const | Возвращает **true**, если эта цифровая подпись действительна и документ не был изменён. |
| [get_OfficeVersion](./get_officeversion/)() | Получает версию Office для цифровой подписи. |
| [get_SignatureType](./get_signaturetype/)() const | Получает тип цифровой подписи. |
| [get_SignatureValue](./get_signaturevalue/)() const | Получает массив байтов, представляющих значение подписи. |
| [get_SignTime](./get_signtime/)() const | Получает время подписи документа. |
| [get_SubjectName](./get_subjectname/)() | Возвращает отличительное имя субъекта сертификата, использованного для подписи документа. |
| [get_VerticalResolution](./get_verticalresolution/)() | Получает вертикальное разрешение для цифровой подписи. |
| [get_WindowsVersion](./get_windowsversion/)() | Получает версию Windows для цифровой подписи. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ToString](./tostring/)() const override | Возвращает удобочитаемую строку, отображающую значение этого объекта. |
| static [Type](./type/)() |  |

## Примеры



Показывает, как проверять и отображать информацию о каждой подписи в документе.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Digitally signed.docx");

for (auto&& signature : doc->get_DigitalSignatures())
{
    std::cout << System::String::Format(u"{0} signature: ", (signature->get_IsValid() ? System::String(u"Valid") : System::String(u"Invalid"))) << std::endl;
    std::cout << System::String::Format(u"\tReason:\t{0}", signature->get_Comments()) << std::endl;
    std::cout << System::String::Format(u"\tType:\t{0}", signature->get_SignatureType()) << std::endl;
    std::cout << System::String::Format(u"\tSign time:\t{0}", signature->get_SignTime()) << std::endl;
    std::cout << System::String::Format(u"\tSubject name:\t{0}", signature->get_CertificateHolder()->get_Certificate()->get_SubjectName()) << std::endl;
    std::cout << System::String::Format(u"\tIssuer name:\t{0}", signature->get_CertificateHolder()->get_Certificate()->get_IssuerName()->get_Name()) << std::endl;
    std::cout << std::endl;
}
```

## См. также

* Namespace [Aspose::Words::DigitalSignatures](../)
* Library [Aspose.Words for C++](../../)
