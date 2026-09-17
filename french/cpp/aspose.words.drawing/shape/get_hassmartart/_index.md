---
title: "Aspose::Words::Drawing::Shape::get_HasSmartArt méthode"
linktitle: "get_HasSmartArt"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Shape::get_HasSmartArt méthode. Renvoie true si cette Shape possède un objet SmartArt en C++."
type: docs
weight: 11000
url: /fr/cpp/aspose.words.drawing/shape/get_hassmartart/
---
## Shape::get_HasSmartArt method


Renvoie **true** si ce [Shape](../) possède un objet SmartArt.

```cpp
bool Aspose::Words::Drawing::Shape::get_HasSmartArt()
```


## Exemples



Montre comment compter le nombre de formes dans un document contenant des objets SmartArt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"SmartArt.docx");

int32_t numberOfSmartArtShapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_Cast<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Shape>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Shape> shape)>>([](System::SharedPtr<Aspose::Words::Drawing::Shape> shape) -> bool
{
    return shape->get_HasSmartArt();
})));

ASSERT_EQ(2, numberOfSmartArtShapes);
```

## Voir aussi

* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
