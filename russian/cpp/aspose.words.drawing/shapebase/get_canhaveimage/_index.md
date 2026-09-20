---
title: "Aspose::Words::Drawing::ShapeBase::get_CanHaveImage method"
linktitle: "get_CanHaveImage"
second_title: "Справочник API Aspose.Words для C++"
description: "метод Aspose::Words::Drawing::ShapeBase::get_CanHaveImage. Возвращает **true**, если тип формы позволяет форме иметь изображение в C++."
type: docs
weight: 12000
url: /ru/cpp/aspose.words.drawing/shapebase/get_canhaveimage/
---
## ShapeBase::get_CanHaveImage method


Возвращает **true**, если тип фигуры позволяет ей иметь изображение.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_CanHaveImage()
```

## Примечания


Хотя Microsoft Word имеет специальный тип формы для изображений, кажется, что в документах Microsoft Word любая форма, кроме групповой формы, может иметь изображение, поэтому это свойство возвращает **true** для всех форм, кроме [GroupShape](../../groupshape/).

## Примеры



Показывает, как вставить и повернуть изображение.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте форму с изображением.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
ASSERT_TRUE(shape->get_CanHaveImage());
ASSERT_TRUE(shape->get_HasImage());

// Поверните изображение на 45 градусов по часовой стрелке.
shape->set_Rotation(45);

doc->Save(get_ArtifactsDir() + u"Shape.Rotate.docx");
```

## См. также

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
