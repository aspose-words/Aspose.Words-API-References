---
title: Aspose::Words::Drawing::Shape::get_HasSmartArt method
linktitle: get_HasSmartArt
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Shape::get_HasSmartArt method. Returns true if this Shape has a SmartArt object in C++.'
type: docs
weight: 11000
url: /cpp/aspose.words.drawing/shape/get_hassmartart/
---
## Shape::get_HasSmartArt method


Returns **true** if this [Shape](../) has a SmartArt object.

```cpp
bool Aspose::Words::Drawing::Shape::get_HasSmartArt()
```


## Examples



Shows how to count the number of shapes in a document with SmartArt objects. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"SmartArt.docx");

int numberOfSmartArtShapes = doc->GetChildNodes(NodeType::Shape, true)
                                 ->LINQ_Cast<SharedPtr<Shape>>()
                                 ->LINQ_Count([](SharedPtr<Shape> shape) { return shape->get_HasSmartArt(); });

ASSERT_EQ(2, numberOfSmartArtShapes);
```

## See Also

* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
