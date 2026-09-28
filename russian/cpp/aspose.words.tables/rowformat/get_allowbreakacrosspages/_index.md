---
title: "Aspose::Words::Tables::RowFormat::get_AllowBreakAcrossPages метод"
linktitle: "get_AllowBreakAcrossPages"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Tables::RowFormat::get_AllowBreakAcrossPages метод. Возвращает true, если текст в строке таблицы может быть разбит при разрыве страницы в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.tables/rowformat/get_allowbreakacrosspages/
---
## RowFormat::get_AllowBreakAcrossPages method


Истина, если текст в строке таблицы может разбиваться при разрыве страницы.

```cpp
bool Aspose::Words::Tables::RowFormat::get_AllowBreakAcrossPages()
```


## Примеры



Показывает, как отключить разбиение строк таблицы по страницам для каждой строки в таблице.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table spanning two pages.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Установите свойство "AllowBreakAcrossPages" в "false", чтобы сохранить строку
// в одну часть, если таблица занимает две страницы, и разрывается вдоль этой строки.
// Если строка слишком велика, чтобы поместиться на одной странице, Microsoft Word перенесёт её на следующую страницу.
// Установите свойство "AllowBreakAcrossPages" в "true", чтобы разрешить разбиение строки на две страницы.
for (auto&& row : System::IterateOver<Aspose::Words::Tables::Row>(table))
{
    row->get_RowFormat()->set_AllowBreakAcrossPages(allowBreakAcrossPages);
}

doc->Save(get_ArtifactsDir() + u"Table.AllowBreakAcrossPages.docx");
```

## См. также

* Class [RowFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
