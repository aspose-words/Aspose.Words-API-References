---
title: "Aspose::Words::Drawing::Shape::get_HasSmartArt metod"
linktitle: "get_HasSmartArt"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Shape::get_HasSmartArt metod. Returnerar true om denna Shape har ett SmartArt‑objekt i C++."
type: docs
weight: 11000
url: /sv/cpp/aspose.words.drawing/shape/get_hassmartart/
---
## Shape::get_HasSmartArt method


Returnerar **true** om detta [Shape](../) har ett SmartArt‑objekt.

```cpp
bool Aspose::Words::Drawing::Shape::get_HasSmartArt()
```


## Exempel



Visar hur man räknar antalet former i ett dokument med SmartArt‑objekt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"SmartArt.docx");

int32_t numberOfSmartArtShapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_Cast<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Shape>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Shape> shape)>>([](System::SharedPtr<Aspose::Words::Drawing::Shape> shape) -> bool
{
    return shape->get_HasSmartArt();
})));

ASSERT_EQ(2, numberOfSmartArtShapes);
```

## Se även

* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
