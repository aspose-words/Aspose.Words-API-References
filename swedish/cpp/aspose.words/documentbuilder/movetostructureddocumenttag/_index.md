---
title: "Aspose::Words::DocumentBuilder::MoveToStructuredDocumentTag metod"
linktitle: "MoveToStructuredDocumentTag"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DocumentBuilder::MoveToStructuredDocumentTag metod. Flyttar markören till den strukturerade dokumenttaggen i C++."
type: docs
weight: 61000
url: /sv/cpp/aspose.words/documentbuilder/movetostructureddocumenttag/
---
## DocumentBuilder::MoveToStructuredDocumentTag(const System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTag\>\&, int32_t) method


Flyttar markören till den strukturerade dokumenttaggen.

```cpp
void Aspose::Words::DocumentBuilder::MoveToStructuredDocumentTag(const System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> &structuredDocumentTag, int32_t characterIndex)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| structuredDocumentTag | const System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTag\>\& | Den strukturerade dokumenttaggen att flytta till. |
| characterIndex | int32_t | Indexet för tecknet i den strukturerade dokumenttaggen. Ett negativt värde låter dig ange en position från slutet av den strukturerade dokumenttaggen. Använd -1 för att flytta till slutet av den strukturerade dokumenttaggen. Om den strukturerade dokumenttaggen är på blocknivå och du vill flytta markören till slutet av dess sista stycke, ange -2. |

## Exempel



Visar hur man flyttar markören för [DocumentBuilder](../) inuti en strukturerad dokumenttagg.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Det finns flera sätt att flytta markören:
// 1 -  Flytta till det första tecknet i den strukturerade dokumenttaggen enligt index.
builder->MoveToStructuredDocumentTag(1, 1);

// 2 -  Flytta till det första tecknet i den strukturerade dokumenttaggen enligt objekt.
auto tag = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTag, 2, true));
builder->MoveToStructuredDocumentTag(tag, 1);
builder->Write(u" New text.");

ASSERT_EQ(u"R New text.ichText", tag->GetText().Trim());

// 3 -  Flytta till slutet av den andra strukturerade dokumenttaggen.
builder->MoveToStructuredDocumentTag(1, -1);
ASSERT_TRUE(builder->get_IsAtEndOfStructuredDocumentTag());

// Hämta för närvarande markerad strukturerad dokumenttagg.
builder->get_CurrentStructuredDocumentTag()->set_Color(System::Drawing::Color::get_Green());

doc->Save(get_ArtifactsDir() + u"Document.MoveToStructuredDocumentTag.docx");
```

## Se även

* Class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::MoveToStructuredDocumentTag(int32_t, int32_t) method


Flyttar markören till en strukturerad dokumenttagg i den aktuella sektionen.

```cpp
void Aspose::Words::DocumentBuilder::MoveToStructuredDocumentTag(int32_t structuredDocumentTagIndex, int32_t characterIndex)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| structuredDocumentTagIndex | int32_t | Indexet för den strukturerade dokumenttaggen att flytta till. |
| characterIndex | int32_t | Indexet för tecknet i den strukturerade dokumenttaggen. Ett negativt värde låter dig ange en position från slutet av den strukturerade dokumenttaggen. Använd -1 för att flytta till slutet av den strukturerade dokumenttaggen. Om den strukturerade dokumenttaggen är på blocknivå och du vill flytta markören till slutet av dess sista stycke, ange -2. |
## Anmärkningar


Navigeringen utförs inom den aktuella berättelsen i den aktuella sektionen. Det vill säga, om du flyttade markören till det primära sidhuvudet i den första sektionen, så specificerade *structuredDocumentTagIndex* indexet för den strukturerade dokumenttaggen i det sidhuvudet i den sektionen.

När *structuredDocumentTagIndex* är större än eller lika med 0, specificerar den ett index från början av sektionen där 0 är den första strukturerade dokumenttaggen. När *structuredDocumentTagIndex* är mindre än 0, specificerar den ett index från slutet av sektionen där -1 är den sista strukturerade dokumenttaggen.

## Exempel



Visar hur man flyttar markören för [DocumentBuilder](../) inuti en strukturerad dokumenttagg.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Det finns flera sätt att flytta markören:
// 1 -  Flytta till det första tecknet i den strukturerade dokumenttaggen enligt index.
builder->MoveToStructuredDocumentTag(1, 1);

// 2 -  Flytta till det första tecknet i den strukturerade dokumenttaggen enligt objekt.
auto tag = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTag, 2, true));
builder->MoveToStructuredDocumentTag(tag, 1);
builder->Write(u" New text.");

ASSERT_EQ(u"R New text.ichText", tag->GetText().Trim());

// 3 -  Flytta till slutet av den andra strukturerade dokumenttaggen.
builder->MoveToStructuredDocumentTag(1, -1);
ASSERT_TRUE(builder->get_IsAtEndOfStructuredDocumentTag());

// Hämta för närvarande markerad strukturerad dokumenttagg.
builder->get_CurrentStructuredDocumentTag()->set_Color(System::Drawing::Color::get_Green());

doc->Save(get_ArtifactsDir() + u"Document.MoveToStructuredDocumentTag.docx");
```

## Se även

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
