---
title: "Метод Aspose::Words::Document::get_WriteProtection"
linktitle: "get_WriteProtection"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Document::get_WriteProtection. Предоставляет доступ к параметрам защиты от записи документа в C++."
type: docs
weight: 61000
url: /ru/cpp/aspose.words/document/get_writeprotection/
---
## Document::get_WriteProtection method


Предоставляет доступ к параметрам защиты документа от записи.

```cpp
System::SharedPtr<Aspose::Words::Settings::WriteProtection> Aspose::Words::Document::get_WriteProtection()
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

* Class [WriteProtection](../../../aspose.words.settings/writeprotection/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
