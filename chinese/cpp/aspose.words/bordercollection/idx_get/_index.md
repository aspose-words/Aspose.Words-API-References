---
title: "Aspose::Words::BorderCollection::idx_get 方法"
linktitle: "idx_get"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::BorderCollection::idx_get 方法。在 C++ 中通过边框类型检索 Border 对象。"
type: docs
weight: 18000
url: /zh/cpp/aspose.words/bordercollection/idx_get/
---
## BorderCollection::idx_get(Aspose::Words::BorderType) method


通过边框类型检索一个 [Border](../../border/) 对象。

```cpp
System::SharedPtr<Aspose::Words::Border> Aspose::Words::BorderCollection::idx_get(Aspose::Words::BorderType borderType)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| borderType | Aspose::Words::BorderType | 一个指定要检索的边框类型的 [BorderType](../../bordertype/) 值。 |
## 备注


请注意，不同文档元素并非都有所有边框。如果请求的边框不适用于当前对象，此方法会抛出异常。

## 示例



展示如何使用边框和阴影装饰文本。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::BorderCollection> borders = builder->get_ParagraphFormat()->get_Borders();
borders->set_DistanceFromText(20);
borders->idx_get(Aspose::Words::BorderType::Left)->set_LineStyle(Aspose::Words::LineStyle::Double);
borders->idx_get(Aspose::Words::BorderType::Right)->set_LineStyle(Aspose::Words::LineStyle::Double);
borders->idx_get(Aspose::Words::BorderType::Top)->set_LineStyle(Aspose::Words::LineStyle::Double);
borders->idx_get(Aspose::Words::BorderType::Bottom)->set_LineStyle(Aspose::Words::LineStyle::Double);

System::SharedPtr<Aspose::Words::Shading> shading = builder->get_ParagraphFormat()->get_Shading();
shading->set_Texture(Aspose::Words::TextureIndex::TextureDiagonalCross);
shading->set_BackgroundPatternColor(System::Drawing::Color::get_LightCoral());
shading->set_ForegroundPatternColor(System::Drawing::Color::get_LightSalmon());

builder->Write(u"This paragraph is formatted with a double border and shading.");
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.ApplyBordersAndShading.docx");
```

## 另见

* Class [Border](../../border/)
* Enum [BorderType](../../bordertype/)
* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## BorderCollection::idx_get(int32_t) method


通过索引检索一个 [Border](../../border/) 对象。

```cpp
System::SharedPtr<Aspose::Words::Border> Aspose::Words::BorderCollection::idx_get(int32_t index)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| index | int32_t | 要检索的边框的零基索引。 |

## 示例



展示边框集合如何共享元素。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Paragraph 1.");
builder->Write(u"Paragraph 2.");

// 由于我们在创建时使用了相同的边框配置
// 这些段落，它们的边框集合共享相同的元素。
System::SharedPtr<Aspose::Words::BorderCollection> firstParagraphBorders = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Borders();
System::SharedPtr<Aspose::Words::BorderCollection> secondParagraphBorders = builder->get_CurrentParagraph()->get_ParagraphFormat()->get_Borders();

for (int32_t i = 0; i < firstParagraphBorders->get_Count(); i++)
{
    ASSERT_TRUE(System::ObjectExt::Equals(firstParagraphBorders->idx_get(i), secondParagraphBorders->idx_get(i)));
    ASSERT_EQ(System::ObjectExt::GetHashCode(firstParagraphBorders->idx_get(i)), System::ObjectExt::GetHashCode(secondParagraphBorders->idx_get(i)));
    ASSERT_FALSE(firstParagraphBorders->idx_get(i)->get_IsVisible());
}

for (auto&& border : System::IterateOver(secondParagraphBorders))
{
    border->set_LineStyle(Aspose::Words::LineStyle::DotDash);
}

// 仅在第二段更改边框的线型后，
// 边框集合不再共享相同的元素。
for (int32_t i = 0; i < firstParagraphBorders->get_Count(); i++)
{
    ASSERT_FALSE(System::ObjectExt::Equals(firstParagraphBorders->idx_get(i), secondParagraphBorders->idx_get(i)));
    ASSERT_NE(System::ObjectExt::GetHashCode(firstParagraphBorders->idx_get(i)), System::ObjectExt::GetHashCode(secondParagraphBorders->idx_get(i)));

    // 更改空白边框的外观会使其可见。
    ASSERT_TRUE(secondParagraphBorders->idx_get(i)->get_IsVisible());
}

doc->Save(get_ArtifactsDir() + u"Border.SharedElements.docx");
```

## 另见

* Class [Border](../../border/)
* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
