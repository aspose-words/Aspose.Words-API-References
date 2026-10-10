---
title: "Classe Aspose::Words::Lists::ListFormat"
linktitle: "ListFormat"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::Lists::ListFormat. Consente di controllare quale formattazione dell'elenco viene applicata a un paragrafo. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.lists/listformat/
---
## ListFormat class


Consente di controllare quale formattazione dell'elenco viene applicata a un paragrafo. Per saperne di più, visita l'articolo di documentazione [Working with Lists](https://docs.aspose.com/words/cpp/working-with-lists/).

```cpp
class ListFormat : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [ApplyBulletDefault](./applybulletdefault/)() | Avvia un nuovo elenco puntato predefinito e lo applica al paragrafo. |
| [ApplyNumberDefault](./applynumberdefault/)() | Avvia un nuovo elenco numerato predefinito e lo applica al paragrafo. |
| [get_IsListItem](./get_islistitem/)() | Vero quando al paragrafo è applicata una formattazione con elenchi puntati o numerati. |
| [get_List](./get_list/)() | Ottiene o imposta l'elenco di cui questo paragrafo è membro. |
| [get_ListLevel](./get_listlevel/)() | Restituisce la formattazione del livello dell'elenco più eventuali sovrascritture di formattazione applicate al paragrafo corrente. |
| [get_ListLevelNumber](./get_listlevelnumber/)() | Ottiene o imposta il numero del livello dell'elenco (da 0 a 8) per il paragrafo. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ListIndent](./listindent/)() | Incrementa di un livello il livello dell'elenco del paragrafo corrente. |
| [ListOutdent](./listoutdent/)() | Decrementa di un livello il livello dell'elenco del paragrafo corrente. |
| [RemoveNumbers](./removenumbers/)() | Rimuove numeri o punti elenco dal paragrafo corrente e imposta il livello dell'elenco a zero. |
| [set_List](./set_list/)(const System::SharedPtr\<Aspose::Words::Lists::List\>\&) | Impostatore per [Aspose::Words::Lists::ListFormat::get_List](./get_list/). |
| [set_ListLevelNumber](./set_listlevelnumber/)(int32_t) | Impostatore per [Aspose::Words::Lists::ListFormat::get_ListLevelNumber](./get_listlevelnumber/). |
| static [Type](./type/)() |  |
## Note


Un paragrafo in un documento Microsoft Word può essere puntato o numerato. Quando un paragrafo è puntato o numerato, si dice che al paragrafo è applicata una formattazione di elenco.

Non si creano oggetti della classe [ListFormat](./) direttamente. Si accede a [ListFormat](./) come proprietà di un altro oggetto che può avere una formattazione di elenco associata. Al momento gli oggetti che possono avere una formattazione di elenco sono: [Paragraph](../../aspose.words/paragraph/), [Style](../../aspose.words/style/) e [DocumentBuilder](../../aspose.words/documentbuilder/).

[ListFormat](./) of a [Paragraph](../../aspose.words/paragraph/) specifies what list formatting and list level is applied to that particular paragraph.

[ListFormat](./) of a [Style](../../aspose.words/style/) (applicable to paragraph styles only) allows to specify what list formatting and list level is applied to all paragraphs of that particular style.

[ListFormat](./) of a [DocumentBuilder](../../aspose.words/documentbuilder/) provides access to the list formatting at the current cursor position inside the [DocumentBuilder](../../aspose.words/documentbuilder/).

La formattazione dell'elenco stessa è memorizzata all'interno di un oggetto [List](../list/) che è conservato separatamente dai paragrafi. Gli oggetti elenco sono memorizzati all'interno di una collezione [ListCollection](../listcollection/). C'è una singola collezione [ListCollection](../listcollection/) per ogni [Document](../../aspose.words/document/).

I paragrafi non appartengono fisicamente a un elenco. I paragrafi fanno semplicemente riferimento a un particolare oggetto elenco tramite la proprietà [List](./get_list/) e a un particolare livello nell'elenco tramite la proprietà [ListLevelNumber](./get_listlevelnumber/). Impostando queste due proprietà si controlla quali punti elenco e numerazioni sono applicati a un paragrafo.

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

* Namespace [Aspose::Words::Lists](../)
* Library [Aspose.Words for C++](../../)
