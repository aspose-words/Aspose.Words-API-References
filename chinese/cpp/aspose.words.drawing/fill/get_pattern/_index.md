---
title: "Aspose::Words::Drawing::Fill::get_Pattern 方法"
linktitle: "get_Pattern"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Fill::get_Pattern 方法。获取填充的 PatternType，适用于 C++。"
type: docs
weight: 17000
url: /zh/cpp/aspose.words.drawing/fill/get_pattern/
---
## Fill::get_Pattern method


获取填充的 [PatternType](../../patterntype/)。

```cpp
Aspose::Words::Drawing::PatternType Aspose::Words::Drawing::Fill::get_Pattern()
```


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
