---
title: "Метод Aspose::Words::Loading::TxtLoadOptions::get_LeadingSpacesOptions"
linktitle: "get_LeadingSpacesOptions"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Loading::TxtLoadOptions::get_LeadingSpacesOptions. Получает или задает предпочтительный вариант обработки начальных пробелов. Значение по умолчанию — ConvertToIndent в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words.loading/txtloadoptions/get_leadingspacesoptions/
---
## TxtLoadOptions::get_LeadingSpacesOptions method


Получает или задает предпочтительный вариант обработки начальных пробелов. Значение по умолчанию — [ConvertToIndent](../../txtleadingspacesoptions/).

```cpp
Aspose::Words::Loading::TxtLeadingSpacesOptions Aspose::Words::Loading::TxtLoadOptions::get_LeadingSpacesOptions() const
```


## Примеры



Показывает, как удалять пробельные символы при загрузке текстовых документов.
```cpp
System::String textDoc = System::String(u"      Line 1 \n") + u"    Line 2   \n" + u" Line 3       ";

// Создайте объект "TxtLoadOptions", который можно передать конструктору документа
// чтобы изменить способ загрузки простого документа.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();

// Установите свойство "LeadingSpacesOptions" в значение "TxtLeadingSpacesOptions.Preserve"
// чтобы сохранить все пробельные символы в начале каждой строки.
// Установите свойство "LeadingSpacesOptions" в значение "TxtLeadingSpacesOptions.ConvertToIndent"
// чтобы удалить все пробельные символы из начала каждой строки,
// а затем примените отступ первой строки слева к абзацу, чтобы имитировать эффект пробелов.
// Установите свойство "LeadingSpacesOptions" в значение "TxtLeadingSpacesOptions.Trim"
// чтобы удалить все пробельные символы из начала каждой строки.
loadOptions->set_LeadingSpacesOptions(txtLeadingSpacesOptions);

// Установите свойство "TrailingSpacesOptions" в значение "TxtTrailingSpacesOptions.Preserve"
// чтобы сохранить все пробельные символы в конце каждой строки.
// Установите свойство "TrailingSpacesOptions" в значение "TxtTrailingSpacesOptions.Trim", чтобы
// удалить все пробельные символы из конца каждой строки.
loadOptions->set_TrailingSpacesOptions(txtTrailingSpacesOptions);

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(textDoc)), loadOptions);
System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

switch (txtLeadingSpacesOptions)
{
    case Aspose::Words::Loading::TxtLeadingSpacesOptions::ConvertToIndent:
        ASPOSE_ASSERT_EQ(37.8, paragraphs->idx_get(0)->get_ParagraphFormat()->get_FirstLineIndent());
        ASPOSE_ASSERT_EQ(25.2, paragraphs->idx_get(1)->get_ParagraphFormat()->get_FirstLineIndent());
        ASPOSE_ASSERT_EQ(6.3, paragraphs->idx_get(2)->get_ParagraphFormat()->get_FirstLineIndent());
        ASSERT_TRUE(paragraphs->idx_get(0)->GetText().StartsWith(u"Line 1"));
        ASSERT_TRUE(paragraphs->idx_get(1)->GetText().StartsWith(u"Line 2"));
        ASSERT_TRUE(paragraphs->idx_get(2)->GetText().StartsWith(u"Line 3"));
        break;

    case Aspose::Words::Loading::TxtLeadingSpacesOptions::Preserve:
        ASSERT_TRUE(paragraphs->LINQ_All(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> p)>>([](System::SharedPtr<Aspose::Words::Node> p) -> bool
        {
            return (System::ExplicitCast<Aspose::Words::Paragraph>(p))->get_ParagraphFormat()->get_FirstLineIndent() == 0.0;
        }))));
        ASSERT_TRUE(paragraphs->idx_get(0)->GetText().StartsWith(u"      Line 1"));
        ASSERT_TRUE(paragraphs->idx_get(1)->GetText().StartsWith(u"    Line 2"));
        ASSERT_TRUE(paragraphs->idx_get(2)->GetText().StartsWith(u" Line 3"));
        break;

    case Aspose::Words::Loading::TxtLeadingSpacesOptions::Trim:
        ASSERT_TRUE(paragraphs->LINQ_All(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> p)>>([](System::SharedPtr<Aspose::Words::Node> p) -> bool
        {
            return (System::ExplicitCast<Aspose::Words::Paragraph>(p))->get_ParagraphFormat()->get_FirstLineIndent() == 0.0;
        }))));
        ASSERT_TRUE(paragraphs->idx_get(0)->GetText().StartsWith(u"Line 1"));
        ASSERT_TRUE(paragraphs->idx_get(1)->GetText().StartsWith(u"Line 2"));
        ASSERT_TRUE(paragraphs->idx_get(2)->GetText().StartsWith(u"Line 3"));
        break;

}

switch (txtTrailingSpacesOptions)
{
    case Aspose::Words::Loading::TxtTrailingSpacesOptions::Preserve:
        ASSERT_TRUE(paragraphs->idx_get(0)->GetText().EndsWith(u"Line 1 \r"));
        ASSERT_TRUE(paragraphs->idx_get(1)->GetText().EndsWith(u"Line 2   \r"));
        ASSERT_TRUE(paragraphs->idx_get(2)->GetText().EndsWith(u"Line 3       \f"));
        break;

    case Aspose::Words::Loading::TxtTrailingSpacesOptions::Trim:
        ASSERT_TRUE(paragraphs->idx_get(0)->GetText().EndsWith(u"Line 1\r"));
        ASSERT_TRUE(paragraphs->idx_get(1)->GetText().EndsWith(u"Line 2\r"));
        ASSERT_TRUE(paragraphs->idx_get(2)->GetText().EndsWith(u"Line 3\f"));
        break;

}
```

## См. также

* Enum [TxtLeadingSpacesOptions](../../txtleadingspacesoptions/)
* Class [TxtLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
