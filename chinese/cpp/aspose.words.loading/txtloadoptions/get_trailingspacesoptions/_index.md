---
title: "Aspose::Words::Loading::TxtLoadOptions::get_TrailingSpacesOptions 方法"
linktitle: "get_TrailingSpacesOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Loading::TxtLoadOptions::get_TrailingSpacesOptions 方法。获取或设置尾随空格处理的首选选项。默认值在 C++ 中为 Trim。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words.loading/txtloadoptions/get_trailingspacesoptions/
---
## TxtLoadOptions::get_TrailingSpacesOptions method


获取或设置尾随空格处理的首选选项。默认值为 [Trim](../../txttrailingspacesoptions/)。

```cpp
Aspose::Words::Loading::TxtTrailingSpacesOptions Aspose::Words::Loading::TxtLoadOptions::get_TrailingSpacesOptions() const
```


## 示例



展示在加载纯文本文档时如何修剪空白字符。
```cpp
System::String textDoc = System::String(u"      Line 1 \n") + u"    Line 2   \n" + u" Line 3       ";

// 创建一个 \"TxtLoadOptions\" 对象，以便我们可以将其传递给文档的构造函数
// 以修改加载纯文本文档的方式。
auto loadOptions = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();

// 将 "LeadingSpacesOptions" 属性设置为 "TxtLeadingSpacesOptions.Preserve"
// 以保留每行开头的所有空白字符。
// 将 "LeadingSpacesOptions" 属性设置为 "TxtLeadingSpacesOptions.ConvertToIndent"
// 删除每行开头的所有空白字符，
// 然后对段落应用左侧首行缩进，以模拟空白字符的效果。
// 将 "LeadingSpacesOptions" 属性设置为 "TxtLeadingSpacesOptions.Trim"
// 删除每行开头的所有空白字符。
loadOptions->set_LeadingSpacesOptions(txtLeadingSpacesOptions);

// 将 "TrailingSpacesOptions" 属性设置为 "TxtTrailingSpacesOptions.Preserve"
// 保留每行末尾的所有空白字符。
// 将 "TrailingSpacesOptions" 属性设置为 "TxtTrailingSpacesOptions.Trim" 以
// 删除每行末尾的所有空白字符。
loadOptions->set_TrailingSpacesOptions(txtTrailingSpacesOptions);

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(textDoc)), loadOptions);
System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

switch (txtLeadingSpacesOptions)
{
    case Aspose::Words::Loading::TxtLeadingSpacesOptions::ConvertToIndent:
        ASPOSE_ASSERT_EQ(37.8, paragraphs->idx_get(0)->get_ParagraphFormat()->get_FirstLineIndent());
        ASPOSE_ASSERT_EQ(25.2, paragraphs->idx_get(1)->get_ParagraphFormat()->get_FirstLineIndent());
        ASPOSE_ASSERT_EQ(6.3, paragraphs->idx_get(2)->get_ParagraphFormat()->get_FirstLineIndent());
        ASSERT_TRUE(paragraphs->idx_get(0)->GetText().StartsWith(u"Line 1"));
        ASSERT_TRUE(paragraphs->idx_get(1)->GetText().StartsWith(u"Line 2"));
        ASSERT_TRUE(paragraphs->idx_get(2)->GetText().StartsWith(u"Line 3"));
        break;

    case Aspose::Words::Loading::TxtLeadingSpacesOptions::Preserve:
        ASSERT_TRUE(paragraphs->LINQ_All(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> p)>>([](System::SharedPtr<Aspose::Words::Node> p) -> bool
        {
            return (System::ExplicitCast<Aspose::Words::Paragraph>(p))->get_ParagraphFormat()->get_FirstLineIndent() == 0.0;
        }))));
        ASSERT_TRUE(paragraphs->idx_get(0)->GetText().StartsWith(u"      Line 1"));
        ASSERT_TRUE(paragraphs->idx_get(1)->GetText().StartsWith(u"    Line 2"));
        ASSERT_TRUE(paragraphs->idx_get(2)->GetText().StartsWith(u" Line 3"));
        break;

    case Aspose::Words::Loading::TxtLeadingSpacesOptions::Trim:
        ASSERT_TRUE(paragraphs->LINQ_All(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> p)>>([](System::SharedPtr<Aspose::Words::Node> p) -> bool
        {
            return (System::ExplicitCast<Aspose::Words::Paragraph>(p))->get_ParagraphFormat()->get_FirstLineIndent() == 0.0;
        }))));
        ASSERT_TRUE(paragraphs->idx_get(0)->GetText().StartsWith(u"Line 1"));
        ASSERT_TRUE(paragraphs->idx_get(1)->GetText().StartsWith(u"Line 2"));
        ASSERT_TRUE(paragraphs->idx_get(2)->GetText().StartsWith(u"Line 3"));
        break;

}

switch (txtTrailingSpacesOptions)
{
    case Aspose::Words::Loading::TxtTrailingSpacesOptions::Preserve:
        ASSERT_TRUE(paragraphs->idx_get(0)->GetText().EndsWith(u"Line 1 \r"));
        ASSERT_TRUE(paragraphs->idx_get(1)->GetText().EndsWith(u"Line 2   \r"));
        ASSERT_TRUE(paragraphs->idx_get(2)->GetText().EndsWith(u"Line 3       \f"));
        break;

    case Aspose::Words::Loading::TxtTrailingSpacesOptions::Trim:
        ASSERT_TRUE(paragraphs->idx_get(0)->GetText().EndsWith(u"Line 1\r"));
        ASSERT_TRUE(paragraphs->idx_get(1)->GetText().EndsWith(u"Line 2\r"));
        ASSERT_TRUE(paragraphs->idx_get(2)->GetText().EndsWith(u"Line 3\f"));
        break;

}
```

## 另见

* Enum [TxtTrailingSpacesOptions](../../txttrailingspacesoptions/)
* Class [TxtLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
