---
title: get_StoryType
second_title: Aspose.Words for C++ API Reference
description: Gets the type of this story.
type: docs
weight: 66
url: /cpp/aspose.words/story/get_storytype/
---
## Story::get_StoryType method


Gets the type of this story.

```cpp
Aspose::Words::StoryType Aspose::Words::Story::get_StoryType() const
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

* Enum [StoryType](../../storytype/)
* Class [Story](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
