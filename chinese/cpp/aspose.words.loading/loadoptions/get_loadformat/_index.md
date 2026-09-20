---
title: "Aspose::Words::Loading::LoadOptions::get_LoadFormat 方法"
linktitle: "get_LoadFormat"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Loading::LoadOptions::get_LoadFormat 方法。指定要加载的文档的格式。默认在 C++ 中为 Auto。"
type: docs
weight: 10000
url: /zh/cpp/aspose.words.loading/loadoptions/get_loadformat/
---
## LoadOptions::get_LoadFormat method


指定要加载的文档的格式。默认是 [Auto](../../../aspose.words/loadformat/)。

```cpp
Aspose::Words::LoadFormat Aspose::Words::Loading::LoadOptions::get_LoadFormat() const
```

## 备注


建议您指定 [Auto](../../../aspose.words/loadformat/) 值，并让 Aspose.Words 自动检测文件格式。如果您已知即将加载的文档的格式，可以显式指定该格式，这将略微减少因自动检测格式而产生的开销，从而缩短加载时间。如果您指定了显式的加载格式但结果错误，将会触发自动检测并进行第二次加载尝试。

## 示例



展示在打开 html 文档时如何指定基础 URI。
```cpp
// 假设我们想加载一个包含相对 URI 链接图像的 .html 文档
// 而图像位于不同的位置。在这种情况下，我们需要将相对 URI 解析为绝对 URI。
// 我们可以使用 HtmlLoadOptions 对象提供基础 URI。
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>(Aspose::Words::LoadFormat::Html, u"", get_ImageDir());

ASSERT_EQ(Aspose::Words::LoadFormat::Html, loadOptions->get_LoadFormat());

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing image.html", loadOptions);

// 虽然图像在输入的 .html 中损坏，但我们的自定义基础 URI 帮助我们修复了链接。
auto imageShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));
ASSERT_TRUE(imageShape->get_IsImage());

// 此输出文档将显示缺失的图像。
doc->Save(get_ArtifactsDir() + u"HtmlLoadOptions.BaseUri.docx");
```

## 另见

* Enum [LoadFormat](../../../aspose.words/loadformat/)
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
