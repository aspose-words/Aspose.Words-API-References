---
title: "Aspose::Words::Loading::LoadOptions::get_BaseUri 方法"
linktitle: "get_BaseUri"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Loading::LoadOptions::get_BaseUri 方法。获取或设置在需要时用于将文档中找到的相对 URI 解析为绝对 URI 的字符串。可以为 null 或空字符串。默认在 C++ 中为 null。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.loading/loadoptions/get_baseuri/
---
## LoadOptions::get_BaseUri method


获取或设置将在需要时用于将文档中找到的相对 URI 解析为绝对 URI 的字符串。可以为 **null** 或空字符串。默认值为 **null**。

```cpp
System::String Aspose::Words::Loading::LoadOptions::get_BaseUri() const
```

## 备注


此属性在以下情况下用于将相对 URI 解析为绝对 URI：

1. 当从流加载 HTML 文档且文档包含带有相对 URI 的图像且在 BASE HTML 元素中未指定基础 URI 时。
1. 当将文档保存为 PDF 等格式时，检索使用相对 URI 链接的图像，以便将这些图像保存到输出文档中。



## 示例



展示如何使用基础 URI 从流中打开带有图像的 HTML 文档。
```cpp
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Document.html");
    // 在加载时传递基础文件夹的 URI
    // 以便能够找到 HTML 文档中任何带有相对 URI 的图像。
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
    loadOptions->set_BaseUri(get_ImageDir());

    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    // 验证文档的第一个形状包含有效的图像。
    auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

    ASSERT_TRUE(shape->get_IsImage());
    ASSERT_FALSE(System::TestTools::IsNull(shape->get_ImageData()->get_ImageBytes()));
    ASSERT_NEAR(32.0, Aspose::Words::ConvertUtil::PointToPixel(shape->get_Width()), 0.01);
    ASSERT_NEAR(32.0, Aspose::Words::ConvertUtil::PointToPixel(shape->get_Height()), 0.01);
}
```

## 另见

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
