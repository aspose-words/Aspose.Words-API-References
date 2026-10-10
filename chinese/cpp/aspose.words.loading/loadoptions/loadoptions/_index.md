---
title: "Aspose::Words::Loading::LoadOptions::LoadOptions 构造函数"
linktitle: "LoadOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Loading::LoadOptions::LoadOptions 构造函数。用 C++ 中的默认值初始化此类的一个新实例。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.loading/loadoptions/loadoptions/
---
## LoadOptions::LoadOptions() constructor


使用默认值初始化此类的新实例。

```cpp
Aspose::Words::Loading::LoadOptions::LoadOptions()
```


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
## LoadOptions::LoadOptions(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) constructor


使用属性设置为指定值，以快捷方式初始化此类的新实例。

```cpp
Aspose::Words::Loading::LoadOptions::LoadOptions(Aspose::Words::LoadFormat loadFormat, const System::String &password, const System::String &baseUri)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| loadFormat | Aspose::Words::LoadFormat | 要加载的文档的格式。 |
| 密码 | const System::String\& | 用于打开加密文档的密码。可以是 **null** 或空字符串。 |
| baseUri | const System::String\& | 用于将相对 URI 解析为绝对路径的字符串。可以是 **null** 或空字符串。 |

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
## LoadOptions::LoadOptions(const System::String\&) constructor


使用指定密码加载加密文档，以快捷方式初始化此类的新实例。

```cpp
Aspose::Words::Loading::LoadOptions::LoadOptions(const System::String &password)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 密码 | const System::String\& | 用于打开加密文档的密码。可以是 **null** 或空字符串。 |

## 示例



展示如何加载加密的 Microsoft Word 文档。
```cpp
System::SharedPtr<Aspose::Words::Document> doc;

// 如果尝试在没有密码的情况下打开加密文档，Aspose.Words 会抛出异常。
ASSERT_THROW(static_cast<std::function<void()>>([&doc]() -> void
{
    doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx");
})(), Aspose::Words::IncorrectPasswordException);

// 在加载此类文档时，密码通过 LoadOptions 对象传递给文档的构造函数。
auto options = System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"docPassword");

// 使用 LoadOptions 对象加载加密文档有两种方式。
// 1 -  通过文件名从本地文件系统加载文档：
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx", options);

// 2 -  从流中加载文档：
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Encrypted.docx");
    doc = System::MakeObject<Aspose::Words::Document>(stream, options);
}
```

## 另见

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
