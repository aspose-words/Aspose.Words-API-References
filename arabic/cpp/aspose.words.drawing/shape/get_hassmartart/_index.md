---
title: "Aspose::Words::Drawing::Shape::get_HasSmartArt طريقة"
linktitle: "get_HasSmartArt"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::Shape::get_HasSmartArt طريقة. تُرجع **true** إذا كان هذا Shape يحتوي على كائن SmartArt في C++."
type: docs
weight: 11000
url: /ar/cpp/aspose.words.drawing/shape/get_hassmartart/
---
## Shape::get_HasSmartArt method


تُرجع **true** إذا كان هذا [Shape](../) يحتوي على كائن SmartArt.

```cpp
bool Aspose::Words::Drawing::Shape::get_HasSmartArt()
```


## أمثلة



يُظهر كيفية عد عدد الأشكال في مستند يحتوي على كائنات SmartArt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"SmartArt.docx");

int32_t numberOfSmartArtShapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_Cast<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Shape>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Shape> shape)>>([](System::SharedPtr<Aspose::Words::Drawing::Shape> shape) -> bool
{
    return shape->get_HasSmartArt();
})));

ASSERT_EQ(2, numberOfSmartArtShapes);
```

## انظر أيضًا

* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
