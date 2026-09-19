---
title: "Metodo Aspose::Words::Loading::TxtLoadOptions::get_DetectNumberingWithWhitespaces"
linktitle: "get_DetectNumberingWithWhitespaces"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Loading::TxtLoadOptions::get_DetectNumberingWithWhitespaces. Consente di specificare come gli elementi di elenco numerati vengono riconosciuti quando il documento è importato da un formato di testo semplice. Il valore predefinito è true in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.loading/txtloadoptions/get_detectnumberingwithwhitespaces/
---
## TxtLoadOptions::get_DetectNumberingWithWhitespaces method


Consente di specificare come vengono riconosciuti gli elementi di elenchi numerati quando il documento è importato da formato di testo semplice. Il valore predefinito è **true**.

```cpp
bool Aspose::Words::Loading::TxtLoadOptions::get_DetectNumberingWithWhitespaces() const
```

## Note


Se questa opzione è impostata su **false**, l'algoritmo di riconoscimento degli elenchi rileva i paragrafi di elenco, quando i numeri degli elenchi terminano con un punto, una parentesi chiusa o simboli di elenco puntato (come "•", "*", "-" o "o").

Se questa opzione è impostata su **true**, gli spazi bianchi sono utilizzati anche come delimitatori dei numeri di elenco: l'algoritmo di riconoscimento degli elenchi per la numerazione in stile arabo (1., 1.1.2.) utilizza sia gli spazi bianchi sia il punto (".") come simboli.

## Esempi



Mostra come rilevare gli elenchi durante il caricamento di documenti di testo semplice.
```cpp
// Crea un documento di testo semplice in una stringa con quattro parti separate che possiamo interpretare come elenchi,
// con delimitatori diversi. Dopo aver caricato il documento di testo semplice in un oggetto "Document",
// Aspose.Words rileverà sempre i primi tre elenchi e aggiungerà un oggetto "List"
// per ciascuno alla proprietà "Lists" del documento.
const System::String textDoc = System::String(u"Full stop delimiters:\n") + u"1. First list item 1\n" + u"2. First list item 2\n" + u"3. First list item 3\n\n" + u"Right bracket delimiters:\n" + u"1) Second list item 1\n" + u"2) Second list item 2\n" + u"3) Second list item 3\n\n" + u"Bullet delimiters:\n" + u"• Third list item 1\n" + u"• Third list item 2\n" + u"• Third list item 3\n\n" + u"Whitespace delimiters:\n" + u"1 Fourth list item 1\n" + u"2 Fourth list item 2\n" + u"3 Fourth list item 3";

// Crea un oggetto "TxtLoadOptions", che possiamo passare al costruttore di un documento
// per modificare il modo in cui carichiamo un documento di testo semplice.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();

// Imposta la proprietà "DetectNumberingWithWhitespaces" su "true" per rilevare gli elementi numerati
// con delimitatori di spazi bianchi, come il quarto elenco nel nostro documento, come elenchi.
// Questo potrebbe anche rilevare falsamente i paragrafi che iniziano con numeri come elenchi.
// Imposta la proprietà "DetectNumberingWithWhitespaces" su "false"
// per non creare elenchi da elementi numerati con delimitatori di spazi bianchi.
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

## Vedi anche

* Class [TxtLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
