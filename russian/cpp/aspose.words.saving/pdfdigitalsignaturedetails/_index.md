---
title: "Aspose::Words::Saving::PdfDigitalSignatureDetails class"
linktitle: "PdfDigitalSignatureDetails"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::PdfDigitalSignatureDetails class. Содержит детали для подписи PDF‑документа цифровой подписью в C++."
type: docs
weight: 22000
url: /ru/cpp/aspose.words.saving/pdfdigitalsignaturedetails/
---
## PdfDigitalSignatureDetails class


Содержит детали подписи PDF‑документа цифровой подписью.

```cpp
class PdfDigitalSignatureDetails : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_CertificateHolder](./get_certificateholder/)() const | Возвращает объект держателя сертификата, содержащий сертификат, использованный для подписи документа. |
| [get_HashAlgorithm](./get_hashalgorithm/)() const | Получает алгоритм хеширования. |
| [get_Location](./get_location/)() const | Получает место подписи. |
| [get_Reason](./get_reason/)() const | Получает причину подписи. |
| [get_SignatureDate](./get_signaturedate/)() const | Получает или задает дату подписи. |
| [get_TimestampSettings](./get_timestampsettings/)() const | Получает или задает настройки временной метки цифровой подписи. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PdfDigitalSignatureDetails](./pdfdigitalsignaturedetails/)() | Инициализирует экземпляр этого класса. |
| [PdfDigitalSignatureDetails](./pdfdigitalsignaturedetails/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&, const System::String\&, const System::String\&, System::DateTime) | Инициализирует экземпляр этого класса. |
| [set_CertificateHolder](./set_certificateholder/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&) | Возвращает объект держателя сертификата, содержащий сертификат, использованный для подписи документа. |
| [set_HashAlgorithm](./set_hashalgorithm/)(Aspose::Words::Saving::PdfDigitalSignatureHashAlgorithm) | Устанавливает алгоритм хеширования. |
| [set_Location](./set_location/)(const System::String\&) | Устанавливает расположение подписи. |
| [set_Reason](./set_reason/)(const System::String\&) | Устанавливает причину подписи. |
| [set_SignatureDate](./set_signaturedate/)(System::DateTime) | Сеттер для [Aspose::Words::Saving::PdfDigitalSignatureDetails::get_SignatureDate](./get_signaturedate/). |
| [set_TimestampSettings](./set_timestampsettings/)(const System::SharedPtr\<Aspose::Words::Saving::PdfDigitalSignatureTimestampSettings\>\&) | Сеттер для [Aspose::Words::Saving::PdfDigitalSignatureDetails::get_TimestampSettings](./get_timestampsettings/). |
| static [Type](./type/)() |  |
## Примечания


В настоящее время цифровая подпись PDF‑документов доступна только на .NET 3.5 и выше.

Чтобы цифрово подписать PDF‑документ, созданный Aspose.Words, установите свойство [DigitalSignatureDetails](../pdfsaveoptions/get_digitalsignaturedetails/) в действительный объект [PdfDigitalSignatureDetails](./) и затем сохраните документ в формате PDF, передав [PdfSaveOptions](../pdfsaveoptions/) в качестве параметра методу [Save()](../).

Aspose.Words создает PKCS#7 подпись для всего PDF‑документа и использует фильтр "Adobe.PPKMS" и субфильтр "adbe.pkcs7.sha1" при создании цифровой подписи.

## См. также

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
