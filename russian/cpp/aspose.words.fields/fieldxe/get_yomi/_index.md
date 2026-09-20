---
title: "метод Aspose::Words::Fields::FieldXE::get_Yomi"
linktitle: "get_Yomi"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FieldXE::get_Yomi method. Получает или задает yomi (первый фонетический символ для сортировки индексов) для записи индекса в C++."
type: docs
weight: 8000
url: /ru/cpp/aspose.words.fields/fieldxe/get_yomi/
---
## FieldXE::get_Yomi method


Получает или задает йоми (первый фонетический символ для сортировки индексов) для записи индекса.

```cpp
System::String Aspose::Words::Fields::FieldXE::get_Yomi()
```


## Примеры



Показывает, как сортировать записи поля INDEX фонетически.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Создайте поле INDEX, которое будет отображать запись для каждого найденного в документе поля XE.
// Каждая запись будет отображать значение свойства Text поля XE слева,
// а номер страницы, содержащей поле XE, — справа.
// Запись INDEX будет собирать все поля XE с совпадающими значениями в свойстве "Text"
// в одну запись, а не создавать отдельную запись для каждого поля XE.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// Таблица INDEX автоматически сортирует свои записи по значениям их свойств Text в алфавитном порядке.
// Установите таблицу INDEX для сортировки записей фонетически с использованием хираганы.
index->set_UseYomi(sortEntriesUsingYomi);

if (sortEntriesUsingYomi)
{
    ASSERT_EQ(u" INDEX  \\y", index->GetFieldCode());
}
else
{
    ASSERT_EQ(u" INDEX ", index->GetFieldCode());
}

// Вставьте 4 поля XE, которые отобразятся как записи в оглавлении поля INDEX.
// Свойство "Text" может содержать написание слова кандзи, произношение которого может быть неоднозначным,
// в то время как версия "Yomi" слова будет точно отражать его произношение с помощью хираганы.
// Если мы зададим нашему полю INDEX использовать Yomi, оно будет сортировать эти записи
// по значению их свойств Yomi, вместо их значений Text.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"愛子");
indexEntry->set_Yomi(u"あ");

ASSERT_EQ(u" XE  愛子 \\y あ", indexEntry->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"明美");
indexEntry->set_Yomi(u"あ");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"恵美");
indexEntry->set_Yomi(u"え");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"愛美");
indexEntry->set_Yomi(u"え");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.Yomi.docx");
```

## См. также

* Class [FieldXE](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
