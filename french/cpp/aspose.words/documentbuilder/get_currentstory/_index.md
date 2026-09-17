---
title: "Aspose::Words::DocumentBuilder::get_CurrentStory méthode"
linktitle: "get_CurrentStory"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::DocumentBuilder::get_CurrentStory méthode. Obtient l’histoire qui est actuellement sélectionnée dans ce DocumentBuilder en C++."
type: docs
weight: 14000
url: /fr/cpp/aspose.words/documentbuilder/get_currentstory/
---
## DocumentBuilder::get_CurrentStory method


Obtient l’histoire qui est actuellement sélectionnée dans ce [DocumentBuilder](../).

```cpp
System::SharedPtr<Aspose::Words::Story> Aspose::Words::DocumentBuilder::get_CurrentStory()
```


## Exemples



Montre comment travailler avec l’histoire actuelle d’un document builder.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Une Story est un type de nœud qui possède des nœuds Paragraph enfants, tels qu’un Body.
ASPOSE_ASSERT_EQ(builder->get_CurrentStory(), doc->get_FirstSection()->get_Body());
ASPOSE_ASSERT_EQ(builder->get_CurrentStory(), builder->get_CurrentParagraph()->get_ParentNode());
ASSERT_EQ(Aspose::Words::StoryType::MainText, builder->get_CurrentStory()->get_StoryType());

builder->get_CurrentStory()->AppendParagraph(u"Text added to current Story.");

// Une Story peut également contenir des tables.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1");
builder->InsertCell();
builder->Write(u"Row 1, cell 2");
builder->EndTable();

ASSERT_TRUE(builder->get_CurrentStory()->get_Tables()->Contains(table));
```

## Voir aussi

* Class [Story](../../story/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
