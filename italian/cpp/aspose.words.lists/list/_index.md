---
title: "Aspose::Words::Lists::List class"
linktitle: "Elenco"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Lists::List class. Rappresenta la formattazione di un elenco. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 1000
url: /it/cpp/aspose.words.lists/list/
---
## List class


Rappresenta la formattazione di un elenco. Per saperne di più, visita l'articolo di documentazione [Working with Lists](https://docs.aspose.com/words/cpp/working-with-lists/).

```cpp
class List : public System::IComparable<System::SharedPtr<Aspose::Words::Lists::List>>
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [CompareTo](./compareto/)(System::SharedPtr\<Aspose::Words::Lists::List\>) override | Confronta l'elenco specificato con l'elenco corrente. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Lists::List\>\&) | Confronta con l'elenco specificato. |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Determina se l'oggetto specificato è uguale in valore all'oggetto corrente. |
| [get_Document](./get_document/)() const | Restituisce il documento proprietario. |
| [get_IsListStyleDefinition](./get_isliststyledefinition/)() | Restituisce **true** se questo elenco è una definizione di uno stile di elenco. |
| [get_IsListStyleReference](./get_isliststylereference/)() | Restituisce **true** se questo elenco è un riferimento a uno stile di elenco. |
| [get_IsMultiLevel](./get_ismultilevel/)() | Restituisce **true** quando l'elenco contiene 9 livelli; **false** quando contiene 1 livello. |
| [get_IsRestartAtEachSection](./get_isrestartateachsection/)() | Specifica se l'elenco deve essere ricominciato in ogni sezione. Il valore predefinito è **false**. |
| [get_ListId](./get_listid/)() const | Ottiene l'identificatore univoco dell'elenco. |
| [get_ListLevels](./get_listlevels/)() | Ottiene la collezione dei livelli dell'elenco per questo elenco. |
| [get_Style](./get_style/)() | Ottiene lo stile di elenco che questo elenco fa riferimento o definisce. |
| [GetHashCode](./gethashcode/)() const override | Calcola il codice hash per questo oggetto elenco. |
| [GetType](./gettype/)() const override |  |
| [HasSameTemplate](./hassametemplate/)(const System::SharedPtr\<Aspose::Words::Lists::List\>\&) | Restituisce true se l'elenco corrente e l'elenco fornito sono creati dallo stesso modello. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_IsRestartAtEachSection](./set_isrestartateachsection/)(bool) | Impostatore per [Aspose::Words::Lists::List::get_IsRestartAtEachSection](./get_isrestartateachsection/). |
| static [Type](./type/)() |  |
## Note


Un elenco in un documento Microsoft Word è un insieme di proprietà di formattazione dell'elenco. Ogni elenco può avere fino a 9 livelli e le proprietà di formattazione, come lo stile di numerazione, il valore iniziale, l'indentazione, la posizione della tabulazione, ecc., sono definite separatamente per ciascun livello.

Un oggetto [List](./) appartiene sempre alla collezione [ListCollection](../listcollection/).

Per creare un nuovo elenco, utilizza i metodi Add della collezione [ListCollection](../listcollection/).

Per modificare la formattazione di un elenco, utilizza gli oggetti [ListLevel](../listlevel/) presenti nella collezione [ListLevels](./get_listlevels/).

Per applicare o rimuovere la formattazione dell'elenco da un paragrafo, utilizza [ListFormat](../listformat/).

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


Mostra come applicare una formattazione personalizzata dell'elenco ai paragrafi quando si utilizza [DocumentBuilder](../../aspose.words/documentbuilder/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Un elenco ci permette di organizzare e decorare insiemi di paragrafi con simboli prefisso e rientri.
// Possiamo creare elenchi nidificati aumentando il livello di rientro.
// Possiamo avviare e terminare un elenco usando la proprietà "ListFormat" di un document builder.
// Ogni paragrafo che aggiungiamo tra l'inizio e la fine di un elenco diventerà un elemento dell'elenco.
// Crea un elenco da un modello Microsoft Word e personalizza i primi due livelli dell'elenco.
System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);

System::SharedPtr<Aspose::Words::Lists::ListLevel> listLevel = list->get_ListLevels()->idx_get(0);
listLevel->get_Font()->set_Color(System::Drawing::Color::get_Red());
listLevel->get_Font()->set_Size(24);
listLevel->set_NumberStyle(Aspose::Words::NumberStyle::OrdinalText);
listLevel->set_StartAt(21);
listLevel->set_NumberFormat(u"\x0000");

listLevel->set_NumberPosition(-36);
listLevel->set_TextPosition(144);
listLevel->set_TabPosition(144);

listLevel = list->get_ListLevels()->idx_get(1);
listLevel->set_Alignment(Aspose::Words::Lists::ListLevelAlignment::Right);
listLevel->set_NumberStyle(Aspose::Words::NumberStyle::Bullet);
listLevel->get_Font()->set_Name(u"Wingdings");
listLevel->get_Font()->set_Color(System::Drawing::Color::get_Blue());
listLevel->get_Font()->set_Size(24);

// Questo valore NumberFormat creerà simboli di elenco puntato a forma di stella.
listLevel->set_NumberFormat(u"\xf0af");
listLevel->set_TrailingCharacter(Aspose::Words::Lists::ListTrailingCharacter::Space);
listLevel->set_NumberPosition(144);

// Crea paragrafi e applica entrambi i livelli dell'elenco della nostra formattazione personalizzata a essi.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ListFormat()->set_List(list);
builder->Writeln(u"The quick brown fox...");
builder->Writeln(u"The quick brown fox...");

builder->get_ListFormat()->ListIndent();
builder->Writeln(u"jumped over the lazy dog.");
builder->Writeln(u"jumped over the lazy dog.");

builder->get_ListFormat()->ListOutdent();
builder->Writeln(u"The quick brown fox...");

builder->get_ListFormat()->RemoveNumbers();

builder->get_Document()->Save(get_ArtifactsDir() + u"Lists.CreateCustomList.docx");
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
