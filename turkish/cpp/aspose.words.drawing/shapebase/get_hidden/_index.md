---
title: "Aspose::Words::Drawing::ShapeBase::get_Hidden metodu"
linktitle: "get_Hidden"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ShapeBase::get_Hidden metodu. Şeklin görünür olup olmadığını belirten boolean değeri alır veya ayarlar C++'de."
type: docs
weight: 22750
url: /tr/cpp/aspose.words.drawing/shapebase/get_hidden/
---
## ShapeBase::get_Hidden method


Şeklin görünür olup olmadığını gösteren bir boolean değeri alır veya ayarlar.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_Hidden()
```


## Örnekler



Şeklin nasıl gizleneceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shadow color.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
if (!shape->get_Hidden())
{
    shape->set_Hidden(true);
}

doc->Save(get_ArtifactsDir() + u"Shape.Hidden.docx");
```

## Ayrıca Bakınız

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
