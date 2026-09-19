---
title: "Aspose::Words::DocumentBuilder::InsertHtml metodo"
linktitle: "InsertHtml"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::DocumentBuilder::InsertHtml metodo. Inserisce una stringa HTML nel documento in C++."
type: docs
weight: 37000
url: /it/cpp/aspose.words/documentbuilder/inserthtml/
---
## DocumentBuilder::InsertHtml(const System::String\&) method


Inserisce una stringa HTML nel documento.

```cpp
void Aspose::Words::DocumentBuilder::InsertHtml(const System::String &html)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| html | const System::String\& | Una stringa HTML da inserire nel documento. |

## Esempi



Mostra come utilizzare un document builder per inserire contenuto html in un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

const System::String html = System::String(u"<p align='right'>Paragraph right</p>") + u"<b>Implicit paragraph left</b>" + u"<div align='center'>Div center</div>" + u"<h1 align='left'>Heading 1 left.</h1>";

builder->InsertHtml(html);

// L'inserimento di codice HTML analizza la formattazione di ogni elemento trasformandola in una formattazione testuale equivalente nel documento.
System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

ASSERT_EQ(u"Paragraph right", paragraphs->idx_get(0)->GetText().Trim());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Right, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Alignment());

ASSERT_EQ(u"Implicit paragraph left", paragraphs->idx_get(1)->GetText().Trim());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Alignment());
ASSERT_TRUE(paragraphs->idx_get(1)->get_Runs()->idx_get(0)->get_Font()->get_Bold());

ASSERT_EQ(u"Div center", paragraphs->idx_get(2)->GetText().Trim());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Center, paragraphs->idx_get(2)->get_ParagraphFormat()->get_Alignment());

ASSERT_EQ(u"Heading 1 left.", paragraphs->idx_get(3)->GetText().Trim());
ASSERT_EQ(u"Heading 1", paragraphs->idx_get(3)->get_ParagraphFormat()->get_Style()->get_Name());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHtml.docx");
```

## Vedi anche

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertHtml(const System::String\&, Aspose::Words::HtmlInsertOptions) method


Inserisce una stringa HTML nel documento. Consente di specificare opzioni aggiuntive.

```cpp
void Aspose::Words::DocumentBuilder::InsertHtml(const System::String &html, Aspose::Words::HtmlInsertOptions options)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| html | const System::String\& | Una stringa HTML da inserire nel documento. |
| opzioni | Aspose::Words::HtmlInsertOptions | Opzioni utilizzate quando viene inserita una stringa HTML. |

## Vedi anche

* Enum [HtmlInsertOptions](../../htmlinsertoptions/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertHtml(const System::String\&, bool) method


Inserisce una stringa HTML nel documento.

```cpp
void Aspose::Words::DocumentBuilder::InsertHtml(const System::String &html, bool useBuilderFormatting)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| html | const System::String\& | Una stringa HTML da inserire nel documento. |
| useBuilderFormatting | bool | Un valore che indica se la formattazione specificata in [DocumentBuilder](../) viene utilizzata come formattazione di base per il testo importato da HTML. |
## Note


Puoi utilizzare questo metodo per inserire un frammento HTML o un intero documento HTML.

Quando *useBuilderFormatting* è **false**, la formattazione di [DocumentBuilder](../) viene ignorata e la formattazione del testo inserito si basa sulla formattazione HTML predefinita. Di conseguenza, il testo appare come viene renderizzato nei browser.

Quando *useBuilderFormatting* è **true**, la formattazione del testo inserito si basa sulla formattazione di [DocumentBuilder](../) e il testo appare come se fosse stato inserito con [Write()](../).

## Esempi



Mostra come applicare la formattazione di un document builder durante l'inserimento di contenuto HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Imposta un allineamento del testo per il builder, inserisci un paragrafo HTML con un allineamento specificato e uno senza.
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Distributed);
builder->InsertHtml(System::String(u"<p align='right'>Paragraph 1.</p>") + u"<p>Paragraph 2.</p>", useBuilderFormatting);

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

// Il primo paragrafo ha un allineamento specificato. Quando InsertHtml analizza il codice HTML,
// il valore di allineamento del paragrafo trovato nel codice HTML sovrascrive sempre il valore del document builder.
ASSERT_EQ(u"Paragraph 1.", paragraphs->idx_get(0)->GetText().Trim());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Right, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Alignment());

// Il secondo paragrafo non ha alcun allineamento specificato. Può avere il suo valore di allineamento riempito
// dal valore del builder a seconda della flag che abbiamo passato al metodo InsertHtml.
ASSERT_EQ(u"Paragraph 2.", paragraphs->idx_get(1)->GetText().Trim());
ASSERT_EQ(useBuilderFormatting ? Aspose::Words::ParagraphAlignment::Distributed : Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Alignment());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHtmlWithFormatting.docx");
```

## Vedi anche

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
