---
title: "Aspose::Words::Lists::ListFormat::RemoveNumbers метод"
linktitle: "RemoveNumbers"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Lists::ListFormat::RemoveNumbers method. Удаляет номера или маркеры из текущего абзаца и устанавливает уровень списка в ноль в C++."
type: docs
weight: 12000
url: /ru/cpp/aspose.words.lists/listformat/removenumbers/
---
## ListFormat::RemoveNumbers method


Удаляет номера или маркеры из текущего абзаца и устанавливает уровень списка в ноль.

```cpp
void Aspose::Words::Lists::ListFormat::RemoveNumbers()
```

## Примечания


Вызов этого метода эквивалентен установке свойства [List](../get_list/) в **null**.

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


Показывает, как удалить форматирование списка из всех абзацев в основном тексте раздела.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ListFormat()->ApplyNumberDefault();
builder->Writeln(u"Numbered list item 1");
builder->Writeln(u"Numbered list item 2");
builder->Writeln(u"Numbered list item 3");
builder->get_ListFormat()->RemoveNumbers();

System::SharedPtr<Aspose::Words::NodeCollection> paras = doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true);
ASSERT_EQ(3, paras->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> n)>>([](System::SharedPtr<Aspose::Words::Node> n) -> bool
{
    return (System::ExplicitCast<Aspose::Words::Paragraph>(n))->get_ListFormat()->get_IsListItem();
}))));

for (auto&& paragraph : System::IterateOver<Aspose::Words::Paragraph>(paras))
{
    paragraph->get_ListFormat()->RemoveNumbers();
}

ASSERT_EQ(0, paras->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> n)>>([](System::SharedPtr<Aspose::Words::Node> n) -> bool
{
    return (System::ExplicitCast<Aspose::Words::Paragraph>(n))->get_ListFormat()->get_IsListItem();
}))));
```

## См. также

* Class [ListFormat](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
