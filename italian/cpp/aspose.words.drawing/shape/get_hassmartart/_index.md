---
title: "Aspose::Words::Drawing::Shape::get_HasSmartArt metodo"
linktitle: "get_HasSmartArt"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Shape::get_HasSmartArt metodo. Restituisce **true** se questo Shape ha un oggetto SmartArt in C++."
type: docs
weight: 11000
url: /it/cpp/aspose.words.drawing/shape/get_hassmartart/
---
## Shape::get_HasSmartArt method


Restituisce **true** se questo [Shape](../) ha un oggetto SmartArt.

```cpp
bool Aspose::Words::Drawing::Shape::get_HasSmartArt()
```


## Esempi



Mostra come contare il numero di forme in un documento con oggetti SmartArt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"SmartArt.docx");

int32_t numberOfSmartArtShapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_Cast<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Shape>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Shape> shape)>>([](System::SharedPtr<Aspose::Words::Drawing::Shape> shape) -> bool
{
    return shape->get_HasSmartArt();
})));

ASSERT_EQ(2, numberOfSmartArtShapes);
```

## Vedi anche

* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
