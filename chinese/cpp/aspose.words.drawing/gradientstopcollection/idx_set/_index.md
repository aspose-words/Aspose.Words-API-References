---
title: "Aspose::Words::Drawing::GradientStopCollection::idx_set 方法"
linktitle: "idx_set"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::GradientStopCollection::idx_set 方法。获取或设置集合中的 GradientStop 对象（C++）。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words.drawing/gradientstopcollection/idx_set/
---
## GradientStopCollection::idx_set method


获取或设置集合中的 [GradientStop](../../gradientstop/) 对象。

```cpp
void Aspose::Words::Drawing::GradientStopCollection::idx_set(int32_t index, const System::SharedPtr<Aspose::Words::Drawing::GradientStop> &value)
```


## 示例



展示如何向渐变填充添加渐变停止点。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);
shape->get_Fill()->TwoColorGradient(System::Drawing::Color::get_Green(), System::Drawing::Color::get_Red(), Aspose::Words::Drawing::GradientStyle::Horizontal, Aspose::Words::Drawing::GradientVariant::Variant2);

// 获取渐变停止点集合。
System::SharedPtr<Aspose::Words::Drawing::GradientStopCollection> gradientStops = shape->get_Fill()->get_GradientStops();

// 更改第一个渐变停止点。
gradientStops->idx_get(0)->set_Color(System::Drawing::Color::get_Aqua());
gradientStops->idx_get(0)->set_Position(0.1);
gradientStops->idx_get(0)->set_Transparency(0.25);

// 在集合末尾添加新的渐变停止点。
auto gradientStop = System::MakeObject<Aspose::Words::Drawing::GradientStop>(System::Drawing::Color::get_Brown(), 0.5);
gradientStops->Add(gradientStop);

// 移除索引为 1 的渐变停止点。
gradientStops->RemoveAt(1);
// 并在相同的索引 1 处插入新的渐变停止点。
gradientStops->Insert(1, System::MakeObject<Aspose::Words::Drawing::GradientStop>(System::Drawing::Color::get_Chocolate(), 0.75, 0.3));

// 移除集合中的最后一个渐变停止点。
gradientStop = gradientStops->idx_get(2);
gradientStops->Remove(gradientStop);

ASSERT_EQ(2, gradientStops->get_Count());

ASPOSE_ASSERT_EQ(System::Drawing::Color::FromArgb(255, 0, 255, 255), gradientStops->idx_get(0)->get_BaseColor());
ASSERT_EQ(System::Drawing::Color::get_Aqua().ToArgb(), gradientStops->idx_get(0)->get_Color().ToArgb());
ASSERT_NEAR(0.1, gradientStops->idx_get(0)->get_Position(), 0.01);
ASSERT_NEAR(0.25, gradientStops->idx_get(0)->get_Transparency(), 0.01);

ASSERT_EQ(System::Drawing::Color::get_Chocolate().ToArgb(), gradientStops->idx_get(1)->get_Color().ToArgb());
ASSERT_NEAR(0.75, gradientStops->idx_get(1)->get_Position(), 0.01);
ASSERT_NEAR(0.3, gradientStops->idx_get(1)->get_Transparency(), 0.01);

// 使用合规选项通过 DML 定义形状
// 如果您想在文档保存后获取 "GradientStops" 属性。
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Strict);

doc->Save(get_ArtifactsDir() + u"Shape.GradientStops.docx", saveOptions);
```

## 另见

* Class [GradientStop](../../gradientstop/)
* Class [GradientStopCollection](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
