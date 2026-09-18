---
title: "Aspose::Words::Loading::TxtLoadOptions::get_DetectNumberingWithWhitespaces Methode"
linktitle: "get_DetectNumberingWithWhitespaces"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Loading::TxtLoadOptions::get_DetectNumberingWithWhitespaces Methode. Ermöglicht die Angabe, wie nummerierte Listenelemente erkannt werden, wenn das Dokument aus einem Nur-Text-Format importiert wird. Der Standardwert ist true in C++."
type: docs
weight: 4000
url: /de/cpp/aspose.words.loading/txtloadoptions/get_detectnumberingwithwhitespaces/
---
## TxtLoadOptions::get_DetectNumberingWithWhitespaces method


Ermöglicht die Angabe, wie nummerierte Listenelemente erkannt werden, wenn das Dokument aus einem Nur-Text-Format importiert wird. Der Standardwert ist **true**.

```cpp
bool Aspose::Words::Loading::TxtLoadOptions::get_DetectNumberingWithWhitespaces() const
```

## Hinweise


Wenn diese Option auf **false** gesetzt ist, erkennt der Listen-Erkennungsalgorithmus List-Absätze, wenn Listennummern entweder mit einem Punkt, einer rechten Klammer oder Aufzählungszeichen (wie "•", "*", "-" oder "o") enden.

Wenn diese Option auf **true** gesetzt ist, werden Leerzeichen ebenfalls als Trennzeichen für Listennummern verwendet: Der Listen-Erkennungsalgorithmus für arabische Nummerierung (1., 1.1.2.) nutzt sowohl Leerzeichen als auch Punkt (".")-Symbole.

## Beispiele



Zeigt, wie Listen beim Laden von Nur-Text-Dokumenten erkannt werden.
```cpp
// Erstellen Sie ein Nur-Text-Dokument in einem String mit vier separaten Teilen, die wir als Listen interpretieren können,
// mit unterschiedlichen Trennzeichen. Beim Laden des Nur-Text-Dokuments in ein "Document"-Objekt,
// Aspose.Words wird immer die ersten drei Listen erkennen und ein "List"-Objekt hinzufügen
// für jede zur "Lists"-Eigenschaft des Dokuments.
const System::String textDoc = System::String(u"Full stop delimiters:\n") + u"1. First list item 1\n" + u"2. First list item 2\n" + u"3. First list item 3\n\n" + u"Right bracket delimiters:\n" + u"1) Second list item 1\n" + u"2) Second list item 2\n" + u"3) Second list item 3\n\n" + u"Bullet delimiters:\n" + u"• Third list item 1\n" + u"• Third list item 2\n" + u"• Third list item 3\n\n" + u"Whitespace delimiters:\n" + u"1 Fourth list item 1\n" + u"2 Fourth list item 2\n" + u"3 Fourth list item 3";

// Erstelle ein \"TxtLoadOptions\"‑Objekt, das wir an den Konstruktor eines Dokuments übergeben können
// um zu ändern, wie wir ein Klartextdokument laden.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();

// Setzen Sie die Eigenschaft "DetectNumberingWithWhitespaces" auf "true", um nummerierte Elemente zu erkennen
// mit Leerzeichen-Trennzeichen, wie zum Beispiel die vierte Liste in unserem Dokument, als Listen.
// Dies kann auch fälschlicherweise Absätze, die mit Zahlen beginnen, als Listen erkennen.
// Setzen Sie die Eigenschaft "DetectNumberingWithWhitespaces" auf "false"
// um keine Listen aus nummerierten Elementen mit Leerzeichen‑Trennzeichen zu erstellen.
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

## Siehe auch

* Class [TxtLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
