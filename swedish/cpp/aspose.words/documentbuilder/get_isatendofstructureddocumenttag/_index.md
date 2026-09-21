---
title: "Aspose::Words::DocumentBuilder::get_IsAtEndOfStructuredDocumentTag method"
linktitle: "get_IsAtEndOfStructuredDocumentTag"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DocumentBuilder::get_IsAtEndOfStructuredDocumentTag‑metod. Returnerar true om markören är i slutet av en strukturerad dokumenttagg i C++."
type: docs
weight: 19000
url: /sv/cpp/aspose.words/documentbuilder/get_isatendofstructureddocumenttag/
---
## DocumentBuilder::get_IsAtEndOfStructuredDocumentTag method


Returnerar **true** om markören är i slutet av en strukturerad dokumenttagg.

```cpp
bool Aspose::Words::DocumentBuilder::get_IsAtEndOfStructuredDocumentTag()
```


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
