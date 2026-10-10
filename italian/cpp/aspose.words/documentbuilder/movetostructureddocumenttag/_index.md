---
title: "Aspose::Words::DocumentBuilder::MoveToStructuredDocumentTag metodo"
linktitle: "MoveToStructuredDocumentTag"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::DocumentBuilder::MoveToStructuredDocumentTag metodo. Sposta il cursore al tag di documento strutturato in C++."
type: docs
weight: 61000
url: /it/cpp/aspose.words/documentbuilder/movetostructureddocumenttag/
---
## DocumentBuilder::MoveToStructuredDocumentTag(const System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTag\>\&, int32_t) method


Sposta il cursore sul tag di documento strutturato.

```cpp
void Aspose::Words::DocumentBuilder::MoveToStructuredDocumentTag(const System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> &structuredDocumentTag, int32_t characterIndex)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| structuredDocumentTag | const System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTag\>\& | Il tag di documento strutturato a cui spostarsi. |
| characterIndex | int32_t | L'indice del carattere all'interno del tag di documento strutturato. Un valore negativo consente di specificare una posizione dalla fine del tag di documento strutturato. Usa -1 per spostarti alla fine del tag di documento strutturato. Se il tag di documento strutturato è a livello di blocco e desideri spostare il cursore alla fine del suo ultimo paragrafo, specifica -2. |

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
## DocumentBuilder::MoveToStructuredDocumentTag(int32_t, int32_t) method


Sposta il cursore su un tag di documento strutturato nella sezione corrente.

```cpp
void Aspose::Words::DocumentBuilder::MoveToStructuredDocumentTag(int32_t structuredDocumentTagIndex, int32_t characterIndex)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| structuredDocumentTagIndex | int32_t | L'indice del tag di documento strutturato a cui spostarsi. |
| characterIndex | int32_t | L'indice del carattere all'interno del tag di documento strutturato. Un valore negativo consente di specificare una posizione dalla fine del tag di documento strutturato. Usa -1 per spostarti alla fine del tag di documento strutturato. Se il tag di documento strutturato è a livello di blocco e desideri spostare il cursore alla fine del suo ultimo paragrafo, specifica -2. |
## Note


La navigazione viene eseguita all'interno della storia corrente della sezione corrente. Cioè, se hai spostato il cursore all'intestazione primaria della prima sezione, allora *structuredDocumentTagIndex* specifica l'indice del tag di documento strutturato all'interno di quell'intestazione di quella sezione.

Quando *structuredDocumentTagIndex* è maggiore o uguale a 0, specifica un indice dall'inizio della sezione, con 0 che rappresenta il primo tag di documento strutturato. Quando *structuredDocumentTagIndex* è minore di 0, specifica un indice dalla fine della sezione, con -1 che rappresenta l'ultimo tag di documento strutturato.

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

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
