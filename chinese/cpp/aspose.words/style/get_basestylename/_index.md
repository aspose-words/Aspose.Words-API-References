---
title: "Aspose::Words::Style::get_BaseStyleName 方法"
linktitle: "get_BaseStyleName"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Style::get_BaseStyleName 方法。获取/设置 C++ 中此样式所基于的样式名称。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words/style/get_basestylename/
---
## Style::get_BaseStyleName method


获取/设置此样式所基于的样式名称。

```cpp
System::String Aspose::Words::Style::get_BaseStyleName()
```


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

## 另见

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
