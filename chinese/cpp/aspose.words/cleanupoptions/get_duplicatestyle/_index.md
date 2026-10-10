---
title: "Aspose::Words::CleanupOptions::get_DuplicateStyle 方法"
linktitle: "get_DuplicateStyle"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::CleanupOptions::get_DuplicateStyle 方法。获取/设置一个标志，指示是否应从文档中删除重复样式。默认值在 C++ 中为 false。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words/cleanupoptions/get_duplicatestyle/
---
## CleanupOptions::get_DuplicateStyle method


获取/设置一个标志，指示是否应从文档中删除重复样式。默认值为 **false**。

```cpp
bool Aspose::Words::CleanupOptions::get_DuplicateStyle() const
```


## 示例



展示如何从文档中删除重复的样式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 向文档添加两个具有相同属性的样式，
// 但名称不同。第二个样式被视为第一个的重复。
System::SharedPtr<Aspose::Words::Style> myStyle = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle1");
myStyle->get_Font()->set_Size(14);
myStyle->get_Font()->set_Name(u"Courier New");
myStyle->get_Font()->set_Color(System::Drawing::Color::get_Blue());

System::SharedPtr<Aspose::Words::Style> duplicateStyle = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle2");
duplicateStyle->get_Font()->set_Size(14);
duplicateStyle->get_Font()->set_Name(u"Courier New");
duplicateStyle->get_Font()->set_Color(System::Drawing::Color::get_Blue());

ASSERT_EQ(6, doc->get_Styles()->get_Count());

// 将这两种样式应用于文档中的不同段落。
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->get_ParagraphFormat()->set_StyleName(myStyle->get_Name());
builder->Writeln(u"Hello world!");

builder->get_ParagraphFormat()->set_StyleName(duplicateStyle->get_Name());
builder->Writeln(u"Hello again!");

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

ASPOSE_ASSERT_EQ(myStyle, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Style());
ASPOSE_ASSERT_EQ(duplicateStyle, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Style());

// 配置一个 CleanOptions 对象，然后调用 Cleanup 方法来替换所有重复的样式
// 使用原始样式，并从文档中删除重复项。
auto cleanupOptions = System::MakeObject<Aspose::Words::CleanupOptions>();
cleanupOptions->set_DuplicateStyle(true);

doc->Cleanup(cleanupOptions);

ASSERT_EQ(5, doc->get_Styles()->get_Count());
ASPOSE_ASSERT_EQ(myStyle, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Style());
ASPOSE_ASSERT_EQ(myStyle, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Style());
```

## 另见

* Class [CleanupOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
