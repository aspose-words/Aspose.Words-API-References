---
title: "Aspose::Words::Saving::PdfDigitalSignatureDetails فئة"
linktitle: "PdfDigitalSignatureDetails"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::PdfDigitalSignatureDetails فئة. يحتوي على تفاصيل توقيع مستند PDF بتوقيع رقمي في C++."
type: docs
weight: 22000
url: /ar/cpp/aspose.words.saving/pdfdigitalsignaturedetails/
---
## PdfDigitalSignatureDetails class


يحتوي على تفاصيل توقيع مستند PDF باستخدام توقيع رقمي.

```cpp
class PdfDigitalSignatureDetails : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_CertificateHolder](./get_certificateholder/)() const | يعيد كائن حامل الشهادة الذي يحتوي على الشهادة المستخدمة لتوقيع المستند. |
| [get_HashAlgorithm](./get_hashalgorithm/)() const | يحصل على خوارزمية التجزئة. |
| [get_Location](./get_location/)() const | يحصل على موقع التوقيع. |
| [get_Reason](./get_reason/)() const | يحصل على سبب التوقيع. |
| [get_SignatureDate](./get_signaturedate/)() const | يحصل أو يضبط تاريخ التوقيع. |
| [get_TimestampSettings](./get_timestampsettings/)() const | يحصل أو يضبط إعدادات الطابع الزمني للتوقيع الرقمي. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PdfDigitalSignatureDetails](./pdfdigitalsignaturedetails/)() | يُهيئ مثيلًا من هذه الفئة. |
| [PdfDigitalSignatureDetails](./pdfdigitalsignaturedetails/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&, const System::String\&, const System::String\&, System::DateTime) | يُهيئ مثيلًا من هذه الفئة. |
| [set_CertificateHolder](./set_certificateholder/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&) | يعيد كائن حامل الشهادة الذي يحتوي على الشهادة المستخدمة لتوقيع المستند. |
| [set_HashAlgorithm](./set_hashalgorithm/)(Aspose::Words::Saving::PdfDigitalSignatureHashAlgorithm) | يضبط خوارزمية التجزئة. |
| [set_Location](./set_location/)(const System::String\&) | يضبط موقع التوقيع. |
| [set_Reason](./set_reason/)(const System::String\&) | يضبط سبب التوقيع. |
| [set_SignatureDate](./set_signaturedate/)(System::DateTime) | دالة تعيين لـ [Aspose::Words::Saving::PdfDigitalSignatureDetails::get_SignatureDate](./get_signaturedate/). |
| [set_TimestampSettings](./set_timestampsettings/)(const System::SharedPtr\<Aspose::Words::Saving::PdfDigitalSignatureTimestampSettings\>\&) | دالة تعيين لـ [Aspose::Words::Saving::PdfDigitalSignatureDetails::get_TimestampSettings](./get_timestampsettings/). |
| static [Type](./type/)() |  |
## ملاحظات


في الوقت الحالي، التوقيع الرقمي على مستندات PDF متاح فقط على .NET 3.5 أو أعلى.

لتوقيع مستند PDF رقمياً عندما يتم إنشاؤه بواسطة Aspose.Words، اضبط خاصية [DigitalSignatureDetails](../pdfsaveoptions/get_digitalsignaturedetails/) إلى كائن [PdfDigitalSignatureDetails](./) صالح ثم احفظ المستند بصيغة PDF مع تمرير [PdfSaveOptions](../pdfsaveoptions/) كمعامل إلى طريقة [Save()](../).

يقوم Aspose.Words بإنشاء توقيع PKCS#7 على كامل مستند PDF ويستخدم مرشح "Adobe.PPKMS" والمرشح الفرعي "adbe.pkcs7.sha1" عند إنشاء توقيع رقمي.

## انظر أيضًا

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
