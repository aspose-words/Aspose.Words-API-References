---
title: "Aspose::Words::Lists::ListFormat::get_ListLevelNumber method"
linktitle: "get_ListLevelNumber"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Lists::ListFormat::get_ListLevelNumber method. Получает или задаёт номер уровня списка (от 0 до 8) для абзаца в C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words.lists/listformat/get_listlevelnumber/
---
## ListFormat::get_ListLevelNumber method


Получает или задает номер уровня списка (от 0 до 8) для абзаца.

```cpp
int32_t Aspose::Words::Lists::ListFormat::get_ListLevelNumber()
```

## Примечания


В документах Word списки могут состоять из 1‑9 уровней, пронумерованных от 0 до 8.

Действует только когда свойство [List](../get_list/) установлено в ссылку на действительный список.

## Примеры



Показывает, как создавать маркированные и нумерованные списки.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Aspose.Words main advantages are:");

// Список позволяет организовывать и оформлять наборы абзацев с помощью префиксных символов и отступов.
// Мы можем создавать вложенные списки, увеличивая уровень отступа.
// Мы можем начинать и завершать список, используя свойство "ListFormat" объекта document builder.
// Каждый абзац, который мы добавляем между началом и концом списка, становится элементом списка.
// Ниже представлены два типа списков, которые мы можем создать с помощью Document Builder.
// 1 -  Маркированный список:
// Этот список будет применять отступ и символ маркера (\"•\") перед каждым абзацем.
builder->get_ListFormat()->ApplyBulletDefault();
builder->Writeln(u"Great performance");
builder->Writeln(u"High reliability");
builder->Writeln(u"Quality code and working");
builder->Writeln(u"Wide variety of features");
builder->Writeln(u"Easy to understand API");

// Завершите маркированный список.
builder->get_ListFormat()->RemoveNumbers();

builder->InsertBreak(Aspose::Words::BreakType::ParagraphBreak);
builder->Writeln(u"Aspose.Words allows:");

// 2 -  Нумерованный список:
// Нумерованные списки создают логический порядок для своих абзацев, нумеруя каждый элемент.
builder->get_ListFormat()->ApplyNumberDefault();

// Этот абзац является первым элементом. Первый элемент нумерованного списка будет иметь символ "1." в качестве маркера пункта.
builder->Writeln(u"Opening documents from different formats:");

ASSERT_EQ(0, builder->get_ListFormat()->get_ListLevelNumber());

// Вызовите метод "ListIndent", чтобы увеличить текущий уровень списка,
// это запустит новый автономный список с более глубоким отступом на текущем элементе первого уровня списка.
builder->get_ListFormat()->ListIndent();

ASSERT_EQ(1, builder->get_ListFormat()->get_ListLevelNumber());

// Это первые три пункта списка второго уровня, которые будут сохранять счёт
// независимо от счёта первого уровня списка. Согласно текущему формату списка,
// они будут иметь символы "a.", "b." и "c.".
builder->Writeln(u"DOC");
builder->Writeln(u"PDF");
builder->Writeln(u"HTML");

// Вызовите метод "ListOutdent", чтобы вернуться к предыдущему уровню списка.
builder->get_ListFormat()->ListOutdent();

ASSERT_EQ(0, builder->get_ListFormat()->get_ListLevelNumber());

// Эти два абзаца продолжат счёт первого уровня списка.
// Эти пункты будут иметь символы "2." и "3."
builder->Writeln(u"Processing documents");
builder->Writeln(u"Saving documents in different formats:");

// Если мы увеличим уровень списка до уровня, к которому ранее уже добавляли элементы,
// вложенный список будет отдельным от предыдущего, и его нумерация начнётся с начала.
// Эти пункты списка будут иметь символы "a.", "b.", "c.", "d." и "e".
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"DOC");
builder->Writeln(u"PDF");
builder->Writeln(u"HTML");
builder->Writeln(u"MHTML");
builder->Writeln(u"Plain text");

// Снова уменьшите уровень списка.
builder->get_ListFormat()->ListOutdent();
builder->Writeln(u"Doing many other things!");

// Завершите нумерованный список.
builder->get_ListFormat()->RemoveNumbers();

doc->Save(get_ArtifactsDir() + u"Lists.ApplyDefaultBulletsAndNumbers.docx");
```


Показывает, как работать с уровнями списка.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

ASSERT_FALSE(builder->get_ListFormat()->get_IsListItem());

// Список позволяет организовывать и оформлять наборы абзацев с помощью префиксных символов и отступов.
// Мы можем создавать вложенные списки, увеличивая уровень отступа.
// Мы можем начинать и завершать список, используя свойство "ListFormat" объекта document builder.
// Каждый абзац, который мы добавляем между началом и концом списка, становится элементом списка.
// Ниже представлены два типа списков, которые мы можем создать с помощью document builder.
// 1 -  Нумерованный список:
// Нумерованные списки создают логический порядок для своих абзацев, нумеруя каждый элемент.
builder->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault));

ASSERT_TRUE(builder->get_ListFormat()->get_IsListItem());

// Установив свойство \"ListLevelNumber\", мы можем увеличить уровень списка
// чтобы начать автономный подсписок в текущем элементе списка.
// Шаблон списка Microsoft Word под названием \"NumberDefault\" использует цифры для создания уровней списка для первого уровня списка.
// Более глубокие уровни списка используют буквы и римские цифры в нижнем регистре.
for (int32_t i = 0; i < 9; i++)
{
    builder->get_ListFormat()->set_ListLevelNumber(i);
    builder->Writeln(System::String(u"Level ") + i);
}

// 2 -  Маркированный список:
// Этот список будет применять отступ и символ маркера (\"•\") перед каждым абзацем.
// Более глубокие уровни этого списка будут использовать разные символы, такие как \"■\" и \"○\".
builder->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault));

for (int32_t i = 0; i < 9; i++)
{
    builder->get_ListFormat()->set_ListLevelNumber(i);
    builder->Writeln(System::String(u"Level ") + i);
}

// Мы можем отключить форматирование списка, чтобы не форматировать последующие абзацы как списки, сняв флаг \"List\".
builder->get_ListFormat()->set_List(nullptr);

ASSERT_FALSE(builder->get_ListFormat()->get_IsListItem());

doc->Save(get_ArtifactsDir() + u"Lists.SpecifyListLevel.docx");
```

## См. также

* Class [ListFormat](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
