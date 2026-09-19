---
title: "Aspose::Words::Lists::ListCollection class"
linktitle: "ListCollection"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Lists::ListCollection class. Memorizza e gestisce la formattazione di elenchi puntati e numerati usati in un documento. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.lists/listcollection/
---
## ListCollection class


Memorizza e gestisce la formattazione di elenchi puntati e numerati usati in un documento. Per saperne di più, visita l'articolo di documentazione [Working with Lists](https://docs.aspose.com/words/cpp/working-with-lists/).

```cpp
class ListCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Lists::List>>
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Add](./add/)(Aspose::Words::Lists::ListTemplate) | Crea un nuovo elenco basato su un modello predefinito e lo aggiunge alla collezione di elenchi nel documento. |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Crea un nuovo elenco che fa riferimento a uno stile di elenco e lo aggiunge alla collezione di elenchi nel documento. |
| [AddCopy](./addcopy/)(const System::SharedPtr\<Aspose::Words::Lists::List\>\&) | Crea un nuovo elenco copiando l'elenco specificato e lo aggiunge alla collezione di elenchi nel documento. |
| [AddSingleLevelList](./addsinglelevellist/)(Aspose::Words::Lists::ListTemplate) | Crea un nuovo elenco a livello singolo basato sul modello predefinito e lo aggiunge alla collezione di elenchi nel documento. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Restituisce il conteggio degli elenchi numerati e puntati nel documento. |
| [get_Document](./get_document/)() const | Restituisce il documento proprietario. |
| [GetEnumerator](./getenumerator/)() override | Restituisce l'oggetto enumeratore che elencherà gli elenchi nel documento. |
| [GetListByListId](./getlistbylistid/)(int32_t) | Ottiene un elenco mediante un identificatore di elenco. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Ottiene un elenco per indice. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
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


Un elenco in un documento Microsoft Word è un insieme di proprietà di formattazione dell'elenco. La formattazione degli elenchi è memorizzata nella collezione [ListCollection](./) separatamente dai paragrafi di testo.

Non si creano oggetti di questa classe. C'è sempre un solo oggetto [ListCollection](./) per documento ed è accessibile tramite la proprietà [Lists](../../aspose.words/documentbase/get_lists/).

Per creare un nuovo elenco basato su un modello di elenco predefinito o su uno stile di elenco, utilizzare il metodo [Add()](../).

Per creare un nuovo elenco con formattazione identica a un elenco esistente, utilizzare il metodo [AddCopy()](../).

Per rendere un paragrafo puntato o numerato, è necessario applicare la formattazione dell'elenco a un paragrafo assegnando un oggetto [List](../list/) alla proprietà [List](../listformat/get_list/) di [ListFormat](../listformat/).

Per rimuovere la formattazione dell'elenco da un paragrafo, utilizzare il metodo [RemoveNumbers](../listformat/removenumbers/).

Se conosci un po' WordprocessingML, potresti sapere che definisce concetti separati per "list" e "list definition". Questo corrisponde esattamente a come la formattazione dell'elenco è memorizzata in un documento Microsoft Word a basso livello. La definizione di [List](../list/) è come uno "schema" e l'elenco è come un'istanza di una definizione di elenco.

Per semplificare il modello di programmazione, Aspose.Words nasconde la distinzione tra elenco e definizione di elenco nello stesso modo in cui Microsoft Word la nasconde nella sua interfaccia utente. Questo ti consente di concentrarti di più su come vuoi che il tuo documento appaia, invece di costruire oggetti di basso livello per soddisfare i requisiti del formato file di Microsoft Word.

Non è possibile eliminare gli elenchi una volta creati nella versione corrente di [Aspose.Words](../../aspose.words/). Questo è simile a Microsoft Word, dove l'utente non ha un controllo esplicito sulle definizioni degli elenchi.

## Esempi



Mostra come lavorare con i livelli di elenco.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

ASSERT_FALSE(builder->get_ListFormat()->get_IsListItem());

// Un elenco ci permette di organizzare e decorare insiemi di paragrafi con simboli prefisso e rientri.
// Possiamo creare elenchi nidificati aumentando il livello di rientro.
// Possiamo avviare e terminare un elenco usando la proprietà "ListFormat" di un document builder.
// Ogni paragrafo che aggiungiamo tra l'inizio e la fine di un elenco diventerà un elemento dell'elenco.
// Di seguito sono riportati due tipi di elenchi che possiamo creare usando un document builder.
// 1 -  Un elenco numerato:
// Gli elenchi numerati creano un ordine logico per i loro paragrafi numerando ogni elemento.
builder->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault));

ASSERT_TRUE(builder->get_ListFormat()->get_IsListItem());

// Impostando la proprietà "ListLevelNumber", possiamo aumentare il livello dell'elenco
// per iniziare una sotto-lista autonoma all'elemento dell'elenco corrente.
// Il modello di elenco di Microsoft Word chiamato "NumberDefault" utilizza numeri per creare livelli di elenco per il primo livello.
// I livelli di elenco più profondi usano lettere e numeri romani minuscoli.
for (int32_t i = 0; i < 9; i++)
{
    builder->get_ListFormat()->set_ListLevelNumber(i);
    builder->Writeln(System::String(u"Level ") + i);
}

// 2 -  Un elenco puntato:
// Questo elenco applicherà un rientro e un simbolo di punto elenco ("•") prima di ogni paragrafo.
// I livelli più profondi di questo elenco utilizzeranno simboli diversi, come "■" e "○".
builder->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault));

for (int32_t i = 0; i < 9; i++)
{
    builder->get_ListFormat()->set_ListLevelNumber(i);
    builder->Writeln(System::String(u"Level ") + i);
}

// Possiamo disabilitare la formattazione degli elenchi per non formattare i paragrafi successivi come elenchi rimuovendo il flag "List".
builder->get_ListFormat()->set_List(nullptr);

ASSERT_FALSE(builder->get_ListFormat()->get_IsListItem());

doc->Save(get_ArtifactsDir() + u"Lists.SpecifyListLevel.docx");
```


Mostra come riavviare la numerazione in un elenco copiando un elenco.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Un elenco ci permette di organizzare e decorare insiemi di paragrafi con simboli prefisso e rientri.
// Possiamo creare elenchi nidificati aumentando il livello di rientro.
// Possiamo avviare e terminare un elenco usando la proprietà "ListFormat" di un document builder.
// Ogni paragrafo che aggiungiamo tra l'inizio e la fine di un elenco diventerà un elemento dell'elenco.
// Crea un elenco da un modello di Microsoft Word e personalizza il suo primo livello di elenco.
System::SharedPtr<Aspose::Words::Lists::List> list1 = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberArabicParenthesis);
list1->get_ListLevels()->idx_get(0)->get_Font()->set_Color(System::Drawing::Color::get_Red());
list1->get_ListLevels()->idx_get(0)->set_Alignment(Aspose::Words::Lists::ListLevelAlignment::Right);

// Applica il nostro elenco a qualche paragrafo.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"List 1 starts below:");
builder->get_ListFormat()->set_List(list1);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

// Possiamo aggiungere una copia di un elenco esistente alla collezione di elenchi del documento
// per creare un elenco simile senza modificare l'originale.
System::SharedPtr<Aspose::Words::Lists::List> list2 = doc->get_Lists()->AddCopy(list1);
list2->get_ListLevels()->idx_get(0)->get_Font()->set_Color(System::Drawing::Color::get_Blue());
list2->get_ListLevels()->idx_get(0)->set_StartAt(10);

// Applica il secondo elenco a nuovi paragrafi.
builder->Writeln(u"List 2 starts below:");
builder->get_ListFormat()->set_List(list2);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

doc->Save(get_ArtifactsDir() + u"Lists.RestartNumberingUsingListCopy.docx");
```

## Vedi anche

* Namespace [Aspose::Words::Lists](../)
* Library [Aspose.Words for C++](../../)
