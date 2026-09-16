---
title: "Aspose::Words::Style::get_Font 方法"
linktitle: "get_Font"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Style::get_Font 方法。获取样式的字符格式（C++）。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words/style/get_font/
---
## Style::get_Font method


获取该样式的字符格式。

```cpp
System::SharedPtr<Aspose::Words::Font> Aspose::Words::Style::get_Font()
```

## 备注


对于列表样式，此属性返回 **null**。

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


展示如何创建并使用带列表格式的段落样式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 创建自定义段落样式。
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle1");
style->get_Font()->set_Size(24);
style->get_Font()->set_Name(u"Verdana");
style->get_ParagraphFormat()->set_SpaceAfter(12);

// 创建列表，并确保使用此样式的段落将使用该列表。
style->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault));
style->get_ListFormat()->set_ListLevelNumber(0);

// 将段落样式应用于文档生成器的当前段落，然后添加一些文本。
builder->get_ParagraphFormat()->set_Style(style);
builder->Writeln(u"Hello World: MyStyle1, bulleted list.");

// 将文档生成器的样式更改为没有列表格式的样式，并写入另一段落。
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));
builder->Writeln(u"Hello World: Normal.");

builder->get_Document()->Save(get_ArtifactsDir() + u"Styles.ParagraphStyleBulletedList.docx");
```

## 另见

* Class [Font](../../font/)
* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
