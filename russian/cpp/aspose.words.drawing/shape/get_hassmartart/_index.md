---
title: "Aspose::Words::Drawing::Shape::get_HasSmartArt метод"
linktitle: "get_HasSmartArt"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Shape::get_HasSmartArt метод. Возвращает **true**, если у этой Shape есть объект SmartArt в C++."
type: docs
weight: 11000
url: /ru/cpp/aspose.words.drawing/shape/get_hassmartart/
---
## Shape::get_HasSmartArt method


Возвращает **true**, если у этой [Shape](../) есть объект SmartArt.

```cpp
bool Aspose::Words::Drawing::Shape::get_HasSmartArt()
```


## Примеры



Показывает, как подсчитать количество фигур в документе с объектами SmartArt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"SmartArt.docx");

int32_t numberOfSmartArtShapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_Cast<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Shape>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Shape> shape)>>([](System::SharedPtr<Aspose::Words::Drawing::Shape> shape) -> bool
{
    return shape->get_HasSmartArt();
})));

ASSERT_EQ(2, numberOfSmartArtShapes);
```

## См. также

* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
