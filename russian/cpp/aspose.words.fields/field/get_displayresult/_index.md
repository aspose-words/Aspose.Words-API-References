---
title: "Aspose::Words::Fields::Field::get_DisplayResult метод"
linktitle: "get_DisplayResult"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::Field::get_DisplayResult метод. Получает текст, представляющий отображаемый результат поля, в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.fields/field/get_displayresult/
---
## Field::get_DisplayResult method


Получает текст, представляющий отображаемый результат поля.

```cpp
System::String Aspose::Words::Fields::Field::get_DisplayResult()
```


## Примеры



Показывает, как получить реальный текст, который поле отображает в документе.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"This document was written by ");
auto fieldAuthor = System::ExplicitCast<Aspose::Words::Fields::FieldAuthor>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true));
fieldAuthor->set_AuthorName(u"John Doe");

// Мы можем использовать свойство DisplayResult, чтобы проверить, какой точный текст
// поле отобразило бы на своем месте в документе.
ASSERT_EQ(System::String::Empty, fieldAuthor->get_DisplayResult());

// Поля не поддерживают точные значения результатов в реальном времени.
// Чтобы убедиться, что наши поля отображают точные результаты в любой момент,
// например, непосредственно перед сохранением, нам нужно обновлять их вручную.
fieldAuthor->Update();

ASSERT_EQ(u"John Doe", fieldAuthor->get_DisplayResult());

doc->Save(get_ArtifactsDir() + u"Field.DisplayResult.docx");
```

## См. также

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
