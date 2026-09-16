---
title: "Aspose::Words::Loading::MarkdownLoadOptions::get_SoftLineBreakCharacter 方法"
linktitle: "get_SoftLineBreakCharacter"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Loading::MarkdownLoadOptions::get_SoftLineBreakCharacter 方法。获取或设置表示软换行的字符值。默认值在 C++ 中为 SPACE (U+0020)。"
type: docs
weight: 4500
url: /zh/cpp/aspose.words.loading/markdownloadoptions/get_softlinebreakcharacter/
---
## MarkdownLoadOptions::get_SoftLineBreakCharacter method


获取或设置一个字符值，表示 **soft line break**。默认值为 **SPACE (U+0020)**。

```cpp
char16_t Aspose::Words::Loading::MarkdownLoadOptions::get_SoftLineBreakCharacter() const
```


## 示例



展示如何设置软换行字符。
```cpp
{
    auto stream = System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(u"line1\nline2"));
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::MarkdownLoadOptions>();
    loadOptions->set_SoftLineBreakCharacter(Aspose::Words::ControlChar::LineBreakChar);
    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    ASSERT_EQ(u"line1\u000bline2", doc->GetText().Trim());
}
```

## 另见

* Class [MarkdownLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
