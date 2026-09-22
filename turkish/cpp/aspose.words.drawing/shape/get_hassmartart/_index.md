---
title: "Aspose::Words::Drawing::Shape::get_HasSmartArt yöntemi"
linktitle: "get_HasSmartArt"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Shape::get_HasSmartArt yöntemi. C++'de bu Shape'in bir SmartArt nesnesi varsa **true** döndürür."
type: docs
weight: 11000
url: /tr/cpp/aspose.words.drawing/shape/get_hassmartart/
---
## Shape::get_HasSmartArt method


**true** döndürür eğer bu [Shape](../) bir SmartArt nesnesine sahipse.

```cpp
bool Aspose::Words::Drawing::Shape::get_HasSmartArt()
```


## Örnekler



SmartArt nesnelerine sahip bir belgede şekil sayısını nasıl sayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"SmartArt.docx");

int32_t numberOfSmartArtShapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_Cast<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Shape>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Shape> shape)>>([](System::SharedPtr<Aspose::Words::Drawing::Shape> shape) -> bool
{
    return shape->get_HasSmartArt();
})));

ASSERT_EQ(2, numberOfSmartArtShapes);
```

## Ayrıca Bakınız

* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
