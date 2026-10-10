---
title: "Metodo Aspose::Words::Drawing::ShapeBase::get_Hidden"
linktitle: "get_Hidden"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Drawing::ShapeBase::get_Hidden. Ottiene o imposta un valore booleano che indica se la forma è visibile in C++."
type: docs
weight: 22750
url: /it/cpp/aspose.words.drawing/shapebase/get_hidden/
---
## ShapeBase::get_Hidden method


Ottiene o imposta un valore booleano che indica se la forma è visibile.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_Hidden()
```


## Esempi



Mostra come nascondere la forma.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shadow color.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
if (!shape->get_Hidden())
{
    shape->set_Hidden(true);
}

doc->Save(get_ArtifactsDir() + u"Shape.Hidden.docx");
```

## Vedi anche

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
