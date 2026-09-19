---
title: "Aspose::Words::Lists::ListFormat::get_IsListItem metodo"
linktitle: "get_IsListItem"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Lists::ListFormat::get_IsListItem metodo. Vero quando il paragrafo ha una formattazione puntata o numerata applicata in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.lists/listformat/get_islistitem/
---
## ListFormat::get_IsListItem method


Vero quando al paragrafo è applicata una formattazione con elenchi puntati o numerati.

```cpp
bool Aspose::Words::Lists::ListFormat::get_IsListItem()
```


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


Mostra come esportare tutti i paragrafi in un documento che sono elementi di elenco.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ListFormat()->ApplyNumberDefault();
builder->Writeln(u"Numbered list item 1");
builder->Writeln(u"Numbered list item 2");
builder->Writeln(u"Numbered list item 3");
builder->get_ListFormat()->RemoveNumbers();

builder->get_ListFormat()->ApplyBulletDefault();
builder->Writeln(u"Bulleted list item 1");
builder->Writeln(u"Bulleted list item 2");
builder->Writeln(u"Bulleted list item 3");
builder->get_ListFormat()->RemoveNumbers();

System::SharedPtr<Aspose::Words::NodeCollection> paras = doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true);

for (auto&& para : paras->LINQ_OfType<System::SharedPtr<Aspose::Words::Paragraph> >()->LINQ_Where(static_cast<System::Func<System::SharedPtr<Aspose::Words::Paragraph>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Paragraph> p)>>([](System::SharedPtr<Aspose::Words::Paragraph> p) -> bool
{
    return p->get_ListFormat()->get_IsListItem();
})))->LINQ_ToList())
{
    std::cout << System::String::Format(u"This paragraph belongs to list ID# {0}, number style \"{1}\"", para->get_ListFormat()->get_List()->get_ListId(), para->get_ListFormat()->get_ListLevel()->get_NumberStyle()) << std::endl;
    std::cout << System::String::Format(u"\t\"{0}\"", para->GetText().Trim()) << std::endl;
}
```

## Vedi anche

* Class [ListFormat](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
