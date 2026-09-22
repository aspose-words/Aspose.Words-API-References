---
title: "Aspose::Words::Story::DeleteShapes yöntemi"
linktitle: "DeleteShapes"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Story::DeleteShapes yöntemi. Bu hikayenin metninden tüm şekilleri C++'da siler."
type: docs
weight: 3000
url: /tr/cpp/aspose.words/story/deleteshapes/
---
## Story::DeleteShapes method


Bu hikayenin metninden tüm şekilleri siler.

```cpp
void Aspose::Words::Story::DeleteShapes()
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

* Class [Story](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
