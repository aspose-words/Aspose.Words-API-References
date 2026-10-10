---
title: "Enum Aspose::Words::Lists::ListTrailingCharacter"
linktitle: "ListTrailingCharacter"
second_title: "Riferimento API Aspose.Words per C++"
description: "Enum Aspose::Words::Lists::ListTrailingCharacter. Specifica il carattere che separa l'etichetta dell'elenco dal testo del paragrafo in C++."
type: docs
weight: 9000
url: /it/cpp/aspose.words.lists/listtrailingcharacter/
---
## ListTrailingCharacter enum


Specifica il carattere che separa l'etichetta dell'elenco dal testo del paragrafo.

```cpp
enum class ListTrailingCharacter
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Tab | 0 | Un carattere di tabulazione è posizionato tra l'etichetta dell'elenco e il testo del paragrafo. |
| Spazio | 1 | Un carattere di spazio è posizionato tra l'etichetta dell'elenco e il testo del paragrafo. |
| Niente | 2 | Non c'è alcun carattere separatore tra l'etichetta dell'elenco e il testo del paragrafo. |

## Note


Usato come valore per la proprietà [TrailingCharacter](../listlevel/get_trailingcharacter/).

## Esempi



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

## Vedi anche

* Namespace [Aspose::Words::Lists](../)
* Library [Aspose.Words for C++](../../)
