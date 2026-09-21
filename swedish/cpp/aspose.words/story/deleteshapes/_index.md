---
title: "Aspose::Words::Story::DeleteShapes metod"
linktitle: "DeleteShapes"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Story::DeleteShapes metod. Raderar alla former från texten i denna berättelse i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words/story/deleteshapes/
---
## Story::DeleteShapes method


Raderar alla former från texten i den här berättelsen.

```cpp
void Aspose::Words::Story::DeleteShapes()
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

* Class [Story](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
