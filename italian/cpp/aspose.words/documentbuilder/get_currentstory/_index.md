---
title: "Aspose::Words::DocumentBuilder::get_CurrentStory metodo"
linktitle: "get_CurrentStory"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::DocumentBuilder::get_CurrentStory metodo. Ottiene la storia attualmente selezionata in questo DocumentBuilder in C++."
type: docs
weight: 14000
url: /it/cpp/aspose.words/documentbuilder/get_currentstory/
---
## DocumentBuilder::get_CurrentStory method


Ottiene la storia attualmente selezionata in questo [DocumentBuilder](../).

```cpp
System::SharedPtr<Aspose::Words::Story> Aspose::Words::DocumentBuilder::get_CurrentStory()
```


## Esempi



Mostra come lavorare con la storia corrente di un document builder.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Una Story è un tipo di nodo che ha nodi Paragraph figli, come un Body.
ASPOSE_ASSERT_EQ(builder->get_CurrentStory(), doc->get_FirstSection()->get_Body());
ASPOSE_ASSERT_EQ(builder->get_CurrentStory(), builder->get_CurrentParagraph()->get_ParentNode());
ASSERT_EQ(Aspose::Words::StoryType::MainText, builder->get_CurrentStory()->get_StoryType());

builder->get_CurrentStory()->AppendParagraph(u"Text added to current Story.");

// Una Story può contenere anche tabelle.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1");
builder->InsertCell();
builder->Write(u"Row 1, cell 2");
builder->EndTable();

ASSERT_TRUE(builder->get_CurrentStory()->get_Tables()->Contains(table));
```

## Vedi anche

* Class [Story](../../story/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
