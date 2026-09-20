---
title: "Aspose::Words::Style::get_LinkedStyleName 方法"
linktitle: "get_LinkedStyleName"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Style::get_LinkedStyleName 方法。获取/设置链接到此样式的 Style 名称。如果在 C++ 中没有链接的样式，则返回空字符串。"
type: docs
weight: 11000
url: /zh/cpp/aspose.words/style/get_linkedstylename/
---
## Style::get_LinkedStyleName method


获取/设置链接到此样式的 [Style](../) 名称。如果没有链接的样式，则返回空字符串。

```cpp
System::String Aspose::Words::Style::get_LinkedStyleName()
```

## 备注


仅允许将段落样式链接到字符样式，反之亦然。

为当前样式设置 LinkedStyleName 会自动导致为链接的样式设置 LinkedStyleName。

分配空字符串等同于取消先前链接的样式。

## 示例



展示如何使用样式别名。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Style with alias.docx");

// 此文档包含一个名为 "MyStyle,MyStyle Alias 1,MyStyle Alias 2" 的样式。
// 如果样式的名称包含多个以逗号分隔的值，则每个子句都是一个单独的别名。
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->idx_get(u"MyStyle");
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"MyStyle Alias 1", u"MyStyle Alias 2"}), style->get_Aliases());
ASSERT_EQ(u"Title", style->get_BaseStyleName());
ASSERT_EQ(u"MyStyle Char", style->get_LinkedStyleName());

// 我们可以使用样式的别名以及名称来引用它。
ASPOSE_ASSERT_EQ(doc->get_Styles()->idx_get(u"MyStyle Alias 1"), doc->get_Styles()->idx_get(u"MyStyle Alias 2"));

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"MyStyle Alias 1"));
builder->Writeln(u"Hello world!");
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"MyStyle Alias 2"));
builder->Write(u"Hello again!");

ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat()->get_Style(), doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->get_ParagraphFormat()->get_Style());
```


展示如何在样式之间进行链接。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Style> styleHeading1 = doc->get_Styles()->idx_get(Aspose::Words::StyleIdentifier::Heading1);

System::SharedPtr<Aspose::Words::Style> styleHeading1Char = doc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"Heading 1 Char");
styleHeading1Char->get_Font()->set_Name(u"Verdana");
styleHeading1Char->get_Font()->set_Bold(true);
styleHeading1Char->get_Font()->get_Border()->set_LineStyle(Aspose::Words::LineStyle::Dot);
styleHeading1Char->get_Font()->get_Border()->set_LineWidth(15);

styleHeading1->set_LinkedStyleName(u"Heading 1 Char");

ASSERT_EQ(u"Heading 1 Char", styleHeading1->get_LinkedStyleName());
ASSERT_EQ(u"Heading 1", styleHeading1Char->get_LinkedStyleName());
```

## 另见

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
