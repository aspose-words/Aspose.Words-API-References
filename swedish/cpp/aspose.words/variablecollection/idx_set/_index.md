---
title: "Aspose::Words::VariableCollection::idx_set-metod"
linktitle: "idx_set"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::VariableCollection::idx_set-metod. Hämtar eller anger en dokumentvariabel med det skiftlägesokänsliga namnet. null‑värden är inte tillåtna som högra sidan av tilldelningen och kommer att ersättas med en tom sträng i C++."
type: docs
weight: 13000
url: /sv/cpp/aspose.words/variablecollection/idx_set/
---
## VariableCollection::idx_set(const System::String\&, const System::String\&) method


Hämtar eller sätter en dokumentvariabel efter det skiftlägesokänsliga namnet. **null**-värden är inte tillåtna på högra sidan av tilldelningen och kommer att ersättas med en tom sträng.

```cpp
void Aspose::Words::VariableCollection::idx_set(const System::String &name, const System::String &value)
```


## Exempel



Visar hur man arbetar med ett dokuments variabelsamling.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::VariableCollection> variables = doc->get_Variables();

// Varje dokument har en samling av nyckel/värde-par variabler, som vi kan lägga till objekt i.
variables->Add(u"Home address", u"123 Main St.");
variables->Add(u"City", u"London");
variables->Add(u"Bedrooms", u"3");

ASSERT_EQ(3, variables->get_Count());

// Vi kan visa värdena på variabler i dokumentkroppen med hjälp av DOCVARIABLE-fält.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDocVariable>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDocVariable, true));
field->set_VariableName(u"Home address");
field->Update();

ASSERT_EQ(u"123 Main St.", field->get_Result());

// Att tilldela värden till befintliga nycklar kommer att uppdatera dem.
variables->Add(u"Home address", u"456 Queen St.");

// Vi måste sedan uppdatera DOCVARIABLE-fält för att säkerställa att de visar ett aktuellt värde.
ASSERT_EQ(u"123 Main St.", field->get_Result());

field->Update();

ASSERT_EQ(u"456 Queen St.", field->get_Result());

// Verifiera att dokumentvariablerna med ett visst namn eller värde finns.
ASSERT_TRUE(variables->Contains(u"City"));
ASSERT_TRUE(variables->LINQ_Any(static_cast<System::Func<System::Collections::Generic::KeyValuePair<System::String, System::String>, bool>>(static_cast<std::function<bool(System::Collections::Generic::KeyValuePair<System::String, System::String> v)>>([](System::Collections::Generic::KeyValuePair<System::String, System::String> v) -> bool
{
    return v.get_Value() == u"London";
}))));

// Variabelsamlingen sorterar automatiskt variabler alfabetiskt efter namn.
ASSERT_EQ(0, variables->IndexOfKey(u"Bedrooms"));
ASSERT_EQ(1, variables->IndexOfKey(u"City"));
ASSERT_EQ(2, variables->IndexOfKey(u"Home address"));

ASSERT_EQ(u"3", variables->idx_get(0));
ASSERT_EQ(u"London", variables->idx_get(u"City"));

// Iterera över variabelsamlingen.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::Collections::Generic::KeyValuePair<System::String, System::String>>> enumerator = doc->get_Variables()->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Name: {0}, Value: {1}", enumerator->get_Current().get_Key(), enumerator->get_Current().get_Value()) << std::endl;
    }
}

// Nedan följer tre sätt att ta bort dokumentvariabler från en samling.
// 1 -  Efter namn:
variables->Remove(u"City");

ASSERT_FALSE(variables->Contains(u"City"));

// 2 -  Efter index:
variables->RemoveAt(1);

ASSERT_FALSE(variables->Contains(u"Home address"));

// 3 -  Rensa hela samlingen på en gång:
variables->Clear();

ASSERT_EQ(0, variables->get_Count());
```

## Se även

* Class [VariableCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## VariableCollection::idx_set(int32_t, const System::String\&) method


Hämtar eller sätter en dokumentvariabel på det angivna indexet. **null**-värden är inte tillåtna på högra sidan av tilldelningen och kommer att ersättas med en tom sträng.

```cpp
void Aspose::Words::VariableCollection::idx_set(int32_t index, const System::String &value)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| index | int32_t | Nollbaserat index för dokumentvariabeln. |

## Exempel



Visar hur man arbetar med ett dokuments variabelsamling.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::VariableCollection> variables = doc->get_Variables();

// Varje dokument har en samling av nyckel/värde-par variabler, som vi kan lägga till objekt i.
variables->Add(u"Home address", u"123 Main St.");
variables->Add(u"City", u"London");
variables->Add(u"Bedrooms", u"3");

ASSERT_EQ(3, variables->get_Count());

// Vi kan visa värdena på variabler i dokumentkroppen med hjälp av DOCVARIABLE-fält.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDocVariable>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDocVariable, true));
field->set_VariableName(u"Home address");
field->Update();

ASSERT_EQ(u"123 Main St.", field->get_Result());

// Att tilldela värden till befintliga nycklar kommer att uppdatera dem.
variables->Add(u"Home address", u"456 Queen St.");

// Vi måste sedan uppdatera DOCVARIABLE-fält för att säkerställa att de visar ett aktuellt värde.
ASSERT_EQ(u"123 Main St.", field->get_Result());

field->Update();

ASSERT_EQ(u"456 Queen St.", field->get_Result());

// Verifiera att dokumentvariablerna med ett visst namn eller värde finns.
ASSERT_TRUE(variables->Contains(u"City"));
ASSERT_TRUE(variables->LINQ_Any(static_cast<System::Func<System::Collections::Generic::KeyValuePair<System::String, System::String>, bool>>(static_cast<std::function<bool(System::Collections::Generic::KeyValuePair<System::String, System::String> v)>>([](System::Collections::Generic::KeyValuePair<System::String, System::String> v) -> bool
{
    return v.get_Value() == u"London";
}))));

// Variabelsamlingen sorterar automatiskt variabler alfabetiskt efter namn.
ASSERT_EQ(0, variables->IndexOfKey(u"Bedrooms"));
ASSERT_EQ(1, variables->IndexOfKey(u"City"));
ASSERT_EQ(2, variables->IndexOfKey(u"Home address"));

ASSERT_EQ(u"3", variables->idx_get(0));
ASSERT_EQ(u"London", variables->idx_get(u"City"));

// Iterera över variabelsamlingen.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::Collections::Generic::KeyValuePair<System::String, System::String>>> enumerator = doc->get_Variables()->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Name: {0}, Value: {1}", enumerator->get_Current().get_Key(), enumerator->get_Current().get_Value()) << std::endl;
    }
}

// Nedan följer tre sätt att ta bort dokumentvariabler från en samling.
// 1 -  Efter namn:
variables->Remove(u"City");

ASSERT_FALSE(variables->Contains(u"City"));

// 2 -  Efter index:
variables->RemoveAt(1);

ASSERT_FALSE(variables->Contains(u"Home address"));

// 3 -  Rensa hela samlingen på en gång:
variables->Clear();

ASSERT_EQ(0, variables->get_Count());
```

## Se även

* Class [VariableCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
