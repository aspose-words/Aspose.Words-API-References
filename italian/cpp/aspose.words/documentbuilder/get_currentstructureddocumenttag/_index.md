---
title: "Aspose::Words::DocumentBuilder::get_CurrentStructuredDocumentTag metodo"
linktitle: "get_CurrentStructuredDocumentTag"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::DocumentBuilder::get_CurrentStructuredDocumentTag metodo. Ottiene il tag di documento strutturato attualmente selezionato in questo DocumentBuilder in C++."
type: docs
weight: 15000
url: /it/cpp/aspose.words/documentbuilder/get_currentstructureddocumenttag/
---
## DocumentBuilder::get_CurrentStructuredDocumentTag method


Ottiene il tag di documento strutturato attualmente selezionato in questo [DocumentBuilder](../).

```cpp
System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> Aspose::Words::DocumentBuilder::get_CurrentStructuredDocumentTag()
```


## Esempi



Mostra come spostare il cursore di [DocumentBuilder](../) all'interno di un tag di documento strutturato.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Esistono diversi modi per spostare il cursore:
// 1 -  Spostati al primo carattere del tag di documento strutturato per indice.
builder->MoveToStructuredDocumentTag(1, 1);

// 2 -  Spostati al primo carattere del tag di documento strutturato per oggetto.
auto tag = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTag, 2, true));
builder->MoveToStructuredDocumentTag(tag, 1);
builder->Write(u" New text.");

ASSERT_EQ(u"R New text.ichText", tag->GetText().Trim());

// 3 -  Spostati alla fine del secondo tag di documento strutturato.
builder->MoveToStructuredDocumentTag(1, -1);
ASSERT_TRUE(builder->get_IsAtEndOfStructuredDocumentTag());

// Ottieni il tag di documento strutturato attualmente selezionato.
builder->get_CurrentStructuredDocumentTag()->set_Color(System::Drawing::Color::get_Green());

doc->Save(get_ArtifactsDir() + u"Document.MoveToStructuredDocumentTag.docx");
```

## Vedi anche

* Class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
