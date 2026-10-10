---
title: "Aspose::Words::ParagraphFormat::get_Style method"
linktitle: "get_Style"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ParagraphFormat::get_Style 方法。获取或设置在 C++ 中应用于此格式的段落样式。"
type: docs
weight: 35000
url: /zh/cpp/aspose.words/paragraphformat/get_style/
---
## ParagraphFormat::get_Style method


获取或设置应用于此格式的段落样式。

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::ParagraphFormat::get_Style()
```


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

* Class [Style](../../style/)
* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
