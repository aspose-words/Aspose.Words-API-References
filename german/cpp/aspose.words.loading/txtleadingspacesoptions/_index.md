---
title: "Aspose::Words::Loading::TxtLeadingSpacesOptions enum"
linktitle: "TxtLeadingSpacesOptions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Loading::TxtLeadingSpacesOptions‑Enum. Gibt die verfügbaren Optionen für den Umgang mit führenden Leerzeichen beim Import aus einer Textdatei in C++ an."
type: docs
weight: 18000
url: /de/cpp/aspose.words.loading/txtleadingspacesoptions/
---
## TxtLeadingSpacesOptions enum


Gibt die verfügbaren Optionen für den Umgang mit führenden Leerzeichen beim Import aus einer [Text](../../aspose.words/loadformat/)-Datei an.

```cpp
enum class TxtLeadingSpacesOptions
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| ConvertToIndent | 0 | Führende Leerzeichen werden entfernt und in linken Einzug umgewandelt. |
| Trimmen | 1 | Führende Leerzeichen werden gekürzt. |
| Beibehalten | 2 | Führende Leerzeichen werden beibehalten. |


## Beispiele



Zeigt, wie Leerzeichen beim Laden von Klartextdokumenten getrimmt werden.
```cpp
System::String textDoc = System::String(u"      Line 1 \n") + u"    Line 2   \n" + u" Line 3       ";

// Erstelle ein \"TxtLoadOptions\"‑Objekt, das wir an den Konstruktor eines Dokuments übergeben können
// um zu ändern, wie wir ein Klartextdokument laden.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();

// Setzen Sie die Eigenschaft "LeadingSpacesOptions" auf "TxtLeadingSpacesOptions.Preserve"
// um alle Whitespace-Zeichen am Anfang jeder Zeile beizubehalten.
// Setzen Sie die Eigenschaft "LeadingSpacesOptions" auf "TxtLeadingSpacesOptions.ConvertToIndent"
// um alle Whitespace-Zeichen am Anfang jeder Zeile zu entfernen,
// und dann einen linken Erstzeileneinzug auf den Absatz anwenden, um den Effekt der Leerzeichen zu simulieren.
// Setze die "LeadingSpacesOptions"-Eigenschaft auf "TxtLeadingSpacesOptions.Trim"
// um alle Leerzeichen am Anfang jeder Zeile zu entfernen.
loadOptions->set_LeadingSpacesOptions(txtLeadingSpacesOptions);

// Setze die "TrailingSpacesOptions"-Eigenschaft auf "TxtTrailingSpacesOptions.Preserve"
// um alle Leerzeichen am Ende jeder Zeile zu erhalten.
// Setze die "TrailingSpacesOptions"-Eigenschaft auf "TxtTrailingSpacesOptions.Trim" um
// entferne alle Leerzeichen am Ende jeder Zeile.
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

## Siehe auch

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
