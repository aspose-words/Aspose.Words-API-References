---
title: "Aspose::Words::Loading::MarkdownLoadOptions::MarkdownLoadOptions 构造函数"
linktitle: "MarkdownLoadOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Loading::MarkdownLoadOptions::MarkdownLoadOptions 构造函数。初始化一个在 C++ 中的 MarkdownLoadOptions 类的新实例。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.loading/markdownloadoptions/markdownloadoptions/
---
## MarkdownLoadOptions::MarkdownLoadOptions constructor


初始化 [MarkdownLoadOptions](../) 类的新实例。

```cpp
Aspose::Words::Loading::MarkdownLoadOptions::MarkdownLoadOptions()
```


## 示例



展示如何在加载文档时保留空行。
```cpp
System::String mdText = System::String::Format(u"{0}Line1{1}{2}Line2{3}{4}", System::Environment::get_NewLine(), System::Environment::get_NewLine(), System::Environment::get_NewLine(), System::Environment::get_NewLine(), System::Environment::get_NewLine());
{
    auto stream = System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(mdText));
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::MarkdownLoadOptions>();
    loadOptions->set_PreserveEmptyLines(true);
    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    ASSERT_EQ(u"\rLine1\r\rLine2\r\f", doc->GetText());
}
```

## 另见

* Class [MarkdownLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
