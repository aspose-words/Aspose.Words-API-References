---
title: "Метод Aspose::Words::DocumentBuilder::get_ListFormat"
linktitle: "get_ListFormat"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::DocumentBuilder::get_ListFormat. Возвращает объект, представляющий текущие свойства форматирования списка в C++."
type: docs
weight: 22000
url: /ru/cpp/aspose.words/documentbuilder/get_listformat/
---
## DocumentBuilder::get_ListFormat method


Возвращает объект, представляющий текущие свойства форматирования списка.

```cpp
System::SharedPtr<Aspose::Words::Lists::ListFormat> Aspose::Words::DocumentBuilder::get_ListFormat()
```


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

## См. также

* Class [ListFormat](../../../aspose.words.lists/listformat/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
