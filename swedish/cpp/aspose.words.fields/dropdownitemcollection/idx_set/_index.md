---
title: "Aspose::Words::Fields::DropDownItemCollection::idx_set metod"
linktitle: "idx_set"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::DropDownItemCollection::idx_set metod. Hämtar eller anger elementet på det angivna indexet i C++."
type: docs
weight: 13000
url: /sv/cpp/aspose.words.fields/dropdownitemcollection/idx_set/
---
## DropDownItemCollection::idx_set method


Hämtar eller anger elementet på det angivna indexet.

```cpp
void Aspose::Words::Fields::DropDownItemCollection::idx_set(int32_t index, const System::String &value)
```


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

* Class [DropDownItemCollection](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
