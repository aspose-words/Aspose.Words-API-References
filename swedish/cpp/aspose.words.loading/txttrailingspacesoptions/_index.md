---
title: "Aspose::Words::Loading::TxtTrailingSpacesOptions-enum"
linktitle: "TxtTrailingSpacesOptions"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Loading::TxtTrailingSpacesOptions-enum. Anger tillgängliga alternativ för hantering av avslutande mellanslag vid import från en Text‑fil i C++."
type: docs
weight: 19000
url: /sv/cpp/aspose.words.loading/txttrailingspacesoptions/
---
## TxtTrailingSpacesOptions enum


Anger tillgängliga alternativ för hantering av efterföljande mellanslag vid import från [Text](../../aspose.words/loadformat/) fil.

```cpp
enum class TxtTrailingSpacesOptions
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Trimma | 0 | Efterföljande mellanslag trimmas. |
| Bevara | 1 | Efterföljande mellanslag bevaras. |


## Exempel



Visar hur man trimmar blanksteg när man laddar in textdokument.
```cpp
System::String textDoc = System::String(u"      Line 1 \n") + u"    Line 2   \n" + u" Line 3       ";

// Skapa ett "TxtLoadOptions"-objekt, som vi kan skicka till ett dokuments konstruktor
// för att ändra hur vi laddar ett klartextdokument.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();

// Ställ in egenskapen "LeadingSpacesOptions" till "TxtLeadingSpacesOptions.Preserve"
// för att bevara alla blankstegstecken i början av varje rad.
// Ställ in egenskapen "LeadingSpacesOptions" till "TxtLeadingSpacesOptions.ConvertToIndent"
// för att ta bort alla blankstegstecken i början av varje rad,
// och applicera sedan en vänster första rad-indragning på stycket för att simulera effekten av blankstegen.
// Ställ in egenskapen "LeadingSpacesOptions" till "TxtLeadingSpacesOptions.Trim"
// för att ta bort alla blankstegstecken i början av varje rad.
loadOptions->set_LeadingSpacesOptions(txtLeadingSpacesOptions);

// Ställ in egenskapen "TrailingSpacesOptions" till "TxtTrailingSpacesOptions.Preserve"
// för att bevara alla blankstegstecken i slutet av varje rad.
// Ställ in egenskapen "TrailingSpacesOptions" till "TxtTrailingSpacesOptions.Trim" för att
// ta bort alla blankstegstecken i slutet av varje rad.
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

## Se även

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
