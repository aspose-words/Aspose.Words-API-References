---
title: "Aspose::Words::Style::get_ParagraphFormat 方法"
linktitle: "get_ParagraphFormat"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Style::get_ParagraphFormat 方法。获取 C++ 中样式的段落格式。"
type: docs
weight: 16000
url: /zh/cpp/aspose.words/style/get_paragraphformat/
---
## Style::get_ParagraphFormat method


获取该样式的段落格式。

```cpp
System::SharedPtr<Aspose::Words::ParagraphFormat> Aspose::Words::Style::get_ParagraphFormat()
```

## 备注


对于字符和列表样式，此属性返回 **null**。

## 示例



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

* Class [ParagraphFormat](../../paragraphformat/)
* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
