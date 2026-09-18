---
title: "Aspose::Words::VariableCollection::idx_get Methode"
linktitle: "idx_get"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::VariableCollection::idx_get Methode. Liest oder setzt eine Dokumentvariable anhand des case‑insensitiven Namens. Null‑Werte sind auf der rechten Seite der Zuweisung nicht erlaubt und werden in C++ durch eine leere Zeichenkette ersetzt."
type: docs
weight: 12000
url: /de/cpp/aspose.words/variablecollection/idx_get/
---
## VariableCollection::idx_get(const System::String\&) method


Liest oder setzt eine Dokumentvariable anhand des case‑insensitiven Namens. **null**‑Werte sind als rechte Seite der Zuweisung nicht zulässig und werden durch eine leere Zeichenkette ersetzt.

```cpp
System::String Aspose::Words::VariableCollection::idx_get(const System::String &name)
```


## Beispiele



Zeigt, wie man mit der Variablensammlung eines Dokuments arbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::VariableCollection> variables = doc->get_Variables();

// Jedes Dokument hat eine Sammlung von Schlüssel/Wert‑Paar‑Variablen, zu der wir Elemente hinzufügen können.
variables->Add(u"Home address", u"123 Main St.");
variables->Add(u"City", u"London");
variables->Add(u"Bedrooms", u"3");

ASSERT_EQ(3, variables->get_Count());

// Wir können die Werte von Variablen im Dokumentkörper mithilfe von DOCVARIABLE‑Feldern anzeigen.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDocVariable>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDocVariable, true));
field->set_VariableName(u"Home address");
field->Update();

ASSERT_EQ(u"123 Main St.", field->get_Result());

// Das Zuweisen von Werten zu bestehenden Schlüsseln aktualisiert diese.
variables->Add(u"Home address", u"456 Queen St.");

// Wir müssen dann die DOCVARIABLE‑Felder aktualisieren, um sicherzustellen, dass sie einen aktuellen Wert anzeigen.
ASSERT_EQ(u"123 Main St.", field->get_Result());

field->Update();

ASSERT_EQ(u"456 Queen St.", field->get_Result());

// Überprüfen Sie, ob die Dokumentvariablen mit einem bestimmten Namen oder Wert existieren.
ASSERT_TRUE(variables->Contains(u"City"));
ASSERT_TRUE(variables->LINQ_Any(static_cast<System::Func<System::Collections::Generic::KeyValuePair<System::String, System::String>, bool>>(static_cast<std::function<bool(System::Collections::Generic::KeyValuePair<System::String, System::String> v)>>([](System::Collections::Generic::KeyValuePair<System::String, System::String> v) -> bool
{
    return v.get_Value() == u"London";
}))));

// Die Variablensammlung sortiert Variablen automatisch alphabetisch nach Namen.
ASSERT_EQ(0, variables->IndexOfKey(u"Bedrooms"));
ASSERT_EQ(1, variables->IndexOfKey(u"City"));
ASSERT_EQ(2, variables->IndexOfKey(u"Home address"));

ASSERT_EQ(u"3", variables->idx_get(0));
ASSERT_EQ(u"London", variables->idx_get(u"City"));

// Durchlaufen Sie die Variablensammlung.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::Collections::Generic::KeyValuePair<System::String, System::String>>> enumerator = doc->get_Variables()->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Name: {0}, Value: {1}", enumerator->get_Current().get_Key(), enumerator->get_Current().get_Value()) << std::endl;
    }
}

// Im Folgenden sind drei Methoden zum Entfernen von Dokumentvariablen aus einer Sammlung aufgeführt.
// 1 -  Nach Namen:
variables->Remove(u"City");

ASSERT_FALSE(variables->Contains(u"City"));

// 2 -  Nach Index:
variables->RemoveAt(1);

ASSERT_FALSE(variables->Contains(u"Home address"));

// 3 -  Die gesamte Sammlung auf einmal leeren:
variables->Clear();

ASSERT_EQ(0, variables->get_Count());
```

## Siehe auch

* Class [VariableCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## VariableCollection::idx_get(int32_t) method


Liest oder setzt eine Dokumentvariable am angegebenen Index. **null**‑Werte sind als rechte Seite der Zuweisung nicht zulässig und werden durch eine leere Zeichenkette ersetzt.

```cpp
System::String Aspose::Words::VariableCollection::idx_get(int32_t index)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| index | int32_t | Nullbasierter Index der Dokumentvariable. |

## Beispiele



Zeigt, wie man mit der Variablensammlung eines Dokuments arbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::VariableCollection> variables = doc->get_Variables();

// Jedes Dokument hat eine Sammlung von Schlüssel/Wert‑Paar‑Variablen, zu der wir Elemente hinzufügen können.
variables->Add(u"Home address", u"123 Main St.");
variables->Add(u"City", u"London");
variables->Add(u"Bedrooms", u"3");

ASSERT_EQ(3, variables->get_Count());

// Wir können die Werte von Variablen im Dokumentkörper mithilfe von DOCVARIABLE‑Feldern anzeigen.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDocVariable>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDocVariable, true));
field->set_VariableName(u"Home address");
field->Update();

ASSERT_EQ(u"123 Main St.", field->get_Result());

// Das Zuweisen von Werten zu bestehenden Schlüsseln aktualisiert diese.
variables->Add(u"Home address", u"456 Queen St.");

// Wir müssen dann die DOCVARIABLE‑Felder aktualisieren, um sicherzustellen, dass sie einen aktuellen Wert anzeigen.
ASSERT_EQ(u"123 Main St.", field->get_Result());

field->Update();

ASSERT_EQ(u"456 Queen St.", field->get_Result());

// Überprüfen Sie, ob die Dokumentvariablen mit einem bestimmten Namen oder Wert existieren.
ASSERT_TRUE(variables->Contains(u"City"));
ASSERT_TRUE(variables->LINQ_Any(static_cast<System::Func<System::Collections::Generic::KeyValuePair<System::String, System::String>, bool>>(static_cast<std::function<bool(System::Collections::Generic::KeyValuePair<System::String, System::String> v)>>([](System::Collections::Generic::KeyValuePair<System::String, System::String> v) -> bool
{
    return v.get_Value() == u"London";
}))));

// Die Variablensammlung sortiert Variablen automatisch alphabetisch nach Namen.
ASSERT_EQ(0, variables->IndexOfKey(u"Bedrooms"));
ASSERT_EQ(1, variables->IndexOfKey(u"City"));
ASSERT_EQ(2, variables->IndexOfKey(u"Home address"));

ASSERT_EQ(u"3", variables->idx_get(0));
ASSERT_EQ(u"London", variables->idx_get(u"City"));

// Durchlaufen Sie die Variablensammlung.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::Collections::Generic::KeyValuePair<System::String, System::String>>> enumerator = doc->get_Variables()->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Name: {0}, Value: {1}", enumerator->get_Current().get_Key(), enumerator->get_Current().get_Value()) << std::endl;
    }
}

// Im Folgenden sind drei Methoden zum Entfernen von Dokumentvariablen aus einer Sammlung aufgeführt.
// 1 -  Nach Namen:
variables->Remove(u"City");

ASSERT_FALSE(variables->Contains(u"City"));

// 2 -  Nach Index:
variables->RemoveAt(1);

ASSERT_FALSE(variables->Contains(u"Home address"));

// 3 -  Die gesamte Sammlung auf einmal leeren:
variables->Clear();

ASSERT_EQ(0, variables->get_Count());
```

## Siehe auch

* Class [VariableCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
