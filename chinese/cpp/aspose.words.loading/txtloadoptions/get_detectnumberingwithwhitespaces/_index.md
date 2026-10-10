---
title: "Aspose::Words::Loading::TxtLoadOptions::get_DetectNumberingWithWhitespaces 方法"
linktitle: "get_DetectNumberingWithWhitespaces"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Loading::TxtLoadOptions::get_DetectNumberingWithWhitespaces 方法。允许指定在文档从纯文本格式导入时如何识别编号列表项。默认值在 C++ 中为 true。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.loading/txtloadoptions/get_detectnumberingwithwhitespaces/
---
## TxtLoadOptions::get_DetectNumberingWithWhitespaces method


允许指定在文档从纯文本格式导入时如何识别编号列表项。默认值为 **true**。

```cpp
bool Aspose::Words::Loading::TxtLoadOptions::get_DetectNumberingWithWhitespaces() const
```

## 备注


如果此选项设置为 **false**，列表识别算法会检测列表段落，当列表编号以点、右括号或项目符号（例如 "•", "*", "-" 或 "o"）结尾时。

如果此选项设置为 **true**，空格也会用作列表编号的分隔符：阿拉伯数字编号（1., 1.1.2.）的列表识别算法同时使用空格和点（"."）符号。

## 示例



展示在加载纯文本文档时如何检测列表。
```cpp
// 在字符串中创建一个包含四个可解释为列表的独立部分的纯文本文档，
// 使用不同的分隔符。将纯文本文档加载到 "Document" 对象时，
// Aspose.Words 将始终检测到前三个列表，并会添加一个 "List" 对象
// 到文档的 "Lists" 属性中。
const System::String textDoc = System::String(u"Full stop delimiters:\n") + u"1. First list item 1\n" + u"2. First list item 2\n" + u"3. First list item 3\n\n" + u"Right bracket delimiters:\n" + u"1) Second list item 1\n" + u"2) Second list item 2\n" + u"3) Second list item 3\n\n" + u"Bullet delimiters:\n" + u"• Third list item 1\n" + u"• Third list item 2\n" + u"• Third list item 3\n\n" + u"Whitespace delimiters:\n" + u"1 Fourth list item 1\n" + u"2 Fourth list item 2\n" + u"3 Fourth list item 3";

// 创建一个 \"TxtLoadOptions\" 对象，以便我们可以将其传递给文档的构造函数
// 以修改加载纯文本文档的方式。
auto loadOptions = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();

// 将 "DetectNumberingWithWhitespaces" 属性设置为 "true" 以检测编号项
// 使用空格分隔符，例如我们文档中的第四个列表，将其识别为列表。
// 这可能会错误地将以数字开头的段落检测为列表。
// 将 "DetectNumberingWithWhitespaces" 属性设置为 "false"
// 以防止从使用空格分隔符的编号项创建列表。
loadOptions->set_DetectNumberingWithWhitespaces(detectNumberingWithWhitespaces);

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(textDoc)), loadOptions);

if (detectNumberingWithWhitespaces)
{
    ASSERT_EQ(4, doc->get_Lists()->get_Count());
    ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> p)>>([](System::SharedPtr<Aspose::Words::Node> p) -> bool
    {
        return p->GetText().Contains(u"Fourth list") && (System::ExplicitCast<Aspose::Words::Paragraph>(p))->get_IsListItem();
    }))));
}
else
{
    ASSERT_EQ(3, doc->get_Lists()->get_Count());
    ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> p)>>([](System::SharedPtr<Aspose::Words::Node> p) -> bool
    {
        return p->GetText().Contains(u"Fourth list") && (System::ExplicitCast<Aspose::Words::Paragraph>(p))->get_IsListItem();
    }))));
}
```

## 另见

* Class [TxtLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
