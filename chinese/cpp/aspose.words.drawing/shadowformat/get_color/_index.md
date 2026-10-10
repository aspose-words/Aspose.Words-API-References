---
title: "Aspose::Words::Drawing::ShadowFormat::get_Color 方法"
linktitle: "get_Color"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::ShadowFormat::get_Color 方法。获取或设置表示阴影颜色的 Color 对象。默认值在 C++ 中为 Black。"
type: docs
weight: 2500
url: /zh/cpp/aspose.words.drawing/shadowformat/get_color/
---
## ShadowFormat::get_Color method


获取或设置一个 **Color** 对象，表示阴影的颜色。默认值是 **Black**。

```cpp
System::Drawing::Color Aspose::Words::Drawing::ShadowFormat::get_Color()
```


## 示例



展示如何获取阴影颜色。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shadow color.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::ShadowFormat> shadowFormat = shape->get_ShadowFormat();

ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), shadowFormat->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::Drawing::ShadowType::ShadowMixed, shadowFormat->get_Type());
```


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
