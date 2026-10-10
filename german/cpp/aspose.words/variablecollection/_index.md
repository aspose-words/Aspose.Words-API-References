---
title: "Aspose::Words::VariableCollection Klasse"
linktitle: "VariableCollection"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::VariableCollection Klasse. Eine Sammlung von Dokumentvariablen. Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel in C++."
type: docs
weight: 73000
url: /de/cpp/aspose.words/variablecollection/
---
## VariableCollection class


Eine Sammlung von Dokumentvariablen. Weitere Informationen finden Sie im Dokumentationsartikel [Work with Document Properties](https://docs.aspose.com/words/cpp/work-with-document-properties/).

```cpp
class VariableCollection : public System::Collections::Generic::IEnumerable<System::Collections::Generic::KeyValuePair<System::String, System::String>>
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Add](./add/)(const System::String\&, const System::String\&) | Fügt der Sammlung eine Dokumentvariable hinzu. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Entfernt alle Elemente aus der Sammlung. |
| [Contains](./contains/)(const System::String\&) | Bestimmt, ob die Sammlung eine Dokumentvariable mit dem angegebenen Namen enthält. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Gibt die Anzahl der in der Sammlung enthaltenen Elemente zurück. |
| [GetEnumerator](./getenumerator/)() override | Gibt ein Enumerator-Objekt zurück, das verwendet werden kann, um über alle Variablen in der Sammlung zu iterieren. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | Liest oder setzt eine Dokumentvariable anhand des case‑insensitiven Namens. **null**‑Werte sind als rechte Seite der Zuweisung nicht zulässig und werden durch eine leere Zeichenkette ersetzt. |
| [idx_get](./idx_get/)(int32_t) | Liest oder setzt eine Dokumentvariable am angegebenen Index. **null**‑Werte sind als rechte Seite der Zuweisung nicht zulässig und werden durch eine leere Zeichenkette ersetzt. |
| [idx_set](./idx_set/)(const System::String\&, const System::String\&) | Liest oder setzt eine Dokumentvariable anhand des case‑insensitiven Namens. **null**‑Werte sind als rechte Seite der Zuweisung nicht zulässig und werden durch eine leere Zeichenkette ersetzt. |
| [idx_set](./idx_set/)(int32_t, const System::String\&) | Liest oder setzt eine Dokumentvariable am angegebenen Index. **null**‑Werte sind als rechte Seite der Zuweisung nicht zulässig und werden durch eine leere Zeichenkette ersetzt. |
| [IndexOfKey](./indexofkey/)(const System::String\&) | Gibt den nullbasierten Index der angegebenen Dokumentvariable in der Sammlung zurück. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | Entfernt eine Dokumentvariable mit dem angegebenen Namen aus der Sammlung. |
| [RemoveAt](./removeat/)(int32_t) | Entfernt eine Dokumentvariable am angegebenen Index. |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| Typedef | Beschreibung |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |
## Hinweise


Variablennamen und -werte sind Zeichenketten.

Variablennamen sind case‑insensitiv.

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
