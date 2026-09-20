---
title: "Método Aspose::Words::Drawing::Shape::get_HasSmartArt"
linktitle: "get_HasSmartArt"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Drawing::Shape::get_HasSmartArt. Devuelve true si esta Shape tiene un objeto SmartArt en C++."
type: docs
weight: 11000
url: /es/cpp/aspose.words.drawing/shape/get_hassmartart/
---
## Shape::get_HasSmartArt method


Devuelve **true** si este [Shape](../) tiene un objeto SmartArt.

```cpp
bool Aspose::Words::Drawing::Shape::get_HasSmartArt()
```


## Ejemplos



Muestra cómo contar el número de formas en un documento con objetos SmartArt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"SmartArt.docx");

int32_t numberOfSmartArtShapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_Cast<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Shape>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Shape> shape)>>([](System::SharedPtr<Aspose::Words::Drawing::Shape> shape) -> bool
{
    return shape->get_HasSmartArt();
})));

ASSERT_EQ(2, numberOfSmartArtShapes);
```

## Ver también

* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
