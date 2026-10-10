---
title: "Aspose::Words::Drawing::Fill::Patterned 方法"
linktitle: "图案"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Fill::Patterned 方法。 在 C++ 中将指定的填充设置为图案。"
type: docs
weight: 26000
url: /zh/cpp/aspose.words.drawing/fill/patterned/
---
## Fill::Patterned(Aspose::Words::Drawing::PatternType) method


将指定填充设置为图案。

```cpp
void Aspose::Words::Drawing::Fill::Patterned(Aspose::Words::Drawing::PatternType patternType)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| patternType | Aspose::Words::Drawing::PatternType | [PatternType](../../patterntype/) |

## 示例



展示如何为形状设置图案。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape stroke pattern border.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Fill> fill = shape->get_Fill();

std::cout << System::String::Format(u"Pattern value is: {0}", fill->get_Pattern()) << std::endl;

// 有几种方法可以将填充指定为图案。
// 1 -  将图案应用于形状填充：
fill->Patterned(Aspose::Words::Drawing::PatternType::DiagonalBrick);

// 2 -  将图案与前景色和背景色一起应用于形状填充：
fill->Patterned(Aspose::Words::Drawing::PatternType::DiagonalBrick, System::Drawing::Color::get_Aqua(), System::Drawing::Color::get_Bisque());

doc->Save(get_ArtifactsDir() + u"Shape.FillPattern.docx");
```

## 另见

* Enum [PatternType](../../patterntype/)
* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
## Fill::Patterned(Aspose::Words::Drawing::PatternType, System::Drawing::Color, System::Drawing::Color) method


将指定填充设置为图案。

```cpp
void Aspose::Words::Drawing::Fill::Patterned(Aspose::Words::Drawing::PatternType patternType, System::Drawing::Color foreColor, System::Drawing::Color backColor)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| patternType | Aspose::Words::Drawing::PatternType | [PatternType](../../patterntype/) |
| foreColor | System::Drawing::Color | 前景填充的颜色。 |
| backColor | System::Drawing::Color | 背景填充的颜色。 |

## 示例



展示如何为形状设置图案。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape stroke pattern border.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Fill> fill = shape->get_Fill();

std::cout << System::String::Format(u"Pattern value is: {0}", fill->get_Pattern()) << std::endl;

// 有几种方法可以将填充指定为图案。
// 1 -  将图案应用于形状填充：
fill->Patterned(Aspose::Words::Drawing::PatternType::DiagonalBrick);

// 2 -  将图案与前景色和背景色一起应用于形状填充：
fill->Patterned(Aspose::Words::Drawing::PatternType::DiagonalBrick, System::Drawing::Color::get_Aqua(), System::Drawing::Color::get_Bisque());

doc->Save(get_ArtifactsDir() + u"Shape.FillPattern.docx");
```

## 另见

* Enum [PatternType](../../patterntype/)
* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
