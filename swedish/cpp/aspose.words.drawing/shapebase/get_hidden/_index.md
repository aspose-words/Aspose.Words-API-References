---
title: "Aspose::Words::Drawing::ShapeBase::get_Hidden metod"
linktitle: "get_Hidden"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::ShapeBase::get_Hidden metod. Hämtar eller anger ett booleskt värde som indikerar om formen är synlig i C++."
type: docs
weight: 22750
url: /sv/cpp/aspose.words.drawing/shapebase/get_hidden/
---
## ShapeBase::get_Hidden method


Hämtar eller anger ett booleskt värde som indikerar om formen är synlig.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_Hidden()
```


## Exempel



Visar hur man döljer formen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shadow color.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
if (!shape->get_Hidden())
{
    shape->set_Hidden(true);
}

doc->Save(get_ArtifactsDir() + u"Shape.Hidden.docx");
```

## Se även

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
