---
title: "Aspose::Words::DocumentBuilder::InsertGroupShape method"
linktitle: "InsertGroupShape"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentBuilder::InsertGroupShape 方法。将作为参数传入的形状分组为一个新的 GroupShape 节点，并在 C++ 中插入到当前位置。"
type: docs
weight: 35500
url: /zh/cpp/aspose.words/documentbuilder/insertgroupshape/
---
## DocumentBuilder::InsertGroupShape(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Drawing::ShapeBase\>\>\&) method


将作为参数传入的形状分组为新的 GroupShape 节点，并插入到当前位置。

```cpp
System::SharedPtr<Aspose::Words::Drawing::GroupShape> Aspose::Words::DocumentBuilder::InsertGroupShape(const System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::ShapeBase>> &shapes)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 形状 | const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Drawing::ShapeBase\>\>\& | 要分组的形状列表。 |
## 备注


新 GroupShape 的位置和尺寸将自动计算。

VML 和 DML 形状不能一起分组。

## 示例



展示如何插入 DML 组形状。
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

// 新 GroupShape 节点的尺寸。
double left = 10;
double top = 10;
double width = 200;
double height = 300;
// 插入具有指定大小的 GroupShape 节点，该节点将插入到指定位置。
System::SharedPtr<Aspose::Words::Drawing::GroupShape> groupShape1 = builder->InsertGroupShape(left, top, width, height, System::ExplicitCast<System::Array<System::SharedPtr<Aspose::Words::Drawing::ShapeBase>>>(System::MakeArray<System::SharedPtr<Aspose::Words::Drawing::Shape>>({shape1, shape2})));

// 插入 GroupShape 节点，位置和尺寸将自动计算。
auto shape3 = System::ExplicitCast<Aspose::Words::Drawing::Shape>(System::ExplicitCast<Aspose::Words::Node>(shape1)->Clone(true));
System::SharedPtr<Aspose::Words::Drawing::GroupShape> groupShape2 = builder->InsertGroupShape(System::MakeArray<System::SharedPtr<Aspose::Words::Drawing::ShapeBase>>({shape3}));

doc->Save(get_ArtifactsDir() + u"Shape.InsertGroupShape.docx");
```


展示如何将 group shape 与 shape 组合。
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

// 将 shapes 合并为 GroupShape 节点，并插入到指定位置。
System::SharedPtr<Aspose::Words::Drawing::GroupShape> groupShape1 = builder->InsertGroupShape(System::MakeArray<System::SharedPtr<Aspose::Words::Drawing::ShapeBase>>({shape1, shape2}));

// 合并 Shape 和 GroupShape 节点。
auto shape3 = System::ExplicitCast<Aspose::Words::Drawing::Shape>(System::ExplicitCast<Aspose::Words::Node>(shape1)->Clone(true));
System::SharedPtr<Aspose::Words::Drawing::GroupShape> groupShape2 = builder->InsertGroupShape(System::MakeArray<System::SharedPtr<Aspose::Words::Drawing::ShapeBase>>({groupShape1, shape3}));

doc->Save(get_ArtifactsDir() + u"Shape.CombineGroupShape.docx");
```

## 另见

* Class [GroupShape](../../../aspose.words.drawing/groupshape/)
* Class [ShapeBase](../../../aspose.words.drawing/shapebase/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertGroupShape(double, double, double, double, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Drawing::ShapeBase\>\>\&) method


将作为参数传入的形状分组为指定大小的新 GroupShape 节点，并插入到指定位置。

```cpp
System::SharedPtr<Aspose::Words::Drawing::GroupShape> Aspose::Words::DocumentBuilder::InsertGroupShape(double left, double top, double width, double height, const System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::ShapeBase>> &shapes)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| left | double | 从原点到 group shape 左侧的距离（单位为点）。 |
| top | double | 从原点到 group shape 顶部的距离（单位为点）。 |
| width | double | group shape 的宽度（单位为点）。不允许负值。 |
| height | double | group shape 的高度（单位为点）。不允许负值。 |
| 形状 | const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Drawing::ShapeBase\>\>\& | 要分组的形状列表。 |

## 示例



展示如何插入 DML 组形状。
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

// 新 GroupShape 节点的尺寸。
double left = 10;
double top = 10;
double width = 200;
double height = 300;
// 插入具有指定大小的 GroupShape 节点，该节点将插入到指定位置。
System::SharedPtr<Aspose::Words::Drawing::GroupShape> groupShape1 = builder->InsertGroupShape(left, top, width, height, System::ExplicitCast<System::Array<System::SharedPtr<Aspose::Words::Drawing::ShapeBase>>>(System::MakeArray<System::SharedPtr<Aspose::Words::Drawing::Shape>>({shape1, shape2})));

// 插入 GroupShape 节点，位置和尺寸将自动计算。
auto shape3 = System::ExplicitCast<Aspose::Words::Drawing::Shape>(System::ExplicitCast<Aspose::Words::Node>(shape1)->Clone(true));
System::SharedPtr<Aspose::Words::Drawing::GroupShape> groupShape2 = builder->InsertGroupShape(System::MakeArray<System::SharedPtr<Aspose::Words::Drawing::ShapeBase>>({shape3}));

doc->Save(get_ArtifactsDir() + u"Shape.InsertGroupShape.docx");
```

## 另见

* Class [GroupShape](../../../aspose.words.drawing/groupshape/)
* Class [ShapeBase](../../../aspose.words.drawing/shapebase/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
