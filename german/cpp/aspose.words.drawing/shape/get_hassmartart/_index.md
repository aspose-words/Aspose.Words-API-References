---
title: "Aspose::Words::Drawing::Shape::get_HasSmartArt Methode"
linktitle: "get_HasSmartArt"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Shape::get_HasSmartArt Methode. Gibt **true** zurück, wenn dieses Shape ein SmartArt-Objekt in C++ hat."
type: docs
weight: 11000
url: /de/cpp/aspose.words.drawing/shape/get_hassmartart/
---
## Shape::get_HasSmartArt method


Gibt **true** zurück, wenn dieses [Shape](../) ein SmartArt-Objekt hat.

```cpp
bool Aspose::Words::Drawing::Shape::get_HasSmartArt()
```


## Beispiele



Zeigt, wie man die Anzahl der Shapes in einem Dokument mit SmartArt-Objekten zählt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"SmartArt.docx");

int32_t numberOfSmartArtShapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_Cast<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Shape>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Shape> shape)>>([](System::SharedPtr<Aspose::Words::Drawing::Shape> shape) -> bool
{
    return shape->get_HasSmartArt();
})));

ASSERT_EQ(2, numberOfSmartArtShapes);
```

## Siehe auch

* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
