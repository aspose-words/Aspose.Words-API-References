---
title: "Aspose::Words::StyleCollection::Add metodo"
linktitle: "Add"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::StyleCollection::Add metodo. Crea un nuovo stile definito dall'utente e lo aggiunge alla collezione in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words/stylecollection/add/
---
## StyleCollection::Add method


Crea un nuovo stile definito dall'utente e lo aggiunge alla raccolta.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::StyleCollection::Add(Aspose::Words::StyleType type, const System::String &name)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| type | Aspose::Words::StyleType | Un valore [StyleType](../../styletype/) che specifica il tipo di stile da creare. |
| name | const System::String\& | Nome sensibile al maiuscolo/minuscolo dello stile da creare. |
## Note


Puoi creare uno stile di carattere, di paragrafo o di elenco.

Quando si crea uno stile di elenco, lo stile viene creato con la formattazione predefinita di elenco numerato (1 \ a \ i).

Genera un'eccezione se esiste già uno stile con questo nome.

## Esempi



Mostra come creare uno stile di elenco e usarlo in un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Un elenco ci permette di organizzare e decorare insiemi di paragrafi con simboli prefisso e rientri.
// Possiamo creare elenchi nidificati aumentando il livello di rientro.
// Possiamo avviare e terminare un elenco usando la proprietà "ListFormat" di un document builder.
// Ogni paragrafo che aggiungiamo tra l'inizio e la fine di un elenco diventerà un elemento dell'elenco.
// Possiamo contenere un intero oggetto List all'interno di uno stile.
System::SharedPtr<Aspose::Words::Style> listStyle = doc->get_Styles()->Add(Aspose::Words::StyleType::List, u"MyListStyle");

System::SharedPtr<Aspose::Words::Lists::List> list1 = listStyle->get_List();

ASSERT_TRUE(list1->get_IsListStyleDefinition());
ASSERT_FALSE(list1->get_IsListStyleReference());
ASSERT_TRUE(list1->get_IsMultiLevel());
ASPOSE_ASSERT_EQ(listStyle, list1->get_Style());

// Modifica l'aspetto di tutti i livelli dell'elenco nel nostro elenco.
for (auto&& level : list1->get_ListLevels())
{
    level->get_Font()->set_Name(u"Verdana");
    level->get_Font()->set_Color(System::Drawing::Color::get_Blue());
    level->get_Font()->set_Bold(true);
}

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Using list style first time:");

// Crea un altro elenco da un elenco all'interno di uno stile.
System::SharedPtr<Aspose::Words::Lists::List> list2 = doc->get_Lists()->Add(listStyle);

ASSERT_FALSE(list2->get_IsListStyleDefinition());
ASSERT_TRUE(list2->get_IsListStyleReference());
ASPOSE_ASSERT_EQ(listStyle, list2->get_Style());

// Aggiungi alcuni elementi di elenco che il nostro elenco formatterà.
builder->get_ListFormat()->set_List(list2);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

builder->Writeln(u"Using list style second time:");

// Crea e applica un altro elenco basato sullo stile dell'elenco.
System::SharedPtr<Aspose::Words::Lists::List> list3 = doc->get_Lists()->Add(listStyle);
builder->get_ListFormat()->set_List(list3);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

builder->get_Document()->Save(get_ArtifactsDir() + u"Lists.CreateAndUseListStyle.docx");
```


Mostra come aggiungere un [Style](../../style/) alla collezione di stili di un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::StyleCollection> styles = doc->get_Styles();
// Imposta i parametri predefiniti per i nuovi stili che potremo aggiungere successivamente a questa collezione.
styles->get_DefaultFont()->set_Name(u"Courier New");
// Se aggiungiamo uno stile di "StyleType.Paragraph", la collezione applicherà i valori di
// la sua proprietà "DefaultParagraphFormat" alla proprietà "ParagraphFormat" dello stile.
styles->get_DefaultParagraphFormat()->set_FirstLineIndent(15.0);
// Aggiungi uno stile, quindi verifica che abbia le impostazioni predefinite.
styles->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");

ASSERT_EQ(u"Courier New", styles->idx_get(4)->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(15.0, styles->idx_get(u"MyStyle")->get_ParagraphFormat()->get_FirstLineIndent());
```

## Vedi anche

* Class [Style](../../style/)
* Enum [StyleType](../../styletype/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
