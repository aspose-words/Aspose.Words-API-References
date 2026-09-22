---
title: "Aspose::Words::Saving::PdfEncryptionDetails class"
linktitle: "PdfEncryptionDetails"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::PdfEncryptionDetails class. يحتوي على تفاصيل تشفير وصلاحيات الوصول لمستند PDF. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 24000
url: /ar/cpp/aspose.words.saving/pdfencryptiondetails/
---
## PdfEncryptionDetails class


يحتوي على تفاصيل تشفير وصلاحيات الوصول لمستند PDF. لمعرفة المزيد، قم بزيارة مقالة الوثائق [Protect or Encrypt a Document](https://docs.aspose.com/words/cpp/protect-or-encrypt-a-document/).

```cpp
class PdfEncryptionDetails : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_OwnerPassword](./get_ownerpassword/)() const | يحدد كلمة مرور المالك للمستند PDF المشفر. |
| [get_Permissions](./get_permissions/)() const | يحدد العمليات المسموح بها للمستخدم على مستند PDF مشفر. القيمة الافتراضية هي [DisallowAll](../pdfpermissions/). |
| [get_UserPassword](./get_userpassword/)() const | يحدد كلمة مرور المستخدم المطلوبة لفتح مستند PDF المشفر. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PdfEncryptionDetails](./pdfencryptiondetails/)(const System::String\&, const System::String\&) | يُهيئ مثيلًا من هذه الفئة. |
| [PdfEncryptionDetails](./pdfencryptiondetails/)(const System::String\&, const System::String\&, Aspose::Words::Saving::PdfPermissions) | يُهيئ مثيلًا من هذه الفئة. |
| [set_OwnerPassword](./set_ownerpassword/)(const System::String\&) | المحدد لـ [Aspose::Words::Saving::PdfEncryptionDetails::get_OwnerPassword](./get_ownerpassword/). |
| [set_Permissions](./set_permissions/)(Aspose::Words::Saving::PdfPermissions) | يحدد العمليات المسموح بها للمستخدم على مستند PDF مشفر. القيمة الافتراضية هي [DisallowAll](../pdfpermissions/). |
| [set_UserPassword](./set_userpassword/)(const System::String\&) | المحدد لـ [Aspose::Words::Saving::PdfEncryptionDetails::get_UserPassword](./get_userpassword/). |
| static [Type](./type/)() |  |
## انظر أيضًا

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
