---
title: "Aspose::Words::Fields::FieldIndex::get_CrossReferenceSeparator метод"
linktitle: "get_CrossReferenceSeparator"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FieldIndex::get_CrossReferenceSeparator метод. Получает или задает последовательность символов, используемую для разделения перекрестных ссылок и других записей в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.fields/fieldindex/get_crossreferenceseparator/
---
## FieldIndex::get_CrossReferenceSeparator method


Получает или задает последовательность символов, используемую для разделения перекрёстных ссылок и других записей.

```cpp
System::String Aspose::Words::Fields::FieldIndex::get_CrossReferenceSeparator()
```


## Примеры



Показывает, как определить перекрестные ссылки в поле INDEX.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Создайте поле INDEX, которое будет отображать запись для каждого найденного в документе поля XE.
// Каждая запись будет отображать значение свойства Text поля XE слева,
// а номер страницы, содержащей поле XE, — справа.
// Запись INDEX будет собирать все поля XE с совпадающими значениями в свойстве "Text"
// в одну запись, а не создавать отдельную запись для каждого поля XE.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// Мы можем настроить поле XE так, чтобы его запись INDEX отображала строку вместо номера страницы.
// Во-первых, для записей, которые заменяют номер страницы строкой,
// укажите пользовательский разделитель между значением свойства Text поля XE и строкой.
index->set_CrossReferenceSeparator(u", see: ");

ASSERT_EQ(u" INDEX  \\k \", see: \"", index->GetFieldCode());

// Вставьте поле XE, которое создает обычную запись INDEX, отображающую номер страницы этого поля,
// и не использует значение CrossReferenceSeparator.
// Запись для этого поля XE будет отображать "Apple, 2".
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Apple");

ASSERT_EQ(u" XE  Apple", indexEntry->GetFieldCode());

// Вставьте еще одно поле XE на странице 3 и задайте значение свойства PageNumberReplacement.
// Это значение будет отображаться вместо номера страницы, на которой находится это поле,
// и значение CrossReferenceSeparator поля INDEX появится перед ним.
// Запись для этого поля XE будет отображать "Banana, see: Tropical fruit".
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Banana");
indexEntry->set_PageNumberReplacement(u"Tropical fruit");

ASSERT_EQ(u" XE  Banana \\t \"Tropical fruit\"", indexEntry->GetFieldCode());

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.CrossReferenceSeparator.docx");
```

## См. также

* Class [FieldIndex](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
