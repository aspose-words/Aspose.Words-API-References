---
title: "Aspose::Words::Range::Replace metodo"
linktitle: "Sostituisci"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Range::Replace metodo. Sostituisce tutte le occorrenze di un modello di caratteri specificato da un'espressione regolare con un'altra stringa in C++."
type: docs
weight: 12000
url: /it/cpp/aspose.words/range/replace/
---
## Range::Replace(const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


Sostituisce tutte le occorrenze di un modello di caratteri specificato da un'espressione regolare con un'altra stringa.

```cpp
int32_t Aspose::Words::Range::Replace(const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| modello | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Un modello di espressione regolare usato per trovare corrispondenze. |
| sostituzione | const System::String\& | Una stringa per sostituire tutte le occorrenze del modello. |

### ReturnValue

Il numero di sostituzioni effettuate.
## Note


Sostituisce l'intera corrispondenza catturata dall'espressione regolare.

Il metodo è in grado di gestire interruzioni sia nelle stringhe del modello che di sostituzione.

Dovresti usare meta-caratteri speciali se hai bisogno di lavorare con le interruzioni:

* **%&p** - paragraph break
* **%&b** - section break
* **%&m** - page break
* **%&l** - manual line break



## Esempi



Mostra come sostituire tutte le occorrenze di un modello di espressione regolare con altro testo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"I decided to get the curtains in gray, ideal for the grey-accented room.");

doc->get_Range()->Replace(System::MakeObject<System::Text::RegularExpressions::Regex>(u"gr(a|e)y"), u"lavender");

ASSERT_EQ(u"I decided to get the curtains in lavender, ideal for the lavender-accented room.", doc->GetText().Trim());
```

## Vedi anche

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Range::Replace(const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Sostituisce tutte le occorrenze di un modello di caratteri specificato da un'espressione regolare con un'altra stringa.

```cpp
int32_t Aspose::Words::Range::Replace(const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| modello | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Un modello di espressione regolare usato per trovare corrispondenze. |
| sostituzione | const System::String\& | Una stringa per sostituire tutte le occorrenze del modello. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | Oggetto [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) per specificare opzioni aggiuntive. |

### ReturnValue

Il numero di sostituzioni effettuate.
## Note


Sostituisce l'intera corrispondenza catturata dall'espressione regolare.

Il metodo è in grado di gestire interruzioni sia nelle stringhe del modello che di sostituzione.

Dovresti usare meta-caratteri speciali se hai bisogno di lavorare con le interruzioni:

* **%&p** - paragraph break
* **%&b** - section break
* **%&m** - page break
* **%&l** - manual line break
* **%&&** - & character



## Vedi anche

* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Range::Replace(const System::String\&, const System::String\&) method


Sostituisce tutte le occorrenze di un modello di stringa di caratteri specificato con una stringa di sostituzione.

```cpp
int32_t Aspose::Words::Range::Replace(const System::String &pattern, const System::String &replacement)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| modello | const System::String\& | Una stringa da sostituire. |
| sostituzione | const System::String\& | Una stringa per sostituire tutte le occorrenze del modello. |

### ReturnValue

Il numero di sostituzioni effettuate.
## Note


Il modello non verrà usato come espressione regolare. Si prega di utilizzare [Replace()](../) se sono necessarie espressioni regolari.

Utilizzata comparazione senza distinzione tra maiuscole e minuscole.

Il metodo è in grado di gestire interruzioni sia nelle stringhe del modello che di sostituzione.

Dovresti usare meta-caratteri speciali se hai bisogno di lavorare con le interruzioni:

* **%&p** - paragraph break
* **%&b** - section break
* **%&m** - page break
* **%&l** - manual line break



## Esempi



Mostra come eseguire un'operazione di ricerca e sostituzione del testo sul contenuto di un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Greetings, _FullName_!");

// Esegui un'operazione di ricerca e sostituzione sul contenuto del nostro documento e verifica il numero di sostituzioni effettuate.
int32_t replacementCount = doc->get_Range()->Replace(u"_FullName_", u"John Doe");

ASSERT_EQ(1, replacementCount);
ASSERT_EQ(u"Greetings, John Doe!", doc->GetText().Trim());
```


Mostra come aggiungere formattazione ai paragrafi in cui un'operazione di trova-e-sostituisci ha trovato corrispondenze.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Every paragraph that ends with a full stop like this one will be right aligned.");
builder->Writeln(u"This one will not!");
builder->Write(u"This one also will.");

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(2)->get_ParagraphFormat()->get_Alignment());

// Possiamo utilizzare un oggetto "FindReplaceOptions" per modificare il processo di ricerca e sostituzione.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Imposta la proprietà "Alignment" su "ParagraphAlignment.Right" per allineare a destra ogni paragrafo
// che contiene una corrispondenza trovata dall'operazione di trova-e-sostituisci.
options->get_ApplyParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Right);

// Sostituisci ogni punto fermo che si trova subito prima di un'interruzione di paragrafo con un punto esclamativo.
int32_t count = doc->get_Range()->Replace(u".&p", u"!&p", options);

ASSERT_EQ(2, count);
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Right, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Right, paragraphs->idx_get(2)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(System::String(u"Every paragraph that ends with a full stop like this one will be right aligned!\r") + u"This one will not!\r" + u"This one also will!", doc->GetText().Trim());
```

## Vedi anche

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Range::Replace(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Sostituisce tutte le occorrenze di un modello di stringa di caratteri specificato con una stringa di sostituzione.

```cpp
int32_t Aspose::Words::Range::Replace(const System::String &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| modello | const System::String\& | Una stringa da sostituire. |
| sostituzione | const System::String\& | Una stringa per sostituire tutte le occorrenze del modello. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | Oggetto [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) per specificare opzioni aggiuntive. |

### ReturnValue

Il numero di sostituzioni effettuate.
## Note


Il modello non verrà usato come espressione regolare. Si prega di utilizzare [Replace()](../) se sono necessarie espressioni regolari.

Il metodo è in grado di gestire interruzioni sia nelle stringhe del modello che di sostituzione.

Dovresti usare meta-caratteri speciali se hai bisogno di lavorare con le interruzioni:

* **%&p** - paragraph break
* **%&b** - section break
* **%&m** - page break
* **%&l** - manual line break
* **%&&** - & character



## Esempi



Mostra come sostituire il testo nel piè di pagina di un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footer.docx");

System::SharedPtr<Aspose::Words::HeaderFooterCollection> headersFooters = doc->get_FirstSection()->get_HeadersFooters();
System::SharedPtr<Aspose::Words::HeaderFooter> footer = headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary);

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_MatchCase(false);
options->set_FindWholeWordsOnly(false);

int32_t currentYear = System::DateTime::get_Now().get_Year();
footer->get_Range()->Replace(u"(C) 2006 Aspose Pty Ltd.", System::String::Format(u"Copyright (C) {0} by Aspose Pty Ltd.", currentYear), options);

doc->Save(get_ArtifactsDir() + u"HeaderFooter.ReplaceText.docx");
```


Mostra come attivare/disattivare la sensibilità al maiuscolo/minuscolo durante un'operazione di ricerca e sostituzione.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Ruby bought a ruby necklace.");

// Possiamo utilizzare un oggetto "FindReplaceOptions" per modificare il processo di ricerca e sostituzione.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Imposta il flag "MatchCase" su "true" per applicare la sensibilità al maiuscolo/minuscolo durante la ricerca delle stringhe da sostituire.
// Imposta il flag "MatchCase" su "false" per ignorare le differenze di maiuscole/minuscole durante la ricerca del testo da sostituire.
options->set_MatchCase(matchCase);

doc->get_Range()->Replace(u"Ruby", u"Jade", options);

ASSERT_EQ(matchCase ? System::String(u"Jade bought a ruby necklace.") : System::String(u"Jade bought a Jade necklace."), doc->GetText().Trim());
```


Mostra come attivare/disattivare le operazioni di ricerca e sostituzione limitate a parole isolate.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Jackson will meet you in Jacksonville.");

// Possiamo utilizzare un oggetto "FindReplaceOptions" per modificare il processo di ricerca e sostituzione.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Imposta il flag "FindWholeWordsOnly" su "true" per sostituire il testo trovato se non fa parte di un'altra parola.
// Imposta il flag "FindWholeWordsOnly" su "false" per sostituire tutto il testo indipendentemente dal contesto.
options->set_FindWholeWordsOnly(findWholeWordsOnly);

doc->get_Range()->Replace(u"Jackson", u"Louis", options);

ASSERT_EQ(findWholeWordsOnly ? System::String(u"Louis will meet you in Jacksonville.") : System::String(u"Louis will meet you in Louisville."), doc->GetText().Trim());
```


Mostra come sostituire tutte le istanze di una stringa di testo in una tabella e cella.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Carrots");
builder->InsertCell();
builder->Write(u"50");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Potatoes");
builder->InsertCell();
builder->Write(u"50");
builder->EndTable();

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_MatchCase(true);
options->set_FindWholeWordsOnly(true);

// Esegui un'operazione di ricerca e sostituzione su un'intera tabella.
table->get_Range()->Replace(u"Carrots", u"Eggs", options);

// Esegui un'operazione di ricerca e sostituzione sull'ultima cella dell'ultima riga della tabella.
table->get_LastRow()->get_LastCell()->get_Range()->Replace(u"50", u"20", options);

ASSERT_EQ(System::String(u"Eggs\a50\a\a") + u"Potatoes\a20\a\a", table->GetText().Trim());
```

## Vedi anche

* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
