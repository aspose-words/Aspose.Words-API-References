---
title: "Metodo Aspose::Words::Lists::ListCollection::AddCopy"
linktitle: "AddCopy"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Lists::ListCollection::AddCopy. Crea una nuova lista copiando la lista specificata e aggiungendola alla collezione di liste nel documento in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.lists/listcollection/addcopy/
---
## ListCollection::AddCopy method


Crea un nuovo elenco copiando l'elenco specificato e lo aggiunge alla collezione di elenchi nel documento.

```cpp
System::SharedPtr<Aspose::Words::Lists::List> Aspose::Words::Lists::ListCollection::AddCopy(const System::SharedPtr<Aspose::Words::Lists::List> &srcList)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| srcList | const System::SharedPtr\<Aspose::Words::Lists::List\>\& | La lista di origine da copiare. |

### ReturnValue

La lista appena creata.
## Note


La lista di origine può provenire da qualsiasi documento. Se la lista di origine appartiene a un documento diverso, viene creata una copia della lista e aggiunta al documento corrente.

Se la lista di origine è un riferimento o una definizione di uno stile di lista, la nuova lista creata non è correlata allo stile di lista originale.

## Esempi



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

* Class [List](../../list/)
* Class [ListCollection](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
