---
title: "Aspose::Words::Math::OfficeMath::GetMathRenderer 方法"
linktitle: "GetMathRenderer"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Math::OfficeMath::GetMathRenderer 方法。创建并返回一个可用于在 C++ 中将此公式渲染为图像的对象。"
type: docs
weight: 9000
url: /zh/cpp/aspose.words.math/officemath/getmathrenderer/
---
## OfficeMath::GetMathRenderer method


创建并返回一个可用于将此方程式渲染为图像的对象。

```cpp
System::SharedPtr<Aspose::Words::Rendering::OfficeMathRenderer> Aspose::Words::Math::OfficeMath::GetMathRenderer()
```


### ReturnValue

此公式的渲染器对象。
## 备注


此方法仅调用 [OfficeMathRenderer](../../../aspose.words.rendering/officemathrenderer/) 构造函数，并将此对象作为参数传递。

## 示例



展示如何将 Office [Math](../../) 对象渲染为本地文件系统中的图像文件。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto math = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(Aspose::Words::NodeType::OfficeMath, 0, true));

// 创建一个 "ImageSaveOptions" 对象，以传递给节点渲染器的 "Save" 方法进行修改。
// 它如何将 OfficeMath 节点渲染为图像。
auto saveOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);

// 将 "Scale" 属性设置为 5，以将对象渲染为原始大小的五倍。
saveOptions->set_Scale(5.0f);

math->GetMathRenderer()->Save(get_ArtifactsDir() + u"Shape.RenderOfficeMath.png", saveOptions);
```

## 另见

* Class [OfficeMathRenderer](../../../aspose.words.rendering/officemathrenderer/)
* Class [OfficeMath](../)
* Namespace [Aspose::Words::Math](../../)
* Library [Aspose.Words for C++](../../../)
