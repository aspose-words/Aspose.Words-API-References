---
title: "Aspose::Words::DocumentBuilder::InsertHtml metod"
linktitle: "InsertHtml"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DocumentBuilder::InsertHtml metod. Infogar en HTML‑sträng i dokumentet i C++."
type: docs
weight: 37000
url: /sv/cpp/aspose.words/documentbuilder/inserthtml/
---
## DocumentBuilder::InsertHtml(const System::String\&) method


Infogar en HTML-sträng i dokumentet.

```cpp
void Aspose::Words::DocumentBuilder::InsertHtml(const System::String &html)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| html | const System::String\& | En HTML‑sträng att infoga i dokumentet. |

## Exempel



Visar hur man använder en dokumentbyggare för att infoga html‑innehåll i ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

const System::String html = System::String(u"<p align='right'>Paragraph right</p>") + u"<b>Implicit paragraph left</b>" + u"<div align='center'>Div center</div>" + u"<h1 align='left'>Heading 1 left.</h1>";

builder->InsertHtml(html);

// Infogning av HTML‑kod analyserar formateringen av varje element till motsvarande dokumenttextformatering.
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

## Se även

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertHtml(const System::String\&, Aspose::Words::HtmlInsertOptions) method


Infogar en HTML-sträng i dokumentet. Tillåter att ange ytterligare alternativ.

```cpp
void Aspose::Words::DocumentBuilder::InsertHtml(const System::String &html, Aspose::Words::HtmlInsertOptions options)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| html | const System::String\& | En HTML‑sträng att infoga i dokumentet. |
| options | Aspose::Words::HtmlInsertOptions | Alternativ som används när en HTML‑sträng infogas. |

## Se även

* Enum [HtmlInsertOptions](../../htmlinsertoptions/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertHtml(const System::String\&, bool) method


Infogar en HTML-sträng i dokumentet.

```cpp
void Aspose::Words::DocumentBuilder::InsertHtml(const System::String &html, bool useBuilderFormatting)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| html | const System::String\& | En HTML‑sträng att infoga i dokumentet. |
| useBuilderFormatting | bool | Ett värde som anger om formatering som specificerats i [DocumentBuilder](../) används som grundformatering för text som importeras från HTML. |
## Anmärkningar


Du kan använda denna metod för att infoga ett HTML‑fragment eller ett helt HTML‑dokument.

När *useBuilderFormatting* är **false**, ignoreras formateringen i [DocumentBuilder](../) och formateringen av den infogade texten baseras på standard‑HTML‑formatering. Som ett resultat ser texten ut som den renderas i webbläsare.

När *useBuilderFormatting* är **true**, baseras formateringen av den infogade texten på formateringen i [DocumentBuilder](../), och texten ser ut som om den hade infogats med [Write()](../).

## Exempel



Visar hur man tillämpar en dokumentbyggares formatering när man infogar HTML-innehåll.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ställ in en textjustering för byggaren, infoga ett HTML-paragraf med en specificerad justering och ett utan.
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Distributed);
builder->InsertHtml(System::String(u"<p align='right'>Paragraph 1.</p>") + u"<p>Paragraph 2.</p>", useBuilderFormatting);

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

// Det första stycket har en specificerad justering. När InsertHtml analyserar HTML-koden,
// värdet för styckets justering som hittas i HTML-koden har alltid företräde framför dokumentbyggarens värde.
ASSERT_EQ(u"Paragraph 1.", paragraphs->idx_get(0)->GetText().Trim());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Right, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Alignment());

// Det andra stycket har ingen justering specificerad. Det kan få sitt justeringsvärde ifyllt
// av byggarens värde beroende på flaggan vi skickade till InsertHtml‑metoden.
ASSERT_EQ(u"Paragraph 2.", paragraphs->idx_get(1)->GetText().Trim());
ASSERT_EQ(useBuilderFormatting ? Aspose::Words::ParagraphAlignment::Distributed : Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Alignment());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHtmlWithFormatting.docx");
```

## Se även

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
