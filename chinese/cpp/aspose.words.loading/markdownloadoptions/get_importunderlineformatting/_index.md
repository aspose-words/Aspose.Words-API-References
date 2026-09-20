---
title: "Aspose::Words::Loading::MarkdownLoadOptions::get_ImportUnderlineFormatting 方法"
linktitle: "get_ImportUnderlineFormatting"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Loading::MarkdownLoadOptions::get_ImportUnderlineFormatting 方法。获取或设置一个布尔值，指示是否将两个加号 \"++\" 的序列识别为下划线文本格式。默认值在 C++ 中为 false。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.loading/markdownloadoptions/get_importunderlineformatting/
---
## MarkdownLoadOptions::get_ImportUnderlineFormatting method


获取或设置一个布尔值，指示是否将两个加号字符 "++" 识别为下划线文本格式。默认值为 **false**。

```cpp
bool Aspose::Words::Loading::MarkdownLoadOptions::get_ImportUnderlineFormatting() const
```


## 示例



展示如何将加号 "++" 识别为下划线文本格式。
```cpp
{
    auto stream = System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_ASCII()->GetBytes(u"++12 and B++"));
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::MarkdownLoadOptions>();
    loadOptions->set_ImportUnderlineFormatting(true);
    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    auto para = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));
    ASSERT_EQ(Aspose::Words::Underline::Single, para->get_Runs()->idx_get(0)->get_Font()->get_Underline());

    loadOptions = System::MakeObject<Aspose::Words::Loading::MarkdownLoadOptions>();
    loadOptions->set_ImportUnderlineFormatting(false);
    doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    para = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));
    ASSERT_EQ(Aspose::Words::Underline::None, para->get_Runs()->idx_get(0)->get_Font()->get_Underline());
}
```

## 另见

* Class [MarkdownLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
