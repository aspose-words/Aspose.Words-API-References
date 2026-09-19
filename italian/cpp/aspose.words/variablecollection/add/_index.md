---
title: "Metodo Aspose::Words::VariableCollection::Add"
linktitle: "Add"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::VariableCollection::Add. Aggiunge una variabile di documento alla raccolta in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words/variablecollection/add/
---
## VariableCollection::Add method


Aggiunge una variabile di documento alla raccolta.

```cpp
void Aspose::Words::VariableCollection::Add(const System::String &name, const System::String &value)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | const System::String\& | Il nome della variabile da aggiungere, senza distinzione tra maiuscole e minuscole. |
| value | const System::String\& | Il valore della variabile. Il valore non può essere **null**, se il valore è null verrà usata una stringa vuota. |

## Esempi



Mostra come lavorare con la raccolta di variabili di un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::VariableCollection> variables = doc->get_Variables();

// Ogni documento ha una raccolta di variabili coppia chiave/valore, a cui possiamo aggiungere elementi.
variables->Add(u"Home address", u"123 Main St.");
variables->Add(u"City", u"London");
variables->Add(u"Bedrooms", u"3");

ASSERT_EQ(3, variables->get_Count());

// Possiamo visualizzare i valori delle variabili nel corpo del documento usando i campi DOCVARIABLE.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDocVariable>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDocVariable, true));
field->set_VariableName(u"Home address");
field->Update();

ASSERT_EQ(u"123 Main St.", field->get_Result());

// L'assegnazione di valori a chiavi esistenti le aggiornerà.
variables->Add(u"Home address", u"456 Queen St.");

// Dovremo quindi aggiornare i campi DOCVARIABLE per garantire che mostrino un valore aggiornato.
ASSERT_EQ(u"123 Main St.", field->get_Result());

field->Update();

ASSERT_EQ(u"456 Queen St.", field->get_Result());

// Verifica che le variabili del documento con un determinato nome o valore esistano.
ASSERT_TRUE(variables->Contains(u"City"));
ASSERT_TRUE(variables->LINQ_Any(static_cast<System::Func<System::Collections::Generic::KeyValuePair<System::String, System::String>, bool>>(static_cast<std::function<bool(System::Collections::Generic::KeyValuePair<System::String, System::String> v)>>([](System::Collections::Generic::KeyValuePair<System::String, System::String> v) -> bool
{
    return v.get_Value() == u"London";
}))));

// La raccolta di variabili ordina automaticamente le variabili alfabeticamente per nome.
ASSERT_EQ(0, variables->IndexOfKey(u"Bedrooms"));
ASSERT_EQ(1, variables->IndexOfKey(u"City"));
ASSERT_EQ(2, variables->IndexOfKey(u"Home address"));

ASSERT_EQ(u"3", variables->idx_get(0));
ASSERT_EQ(u"London", variables->idx_get(u"City"));

// Enumera la raccolta di variabili.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::Collections::Generic::KeyValuePair<System::String, System::String>>> enumerator = doc->get_Variables()->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Name: {0}, Value: {1}", enumerator->get_Current().get_Key(), enumerator->get_Current().get_Value()) << std::endl;
    }
}

// Di seguito sono riportati tre modi per rimuovere le variabili di documento da una raccolta.
// 1 -  Per nome:
variables->Remove(u"City");

ASSERT_FALSE(variables->Contains(u"City"));

// 2 -  Per indice:
variables->RemoveAt(1);

ASSERT_FALSE(variables->Contains(u"Home address"));

// 3 -  Cancella l'intera raccolta in una volta:
variables->Clear();

ASSERT_EQ(0, variables->get_Count());
```

## Vedi anche

* Class [VariableCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
