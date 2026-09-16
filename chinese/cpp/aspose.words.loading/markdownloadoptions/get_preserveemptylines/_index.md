---
title: "Aspose::Words::Loading::MarkdownLoadOptions::get_PreserveEmptyLines 方法"
linktitle: "get_PreserveEmptyLines"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Loading::MarkdownLoadOptions::get_PreserveEmptyLines 方法。获取或设置一个布尔值，指示在加载 Markdown 文档时是否保留空行。默认值为 false。通常，Markdown 中块级元素之间的空行会被忽略。文档开头和结尾的空行也会被忽略。此选项允许在 C++ 中导入这些空行。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.loading/markdownloadoptions/get_preserveemptylines/
---
## MarkdownLoadOptions::get_PreserveEmptyLines method


获取或设置一个布尔值，指示在加载 [Markdown](../../../aspose.words/loadformat/) 文档时是否保留空行。默认值为 **false**。通常，Markdown 中块级元素之间的空行会被忽略。文档开头和结尾的空行也会被忽略。此选项允许导入这些空行。

```cpp
bool Aspose::Words::Loading::MarkdownLoadOptions::get_PreserveEmptyLines() const
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
