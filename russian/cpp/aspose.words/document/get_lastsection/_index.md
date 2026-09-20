---
title: "Метод Aspose::Words::Document::get_LastSection"
linktitle: "get_LastSection"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Document::get_LastSection. Получает последний раздел в документе на C++."
type: docs
weight: 35000
url: /ru/cpp/aspose.words/document/get_lastsection/
---
## Document::get_LastSection method


Получает последний раздел в документе.

```cpp
System::SharedPtr<Aspose::Words::Section> Aspose::Words::Document::get_LastSection()
```


## Примеры



Показывает, как создать новую секцию с помощью DocumentBuilder.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Пустой документ содержит одну секцию по умолчанию,
// которая содержит дочерние узлы, которые мы можем редактировать.
ASSERT_EQ(1, doc->get_Sections()->get_Count());

// Используйте DocumentBuilder, чтобы добавить текст в первую секцию.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Создайте вторую секцию, вставив разрыв секции.
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

ASSERT_EQ(2, doc->get_Sections()->get_Count());

// Каждая секция имеет свои собственные настройки разметки страницы.
// Мы можем разбить текст во второй секции на две колонки.
// Это не повлияет на текст в первой секции.
doc->get_LastSection()->get_PageSetup()->get_TextColumns()->SetCount(2);
builder->Writeln(u"Column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Column 2.");

ASSERT_EQ(1, doc->get_FirstSection()->get_PageSetup()->get_TextColumns()->get_Count());
ASSERT_EQ(2, doc->get_LastSection()->get_PageSetup()->get_TextColumns()->get_Count());

doc->Save(get_ArtifactsDir() + u"Section.Create.docx");
```

## См. также

* Class [Section](../../section/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
