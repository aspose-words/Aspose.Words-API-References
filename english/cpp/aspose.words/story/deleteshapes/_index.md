---
title: Aspose::Words::Story::DeleteShapes method
linktitle: DeleteShapes
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Story::DeleteShapes method. Deletes all shapes from the text of this story in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words/story/deleteshapes/
---
## Story::DeleteShapes method


Deletes all shapes from the text of this story.

```cpp
void Aspose::Words::Story::DeleteShapes()
```


## Examples



Shows how to remove all shapes from a node. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Use a DocumentBuilder to insert a shape. This is an inline shape,
// which has a parent Paragraph, which is a child node of the first section's Body.
builder->InsertShape(ShapeType::Cube, 100.0, 100.0);

ASSERT_EQ(1, doc->GetChildNodes(NodeType::Shape, true)->get_Count());

// We can delete all shapes from the child paragraphs of this Body.
ASSERT_EQ(StoryType::MainText, doc->get_FirstSection()->get_Body()->get_StoryType());
doc->get_FirstSection()->get_Body()->DeleteShapes();

ASSERT_EQ(0, doc->GetChildNodes(NodeType::Shape, true)->get_Count());
```

## See Also

* Class [Story](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
