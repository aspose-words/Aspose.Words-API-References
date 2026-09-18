---
title: "Aspose::Words::Drawing::ShapeBase::get_Hidden Methode"
linktitle: "get_Hidden"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ShapeBase::get_Hidden Methode. Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob die Form in C++ sichtbar ist."
type: docs
weight: 22750
url: /de/cpp/aspose.words.drawing/shapebase/get_hidden/
---
## ShapeBase::get_Hidden method


Liest oder setzt einen booleschen Wert, der angibt, ob die Form sichtbar ist.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_Hidden()
```


## Beispiele



Zeigt, wie man die Form ausblendet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shadow color.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
if (!shape->get_Hidden())
{
    shape->set_Hidden(true);
}

doc->Save(get_ArtifactsDir() + u"Shape.Hidden.docx");
```

## Siehe auch

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
