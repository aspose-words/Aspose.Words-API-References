---
title: "Enum Aspose::Words::Loading::TxtTrailingSpacesOptions"
linktitle: "TxtTrailingSpacesOptions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Enum Aspose::Words::Loading::TxtTrailingSpacesOptions. Specifica le opzioni disponibili per la gestione degli spazi finali durante l'importazione da un file Text in C++."
type: docs
weight: 19000
url: /it/cpp/aspose.words.loading/txttrailingspacesoptions/
---
## TxtTrailingSpacesOptions enum


Specifica le opzioni disponibili per la gestione degli spazi finali durante l'importazione da un file [Text](../../aspose.words/loadformat/).

```cpp
enum class TxtTrailingSpacesOptions
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Trim | 0 | Gli spazi finali vengono rimossi. |
| Preserve | 1 | Gli spazi finali vengono conservati. |


## Esempi



Mostra come rimuovere gli spazi bianchi durante il caricamento di documenti di testo semplice.
```cpp
System::String textDoc = System::String(u"      Line 1 \n") + u"    Line 2   \n" + u" Line 3       ";

// Crea un oggetto "TxtLoadOptions", che possiamo passare al costruttore di un documento
// per modificare il modo in cui carichiamo un documento di testo semplice.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();

// Imposta la proprietà "LeadingSpacesOptions" su "TxtLeadingSpacesOptions.Preserve"
// per preservare tutti i caratteri di spaziatura all'inizio di ogni riga.
// Imposta la proprietà "LeadingSpacesOptions" su "TxtLeadingSpacesOptions.ConvertToIndent"
// per rimuovere tutti i caratteri di spaziatura dall'inizio di ogni riga,
// e quindi applica un rientro sinistro alla prima riga del paragrafo per simulare l'effetto degli spazi.
// Imposta la proprietà "LeadingSpacesOptions" su "TxtLeadingSpacesOptions.Trim"
// per rimuovere tutti i caratteri di spaziatura dall'inizio di ogni riga.
loadOptions->set_LeadingSpacesOptions(txtLeadingSpacesOptions);

// Imposta la proprietà "TrailingSpacesOptions" su "TxtTrailingSpacesOptions.Preserve"
// per preservare tutti i caratteri di spaziatura alla fine di ogni riga.
// Imposta la proprietà "TrailingSpacesOptions" su "TxtTrailingSpacesOptions.Trim" per
// rimuovere tutti i caratteri di spaziatura dalla fine di ogni riga.
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

## Vedi anche

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
