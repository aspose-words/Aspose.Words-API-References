---
title: "Aspose::Words::Story::get_StoryType yöntemi"
linktitle: "get_StoryType"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Story::get_StoryType yöntemi. Bu hikayenin türünü C++'da alır."
type: docs
weight: 7000
url: /tr/cpp/aspose.words/story/get_storytype/
---
## Story::get_StoryType method


Bu hikayenin tipini alır.

```cpp
Aspose::Words::StoryType Aspose::Words::Story::get_StoryType() override
```


## Örnekler



Bir düğümden tüm şekilleri nasıl kaldıracağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bir şekil eklemek için DocumentBuilder kullanın. Bu bir satır içi şekildir,
// bu, bir üst Paragraph'a sahiptir ve bu Paragraph, ilk bölümün Body'sunun bir alt düğümüdür.
builder->InsertShape(Aspose::Words::Drawing::ShapeType::Cube, 100.0, 100.0);

ASSERT_EQ(1, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());

// Bu Body'nin alt paragraflarındaki tüm şekilleri silebiliriz.
ASSERT_EQ(Aspose::Words::StoryType::MainText, doc->get_FirstSection()->get_Body()->get_StoryType());
doc->get_FirstSection()->get_Body()->DeleteShapes();

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());
```

## Ayrıca Bakınız

* Enum [StoryType](../../storytype/)
* Class [Story](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
