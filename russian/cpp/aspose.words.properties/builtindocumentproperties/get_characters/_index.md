---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Characters метод"
linktitle: "get_Characters"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Characters метод. Представляет оценку количества символов в документе в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.properties/builtindocumentproperties/get_characters/
---
## BuiltInDocumentProperties::get_Characters method


Представляет оценку количества символов в документе.

```cpp
int32_t Aspose::Words::Properties::BuiltInDocumentProperties::get_Characters()
```

## Примечания


Aspose.Words обновляет это свойство, когда вы вызываете [UpdateWordCount](../../../aspose.words/document/updatewordcount/).

## Примеры



Показывает, как обновить все метки списков в документе.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder->Write(System::String(u"Ut enim ad minim veniam, ") + u"quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Aspose.Words не отслеживает такие метрики документа в реальном времени.
ASSERT_EQ(0, doc->get_BuiltInDocumentProperties()->get_Characters());
ASSERT_EQ(0, doc->get_BuiltInDocumentProperties()->get_Words());
ASSERT_EQ(1, doc->get_BuiltInDocumentProperties()->get_Paragraphs());
ASSERT_EQ(1, doc->get_BuiltInDocumentProperties()->get_Lines());

// Чтобы получить точные значения трёх из этих свойств, их необходимо обновить вручную.
doc->UpdateWordCount();

ASSERT_EQ(196, doc->get_BuiltInDocumentProperties()->get_Characters());
ASSERT_EQ(36, doc->get_BuiltInDocumentProperties()->get_Words());
ASSERT_EQ(2, doc->get_BuiltInDocumentProperties()->get_Paragraphs());

// Для подсчёта строк нам потребуется вызвать определённую перегрузку метода обновления.
ASSERT_EQ(1, doc->get_BuiltInDocumentProperties()->get_Lines());

doc->UpdateWordCount(true);

ASSERT_EQ(4, doc->get_BuiltInDocumentProperties()->get_Lines());
```

## См. также

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
