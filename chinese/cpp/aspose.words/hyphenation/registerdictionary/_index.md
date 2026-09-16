---
title: "Aspose::Words::Hyphenation::RegisterDictionary method"
linktitle: "RegisterDictionary"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Hyphenation::RegisterDictionary method. 从流中为指定语言注册并加载断字字典。如果字典无法读取或格式无效，则在 C++ 中抛出异常。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words/hyphenation/registerdictionary/
---
## Hyphenation::RegisterDictionary(const System::String\&, const System::SharedPtr\<System::IO::Stream\>\&) method


从流中为指定语言注册并加载连字符字典。如果字典无法读取或格式无效，则抛出异常。

```cpp
static void Aspose::Words::Hyphenation::RegisterDictionary(const System::String &language, const System::SharedPtr<System::IO::Stream> &stream)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 语言 | const System::String\& | 语言名称，例如 "en-US"。有关 "culture name" 请参阅 .NET 文档，详细信息请参阅 RFC 4646。 |
| 流 | const System::SharedPtr\<System::IO::Stream\>\& | OpenOffice 格式的字典文件的流。 |

## 另见

* Class [Hyphenation](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Hyphenation::RegisterDictionary(const System::String\&, const System::String\&) method


从文件为指定语言注册并加载断字字典。如果字典无法读取或格式无效，则会抛出异常。此方法还可用于注册 Null 字典，以防止对同一语言重复调用 [Callback](../get_callback/)。

```cpp
static void Aspose::Words::Hyphenation::RegisterDictionary(const System::String &language, const System::String &fileName)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 语言 | const System::String\& | 语言名称，例如 "en-US"。有关 "culture name" 请参阅 .NET 文档，详细信息请参阅 RFC 4646。 |
| fileName | const System::String\& | Open Office 格式的字典文件路径。如果此参数为 **null** 或空字符串，则注册的是 Null 字典，且不再为该语言调用回调。要再次启用回调，请使用 [UnregisterDictionary()](../) 方法。 |

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
## Hyphenation::RegisterDictionary(System::String, std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> static void Aspose::Words::Hyphenation::RegisterDictionary(System::String language, std::basic_istream<CharType, Traits> &stream)
```

## 另见

* Class [Hyphenation](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
