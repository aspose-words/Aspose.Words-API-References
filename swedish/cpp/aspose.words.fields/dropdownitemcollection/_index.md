---
title: "Aspose::Words::Fields::DropDownItemCollection class"
linktitle: "DropDownItemCollection"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::DropDownItemCollection class. En samling av strängar som representerar alla objekt i ett rullgardinsformulärfält. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.fields/dropdownitemcollection/
---
## DropDownItemCollection class


En samling strängar som representerar alla objekt i ett rullgardinsformulärfält. För att lära dig mer, besök [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) dokumentationsartikel.

```cpp
class DropDownItemCollection : public System::Collections::Generic::IEnumerable<System::String>,
                               public Aspose::Words::IComplexAttr
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Add](./add/)(const System::String\&) | Lägger till en sträng i slutet av samlingen. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Tar bort alla element från samlingen. |
| [Contains](./contains/)(const System::String\&) | Avgör om samlingen innehåller det angivna värdet. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Hämtar antalet element som finns i samlingen. |
| [GetEnumerator](./getenumerator/)() override | Returnerar ett enumerator-objekt som kan användas för att iterera över alla objekt i samlingen. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Hämtar eller anger elementet på det angivna indexet. |
| [idx_set](./idx_set/)(int32_t, const System::String\&) | Hämtar eller anger elementet på det angivna indexet. |
| [IndexOf](./indexof/)(const System::String\&) | Returnerar det nollbaserade indexet för det angivna värdet i samlingen. |
| [Insert](./insert/)(int32_t, const System::String\&) | Infogar en sträng i samlingen på det angivna indexet. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | Tar bort det angivna värdet från samlingen. |
| [RemoveAt](./removeat/)(int32_t) | Tar bort ett värde på det angivna indexet. |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| Typedef | Beskrivning |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |

## Exempel



Visar hur man infogar ett kombinationsruta-fält och redigerar elementen i dess objektssamling.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga en kombinationsruta och verifiera sedan dess samling av rullgardinsobjekt.
// I Microsoft Word kommer användaren att klicka på kombinationsrutan,
// och sedan välja ett av texterna i samlingen för att visas.
System::ArrayPtr<System::String> items = System::MakeArray<System::String>({u"One", u"Two", u"Three"});
System::SharedPtr<Aspose::Words::Fields::FormField> comboBoxField = builder->InsertComboBox(u"DropDown", items, 0);
System::SharedPtr<Aspose::Words::Fields::DropDownItemCollection> dropDownItems = comboBoxField->get_DropDownItems();

ASSERT_EQ(3, dropDownItems->get_Count());
ASSERT_EQ(u"One", dropDownItems->idx_get(0));
ASSERT_EQ(1, dropDownItems->IndexOf(u"Two"));
ASSERT_TRUE(dropDownItems->Contains(u"Three"));

// Det finns två sätt att lägga till ett nytt objekt i en befintlig samling av rullgardinsobjekt.
// 1 -  Lägg till ett objekt i slutet av samlingen:
dropDownItems->Add(u"Four");

// 2 -  Infoga ett objekt före ett annat objekt på ett angivet index:
dropDownItems->Insert(3, u"Three and a half");

ASSERT_EQ(5, dropDownItems->get_Count());

// Iterera över samlingen och skriv ut varje element.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::String>> dropDownCollectionEnumerator = dropDownItems->GetEnumerator();
    while (dropDownCollectionEnumerator->MoveNext())
    {
        std::cout << dropDownCollectionEnumerator->get_Current() << std::endl;
    }
}

// Det finns två sätt att ta bort element från en samling av rullgardinsobjekt.
// 1 -  Ta bort ett objekt med innehåll som är lika med den överförda strängen:
dropDownItems->Remove(u"Four");

// 2 -  Ta bort ett objekt på ett index:
dropDownItems->RemoveAt(3);

ASSERT_EQ(3, dropDownItems->get_Count());
ASSERT_FALSE(dropDownItems->Contains(u"Three and a half"));
ASSERT_FALSE(dropDownItems->Contains(u"Four"));

doc->Save(get_ArtifactsDir() + u"FormFields.DropDownItemCollection.html");

// Töm hela samlingen av rullgardinsalternativ.
dropDownItems->Clear();
```

## Se även

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
