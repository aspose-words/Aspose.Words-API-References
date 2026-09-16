---
title: "Aspose::Words::Loading::HtmlLoadOptions::HtmlLoadOptions 构造函数"
linktitle: "HtmlLoadOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Loading::HtmlLoadOptions::HtmlLoadOptions 构造函数。在 C++ 中使用默认值初始化此类的新实例。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.loading/htmlloadoptions/htmlloadoptions/
---
## HtmlLoadOptions::HtmlLoadOptions() constructor


使用默认值初始化此类的新实例。

```cpp
Aspose::Words::Loading::HtmlLoadOptions::HtmlLoadOptions()
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
## HtmlLoadOptions::HtmlLoadOptions(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) constructor


使用属性设置为指定值，以快捷方式初始化此类的新实例。

```cpp
Aspose::Words::Loading::HtmlLoadOptions::HtmlLoadOptions(Aspose::Words::LoadFormat loadFormat, const System::String &password, const System::String &baseUri)
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
* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
## HtmlLoadOptions::HtmlLoadOptions(const System::String\&) constructor


使用指定密码加载加密文档，以快捷方式初始化此类的新实例。

```cpp
Aspose::Words::Loading::HtmlLoadOptions::HtmlLoadOptions(const System::String &password)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 密码 | const System::String\& | 用于打开加密文档的密码。可以是 **null** 或空字符串。 |

## 示例



展示如何加密 Html 文档，然后使用密码打开它。
```cpp
// 从加密的 .docx 创建并签署加密的 HTML 文档。
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_Comments(u"Comment");
signOptions->set_SignTime(System::DateTime::get_Now());
signOptions->set_DecryptionPassword(u"docPassword");

System::String inputFileName = get_MyDir() + u"Encrypted.docx";
System::String outputFileName = get_ArtifactsDir() + u"HtmlLoadOptions.EncryptedHtml.html";
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(inputFileName, outputFileName, certificateHolder, signOptions);

// 要加载并读取此文档，我们需要传递其解密
// 密码，使用 HtmlLoadOptions 对象。
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>(u"docPassword");

ASSERT_EQ(signOptions->get_DecryptionPassword(), loadOptions->get_Password());

auto doc = System::MakeObject<Aspose::Words::Document>(outputFileName, loadOptions);

ASSERT_EQ(u"Test encrypted document.", doc->GetText().Trim());
```

## 另见

* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
