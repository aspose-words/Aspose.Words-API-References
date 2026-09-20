---
title: "Aspose::Words::DocumentBuilder::InsertShape 方法"
linktitle: "InsertShape"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentBuilder::InsertShape 方法。在 C++ 中插入具有指定位置、大小和文本换行类型的自由浮动形状。"
type: docs
weight: 45000
url: /zh/cpp/aspose.words/documentbuilder/insertshape/
---
## DocumentBuilder::InsertShape(Aspose::Words::Drawing::ShapeType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


插入具有指定位置、大小和文本环绕类型的自由浮动形状。

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertShape(Aspose::Words::Drawing::ShapeType shapeType, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| shapeType | Aspose::Words::Drawing::ShapeType | 要插入到文档中的形状类型 |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | 指定相对于形状的水平距离的测量基准。 |
| left | double | 从原点到形状左侧的距离（以点为单位）。 |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | 指定相对于形状的垂直距离的测量基准。 |
| top | double | 从原点到形状顶部的距离（以点为单位）。 |
| width | double | 形状的宽度（以点为单位）。 |
| height | double | 形状的高度（以点为单位）。 |
| wrapType | Aspose::Words::Drawing::WrapType | 指定文本如何环绕形状换行。 |

### ReturnValue

已插入的形状节点。

## 示例



展示如何向文档插入 DML 形状。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 以下是形状可能具有的两种环绕类型。
// 1 -  浮动：
builder->InsertShape(Aspose::Words::Drawing::ShapeType::TopCornersRounded, Aspose::Words::Drawing::RelativeHorizontalPosition::Page, 100, Aspose::Words::Drawing::RelativeVerticalPosition::Page, 100, 50, 50, Aspose::Words::Drawing::WrapType::None);

// 2 -  行内：
builder->InsertShape(Aspose::Words::Drawing::ShapeType::DiagonalCornersRounded, 50, 50);

// 如果您需要创建 \"non-primitive\" 形状，例如 SingleCornerSnipped、TopCornersSnipped、DiagonalCornersSnipped，
// TopCornersOneRoundedOneSnipped、SingleCornerRounded、TopCornersRounded 或 DiagonalCornersRounded，
// 那么请使用 \"Strict\" 或 \"Transitional\" 合规性保存文档，这允许将形状保存为 DML。
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx);
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Transitional);

doc->Save(get_ArtifactsDir() + u"Shape.ShapeInsertion.docx", saveOptions);
```

## 另见

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ShapeType](../../../aspose.words.drawing/shapetype/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertShape(Aspose::Words::Drawing::ShapeType, double, double) method


插入具有指定类型和大小的内联形状。

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertShape(Aspose::Words::Drawing::ShapeType shapeType, double width, double height)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| shapeType | Aspose::Words::Drawing::ShapeType | 要插入到文档中的形状类型。 |
| width | double | 形状的宽度（以点为单位）。 |
| height | double | 形状的高度（以点为单位）。 |

### ReturnValue

已插入的形状节点。

## 示例



展示如何向文档插入 DML 形状。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 以下是形状可能具有的两种环绕类型。
// 1 -  浮动：
builder->InsertShape(Aspose::Words::Drawing::ShapeType::TopCornersRounded, Aspose::Words::Drawing::RelativeHorizontalPosition::Page, 100, Aspose::Words::Drawing::RelativeVerticalPosition::Page, 100, 50, 50, Aspose::Words::Drawing::WrapType::None);

// 2 -  行内：
builder->InsertShape(Aspose::Words::Drawing::ShapeType::DiagonalCornersRounded, 50, 50);

// 如果您需要创建 \"non-primitive\" 形状，例如 SingleCornerSnipped、TopCornersSnipped、DiagonalCornersSnipped，
// TopCornersOneRoundedOneSnipped、SingleCornerRounded、TopCornersRounded 或 DiagonalCornersRounded，
// 那么请使用 \"Strict\" 或 \"Transitional\" 合规性保存文档，这允许将形状保存为 DML。
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx);
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Transitional);

doc->Save(get_ArtifactsDir() + u"Shape.ShapeInsertion.docx", saveOptions);
```

## 另见

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ShapeType](../../../aspose.words.drawing/shapetype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
