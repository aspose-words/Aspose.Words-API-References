---
title: "Aspose::Words::Markup::SdtListItem klass"
linktitle: "SdtListItem"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Markup::SdtListItem-klass. Detta element specificerar ett enskilt listobjekt inom en föräldra-ComboBox eller DropDownList strukturerad dokumenttagg. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 8000
url: /sv/cpp/aspose.words.markup/sdtlistitem/
---
## SdtListItem class


Detta element specificerar ett enskilt listobjekt inom en föräldra-[ComboBox](../sdttype/) eller [DropDownList](../sdttype/) strukturerad dokumenttagg. För att lära dig mer, besök dokumentationsartikeln [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class SdtListItem : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_DisplayText](./get_displaytext/)() const | Hämtar texten som ska visas i körinnehållet i stället för innehållet i attributet [Value](./get_value/) för detta listobjekt. |
| [get_Value](./get_value/)() const | Hämtar värdet för detta listobjekt. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [SdtListItem](./sdtlistitem/)(const System::String\&, const System::String\&) | Initierar en ny instans av den här klassen. |
| [SdtListItem](./sdtlistitem/)(const System::String\&) | Initierar en ny instans av den här klassen. |
| static [Type](./type/)() |  |

## Exempel



Visar hur man arbetar med strukturerade dokumenttaggar för rullgardinslistor.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::DropDownList, Aspose::Words::Markup::MarkupLevel::Block);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(tag);

// En strukturerad dokumenttagg för rullgardinslista är ett formulär som tillåter användaren att
// välja ett alternativ från en lista genom att vänsterklicka och öppna formuläret i Microsoft Word.
// Egenskapen "ListItems" innehåller alla listobjekt, och varje listobjekt är ett "SdtListItem".
System::SharedPtr<Aspose::Words::Markup::SdtListItemCollection> listItems = tag->get_ListItems();
listItems->Add(System::MakeObject<Aspose::Words::Markup::SdtListItem>(u"Value 1"));

ASSERT_EQ(listItems->idx_get(0)->get_DisplayText(), listItems->idx_get(0)->get_Value());

// Lägg till 3 ytterligare listobjekt. Initiera dessa objekt med en annan konstruktor än det första objektet
// för att visa strängar som skiljer sig från deras värden.
listItems->Add(System::MakeObject<Aspose::Words::Markup::SdtListItem>(u"Item 2", u"Value 2"));
listItems->Add(System::MakeObject<Aspose::Words::Markup::SdtListItem>(u"Item 3", u"Value 3"));
listItems->Add(System::MakeObject<Aspose::Words::Markup::SdtListItem>(u"Item 4", u"Value 4"));

ASSERT_EQ(4, listItems->get_Count());

// Rullgardinslistan visar det första objektet. Tilldela ett annat listobjekt till "SelectedValue" för att visa det.
listItems->set_SelectedValue(listItems->idx_get(3));

ASSERT_EQ(u"Value 4", listItems->get_SelectedValue()->get_Value());

// Iterera över samlingen och skriv ut varje element.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Markup::SdtListItem>>> enumerator = listItems->GetEnumerator();
    while (enumerator->MoveNext())
    {
        if (enumerator->get_Current() != nullptr)
        {
            std::cout << System::String::Format(u"List item: {0}, value: {1}", enumerator->get_Current()->get_DisplayText(), enumerator->get_Current()->get_Value()) << std::endl;
        }
    }
}

// Ta bort det sista listobjektet.
listItems->RemoveAt(3);

ASSERT_EQ(3, listItems->get_Count());

// Eftersom vår rullgardinskontroll är inställd på att visa det borttagna objektet som standard, ge den ett objekt att visa som faktiskt finns.
listItems->set_SelectedValue(listItems->idx_get(1));

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.ListItemCollection.docx");

// Använd metoden "Clear" för att tömma hela rullgardinsobjektssamlingen på en gång.
listItems->Clear();

ASSERT_EQ(0, listItems->get_Count());
```

## Se även

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
