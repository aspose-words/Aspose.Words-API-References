---
title: "Aspose::Words::StyleCollection 类"
linktitle: "StyleCollection"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::StyleCollection 类。一个 Style 对象的集合，表示文档中内置和用户自定义的样式。了解更多，请访问 C++ 文档文章。"
type: docs
weight: 65000
url: /zh/cpp/aspose.words/stylecollection/
---
## StyleCollection class


一个 [Style](../style/) 对象的集合，表示文档中内置和用户自定义的样式。了解更多，请访问 [Working with Styles and Themes](https://docs.aspose.com/words/cpp/working-with-styles-and-themes/) 文档文章。

```cpp
class StyleCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Style>>
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Add](./add/)(Aspose::Words::StyleType, const System::String\&) | 创建一个新的用户自定义样式并将其添加到集合中。 |
| [AddCopy](./addcopy/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | 将样式复制到此集合中。 |
| [ClearQuickStyleGallery](./clearquickstylegallery/)() | 从快速 [Style](../style/) 画廊面板中移除所有样式。 |
| [get_Count](./get_count/)() | 获取集合中样式的数量。 |
| [get_DefaultFont](./get_defaultfont/)() | 获取文档默认的文本格式。 |
| [get_DefaultParagraphFormat](./get_defaultparagraphformat/)() | 获取文档默认的段落格式。 |
| [get_Document](./get_document/)() const | 获取所属文档。 |
| [GetEnumerator](./getenumerator/)() override | 获取一个枚举器对象，用于按名称的字母顺序枚举样式。 |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | 按名称或别名获取样式。 |
| [idx_get](./idx_get/)(Aspose::Words::StyleIdentifier) | 通过其与区域无关的标识符获取内置样式。 |
| [idx_get](./idx_get/)(int32_t) | 按索引获取样式。 |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
