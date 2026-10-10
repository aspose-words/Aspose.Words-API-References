---
title: "Aspose::Words::Lists::ListLevel class"
linktitle: "ListLevel"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Lists::ListLevel 类。定义列表级别的格式。欲了解更多，请访问 C++ 中的文档文章。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.lists/listlevel/
---
## ListLevel class


定义列表级别的格式。要了解更多信息，请访问 [Working with Lists](https://docs.aspose.com/words/cpp/working-with-lists/) 文档文章。

```cpp
class ListLevel : public Aspose::Words::IRunAttrSource
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [CreatePictureBullet](./createpicturebullet/)() | 为当前列表级别创建图片项目符号形状。 |
| [DeletePictureBullet](./deletepicturebullet/)() | 删除当前列表级别的图片项目符号。 |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Lists::ListLevel\>\&) | 与指定的 [ListLevel](./) 进行比较。 |
| [get_Alignment](./get_alignment/)() const | 获取或设置列表项实际编号的对齐方式。 |
| [get_CustomNumberStyleFormat](./get_customnumberstyleformat/)() | 获取或设置此列表级别的自定义编号样式格式。例如："a, ç, ĝ, ..."。 |
| [get_Font](./get_font/)() | 指定用于列表标签的字符格式。 |
| [get_ImageData](./get_imagedata/)() | 返回当前列表级别的图片项目符号形状的图像数据。 |
| [get_IsLegal](./get_islegal/)() const | 如果该级别将所有继承的编号转换为阿拉伯数字则为 true，否则如果保留其编号样式则为 false。 |
| [get_LinkedStyle](./get_linkedstyle/)() | 获取或设置与此列表级别关联的段落样式。 |
| [get_NumberFormat](./get_numberformat/)() const | 返回或设置列表级别的编号格式。 |
| [get_NumberPosition](./get_numberposition/)() const | 返回或设置列表级别的编号或项目符号的位置（以点为单位）。 |
| [get_NumberStyle](./get_numberstyle/)() const | 返回或设置此列表级别的编号样式。 |
| [get_RestartAfterLevel](./get_restartafterlevel/)() const | 设置或返回在指定列表级别重新开始编号之前必须出现的列表级别。 |
| [get_StartAt](./get_startat/)() | 返回或设置此列表级别的起始编号。 |
| [get_TabPosition](./get_tabposition/)() const | 返回或设置列表级别的制表位位置（以点为单位）。 |
| [get_TextPosition](./get_textposition/)() const | 返回或设置列表级别换行文本第二行的位置（以点为单位）。 |
| [get_TrailingCharacter](./get_trailingcharacter/)() const | 返回或设置列表级别在编号后插入的字符。 |
| static [GetEffectiveValue](./geteffectivevalue/)(int32_t, Aspose::Words::NumberStyle, const System::String\&) | 报告指定列表项索引的 [ListLevel](./) 对象的字符串表示形式。参数指定 [NumberStyle](../../aspose.words/numberstyle/) 并在指定 [Custom](../../aspose.words/numberstyle/) 时使用可选的格式字符串。 |
| [GetHashCode](./gethashcode/)() const override | 计算此对象的哈希码。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [RemoveTabStop](./removetabstop/)() | 从列表级别中移除制表位。 |
| [set_Alignment](./set_alignment/)(Aspose::Words::Lists::ListLevelAlignment) | 用于设置 [Aspose::Words::Lists::ListLevel::get_Alignment](./get_alignment/) 的 setter。 |
| [set_CustomNumberStyleFormat](./set_customnumberstyleformat/)(const System::String\&) | 用于设置 [Aspose::Words::Lists::ListLevel::get_CustomNumberStyleFormat](./get_customnumberstyleformat/) 的 setter。 |
| [set_IsLegal](./set_islegal/)(bool) | 用于设置 [Aspose::Words::Lists::ListLevel::get_IsLegal](./get_islegal/) 的 setter。 |
| [set_LinkedStyle](./set_linkedstyle/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | 用于设置 [Aspose::Words::Lists::ListLevel::get_LinkedStyle](./get_linkedstyle/) 的 setter。 |
| [set_NumberFormat](./set_numberformat/)(const System::String\&) | 用于设置 [Aspose::Words::Lists::ListLevel::get_NumberFormat](./get_numberformat/) 的 setter。 |
| [set_NumberPosition](./set_numberposition/)(double) | 用于设置 [Aspose::Words::Lists::ListLevel::get_NumberPosition](./get_numberposition/) 的 setter。 |
| [set_NumberStyle](./set_numberstyle/)(Aspose::Words::NumberStyle) | 用于设置 [Aspose::Words::Lists::ListLevel::get_NumberStyle](./get_numberstyle/) 的 setter。 |
| [set_RestartAfterLevel](./set_restartafterlevel/)(int32_t) | 用于设置 [Aspose::Words::Lists::ListLevel::get_RestartAfterLevel](./get_restartafterlevel/) 的 setter。 |
| [set_StartAt](./set_startat/)(int32_t) | 用于设置 [Aspose::Words::Lists::ListLevel::get_StartAt](./get_startat/) 的 setter。 |
| [set_TabPosition](./set_tabposition/)(double) | 用于设置 [Aspose::Words::Lists::ListLevel::get_TabPosition](./get_tabposition/) 的 setter。 |
| [set_TextPosition](./set_textposition/)(double) | 用于设置 [Aspose::Words::Lists::ListLevel::get_TextPosition](./get_textposition/) 的 setter。 |
| [set_TrailingCharacter](./set_trailingcharacter/)(Aspose::Words::Lists::ListTrailingCharacter) | 用于设置 [Aspose::Words::Lists::ListLevel::get_TrailingCharacter](./get_trailingcharacter/) 的 setter。 |
| static [Type](./type/)() |  |
## 备注


您不应创建此类的对象。 当创建列表时，会自动创建 [List](../list/) 级别对象。 您可以通过 [ListLevelCollection](../listlevelcollection/) 集合访问 [ListLevel](./) 对象。

使用 [ListLevel](./) 的属性来为各个列表级别指定列表格式。

## 示例



展示在使用 [DocumentBuilder](../../aspose.words/documentbuilder/) 时如何对段落应用自定义列表格式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 列表允许我们使用前缀符号和缩进来组织和装饰段落集合。
// 我们可以通过增加缩进级别来创建嵌套列表。
// 我们可以使用文档生成器的 "ListFormat" 属性来开始和结束列表。
// 我们在列表开始和结束之间添加的每个段落都会成为列表中的一项。
// 从 Microsoft Word 模板创建列表，并自定义其前两个列表级别。
System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);

System::SharedPtr<Aspose::Words::Lists::ListLevel> listLevel = list->get_ListLevels()->idx_get(0);
listLevel->get_Font()->set_Color(System::Drawing::Color::get_Red());
listLevel->get_Font()->set_Size(24);
listLevel->set_NumberStyle(Aspose::Words::NumberStyle::OrdinalText);
listLevel->set_StartAt(21);
listLevel->set_NumberFormat(u"\x0000");

listLevel->set_NumberPosition(-36);
listLevel->set_TextPosition(144);
listLevel->set_TabPosition(144);

listLevel = list->get_ListLevels()->idx_get(1);
listLevel->set_Alignment(Aspose::Words::Lists::ListLevelAlignment::Right);
listLevel->set_NumberStyle(Aspose::Words::NumberStyle::Bullet);
listLevel->get_Font()->set_Name(u"Wingdings");
listLevel->get_Font()->set_Color(System::Drawing::Color::get_Blue());
listLevel->get_Font()->set_Size(24);

// 此 NumberFormat 值将生成星形项目符号列表符号。
listLevel->set_NumberFormat(u"\xf0af");
listLevel->set_TrailingCharacter(Aspose::Words::Lists::ListTrailingCharacter::Space);
listLevel->set_NumberPosition(144);

// 创建段落并将我们自定义列表格式的两个级别应用于这些段落。
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ListFormat()->set_List(list);
builder->Writeln(u"The quick brown fox...");
builder->Writeln(u"The quick brown fox...");

builder->get_ListFormat()->ListIndent();
builder->Writeln(u"jumped over the lazy dog.");
builder->Writeln(u"jumped over the lazy dog.");

builder->get_ListFormat()->ListOutdent();
builder->Writeln(u"The quick brown fox...");

builder->get_ListFormat()->RemoveNumbers();

builder->get_Document()->Save(get_ArtifactsDir() + u"Lists.CreateCustomList.docx");
```

## 另见

* Namespace [Aspose::Words::Lists](../)
* Library [Aspose.Words for C++](../../)
