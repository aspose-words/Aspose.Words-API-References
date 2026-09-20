---
title: "Método Aspose::Words::Drawing::ShapeBase::get_Hidden"
linktitle: "get_Hidden"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Drawing::ShapeBase::get_Hidden. Obtiene o establece un valor booleano que indica si la forma es visible en C++."
type: docs
weight: 22750
url: /es/cpp/aspose.words.drawing/shapebase/get_hidden/
---
## ShapeBase::get_Hidden method


Obtiene o establece un valor booleano que indica si la forma es visible.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_Hidden()
```


## Ejemplos



Muestra cómo ocultar la forma.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shadow color.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
if (!shape->get_Hidden())
{
    shape->set_Hidden(true);
}

doc->Save(get_ArtifactsDir() + u"Shape.Hidden.docx");
```

## Ver también

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
