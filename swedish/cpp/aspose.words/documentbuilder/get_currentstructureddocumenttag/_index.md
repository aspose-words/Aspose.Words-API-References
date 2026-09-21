---
title: "Aspose::Words::DocumentBuilder::get_CurrentStructuredDocumentTag‑metod"
linktitle: "get_CurrentStructuredDocumentTag"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DocumentBuilder::get_CurrentStructuredDocumentTag‑metod. Hämtar den strukturerade dokumenttaggen som för närvarande är markerad i denna DocumentBuilder i C++."
type: docs
weight: 15000
url: /sv/cpp/aspose.words/documentbuilder/get_currentstructureddocumenttag/
---
## DocumentBuilder::get_CurrentStructuredDocumentTag method


Hämtar den strukturerade dokumenttaggen som för närvarande är markerad i denna [DocumentBuilder](../).

```cpp
System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> Aspose::Words::DocumentBuilder::get_CurrentStructuredDocumentTag()
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

* Class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
