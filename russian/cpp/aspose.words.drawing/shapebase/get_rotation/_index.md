---
title: "Метод Aspose::Words::Drawing::ShapeBase::get_Rotation"
linktitle: "get_Rotation"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Drawing::ShapeBase::get_Rotation. Определяет угол (в градусах), на который поворачивается фигура. Положительное значение соответствует вращению по часовой стрелке в C++."
type: docs
weight: 45000
url: /ru/cpp/aspose.words.drawing/shapebase/get_rotation/
---
## ShapeBase::get_Rotation method


Определяет угол (в градусах), на который повернута фигура. Положительное значение соответствует углу вращения по часовой стрелке.

```cpp
double Aspose::Words::Drawing::ShapeBase::get_Rotation()
```

## Примечания


Значение по умолчанию равно 0.

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
