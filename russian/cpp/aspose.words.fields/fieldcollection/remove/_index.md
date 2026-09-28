---
title: "Метод Aspose::Words::Fields::FieldCollection::Remove"
linktitle: "Remove"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Fields::FieldCollection::Remove. Удаляет указанное поле из этой коллекции и из документа в C++."
type: docs
weight: 8000
url: /ru/cpp/aspose.words.fields/fieldcollection/remove/
---
## FieldCollection::Remove method


Удаляет указанное поле из этой коллекции и из документа.

```cpp
void Aspose::Words::Fields::FieldCollection::Remove(const System::SharedPtr<Aspose::Words::Fields::Field> &field)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| поле | const System::SharedPtr\<Aspose::Words::Fields::Field\>\& | Поле для удаления. |

## Примеры



Показывает, как удалять поля из коллекции полей.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertField(u" DATE \\@ \"dddd, d MMMM yyyy\" ");
builder->InsertField(u" TIME ");
builder->InsertField(u" REVNUM ");
builder->InsertField(u" AUTHOR  \"John Doe\" ");
builder->InsertField(u" SUBJECT \"My Subject\" ");
builder->InsertField(u" QUOTE \"Hello world!\" ");
doc->UpdateFields();

System::SharedPtr<Aspose::Words::Fields::FieldCollection> fields = doc->get_Range()->get_Fields();

ASSERT_EQ(6, fields->get_Count());

// Ниже представлены четыре способа удаления полей из коллекции полей.
// 1 -  Получить поле, которое удалит себя:
fields->idx_get(0)->Remove();
ASSERT_EQ(5, fields->get_Count());

// 2 -  Получить коллекцию, чтобы удалить поле, которое мы передаём её методу удаления:
System::SharedPtr<Aspose::Words::Fields::Field> lastField = fields->idx_get(3);
fields->Remove(lastField);
ASSERT_EQ(4, fields->get_Count());

// 3 -  Удалить поле из коллекции по индексу:
fields->RemoveAt(2);
ASSERT_EQ(3, fields->get_Count());

// 4 -  Удалить все поля из коллекции сразу:
fields->Clear();
ASSERT_EQ(0, fields->get_Count());
```

## См. также

* Class [Field](../../field/)
* Class [FieldCollection](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
