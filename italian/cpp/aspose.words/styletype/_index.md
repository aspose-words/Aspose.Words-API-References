---
title: "Aspose::Words::StyleType enum"
linktitle: "StyleType"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::StyleType enum. Rappresenta il tipo di stile in C++."
type: docs
weight: 119000
url: /it/cpp/aspose.words/styletype/
---
## StyleType enum


Rappresenta il tipo di stile.

```cpp
enum class StyleType
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Paragraph | 1 | Lo stile è uno stile di paragrafo. |
| Character | 2 | Lo stile è uno stile di carattere. |
| Table | 3 | Lo stile è uno stile di tabella. |
| Elenco | 4 | Lo stile è uno stile di elenco. |


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

## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
