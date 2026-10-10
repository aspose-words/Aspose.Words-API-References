---
title: "Aspose::Words::Loading::HtmlLoadOptions::get_SupportVml 方法"
linktitle: "get_SupportVml"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Loading::HtmlLoadOptions::get_SupportVml 方法。获取或设置一个值，以指示是否在 C++ 中支持 VML 图像。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words.loading/htmlloadoptions/get_supportvml/
---
## HtmlLoadOptions::get_SupportVml method


获取或设置一个值，指示是否支持 VML 图像。

```cpp
bool Aspose::Words::Loading::HtmlLoadOptions::get_SupportVml() const
```


## 示例



展示如何在加载 HTML 文档时支持条件注释。
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();

// 如果该值为 true，则在解析加载的文档时会考虑 VML 代码。
loadOptions->set_SupportVml(supportVml);

// 此文档在 "<!--[if gte vml 1]>" 标记中包含 JPEG 图像，
// 并且在 "<![if !vml]>" 标记中包含不同的 PNG 图像。
// 如果我们将 "SupportVml" 标志设置为 "true"，则 Aspose.Words 将加载 JPEG。
// 如果我们将此标志设置为 "false"，则 Aspose.Words 只会加载 PNG。
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"VML conditional.htm", loadOptions);

if (supportVml)
{
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Jpeg, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_ImageData()->get_ImageType());
}
else
{
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Png, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_ImageData()->get_ImageType());
}
```

## 另见

* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
