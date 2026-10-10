---
title: "Classe Aspose::Words::VariableCollection"
linktitle: "VariableCollection"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::VariableCollection. Una collezione di variabili del documento. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 73000
url: /it/cpp/aspose.words/variablecollection/
---
## VariableCollection class


Una raccolta di variabili del documento. Per saperne di più, visita l'articolo di documentazione [Work with Document Properties](https://docs.aspose.com/words/cpp/work-with-document-properties/).

```cpp
class VariableCollection : public System::Collections::Generic::IEnumerable<System::Collections::Generic::KeyValuePair<System::String, System::String>>
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Add](./add/)(const System::String\&, const System::String\&) | Aggiunge una variabile di documento alla raccolta. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Rimuove tutti gli elementi dalla collezione. |
| [Contains](./contains/)(const System::String\&) | Determina se la raccolta contiene una variabile di documento con il nome specificato. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Ottiene il numero di elementi contenuti nella raccolta. |
| [GetEnumerator](./getenumerator/)() override | Restituisce un oggetto enumeratore che può essere usato per iterare su tutte le variabili nella raccolta. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | Ottiene o imposta una variabile di documento tramite il nome non sensibile a maiuscole/minuscole. I valori **null** non sono consentiti come lato destro dell'assegnazione e saranno sostituiti da una stringa vuota. |
| [idx_get](./idx_get/)(int32_t) | Ottiene o imposta una variabile di documento all'indice specificato. I valori **null** non sono consentiti come lato destro dell'assegnazione e saranno sostituiti da una stringa vuota. |
| [idx_set](./idx_set/)(const System::String\&, const System::String\&) | Ottiene o imposta una variabile di documento tramite il nome non sensibile a maiuscole/minuscole. I valori **null** non sono consentiti come lato destro dell'assegnazione e saranno sostituiti da una stringa vuota. |
| [idx_set](./idx_set/)(int32_t, const System::String\&) | Ottiene o imposta una variabile di documento all'indice specificato. I valori **null** non sono consentiti come lato destro dell'assegnazione e saranno sostituiti da una stringa vuota. |
| [IndexOfKey](./indexofkey/)(const System::String\&) | Restituisce l'indice basato su zero della variabile di documento specificata nella raccolta. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | Rimuove una variabile di documento con il nome specificato dalla raccolta. |
| [RemoveAt](./removeat/)(int32_t) | Rimuove una variabile di documento all'indice specificato. |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| Typedef | Descrizione |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |
## Note


I nomi e i valori delle variabili sono stringhe.

I nomi delle variabili non sono sensibili a maiuscole/minuscole.

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
