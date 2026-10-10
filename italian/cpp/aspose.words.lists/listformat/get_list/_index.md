---
title: "Metodo Aspose::Words::Lists::ListFormat::get_List"
linktitle: "get_List"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Lists::ListFormat::get_List. Ottiene o imposta l'elenco di cui questo paragrafo è membro in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.lists/listformat/get_list/
---
## ListFormat::get_List method


Ottiene o imposta l'elenco di cui questo paragrafo è membro.

```cpp
System::SharedPtr<Aspose::Words::Lists::List> Aspose::Words::Lists::ListFormat::get_List()
```

## Note


L'elenco che viene assegnato a questa proprietà deve appartenere al documento corrente.

L'elenco che viene assegnato a questa proprietà non deve essere una definizione di stile dell'elenco.

Impostare questa proprietà su **null** rimuove i punti elenco e la numerazione dal paragrafo e imposta il numero del livello dell'elenco a zero. Impostare questa proprietà su **null** è equivalente a chiamare [RemoveNumbers](../removenumbers/).

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


Mostra come annidare un elenco all'interno di un altro elenco.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Un elenco ci permette di organizzare e decorare insiemi di paragrafi con simboli prefisso e rientri.
// Possiamo creare elenchi nidificati aumentando il livello di rientro.
// Possiamo avviare e terminare un elenco usando la proprietà "ListFormat" di un document builder.
// Ogni paragrafo che aggiungiamo tra l'inizio e la fine di un elenco diventerà un elemento dell'elenco.
// Crea un elenco outline per le intestazioni.
System::SharedPtr<Aspose::Words::Lists::List> outlineList = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::OutlineNumbers);
builder->get_ListFormat()->set_List(outlineList);
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"This is my Chapter 1");

// Crea un elenco numerato.
System::SharedPtr<Aspose::Words::Lists::List> numberedList = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);
builder->get_ListFormat()->set_List(numberedList);
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Normal);
builder->Writeln(u"Numbered list item 1.");

// Ogni paragrafo che contiene un elenco avrà questo flag.
ASSERT_TRUE(builder->get_CurrentParagraph()->get_IsListItem());
ASSERT_TRUE(builder->get_ParagraphFormat()->get_IsListItem());

// Crea un elenco puntato.
System::SharedPtr<Aspose::Words::Lists::List> bulletedList = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault);
builder->get_ListFormat()->set_List(bulletedList);
builder->get_ParagraphFormat()->set_LeftIndent(72);
builder->Writeln(u"Bulleted list item 1.");
builder->Writeln(u"Bulleted list item 2.");
builder->get_ParagraphFormat()->ClearFormatting();

// Ripristina l'elenco numerato.
builder->get_ListFormat()->set_List(numberedList);
builder->Writeln(u"Numbered list item 2.");
builder->Writeln(u"Numbered list item 3.");

// Ripristina l'elenco outline.
builder->get_ListFormat()->set_List(outlineList);
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"This is my Chapter 2");

builder->get_ParagraphFormat()->ClearFormatting();

builder->get_Document()->Save(get_ArtifactsDir() + u"Lists.NestedLists.docx");
```

## Vedi anche

* Class [List](../../list/)
* Class [ListFormat](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
