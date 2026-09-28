---
title: "Aspose::Words::Drawing::ShapeBase::get_Hidden метод"
linktitle: "get_Hidden"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::ShapeBase::get_Hidden метод. Получает или задает логическое значение, указывающее, видима ли фигура в C++."
type: docs
weight: 22750
url: /ru/cpp/aspose.words.drawing/shapebase/get_hidden/
---
## ShapeBase::get_Hidden method


Получает или задает логическое значение, указывающее, видима ли фигура.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_Hidden()
```


## Примеры



Показывает, как скрыть фигуру.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shadow color.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
if (!shape->get_Hidden())
{
    shape->set_Hidden(true);
}

doc->Save(get_ArtifactsDir() + u"Shape.Hidden.docx");
```

## См. также

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
