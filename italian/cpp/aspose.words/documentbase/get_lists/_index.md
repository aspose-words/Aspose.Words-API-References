---
title: "Metodo Aspose::Words::DocumentBase::get_Lists"
linktitle: "get_Lists"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::DocumentBase::get_Lists. Fornisce l'accesso alla formattazione delle liste utilizzata nel documento in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words/documentbase/get_lists/
---
## DocumentBase::get_Lists method


Fornisce l'accesso alla formattazione delle liste utilizzata nel documento.

```cpp
System::SharedPtr<Aspose::Words::Lists::ListCollection> Aspose::Words::DocumentBase::get_Lists() const
```

## Note


Per ulteriori informazioni, vedere la descrizione della classe [ListCollection](../../../aspose.words.lists/listcollection/).

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

## Vedi anche

* Class [ListCollection](../../../aspose.words.lists/listcollection/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
