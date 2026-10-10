---
title: "Aspose::Words::Style::get_AutomaticallyUpdate 方法"
linktitle: "get_AutomaticallyUpdate"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Style::get_AutomaticallyUpdate 方法。指定此样式是否根据 C++ 中的相应值自动重新定义。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words/style/get_automaticallyupdate/
---
## Style::get_AutomaticallyUpdate method


指定此样式是否根据相应的值自动重新定义。

```cpp
bool Aspose::Words::Style::get_AutomaticallyUpdate() const
```

## 备注


如果属性值设置为 true，MS Word 会在相应的段落格式被更改后自动重新定义当前样式。

AutomaticallyUpdate 属性仅适用于段落样式。

默认值为 **false**。

## 示例



展示如何创建并应用自定义样式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");
style->get_Font()->set_Name(u"Times New Roman");
style->get_Font()->set_Size(16);
style->get_Font()->set_Color(System::Drawing::Color::get_Navy());
// 自动重新定义样式。
style->set_AutomaticallyUpdate(true);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 将文档中的一种样式应用于文档生成器正在创建的段落。
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"MyStyle"));
builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Style> firstParagraphStyle = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Style();

ASPOSE_ASSERT_EQ(style, firstParagraphStyle);

// 从文档的样式集合中移除我们的自定义样式。
doc->get_Styles()->idx_get(u"MyStyle")->Remove();

firstParagraphStyle = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Style();

// 任何使用了已移除样式的文本将恢复为默认格式。
ASSERT_FALSE(doc->get_Styles()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Style>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Style> s)>>([](System::SharedPtr<Aspose::Words::Style> s) -> bool
{
    return s->get_Name() == u"MyStyle";
}))));
ASSERT_EQ(u"Times New Roman", firstParagraphStyle->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(12.0, firstParagraphStyle->get_Font()->get_Size());
ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), firstParagraphStyle->get_Font()->get_Color().ToArgb());
```

## 另见

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
