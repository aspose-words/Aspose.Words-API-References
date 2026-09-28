---
title: "Aspose::Words::Settings::WriteProtection::ValidatePassword метод"
linktitle: "ValidatePassword"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Settings::WriteProtection::ValidatePassword метод. Возвращает true, если указанный пароль совпадает с паролем защиты от записи, которым документ был защищён. Если документ не защищён паролем от записи, возвращает false в C++."
type: docs
weight: 8000
url: /ru/cpp/aspose.words.settings/writeprotection/validatepassword/
---
## WriteProtection::ValidatePassword method


Возвращает **true**, если указанный пароль совпадает с паролем защиты записи, которым документ был защищён. Если документ не защищён паролем записи, возвращает **false**.

```cpp
bool Aspose::Words::Settings::WriteProtection::ValidatePassword(const System::String &password)
```


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
