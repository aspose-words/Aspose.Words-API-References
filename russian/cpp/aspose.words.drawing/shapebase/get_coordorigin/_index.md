---
title: "Aspose::Words::Drawing::ShapeBase::get_CoordOrigin метод"
linktitle: "get_CoordOrigin"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::ShapeBase::get_CoordOrigin метод. Координаты в левом верхнем углу содержащего блока этой фигуры в C++."
type: docs
weight: 13000
url: /ru/cpp/aspose.words.drawing/shapebase/get_coordorigin/
---
## ShapeBase::get_CoordOrigin method


Координаты в левом верхнем углу содержащего блока этой фигуры.

```cpp
System::Drawing::Point Aspose::Words::Drawing::ShapeBase::get_CoordOrigin()
```

## Примечания


Значение по умолчанию — (0,0).

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


Показывает, как преобразовать положение координат x и y на координатной плоскости фигуры в положение на координатной плоскости родительской фигуры.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Вставьте групповую фигуру и разместите её на 100 пунктов ниже и правее
// от исходной точки координат x и Y документа.
auto group = System::MakeObject<Aspose::Words::Drawing::GroupShape>(doc);
group->set_Bounds(System::Drawing::RectangleF(100.0f, 100.0f, 500.0f, 500.0f));

// Используйте метод "LocalToParent", чтобы определить, что (0, 0) во внутренних координатах x и y группы
// соответствует (100, 100) в координатной системе её родительской фигуры. Родителем групповой фигуры является сам документ.
ASPOSE_ASSERT_EQ(System::Drawing::PointF(100.0f, 100.0f), group->LocalToParent(System::Drawing::PointF(0.0f, 0.0f)));

// По умолчанию внутренняя координатная плоскость фигуры имеет верхний левый угол в (0, 0),
// а нижний правый угол в (1000, 1000). Из‑за своего размера наша групповая фигура покрывает область 500pt × 500pt
// в плоскости документа. Это означает, что перемещение на 1pt в координатной плоскости документа будет преобразовано
// в перемещение на 2pt в координатной плоскости групповой фигуры.
ASPOSE_ASSERT_EQ(System::Drawing::PointF(150.0f, 150.0f), group->LocalToParent(System::Drawing::PointF(100.0f, 100.0f)));
ASPOSE_ASSERT_EQ(System::Drawing::PointF(200.0f, 200.0f), group->LocalToParent(System::Drawing::PointF(200.0f, 200.0f)));
ASPOSE_ASSERT_EQ(System::Drawing::PointF(250.0f, 250.0f), group->LocalToParent(System::Drawing::PointF(300.0f, 300.0f)));

// Переместите начало координат осей x и y группы фигур из верхнего левого угла в центр.
// Это сместит внутренние координаты группы относительно координат документа ещё дальше.
group->set_CoordOrigin(System::Drawing::Point(-250, -250));

ASPOSE_ASSERT_EQ(System::Drawing::PointF(375.0f, 375.0f), group->LocalToParent(System::Drawing::PointF(300.0f, 300.0f)));

// Изменение масштаба координатной плоскости также повлияет на относительные положения.
group->set_CoordSize(System::Drawing::Size(500, 500));

ASPOSE_ASSERT_EQ(System::Drawing::PointF(650.0f, 650.0f), group->LocalToParent(System::Drawing::PointF(300.0f, 300.0f)));

// Если мы хотим добавить фигуру в эту группу, определяя её расположение на основе положения в документе,
// нам потребуется сначала подтвердить положение в группе фигур, которое будет соответствовать положению в документе.
ASPOSE_ASSERT_EQ(System::Drawing::PointF(700.0f, 700.0f), group->LocalToParent(System::Drawing::PointF(350.0f, 350.0f)));

auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(100);
shape->set_Height(100);
shape->set_Left(700);
shape->set_Top(700);

group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::GroupShape>>(group);

doc->Save(get_ArtifactsDir() + u"Shape.LocalToParent.docx");
```

## См. также

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
