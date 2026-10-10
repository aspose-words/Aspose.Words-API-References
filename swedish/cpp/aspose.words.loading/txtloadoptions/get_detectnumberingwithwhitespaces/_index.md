---
title: "Aspose::Words::Loading::TxtLoadOptions::get_DetectNumberingWithWhitespaces‑metod"
linktitle: "get_DetectNumberingWithWhitespaces"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Loading::TxtLoadOptions::get_DetectNumberingWithWhitespaces‑metod. Gör det möjligt att ange hur numrerade listobjekt identifieras när dokumentet importeras från vanligt textformat. Standardvärdet är true i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.loading/txtloadoptions/get_detectnumberingwithwhitespaces/
---
## TxtLoadOptions::get_DetectNumberingWithWhitespaces method


Gör det möjligt att ange hur numrerade listobjekt identifieras när ett dokument importeras från vanligt textformat. Standardvärdet är **true**.

```cpp
bool Aspose::Words::Loading::TxtLoadOptions::get_DetectNumberingWithWhitespaces() const
```

## Anmärkningar


Om detta alternativ är satt till **false**, identifierar listigenkänningsalgoritmen listparagrafer när listnummer avslutas med antingen punkt, höger parentes eller punktlistsymboler (såsom "•", "*", "-" eller "o").

Om detta alternativ är satt till **true**, används också mellanslag som avgränsare för listnummer: listigenkänningsalgoritmen för arabiskt numreringsstil (1., 1.1.2.) använder både mellanslag och punkt (".")‑symboler.

## Exempel



Visar hur man identifierar listor när man laddar in rena textdokument.
```cpp
// Skapa ett rent textdokument i en sträng med fyra separata delar som vi kan tolka som listor,
// med olika avgränsare. Vid inläsning av det rena textdokumentet i ett "Document"‑objekt,
// Aspose.Words kommer alltid att identifiera de första tre listorna och kommer att lägga till ett "List"‑objekt
// för varje till dokumentets egenskap "Lists".
const System::String textDoc = System::String(u"Full stop delimiters:\n") + u"1. First list item 1\n" + u"2. First list item 2\n" + u"3. First list item 3\n\n" + u"Right bracket delimiters:\n" + u"1) Second list item 1\n" + u"2) Second list item 2\n" + u"3) Second list item 3\n\n" + u"Bullet delimiters:\n" + u"• Third list item 1\n" + u"• Third list item 2\n" + u"• Third list item 3\n\n" + u"Whitespace delimiters:\n" + u"1 Fourth list item 1\n" + u"2 Fourth list item 2\n" + u"3 Fourth list item 3";

// Skapa ett "TxtLoadOptions"-objekt, som vi kan skicka till ett dokuments konstruktor
// för att ändra hur vi laddar ett klartextdokument.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();

// Ställ in egenskapen "DetectNumberingWithWhitespaces" till "true" för att identifiera numrerade objekt
// med mellanslagsavgränsare, såsom den fjärde listan i vårt dokument, som listor.
// Detta kan också felaktigt identifiera stycken som börjar med siffror som listor.
// Ställ in egenskapen "DetectNumberingWithWhitespaces" till "false"
// för att inte skapa listor från numrerade objekt med mellanslagsavgränsare.
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

## Se även

* Class [TxtLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
