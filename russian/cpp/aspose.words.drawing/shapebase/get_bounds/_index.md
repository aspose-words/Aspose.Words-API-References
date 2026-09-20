---
title: "Aspose::Words::Drawing::ShapeBase::get_Bounds метод"
linktitle: "get_Bounds"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::ShapeBase::get_Bounds метод. Получает или задает расположение и размер содержащего блока фигуры в C++."
type: docs
weight: 9000
url: /ru/cpp/aspose.words.drawing/shapebase/get_bounds/
---
## ShapeBase::get_Bounds method


Получает или задает расположение и размер содержащего блока фигуры.

```cpp
System::Drawing::RectangleF Aspose::Words::Drawing::ShapeBase::get_Bounds()
```

## Примечания


Игнорирует блокировку соотношения сторон при установке.

Для формы верхнего уровня значение задаётся в пунктах и относительно привязки формы.

Для фигур в группе значение находится в системе координат и единицах родительской группы.

## Примеры



Показывает, как создать и заполнить групповую фигуру.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Создайте групповую фигуру. Групповая фигура может отображать коллекцию дочерних узлов фигур.
// В Microsoft Word щелчок внутри границы групповой фигуры или по одной из её дочерних фигур будет
// выбирать все остальные дочерние фигуры внутри этой группы и позволять масштабировать и перемещать все фигуры одновременно.
auto group = System::MakeObject<Aspose::Words::Drawing::GroupShape>(doc);

ASSERT_EQ(Aspose::Words::Drawing::WrapType::None, group->get_WrapType());

// Создайте групповую фигуру размером 400pt x 400pt и разместите её в начале координат плавающих фигур документа.
group->set_Bounds(System::Drawing::RectangleF(0.0f, 0.0f, 400.0f, 400.0f));

// Установите размер внутренней координатной плоскости группы в 500 x 500pt.
// Верхний левый угол группы будет иметь координаты x и y (0, 0),
// а нижний правый угол будет иметь координаты x и y (500, 500).
group->set_CoordSize(System::Drawing::Size(500, 500));

// Установите координаты верхнего левого угла группы в (-250, -250).
// Центр группы теперь будет иметь координаты x и y (0, 0),
// а нижний правый угол будет находиться в (250, 250).
group->set_CoordOrigin(System::Drawing::Point(-250, -250));

// Создайте прямоугольник, который отобразит границу этой групповой фигуры, и добавьте его в группу.
auto child1 = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
child1->set_Width(group->get_CoordSize().get_Width());
child1->set_Height(group->get_CoordSize().get_Height());
child1->set_Left(group->get_CoordOrigin().get_X());
child1->set_Top(group->get_CoordOrigin().get_Y());
group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(child1);

// Как только фигура становится частью групповой фигуры, мы можем получить к ней доступ как к дочернему узлу и затем изменить её.
(System::ExplicitCast<Aspose::Words::Drawing::Shape>(group->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_Stroke()->set_DashStyle(Aspose::Words::Drawing::DashStyle::Dash);

// Создайте небольшую красную звезду и вставьте её в группу.
// Выровняйте фигуру с координатным началом группы, которое мы переместили в центр.
auto child2 = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Star);
child2->set_Width(20);
child2->set_Height(20);
child2->set_Left(-10);
child2->set_Top(-10);
child2->set_FillColor(System::Drawing::Color::get_Red());
group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(child2);

// Вставьте прямоугольник, а затем вставьте чуть меньший прямоугольник в том же месте с изображением.
// Новые фигуры, которые мы добавляем в группу, перекрывают более старые фигуры. Светло‑голубой прямоугольник будет частично перекрывать красную звезду,
// а затем фигура с изображением перекроет светло‑голубой прямоугольник, используя его как рамку.
// Мы не можем использовать свойства "ZOrder" фигур для управления их расположением внутри групповой фигуры.
auto child3 = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
child3->set_Width(250);
child3->set_Height(250);
child3->set_Left(-250);
child3->set_Top(-250);
child3->set_FillColor(System::Drawing::Color::get_LightBlue());
group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(child3);

auto child4 = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Image);
child4->set_Width(200);
child4->set_Height(200);
child4->set_Left(-225);
child4->set_Top(-225);
group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(child4);

(System::ExplicitCast<Aspose::Words::Drawing::Shape>(group->GetChild(Aspose::Words::NodeType::Shape, 3, true)))->get_ImageData()->SetImage(get_ImageDir() + u"Logo.jpg");

// Вставьте текстовое поле в групповую фигуру. Установите свойство "Left", чтобы правая грань текстового поля
// касалась правой границы групповой фигуры. Установите свойство "Top", чтобы текстовое поле располагалось за пределами
// границы групповой фигуры, с его верхним краем, выровненным по нижнему полю групповой фигуры.
auto child5 = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::TextBox);
child5->set_Width(200);
child5->set_Height(50);
child5->set_Left(group->get_CoordSize().get_Width() + group->get_CoordOrigin().get_X() - 200);
child5->set_Top(group->get_CoordSize().get_Height() + group->get_CoordOrigin().get_Y());
group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(child5);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertNode(group);
builder->MoveTo((System::ExplicitCast<Aspose::Words::Drawing::Shape>(group->GetChild(Aspose::Words::NodeType::Shape, 4, true)))->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc)));
builder->Write(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"Shape.GroupShape.docx");
```


Показывает, как проверить границы содержащего блока фигуры.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Line, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 50, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 50, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->set_StrokeColor(System::Drawing::Color::get_Orange());

// Хотя сама линия занимает мало места на странице документа,
// она занимает прямоугольный содержащий блок, размер которого мы можем определить с помощью свойств "Bounds".
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(50.0f, 50.0f, 100.0f, 100.0f), shape->get_Bounds());
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(50.0f, 50.0f, 100.0f, 100.0f), shape->get_BoundsInPoints());

// Создайте групповую фигуру, а затем задайте размер её содержащего блока с помощью свойства "Bounds".
auto group = System::MakeObject<Aspose::Words::Drawing::GroupShape>(doc);
group->set_Bounds(System::Drawing::RectangleF(0.0f, 100.0f, 250.0f, 250.0f));

ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(0.0f, 100.0f, 250.0f, 250.0f), group->get_BoundsInPoints());

// Создайте прямоугольник, проверьте размер его ограничивающего блока и затем добавьте его в групповую фигуру.
shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(100);
shape->set_Height(100);
shape->set_Left(700);
shape->set_Top(700);

ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(700.0f, 700.0f, 100.0f, 100.0f), shape->get_BoundsInPoints());

group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

// Координатная плоскость групповой фигуры имеет начало в левом верхнем углу её содержащего блока,
// а координаты x и y (1000, 1000) находятся в правом нижнем углу.
// Наша групповая фигура имеет размер 250×250pt, поэтому каждый 4pt на координатной плоскости групповой фигуры
// соответствует 1pt в координатной плоскости тела документа.
// Каждая вставляемая фигура также уменьшится в размере в 4 раза.
// Изменение свойства "BoundsInPoints" фигуры отразит это.
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(175.0f, 275.0f, 25.0f, 25.0f), shape->get_BoundsInPoints());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::GroupShape>>(group);

// Вставьте фигуру и разместите её за пределами блока, содержащего групповую фигуру.
shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(100);
shape->set_Height(100);
shape->set_Left(1000);
shape->set_Top(1000);

group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

// Отпечаток групповой фигуры в теле документа увеличился, но содержащий блок остался прежним.
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(0.0f, 100.0f, 250.0f, 250.0f), group->get_BoundsInPoints());
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(250.0f, 350.0f, 25.0f, 25.0f), shape->get_BoundsInPoints());

doc->Save(get_ArtifactsDir() + u"Shape.Bounds.docx");
```

## См. также

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
