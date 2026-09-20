---
title: "Aspose::Words::Drawing::ShadowFormat::get_Transparency 方法"
linktitle: "get_Transparency"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::ShadowFormat::get_Transparency 方法。获取或设置阴影效果的透明度，取值范围为 0.0（不透明）和 1.0（透明）。默认值在 C++ 中为 0.0。"
type: docs
weight: 2750
url: /zh/cpp/aspose.words.drawing/shadowformat/get_transparency/
---
## ShadowFormat::get_Transparency method


获取或设置阴影效果的透明度程度，取值范围为 0.0（不透明）到 1.0（透明）。默认值为 0.0。

```cpp
double Aspose::Words::Drawing::ShadowFormat::get_Transparency()
```


## 示例



展示如何设置具有透明度的颜色。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shadow color.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

System::SharedPtr<Aspose::Words::Drawing::ShadowFormat> shadowFormat = shape->get_ShadowFormat();
shadowFormat->set_Type(Aspose::Words::Drawing::ShadowType::Shadow21);
shadowFormat->set_Color(System::Drawing::Color::get_Red());
shadowFormat->set_Transparency(0.8);

doc->Save(get_ArtifactsDir() + u"Shape.ShadowFormatTransparency.docx");
```

## 另见

* Class [ShadowFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
