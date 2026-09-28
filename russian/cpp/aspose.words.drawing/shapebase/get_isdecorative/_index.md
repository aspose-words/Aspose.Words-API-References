---
title: "Метод Aspose::Words::Drawing::ShapeBase::get_IsDecorative"
linktitle: "get_IsDecorative"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Drawing::ShapeBase::get_IsDecorative. Получает или задает флаг, указывающий, является ли фигура декоративной в документе, в C++."
type: docs
weight: 25000
url: /ru/cpp/aspose.words.drawing/shapebase/get_isdecorative/
---
## ShapeBase::get_IsDecorative method


Получает или задает флаг, указывающий, является ли фигура декоративной в документе.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsDecorative()
```


## Примеры



Показывает, как установить, что фигура является декоративной.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Decorative shapes.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));
ASSERT_TRUE(shape->get_IsDecorative());

// Если "AlternativeText" не пуст, фигура не может быть декоративной.
// Поэтому наше значение изменилось на 'false'.
shape->set_AlternativeText(u"Alternative text.");
ASSERT_FALSE(shape->get_IsDecorative());

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->MoveToDocumentEnd();
// Создайте новую фигуру как декоративную.
shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 100);
shape->set_IsDecorative(true);

doc->Save(get_ArtifactsDir() + u"Shape.IsDecorative.docx");
```

## См. также

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
