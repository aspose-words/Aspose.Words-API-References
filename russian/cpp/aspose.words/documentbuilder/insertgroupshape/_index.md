---
title: "Метод Aspose::Words::DocumentBuilder::InsertGroupShape"
linktitle: "InsertGroupShape"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::DocumentBuilder::InsertGroupShape. Группирует переданные в параметре фигуры в новый узел GroupShape, который вставляется в текущую позицию в C++."
type: docs
weight: 35500
url: /ru/cpp/aspose.words/documentbuilder/insertgroupshape/
---
## DocumentBuilder::InsertGroupShape(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Drawing::ShapeBase\>\>\&) method


Группирует переданные в параметре фигуры в новый узел GroupShape, который вставляется в текущую позицию.

```cpp
System::SharedPtr<Aspose::Words::Drawing::GroupShape> Aspose::Words::DocumentBuilder::InsertGroupShape(const System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::ShapeBase>> &shapes)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| фигуры | const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Drawing::ShapeBase\>\>\& | Список фигур для группировки. |
## Примечания


Позиция и размеры нового GroupShape будут вычислены автоматически.

Фигуры VML и DML нельзя группировать вместе.

## Примеры



Показывает, как вставить DML GroupShape.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape1 = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 200, 250);
shape1->set_Left(20);
shape1->set_Top(20);
shape1->get_Stroke()->set_Color(System::Drawing::Color::get_Red());

System::SharedPtr<Aspose::Words::Drawing::Shape> shape2 = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Ellipse, 150, 200);
shape2->set_Left(40);
shape2->set_Top(50);
shape2->get_Stroke()->set_Color(System::Drawing::Color::get_Green());

// Размеры нового узла GroupShape.
double left = 10;
double top = 10;
double width = 200;
double height = 300;
// Вставить узел GroupShape заданного размера, который будет вставлен в указанную позицию.
System::SharedPtr<Aspose::Words::Drawing::GroupShape> groupShape1 = builder->InsertGroupShape(left, top, width, height, System::ExplicitCast<System::Array<System::SharedPtr<Aspose::Words::Drawing::ShapeBase>>>(System::MakeArray<System::SharedPtr<Aspose::Words::Drawing::Shape>>({shape1, shape2})));

// Вставить узел GroupShape, позиция и размеры которого будут вычислены автоматически.
auto shape3 = System::ExplicitCast<Aspose::Words::Drawing::Shape>(System::ExplicitCast<Aspose::Words::Node>(shape1)->Clone(true));
System::SharedPtr<Aspose::Words::Drawing::GroupShape> groupShape2 = builder->InsertGroupShape(System::MakeArray<System::SharedPtr<Aspose::Words::Drawing::ShapeBase>>({shape3}));

doc->Save(get_ArtifactsDir() + u"Shape.InsertGroupShape.docx");
```


Показывает, как объединить GroupShape с фигурой.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape1 = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 200, 250);
shape1->set_Left(20);
shape1->set_Top(20);
shape1->get_Stroke()->set_Color(System::Drawing::Color::get_Red());

System::SharedPtr<Aspose::Words::Drawing::Shape> shape2 = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Ellipse, 150, 200);
shape2->set_Left(40);
shape2->set_Top(50);
shape2->get_Stroke()->set_Color(System::Drawing::Color::get_Green());

// Объединить фигуры в узел GroupShape, который вставляется в указанную позицию.
System::SharedPtr<Aspose::Words::Drawing::GroupShape> groupShape1 = builder->InsertGroupShape(System::MakeArray<System::SharedPtr<Aspose::Words::Drawing::ShapeBase>>({shape1, shape2}));

// Объединить узлы Shape и GroupShape.
auto shape3 = System::ExplicitCast<Aspose::Words::Drawing::Shape>(System::ExplicitCast<Aspose::Words::Node>(shape1)->Clone(true));
System::SharedPtr<Aspose::Words::Drawing::GroupShape> groupShape2 = builder->InsertGroupShape(System::MakeArray<System::SharedPtr<Aspose::Words::Drawing::ShapeBase>>({groupShape1, shape3}));

doc->Save(get_ArtifactsDir() + u"Shape.CombineGroupShape.docx");
```

## См. также

* Class [GroupShape](../../../aspose.words.drawing/groupshape/)
* Class [ShapeBase](../../../aspose.words.drawing/shapebase/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertGroupShape(double, double, double, double, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Drawing::ShapeBase\>\>\&) method


Группирует переданные в параметре фигуры в новый узел GroupShape указанного размера, который вставляется в указанную позицию.

```cpp
System::SharedPtr<Aspose::Words::Drawing::GroupShape> Aspose::Words::DocumentBuilder::InsertGroupShape(double left, double top, double width, double height, const System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::ShapeBase>> &shapes)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| left | double | Расстояние в пунктах от начала координат до левой стороны GroupShape. |
| top | double | Расстояние в пунктах от начала координат до верхней стороны GroupShape. |
| width | double | Ширина GroupShape в пунктах. Отрицательное значение недопустимо. |
| height | double | Высота GroupShape в пунктах. Отрицательное значение недопустимо. |
| фигуры | const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Drawing::ShapeBase\>\>\& | Список фигур для группировки. |

## Примеры



Показывает, как вставить DML GroupShape.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape1 = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 200, 250);
shape1->set_Left(20);
shape1->set_Top(20);
shape1->get_Stroke()->set_Color(System::Drawing::Color::get_Red());

System::SharedPtr<Aspose::Words::Drawing::Shape> shape2 = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Ellipse, 150, 200);
shape2->set_Left(40);
shape2->set_Top(50);
shape2->get_Stroke()->set_Color(System::Drawing::Color::get_Green());

// Размеры нового узла GroupShape.
double left = 10;
double top = 10;
double width = 200;
double height = 300;
// Вставить узел GroupShape заданного размера, который будет вставлен в указанную позицию.
System::SharedPtr<Aspose::Words::Drawing::GroupShape> groupShape1 = builder->InsertGroupShape(left, top, width, height, System::ExplicitCast<System::Array<System::SharedPtr<Aspose::Words::Drawing::ShapeBase>>>(System::MakeArray<System::SharedPtr<Aspose::Words::Drawing::Shape>>({shape1, shape2})));

// Вставить узел GroupShape, позиция и размеры которого будут вычислены автоматически.
auto shape3 = System::ExplicitCast<Aspose::Words::Drawing::Shape>(System::ExplicitCast<Aspose::Words::Node>(shape1)->Clone(true));
System::SharedPtr<Aspose::Words::Drawing::GroupShape> groupShape2 = builder->InsertGroupShape(System::MakeArray<System::SharedPtr<Aspose::Words::Drawing::ShapeBase>>({shape3}));

doc->Save(get_ArtifactsDir() + u"Shape.InsertGroupShape.docx");
```

## См. также

* Class [GroupShape](../../../aspose.words.drawing/groupshape/)
* Class [ShapeBase](../../../aspose.words.drawing/shapebase/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
