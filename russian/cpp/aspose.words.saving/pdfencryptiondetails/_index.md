---
title: "Aspose::Words::Saving::PdfEncryptionDetails class"
linktitle: "PdfEncryptionDetails"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::PdfEncryptionDetails class. Содержит детали шифрования и разрешений доступа для PDF‑документа. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 24000
url: /ru/cpp/aspose.words.saving/pdfencryptiondetails/
---
## PdfEncryptionDetails class


Содержит детали шифрования и прав доступа для PDF‑документа. Чтобы узнать больше, посетите статью документации [Protect or Encrypt a Document](https://docs.aspose.com/words/cpp/protect-or-encrypt-a-document/).

```cpp
class PdfEncryptionDetails : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_OwnerPassword](./get_ownerpassword/)() const | Указывает пароль владельца для зашифрованного PDF‑документа. |
| [get_Permissions](./get_permissions/)() const | Указывает операции, разрешённые пользователю на зашифрованном PDF‑документе. Значение по умолчанию — [DisallowAll](../pdfpermissions/). |
| [get_UserPassword](./get_userpassword/)() const | Указывает пароль пользователя, необходимый для открытия зашифрованного PDF‑документа. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PdfEncryptionDetails](./pdfencryptiondetails/)(const System::String\&, const System::String\&) | Инициализирует экземпляр этого класса. |
| [PdfEncryptionDetails](./pdfencryptiondetails/)(const System::String\&, const System::String\&, Aspose::Words::Saving::PdfPermissions) | Инициализирует экземпляр этого класса. |
| [set_OwnerPassword](./set_ownerpassword/)(const System::String\&) | Сеттер для [Aspose::Words::Saving::PdfEncryptionDetails::get_OwnerPassword](./get_ownerpassword/). |
| [set_Permissions](./set_permissions/)(Aspose::Words::Saving::PdfPermissions) | Указывает операции, разрешённые пользователю на зашифрованном PDF‑документе. Значение по умолчанию — [DisallowAll](../pdfpermissions/). |
| [set_UserPassword](./set_userpassword/)(const System::String\&) | Сеттер для [Aspose::Words::Saving::PdfEncryptionDetails::get_UserPassword](./get_userpassword/). |
| static [Type](./type/)() |  |
## См. также

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
