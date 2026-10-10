---
title: "Aspose::Words::Hyphenation::UnregisterDictionary method"
linktitle: "UnregisterDictionary"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Hyphenation::UnregisterDictionary method. 为指定语言取消注册断字字典。这不同于注册 Null 字典。取消注册字典会在 C++ 中为指定语言启用回调。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words/hyphenation/unregisterdictionary/
---
## Hyphenation::UnregisterDictionary method


为指定语言注销连字符字典。这不同于注册 Null 字典。注销字典后将启用该语言的回调。

```cpp
static void Aspose::Words::Hyphenation::UnregisterDictionary(const System::String &language)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 语言 | const System::String\& | 语言名称，例如 "en-US"。有关 "culture name" 请参阅 .NET 文档，详细信息请参阅 RFC 4646。如果 **null** 或空字符串，则所有字典都会被取消注册。 |

## 示例



展示如何注册断字字典。
```cpp
// 断字字典包含一系列字符串，用于定义该字典语言的断字规则。
// 当文档包含的文本行中，一个单词可以被拆分并在下一行继续时，
// 连字符处理将遍历字典的字符串列表，以查找该词的子字符串。
// 如果字典包含子字符串，则连字符处理会将单词拆分为两行。
// 通过该子字符串并在前半部分添加连字符。
// 从本地文件系统注册一个字典文件到 "de-CH" 区域设置。
Aspose::Words::Hyphenation::RegisterDictionary(u"de-CH", get_MyDir() + u"hyph_de_CH.dic");

ASSERT_TRUE(Aspose::Words::Hyphenation::IsDictionaryRegistered(u"de-CH"));

// 打开一个包含文本的文档，其区域设置与我们的字典匹配，
// 并将其保存为固定页格式。该文档中的文本将被断字。
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"German text.docx");

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->LINQ_OfType<System::SharedPtr<Aspose::Words::Run> >()->LINQ_All(static_cast<System::Func<System::SharedPtr<Aspose::Words::Run>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Run> r)>>([](System::SharedPtr<Aspose::Words::Run> r) -> bool
{
    return r->get_Font()->get_LocaleId() == System::MakeObject<System::Globalization::CultureInfo>(u"de-CH")->get_LCID();
}))));

doc->Save(get_ArtifactsDir() + u"Hyphenation.Dictionary.Registered.pdf");

// 在取消注册字典后重新加载文档，
// 并将其保存为另一个 PDF，该 PDF 将不包含断字文本。
Aspose::Words::Hyphenation::UnregisterDictionary(u"de-CH");

ASSERT_FALSE(Aspose::Words::Hyphenation::IsDictionaryRegistered(u"de-CH"));

doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"German text.docx");
doc->Save(get_ArtifactsDir() + u"Hyphenation.Dictionary.Unregistered.pdf");
```

## 另见

* Class [Hyphenation](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
