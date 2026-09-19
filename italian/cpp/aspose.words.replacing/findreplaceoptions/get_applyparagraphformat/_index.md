---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_ApplyParagraphFormat metodo"
linktitle: "get_ApplyParagraphFormat"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_ApplyParagraphFormat metodo. Formattazione del paragrafo applicata al nuovo contenuto in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.replacing/findreplaceoptions/get_applyparagraphformat/
---
## FindReplaceOptions::get_ApplyParagraphFormat method


[Paragraph](../../../aspose.words/paragraph/) formatting applied to new content.

```cpp
System::SharedPtr<Aspose::Words::ParagraphFormat> Aspose::Words::Replacing::FindReplaceOptions::get_ApplyParagraphFormat() const
```


## Esempi



Mostra come aggiungere formattazione ai paragrafi in cui un'operazione di trova-e-sostituisci ha trovato corrispondenze.
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

// Possiamo utilizzare un oggetto "FindReplaceOptions" per modificare il processo di ricerca e sostituzione.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Imposta la proprietà "Alignment" su "ParagraphAlignment.Right" per allineare a destra ogni paragrafo
// che contiene una corrispondenza trovata dall'operazione di trova-e-sostituisci.
options->get_ApplyParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Right);

// Sostituisci ogni punto fermo che si trova subito prima di un'interruzione di paragrafo con un punto esclamativo.
int32_t count = doc->get_Range()->Replace(u".&p", u"!&p", options);

ASSERT_EQ(2, count);
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Right, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Right, paragraphs->idx_get(2)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(System::String(u"Every paragraph that ends with a full stop like this one will be right aligned!\r") + u"This one will not!\r" + u"This one also will!", doc->GetText().Trim());
```

## Vedi anche

* Class [ParagraphFormat](../../../aspose.words/paragraphformat/)
* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
