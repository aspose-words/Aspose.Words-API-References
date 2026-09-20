---
title: "Aspose::Words::Lists::ListTrailingCharacter enum"
linktitle: "ListTrailingCharacter"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Lists::ListTrailingCharacter 枚举。指定在 C++ 中用于分隔列表标签和段落文本的字符。"
type: docs
weight: 9000
url: /zh/cpp/aspose.words.lists/listtrailingcharacter/
---
## ListTrailingCharacter enum


指定将列表标签与段落文本分开的字符。

```cpp
enum class ListTrailingCharacter
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| 制表符 | 0 | 制表符字符放置在列表标签和段落文本之间。 |
| 空格 | 1 | 空格字符放置在列表标签和段落文本之间。 |
| 无 | 2 | 列表标签和段落文本之间没有分隔符字符。 |

## 备注


用作 [TrailingCharacter](../listlevel/get_trailingcharacter/) 属性的取值。

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
