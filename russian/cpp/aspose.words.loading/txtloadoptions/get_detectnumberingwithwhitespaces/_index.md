---
title: "метод Aspose::Words::Loading::TxtLoadOptions::get_DetectNumberingWithWhitespaces"
linktitle: "get_DetectNumberingWithWhitespaces"
second_title: "Справочник API Aspose.Words для C++"
description: "метод Aspose::Words::Loading::TxtLoadOptions::get_DetectNumberingWithWhitespaces. Позволяет указать, как распознаются элементы нумерованных списков при импорте документа из формата простого текста. Значение по умолчанию — true в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.loading/txtloadoptions/get_detectnumberingwithwhitespaces/
---
## TxtLoadOptions::get_DetectNumberingWithWhitespaces method


Позволяет указать, как распознавать элементы нумерованных списков при импорте документа из формата простого текста. Значение по умолчанию — **true**.

```cpp
bool Aspose::Words::Loading::TxtLoadOptions::get_DetectNumberingWithWhitespaces() const
```

## Примечания


Если эта опция установлена в **false**, алгоритм распознавания списков определяет абзацы списков, когда номера списков заканчиваются точкой, правой скобкой или символами маркеров (например, "•", "*", "-" или "o").

Если эта опция установлена в **true**, пробелы также используются в качестве разделителей номеров списков: алгоритм распознавания списков для арабской нумерации (1., 1.1.2.) использует как пробелы, так и точку (".") в качестве символов.

## Примеры



Показывает, как обнаруживать списки при загрузке документов простого текста.
```cpp
// Создайте документ простого текста в строке с четырьмя отдельными частями, которые мы можем интерпретировать как списки,
// с разными разделителями. При загрузке документа простого текста в объект "Document",
// Aspose.Words всегда будет обнаруживать первые три списка и добавит объект "List"
// для каждого в свойство "Lists" документа.
const System::String textDoc = System::String(u"Full stop delimiters:\n") + u"1. First list item 1\n" + u"2. First list item 2\n" + u"3. First list item 3\n\n" + u"Right bracket delimiters:\n" + u"1) Second list item 1\n" + u"2) Second list item 2\n" + u"3) Second list item 3\n\n" + u"Bullet delimiters:\n" + u"• Third list item 1\n" + u"• Third list item 2\n" + u"• Third list item 3\n\n" + u"Whitespace delimiters:\n" + u"1 Fourth list item 1\n" + u"2 Fourth list item 2\n" + u"3 Fourth list item 3";

// Создайте объект "TxtLoadOptions", который можно передать конструктору документа
// чтобы изменить способ загрузки простого документа.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();

// Установите свойство "DetectNumberingWithWhitespaces" в значение "true", чтобы обнаруживать нумерованные элементы
// с разделителями пробелами, например, четвертый список в нашем документе, как списки.
// Это также может ошибочно распознавать абзацы, начинающиеся с цифр, как списки.
// Установите свойство "DetectNumberingWithWhitespaces" в значение "false"
// чтобы не создавать списки из нумерованных элементов с разделителями пробелами.
loadOptions->set_DetectNumberingWithWhitespaces(detectNumberingWithWhitespaces);

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(textDoc)), loadOptions);

if (detectNumberingWithWhitespaces)
{
    ASSERT_EQ(4, doc->get_Lists()->get_Count());
    ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> p)>>([](System::SharedPtr<Aspose::Words::Node> p) -> bool
    {
        return p->GetText().Contains(u"Fourth list") && (System::ExplicitCast<Aspose::Words::Paragraph>(p))->get_IsListItem();
    }))));
}
else
{
    ASSERT_EQ(3, doc->get_Lists()->get_Count());
    ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> p)>>([](System::SharedPtr<Aspose::Words::Node> p) -> bool
    {
        return p->GetText().Contains(u"Fourth list") && (System::ExplicitCast<Aspose::Words::Paragraph>(p))->get_IsListItem();
    }))));
}
```

## См. также

* Class [TxtLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
