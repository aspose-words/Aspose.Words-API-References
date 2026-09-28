---
title: "Метод Aspose::Words::Drawing::ShapeBase::get_DistanceRight"
linktitle: "get_DistanceRight"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Drawing::ShapeBase::get_DistanceRight. Возвращает или задаёт расстояние (в пунктах) между текстом документа и правым краем фигуры в C++."
type: docs
weight: 17000
url: /ru/cpp/aspose.words.drawing/shapebase/get_distanceright/
---
## ShapeBase::get_DistanceRight method


Возвращает или задает расстояние (в пунктах) между текстом документа и правым краем фигуры.

```cpp
double Aspose::Words::Drawing::ShapeBase::get_DistanceRight()
```

## Примечания


Значение по умолчанию — 1/8 дюйма.

Имеет эффект только для фигур верхнего уровня.

## Примеры



Показывает, как установить расстояние обтекания текста, окружающего фигуру.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте прямоугольник и заставьте текст плотно обтекать его границы.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 150, 150);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Tight);

// Установите минимальное расстояние между фигурой и окружающим текстом в 40pt со всех сторон.
shape->set_DistanceTop(40);
shape->set_DistanceBottom(40);
shape->set_DistanceLeft(40);
shape->set_DistanceRight(40);

// Переместите фигуру ближе к центру страницы, а затем поверните её на 60 градусов по часовой стрелке.
shape->set_Top(75);
shape->set_Left(150);
shape->set_Rotation(60);

// Добавьте текст, который будет обтекать фигуру.
builder->get_Font()->set_Size(24);
builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ") + u"Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

doc->Save(get_ArtifactsDir() + u"Shape.Coordinates.docx");
```

## См. также

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
