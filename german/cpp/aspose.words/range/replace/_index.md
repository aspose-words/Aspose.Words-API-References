---
title: "Aspose::Words::Range::Replace-Methode"
linktitle: "Ersetzen"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Range::Replace-Methode. Ersetzt alle Vorkommen eines Zeichenmusters, das durch einen regulären Ausdruck angegeben ist, durch einen anderen String in C++."
type: docs
weight: 12000
url: /de/cpp/aspose.words/range/replace/
---
## Range::Replace(const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


Ersetzt alle Vorkommen eines durch einen regulären Ausdruck angegebenen Zeichenmusters durch eine andere Zeichenfolge.

```cpp
int32_t Aspose::Words::Range::Replace(const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Muster | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Ein reguläres Ausdrucksmuster, das zum Finden von Übereinstimmungen verwendet wird. |
| Ersetzung | const System::String\& | Ein String, um alle Vorkommen des Musters zu ersetzen. |

### ReturnValue

Die Anzahl der vorgenommenen Ersetzungen.
## Hinweise


Ersetzt das gesamte vom regulären Ausdruck erfasste Match.

Die Methode kann Zeilenumbrüche sowohl im Muster- als auch im Ersetzungsstring verarbeiten.

Sie sollten spezielle Metazeichen verwenden, wenn Sie mit Zeilenumbrüchen arbeiten müssen:

* **%&p** - paragraph break
* **%&b** - section break
* **%&m** - page break
* **%&l** - manual line break



## Beispiele



Zeigt, wie man alle Vorkommen eines regulären Ausdrucksmusters durch anderen Text ersetzt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"I decided to get the curtains in gray, ideal for the grey-accented room.");

doc->get_Range()->Replace(System::MakeObject<System::Text::RegularExpressions::Regex>(u"gr(a|e)y"), u"lavender");

ASSERT_EQ(u"I decided to get the curtains in lavender, ideal for the lavender-accented room.", doc->GetText().Trim());
```

## Siehe auch

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Range::Replace(const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Ersetzt alle Vorkommen eines durch einen regulären Ausdruck angegebenen Zeichenmusters durch eine andere Zeichenfolge.

```cpp
int32_t Aspose::Words::Range::Replace(const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Muster | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Ein reguläres Ausdrucksmuster, das zum Finden von Übereinstimmungen verwendet wird. |
| Ersetzung | const System::String\& | Ein String, um alle Vorkommen des Musters zu ersetzen. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)-Objekt, um zusätzliche Optionen anzugeben. |

### ReturnValue

Die Anzahl der vorgenommenen Ersetzungen.
## Hinweise


Ersetzt das gesamte vom regulären Ausdruck erfasste Match.

Die Methode kann Zeilenumbrüche sowohl im Muster- als auch im Ersetzungsstring verarbeiten.

Sie sollten spezielle Metazeichen verwenden, wenn Sie mit Zeilenumbrüchen arbeiten müssen:

* **%&p** - paragraph break
* **%&b** - section break
* **%&m** - page break
* **%&l** - manual line break
* **%&&** - & character



## Siehe auch

* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Range::Replace(const System::String\&, const System::String\&) method


Ersetzt alle Vorkommen eines angegebenen Zeichenfolgenmusters durch eine Ersatzzeichenfolge.

```cpp
int32_t Aspose::Words::Range::Replace(const System::String &pattern, const System::String &replacement)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Muster | const System::String\& | Ein zu ersetzender String. |
| Ersetzung | const System::String\& | Ein String, um alle Vorkommen des Musters zu ersetzen. |

### ReturnValue

Die Anzahl der vorgenommenen Ersetzungen.
## Hinweise


Das Muster wird nicht als regulärer Ausdruck verwendet. Bitte verwenden Sie [Replace()](../), wenn Sie reguläre Ausdrücke benötigen.

Verwendet einen Vergleich ohne Groß-/Kleinschreibung.

Die Methode kann Zeilenumbrüche sowohl im Muster- als auch im Ersetzungsstring verarbeiten.

Sie sollten spezielle Metazeichen verwenden, wenn Sie mit Zeilenumbrüchen arbeiten müssen:

* **%&p** - paragraph break
* **%&b** - section break
* **%&m** - page break
* **%&l** - manual line break



## Beispiele



Zeigt, wie man eine Suchen‑und‑Ersetzen‑Textoperation am Inhalt eines Dokuments durchführt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Greetings, _FullName_!");

// Führen Sie eine Suchen‑und‑Ersetzen‑Operation am Inhalt unseres Dokuments durch und überprüfen Sie die Anzahl der vorgenommenen Ersetzungen.
int32_t replacementCount = doc->get_Range()->Replace(u"_FullName_", u"John Doe");

ASSERT_EQ(1, replacementCount);
ASSERT_EQ(u"Greetings, John Doe!", doc->GetText().Trim());
```


Zeigt, wie man Formatierungen zu Absätzen hinzufügt, in denen ein Suchen‑und‑Ersetzen‑Vorgang Treffer gefunden hat.
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

// Wir können ein "FindReplaceOptions"‑Objekt verwenden, um den Suchen‑und‑Ersetzen‑Vorgang zu ändern.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Setzen Sie die Eigenschaft "Alignment" auf "ParagraphAlignment.Right", um jeden Absatz rechtsbündig auszurichten.
// die einen Treffer enthält, den der Suchen‑und‑Ersetzen‑Vorgang findet.
options->get_ApplyParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Right);

// Ersetzen Sie jeden Punkt, der unmittelbar vor einem Absatzumbruch steht, durch ein Ausrufezeichen.
int32_t count = doc->get_Range()->Replace(u".&p", u"!&p", options);

ASSERT_EQ(2, count);
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Right, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Right, paragraphs->idx_get(2)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(System::String(u"Every paragraph that ends with a full stop like this one will be right aligned!\r") + u"This one will not!\r" + u"This one also will!", doc->GetText().Trim());
```

## Siehe auch

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Range::Replace(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Ersetzt alle Vorkommen eines angegebenen Zeichenfolgenmusters durch eine Ersatzzeichenfolge.

```cpp
int32_t Aspose::Words::Range::Replace(const System::String &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Muster | const System::String\& | Ein zu ersetzender String. |
| Ersetzung | const System::String\& | Ein String, um alle Vorkommen des Musters zu ersetzen. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)-Objekt, um zusätzliche Optionen anzugeben. |

### ReturnValue

Die Anzahl der vorgenommenen Ersetzungen.
## Hinweise


Das Muster wird nicht als regulärer Ausdruck verwendet. Bitte verwenden Sie [Replace()](../), wenn Sie reguläre Ausdrücke benötigen.

Die Methode kann Zeilenumbrüche sowohl im Muster- als auch im Ersetzungsstring verarbeiten.

Sie sollten spezielle Metazeichen verwenden, wenn Sie mit Zeilenumbrüchen arbeiten müssen:

* **%&p** - paragraph break
* **%&b** - section break
* **%&m** - page break
* **%&l** - manual line break
* **%&&** - & character



## Beispiele



Zeigt, wie man Text in der Fußzeile eines Dokuments ersetzt.
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


Zeigt, wie die Groß‑/Kleinschreibung bei einer Suchen‑und‑Ersetzen‑Operation umgeschaltet wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Ruby bought a ruby necklace.");

// Wir können ein "FindReplaceOptions"‑Objekt verwenden, um den Suchen‑und‑Ersetzen‑Vorgang zu ändern.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Setzen Sie das "MatchCase"‑Flag auf "true", um bei der Suche nach zu ersetzenden Zeichenketten die Groß‑/Kleinschreibung zu berücksichtigen.
// Setzen Sie das "MatchCase"‑Flag auf "false", um die Groß‑/Kleinschreibung bei der Suche nach zu ersetzendem Text zu ignorieren.
options->set_MatchCase(matchCase);

doc->get_Range()->Replace(u"Ruby", u"Jade", options);

ASSERT_EQ(matchCase ? System::String(u"Jade bought a ruby necklace.") : System::String(u"Jade bought a Jade necklace."), doc->GetText().Trim());
```


Zeigt, wie man eigenständige wort‑nur‑Suchen‑und‑Ersetzen‑Operationen umschaltet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Jackson will meet you in Jacksonville.");

// Wir können ein "FindReplaceOptions"‑Objekt verwenden, um den Suchen‑und‑Ersetzen‑Vorgang zu ändern.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Setzen Sie das Flag "FindWholeWordsOnly" auf "true", um den gefundenen Text zu ersetzen, wenn er nicht Teil eines anderen Wortes ist.
// Setzen Sie das Flag "FindWholeWordsOnly" auf "false", um allen Text zu ersetzen, unabhängig von seiner Umgebung.
options->set_FindWholeWordsOnly(findWholeWordsOnly);

doc->get_Range()->Replace(u"Jackson", u"Louis", options);

ASSERT_EQ(findWholeWordsOnly ? System::String(u"Louis will meet you in Jacksonville.") : System::String(u"Louis will meet you in Louisville."), doc->GetText().Trim());
```


Zeigt, wie man alle Instanzen von String von Text in einer Tabelle und Zelle ersetzt.
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

// Führen Sie eine Suchen‑und‑Ersetzen‑Operation für eine gesamte Tabelle durch.
table->get_Range()->Replace(u"Carrots", u"Eggs", options);

// Führen Sie eine Suchen‑und‑Ersetzen‑Operation für die letzte Zelle der letzten Zeile der Tabelle durch.
table->get_LastRow()->get_LastCell()->get_Range()->Replace(u"50", u"20", options);

ASSERT_EQ(System::String(u"Eggs\a50\a\a") + u"Potatoes\a20\a\a", table->GetText().Trim());
```

## Siehe auch

* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
