---
title: "Aspose::Words::Drawing::GradientStopCollection 类"
linktitle: "GradientStopCollection"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::GradientStopCollection 类。包含 GradientStop 对象的集合。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.drawing/gradientstopcollection/
---
## GradientStopCollection class


包含一组 [GradientStop](../gradientstop/) 对象。欲了解更多，请访问 [Working with Graphic Elements](https://docs.aspose.com/words/cpp/working-with-graphic-elements/) 文档文章。

```cpp
class GradientStopCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Drawing::GradientStop>>
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Drawing::GradientStop\>\&) | 向渐变添加指定的 [GradientStop](../gradientstop/) 。 |
| [get_Count](./get_count/)() | 获取一个整数值，指示集合中的项目数量。 |
| [GetEnumerator](./getenumerator/)() override | 返回一个遍历集合的枚举器。 |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | 获取或设置集合中的 [GradientStop](../gradientstop/) 对象。 |
| [idx_set](./idx_set/)(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::GradientStop\>\&) | 获取或设置集合中的 [GradientStop](../gradientstop/) 对象。 |
| [Insert](./insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::GradientStop\>\&) | 在指定索引处向集合插入一个 [GradientStop](../gradientstop/)。 |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::SharedPtr\<Aspose::Words::Drawing::GradientStop\>\&) | 从集合中移除指定的 [GradientStop](../gradientstop/)。 |
| [RemoveAt](./removeat/)(int32_t) | 在指定索引处从集合中移除一个 [GradientStop](../gradientstop/)。 |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
