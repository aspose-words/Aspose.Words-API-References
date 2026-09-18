---
title: "Aspose::Words::DocumentBuilder::InsertHtml Methode"
linktitle: "InsertHtml"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentBuilder::InsertHtml Methode. Fügt einen HTML-String in das Dokument in C++ ein."
type: docs
weight: 37000
url: /de/cpp/aspose.words/documentbuilder/inserthtml/
---
## DocumentBuilder::InsertHtml(const System::String\&) method


Fügt eine HTML-Zeichenkette in das Dokument ein.

```cpp
void Aspose::Words::DocumentBuilder::InsertHtml(const System::String &html)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| html | const System::String\& | Ein HTML-String, der in das Dokument eingefügt werden soll. |

## Beispiele



Zeigt, wie man einen DocumentBuilder verwendet, um HTML-Inhalt in ein Dokument einzufügen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

const System::String html = System::String(u"<p align='right'>Paragraph right</p>") + u"<b>Implicit paragraph left</b>" + u"<div align='center'>Div center</div>" + u"<h1 align='left'>Heading 1 left.</h1>";

builder->InsertHtml(html);

// Das Einfügen von HTML-Code analysiert die Formatierung jedes Elements in eine äquivalente Dokumenttextformatierung.
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

## Siehe auch

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertHtml(const System::String\&, Aspose::Words::HtmlInsertOptions) method


Fügt eine HTML-Zeichenkette in das Dokument ein. Ermöglicht das Angeben zusätzlicher Optionen.

```cpp
void Aspose::Words::DocumentBuilder::InsertHtml(const System::String &html, Aspose::Words::HtmlInsertOptions options)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| html | const System::String\& | Ein HTML-String, der in das Dokument eingefügt werden soll. |
| options | Aspose::Words::HtmlInsertOptions | Optionen, die verwendet werden, wenn ein HTML-String eingefügt wird. |

## Siehe auch

* Enum [HtmlInsertOptions](../../htmlinsertoptions/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertHtml(const System::String\&, bool) method


Fügt eine HTML-Zeichenkette in das Dokument ein.

```cpp
void Aspose::Words::DocumentBuilder::InsertHtml(const System::String &html, bool useBuilderFormatting)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| html | const System::String\& | Ein HTML-String, der in das Dokument eingefügt werden soll. |
| useBuilderFormatting | bool | Ein Wert, der angibt, ob die im [DocumentBuilder](../) angegebene Formatierung als Basisformatierung für aus HTML importierten Text verwendet wird. |
## Hinweise


Sie können diese Methode verwenden, um ein HTML‑Fragment oder ein komplettes HTML‑Dokument einzufügen.

Wenn *useBuilderFormatting* **false** ist, wird die Formatierung des [DocumentBuilder](../) ignoriert und die Formatierung des eingefügten Textes basiert auf der Standard‑HTML‑Formatierung. Infolgedessen sieht der Text so aus, wie er in Browsern gerendert wird.

Wenn *useBuilderFormatting* **true** ist, basiert die Formatierung des eingefügten Textes auf der Formatierung des [DocumentBuilder](../), und der Text sieht so aus, als wäre er mit [Write()](../) eingefügt worden.

## Beispiele



Zeigt, wie die Formatierung des DocumentBuilder beim Einfügen von HTML‑Inhalten angewendet wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Legen Sie eine Textausrichtung für den Builder fest, fügen Sie einen HTML‑Absatz mit einer angegebenen Ausrichtung und einen ohne ein.
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Distributed);
builder->InsertHtml(System::String(u"<p align='right'>Paragraph 1.</p>") + u"<p>Paragraph 2.</p>", useBuilderFormatting);

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

// Der erste Absatz hat eine festgelegte Ausrichtung. Wenn InsertHtml den HTML‑Code analysiert,
// überschreibt der im HTML‑Code gefundene Absatzausrichtungswert stets den Wert des DocumentBuilder.
ASSERT_EQ(u"Paragraph 1.", paragraphs->idx_get(0)->GetText().Trim());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Right, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Alignment());

// Der zweite Absatz hat keine Ausrichtung angegeben. Er kann seinen Ausrichtungswert erhalten
// durch den Wert des Builders, abhängig von dem Flag, das wir an die InsertHtml‑Methode übergeben haben.
ASSERT_EQ(u"Paragraph 2.", paragraphs->idx_get(1)->GetText().Trim());
ASSERT_EQ(useBuilderFormatting ? Aspose::Words::ParagraphAlignment::Distributed : Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Alignment());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHtmlWithFormatting.docx");
```

## Siehe auch

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
