---
title: "Metodo Aspose::Words::Paragraph::JoinRunsWithSameFormatting"
linktitle: "JoinRunsWithSameFormatting"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Paragraph::JoinRunsWithSameFormatting. Unisce le run con la stessa formattazione nel paragrafo in C++."
type: docs
weight: 31000
url: /it/cpp/aspose.words/paragraph/joinrunswithsameformatting/
---
## Paragraph::JoinRunsWithSameFormatting() method


Unisce le run con la stessa formattazione nel paragrafo.

```cpp
int32_t Aspose::Words::Paragraph::JoinRunsWithSameFormatting()
```


### ReturnValue

Numero di unioni eseguite. Quando **N** run adiacenti vengono unite, contano come **N - 1** unioni.

## Esempi



Mostra come semplificare i paragrafi unendo le run superflue.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci quattro run di testo nel paragrafo.
builder->Write(u"Run 1. ");
builder->Write(u"Run 2. ");
builder->Write(u"Run 3. ");
builder->Write(u"Run 4. ");

// Se apriamo questo documento in Microsoft Word, il paragrafo apparirà come un unico corpo di testo continuo.
// Tuttavia, sarà composto da quattro run separate con la stessa formattazione. Paragrafi frammentati come questo
// possono verificarsi quando modifichiamo manualmente parti di un paragrafo più volte in Microsoft Word.
System::SharedPtr<Aspose::Words::Paragraph> para = builder->get_CurrentParagraph();

ASSERT_EQ(4, para->get_Runs()->get_Count());

// Cambia lo stile dell'ultima run per distinguerla dalle prime tre.
para->get_Runs()->idx_get(3)->get_Font()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Emphasis);

// Possiamo eseguire il metodo "JoinRunsWithSameFormatting" per ottimizzare il contenuto del documento
// unendo run simili in una sola, riducendone il numero complessivo.
// Questo metodo restituisce anche il numero di run che ha unito.
// Queste due unioni sono avvenute per combinare le Run #1, #2 e #3,
// escludendo Run #4 perché ha uno stile incompatibile.
ASSERT_EQ(2, para->JoinRunsWithSameFormatting());

// Il numero di run rimanenti sarà uguale al conteggio originale
// meno il numero di unioni di run che il metodo "JoinRunsWithSameFormatting" ha eseguito.
ASSERT_EQ(2, para->get_Runs()->get_Count());
ASSERT_EQ(u"Run 1. Run 2. Run 3. ", para->get_Runs()->idx_get(0)->get_Text());
ASSERT_EQ(u"Run 4. ", para->get_Runs()->idx_get(1)->get_Text());
```

## Vedi anche

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Paragraph::JoinRunsWithSameFormatting(const System::SharedPtr\<Aspose::Words::JoinRunsOptions\>\&) method


Unisce le run con la stessa formattazione nel paragrafo.

```cpp
int32_t Aspose::Words::Paragraph::JoinRunsWithSameFormatting(const System::SharedPtr<Aspose::Words::JoinRunsOptions> &options)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| opzioni | const System::SharedPtr\<Aspose::Words::JoinRunsOptions\>\& | Opzioni aggiuntive |

### ReturnValue

Numero di unioni eseguite. Quando **N** run adiacenti vengono unite, contano come **N - 1** unioni.

## Esempi



Mostra come unire le sequenze con la stessa formattazione ignorando gli attributi ridondanti e insignificanti.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Crea sequenze con formattazione visibile identica ma con alcune differenze interne.
builder->get_Font()->set_Name(u"Arial");
builder->get_Font()->set_Size(12);
builder->Write(u"Hello ");
builder->Write(u"world");

// Verifica le sequenze prima dell'unione.
ASSERT_EQ(2, doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->get_Count());
ASSERT_EQ(u"Hello ", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Text());
ASSERT_EQ(u"world", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(1)->get_Text());

// Configura le opzioni per ignorare gli attributi ridondanti e insignificanti durante l'unione.
auto options = System::MakeObject<Aspose::Words::JoinRunsOptions>();
options->set_IgnoreRedundant(true);
// Ignora le proprietà ridondanti delle sequenze che non influenzano l'aspetto.
options->set_IgnoreInsignificant(true);
// Ignora le differenze insignificanti come le sequenze composte solo da spazi bianchi.

// Unisci le sequenze che hanno la stessa formattazione visibile utilizzando le opzioni estese.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->JoinRunsWithSameFormatting(options);

// Verifica che le sequenze siano state unite correttamente.
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->get_Count());
ASSERT_EQ(u"Hello world", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Text());

doc->Save(get_ArtifactsDir() + u"Paragraph.JoinRunsWithSameFormattingWithOptions.docx");
```

## Vedi anche

* Class [JoinRunsOptions](../../joinrunsoptions/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
