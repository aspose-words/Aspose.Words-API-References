---
title: "Aspose::Words::Settings::WriteProtection::SetPassword метод"
linktitle: "SetPassword"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Settings::WriteProtection::SetPassword метод. Устанавливает пароль защиты от записи для документа в C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words.settings/writeprotection/setpassword/
---
## WriteProtection::SetPassword method


Устанавливает пароль защиты записи для документа.

```cpp
void Aspose::Words::Settings::WriteProtection::SetPassword(const System::String &password)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| password | const System::String\& | Пароль для установки. Не может быть **null**, но может быть пустой строкой. |
## Примечания


Если пароль установлен, Microsoft Word потребует от пользователя ввести его или открыть документ только для чтения.

## Примеры



Показывает, как защитить документ паролем.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world! This document is protected.");

// Введите пароль длиной до 15 символов, а затем проверьте статус защиты документа.
doc->get_WriteProtection()->SetPassword(u"MyPassword");
doc->get_WriteProtection()->set_ReadOnlyRecommended(true);

ASSERT_TRUE(doc->get_WriteProtection()->get_IsWriteProtected());
ASSERT_TRUE(doc->get_WriteProtection()->ValidatePassword(u"MyPassword"));

// Защита не препятствует программному редактированию документа и не шифрует его содержимое.
doc->Save(get_ArtifactsDir() + u"Document.WriteProtection.docx");
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.WriteProtection.docx");

ASSERT_TRUE(doc->get_WriteProtection()->get_IsWriteProtected());

builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->Writeln(u"Writing text in a protected document.");

ASSERT_EQ(System::String(u"Hello world! This document is protected.") + u"\rWriting text in a protected document.", doc->GetText().Trim());
```

## См. также

* Class [WriteProtection](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
