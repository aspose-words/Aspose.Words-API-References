---
title: "Метод Aspose::Words::Fields::Field::get_IsDirty"
linktitle: "get_IsDirty"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Fields::Field::get_IsDirty. Получает или задает, является ли текущий результат поля более некорректным (устаревшим) из‑за других изменений, внесённых в документ в C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words.fields/field/get_isdirty/
---
## Field::get_IsDirty method


Получает или задает, является ли текущий результат поля более некорректным (устаревшим) из‑за других изменений, внесённых в документ.

```cpp
bool Aspose::Words::Fields::Field::get_IsDirty()
```


## Примеры



Показывает, как использовать специальное свойство для обновления результата поля.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Задайте встроенное свойство документа "Author", а затем отобразите его с помощью поля.
doc->get_BuiltInDocumentProperties()->set_Author(u"John Doe");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldAuthor>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true));

ASSERT_FALSE(field->get_IsDirty());
ASSERT_EQ(u"John Doe", field->get_Result());

// Обновите свойство. Поле всё ещё отображает старое значение.
doc->get_BuiltInDocumentProperties()->set_Author(u"John & Jane Doe");

ASSERT_EQ(u"John Doe", field->get_Result());

// Поскольку значение поля устарело, мы можем пометить его как "dirty".
// Это значение останется устаревшим, пока мы не обновим поле вручную с помощью метода Field.Update().
field->set_IsDirty(true);

{
    auto docStream = System::MakeObject<System::IO::MemoryStream>();
    // Если мы сохраним без вызова метода обновления,
    // поле будет продолжать отображать устаревшее значение в выходном документе.
    doc->Save(docStream, Aspose::Words::SaveFormat::Docx);

    // Объект LoadOptions имеет опцию обновления всех полей
    // отмеченных как "dirty" при загрузке документа.
    auto options = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
    options->set_UpdateDirtyFields(updateDirtyFields);
    doc = System::MakeObject<Aspose::Words::Document>(docStream, options);

    ASSERT_EQ(u"John & Jane Doe", doc->get_BuiltInDocumentProperties()->get_Author());

    field = System::ExplicitCast<Aspose::Words::Fields::FieldAuthor>(doc->get_Range()->get_Fields()->idx_get(0));

    // Обновление таких dirty‑полей автоматически сбрасывает их флаг "IsDirty" в false.
    if (updateDirtyFields)
    {
        ASSERT_EQ(u"John & Jane Doe", field->get_Result());
        ASSERT_FALSE(field->get_IsDirty());
    }
    else
    {
        ASSERT_EQ(u"John Doe", field->get_Result());
        ASSERT_TRUE(field->get_IsDirty());
    }
}
```

## См. также

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
