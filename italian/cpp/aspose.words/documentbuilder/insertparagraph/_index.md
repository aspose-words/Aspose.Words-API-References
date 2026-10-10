---
title: "Metodo Aspose::Words::DocumentBuilder::InsertParagraph"
linktitle: "InsertParagraph"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::DocumentBuilder::InsertParagraph. Inserisce un'interruzione di paragrafo nel documento in C++."
type: docs
weight: 44000
url: /it/cpp/aspose.words/documentbuilder/insertparagraph/
---
## DocumentBuilder::InsertParagraph method


Inserisce un'interruzione di paragrafo nel documento.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::DocumentBuilder::InsertParagraph()
```


### ReturnValue

Il nodo del paragrafo appena inserito. È lo stesso nodo di [CurrentParagraph](../get_currentparagraph/).
## Note


Viene utilizzata la formattazione del paragrafo corrente specificata dalla proprietà [ParagraphFormat](../get_paragraphformat/).

Divide il paragrafo corrente in due. Dopo aver inserito il paragrafo, il cursore viene posizionato all'inizio del nuovo paragrafo.

Viene generata un'eccezione se non è possibile inserire un'interruzione di paragrafo nella posizione corrente del cursore.

## Esempi



Mostra come inserire un paragrafo nel documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Font> font = builder->get_Font();
font->set_Size(16);
font->set_Bold(true);
font->set_Color(System::Drawing::Color::get_Blue());
font->set_Name(u"Arial");
font->set_Underline(Aspose::Words::Underline::Dash);

System::SharedPtr<Aspose::Words::ParagraphFormat> paragraphFormat = builder->get_ParagraphFormat();
paragraphFormat->set_FirstLineIndent(8);
paragraphFormat->set_Alignment(Aspose::Words::ParagraphAlignment::Justify);
paragraphFormat->set_AddSpaceBetweenFarEastAndAlpha(true);
paragraphFormat->set_AddSpaceBetweenFarEastAndDigit(true);
paragraphFormat->set_KeepTogether(true);

// Il metodo "Writeln" termina il paragrafo dopo aver aggiunto il testo
// e poi avvia una nuova riga, aggiungendo un nuovo paragrafo.
builder->Writeln(u"Hello world!");

ASSERT_TRUE(builder->get_CurrentParagraph()->get_IsEndOfDocument());
```

## Vedi anche

* Class [Paragraph](../../paragraph/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
