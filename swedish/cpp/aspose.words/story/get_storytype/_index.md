---
title: "Aspose::Words::Story::get_StoryType metod"
linktitle: "get_StoryType"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Story::get_StoryType metod. Hämtar typen av detta story i C++."
type: docs
weight: 7000
url: /sv/cpp/aspose.words/story/get_storytype/
---
## Story::get_StoryType method


Hämtar typen av den här storyn.

```cpp
Aspose::Words::StoryType Aspose::Words::Story::get_StoryType() override
```


## Exempel



Visar hur man tar bort alla former från en nod.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Använd en DocumentBuilder för att infoga en form. Detta är en inline-form,
// som har ett föräldra-Paragraph, som är ett barnnod till den första sektionens Body.
builder->InsertShape(Aspose::Words::Drawing::ShapeType::Cube, 100.0, 100.0);

ASSERT_EQ(1, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());

// Vi kan ta bort alla former från de underordnade styckena i detta Body.
ASSERT_EQ(Aspose::Words::StoryType::MainText, doc->get_FirstSection()->get_Body()->get_StoryType());
doc->get_FirstSection()->get_Body()->DeleteShapes();

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());
```

## Se även

* Enum [StoryType](../../storytype/)
* Class [Story](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
