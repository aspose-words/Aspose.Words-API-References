---
title: "Aspose::Words::Hyphenation::IsDictionaryRegistered 方法"
linktitle: "IsDictionaryRegistered"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Hyphenation::IsDictionaryRegistered 方法。若指定语言没有已注册的字典或已注册的字典为 Null，则返回 false；否则在 C++ 中返回 true。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words/hyphenation/isdictionaryregistered/
---
## Hyphenation::IsDictionaryRegistered method


如果指定语言没有注册字典或注册的是 Null 字典，则返回 **false**，否则返回 **true**。

```cpp
static bool Aspose::Words::Hyphenation::IsDictionaryRegistered(const System::String &language)
```


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
