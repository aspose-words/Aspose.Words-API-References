---
title: "Aspose::Words::Style class"
linktitle: "Style"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Style class。表示单个内置或用户定义的样式。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 64000
url: /zh/cpp/aspose.words/style/
---
## Style class


表示单个内置或用户定义的样式。要了解更多，请访问 [Working with Styles and Themes](https://docs.aspose.com/words/cpp/working-with-styles-and-themes/) 文档文章。

```cpp
class Style : public Aspose::Words::IParaAttrSource,
              public Aspose::Words::IRunAttrSource
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | 与指定的样式进行比较。仅比较内置样式的 Styles Istds。默认样式不包含在比较中。基样式、链接样式和下一段落样式会递归比较。 |
| [get_Aliases](./get_aliases/)() | 获取此样式的所有别名。如果样式没有别名，则返回空字符串数组。 |
| [get_AutomaticallyUpdate](./get_automaticallyupdate/)() const | 指定此样式是否根据相应的值自动重新定义。 |
| [get_BaseStyleName](./get_basestylename/)() | 获取/设置此样式所基于的样式名称。 |
| [get_BuiltIn](./get_builtin/)() | 如果此样式是 MS Word 中的内置样式之一，则为 True。 |
| [get_Document](./get_document/)() | 获取所属文档。 |
| [get_Font](./get_font/)() | 获取该样式的字符格式。 |
| [get_IsHeading](./get_isheading/)() | 当样式是内置标题样式之一时，为 True。 |
| [get_IsQuickStyle](./get_isquickstyle/)() const | 指定此样式是否显示在 MS Word UI 中的快速 [Style](./) 画廊。 |
| [get_LinkedStyleName](./get_linkedstylename/)() | 获取/设置链接到此样式的 [Style](./) 名称。如果没有链接的样式，则返回空字符串。 |
| [get_List](./get_list/)() | 获取定义此列表样式格式的列表。 |
| [get_ListFormat](./get_listformat/)() | 提供对段落样式的列表格式属性的访问。 |
| [get_Locked](./get_locked/)() const | 指定此样式是否被锁定。 |
| [get_Name](./get_name/)() const | 获取或设置样式的名称。 |
| [get_NextParagraphStyleName](./get_nextparagraphstylename/)() | 获取/设置在使用指定样式格式化的段落后插入的新段落自动应用的样式名称。 |
| [get_ParagraphFormat](./get_paragraphformat/)() | 获取该样式的段落格式。 |
| [get_Priority](./get_priority/)() const | 获取/设置表示在“样式”任务窗格中对样式排序优先级的整数值。 |
| [get_SemiHidden](./get_semihidden/)() const | 获取/设置样式是否从“样式”画廊和“样式”任务窗格中隐藏。 |
| [get_StyleIdentifier](./get_styleidentifier/)() const | 获取内置样式的区域无关标识符。 |
| [get_Styles](./get_styles/)() const | 获取此样式所属的样式集合。 |
| [get_Type](./get_type/)() const | 获取样式类型（段落或字符）。 |
| [get_UnhideWhenUsed](./get_unhidewhenused/)() const | 获取/设置当前文档中使用的样式是否从“样式”画廊和“样式”任务窗格中取消隐藏。当使用的样式应显示在“样式”画廊中时，为 True。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | 从文档中移除指定的样式。 |
| [set_AutomaticallyUpdate](./set_automaticallyupdate/)(bool) | 用于设置 [Aspose::Words::Style::get_AutomaticallyUpdate](./get_automaticallyupdate/) 的 setter。 |
| [set_BaseStyleName](./set_basestylename/)(const System::String\&) | 用于设置 [Aspose::Words::Style::get_BaseStyleName](./get_basestylename/) 的 setter。 |
| [set_IsQuickStyle](./set_isquickstyle/)(bool) | 用于设置 [Aspose::Words::Style::get_IsQuickStyle](./get_isquickstyle/) 的 setter。 |
| [set_LinkedStyleName](./set_linkedstylename/)(const System::String\&) | 用于设置 [Aspose::Words::Style::get_LinkedStyleName](./get_linkedstylename/) 的 setter。 |
| [set_Locked](./set_locked/)(bool) | 用于设置 [Aspose::Words::Style::get_Locked](./get_locked/) 的 setter。 |
| [set_Name](./set_name/)(const System::String\&) | 用于设置 [Aspose::Words::Style::get_Name](./get_name/) 的 setter。 |
| [set_NextParagraphStyleName](./set_nextparagraphstylename/)(const System::String\&) | 用于设置 [Aspose::Words::Style::get_NextParagraphStyleName](./get_nextparagraphstylename/) 的 setter。 |
| [set_Priority](./set_priority/)(int32_t) | 用于设置 [Aspose::Words::Style::get_Priority](./get_priority/) 的 setter。 |
| [set_SemiHidden](./set_semihidden/)(bool) | 用于设置 [Aspose::Words::Style::get_SemiHidden](./get_semihidden/) 的 setter。 |
| [set_UnhideWhenUsed](./set_unhidewhenused/)(bool) | 用于设置 [Aspose::Words::Style::get_UnhideWhenUsed](./get_unhidewhenused/) 的 setter。 |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
