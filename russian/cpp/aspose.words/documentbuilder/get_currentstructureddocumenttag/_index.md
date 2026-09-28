---
title: "Aspose::Words::DocumentBuilder::get_CurrentStructuredDocumentTag метод"
linktitle: "get_CurrentStructuredDocumentTag"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::DocumentBuilder::get_CurrentStructuredDocumentTag метод. Получает структурированный тег документа, который в данный момент выбран в этом DocumentBuilder на C++."
type: docs
weight: 15000
url: /ru/cpp/aspose.words/documentbuilder/get_currentstructureddocumenttag/
---
## DocumentBuilder::get_CurrentStructuredDocumentTag method


Получает структурированный тег документа, который в данный момент выбран в этом [DocumentBuilder](../).

```cpp
System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> Aspose::Words::DocumentBuilder::get_CurrentStructuredDocumentTag()
```


## Примеры



Показывает, как переместить курсор [DocumentBuilder](../) внутри структурного тега документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Существует несколько способов перемещения курсора:
// 1 -  Перейти к первому символу структурированного тега документа по индексу.
builder->MoveToStructuredDocumentTag(1, 1);

// 2 -  Перейти к первому символу структурированного тега документа по объекту.
auto tag = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTag, 2, true));
builder->MoveToStructuredDocumentTag(tag, 1);
builder->Write(u" New text.");

ASSERT_EQ(u"R New text.ichText", tag->GetText().Trim());

// 3 -  Перейти к концу второго структурированного тега документа.
builder->MoveToStructuredDocumentTag(1, -1);
ASSERT_TRUE(builder->get_IsAtEndOfStructuredDocumentTag());

// Получить текущий выбранный структурированный тег документа.
builder->get_CurrentStructuredDocumentTag()->set_Color(System::Drawing::Color::get_Green());

doc->Save(get_ArtifactsDir() + u"Document.MoveToStructuredDocumentTag.docx");
```

## См. также

* Class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
