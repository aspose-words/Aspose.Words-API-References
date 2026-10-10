---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_SmartParagraphBreakReplacement method"
linktitle: "get_SmartParagraphBreakReplacement"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_SmartParagraphBreakReplacement 方法。获取或设置一个布尔值，指示在没有下一个兄弟段落时是否允许替换段落换行符。默认值在 C++ 中为 false。"
type: docs
weight: 16000
url: /zh/cpp/aspose.words.replacing/findreplaceoptions/get_smartparagraphbreakreplacement/
---
## FindReplaceOptions::get_SmartParagraphBreakReplacement method


获取或设置一个布尔值，指示在没有下一个同级段落时是否允许替换段落换行符。默认值为 **false**。

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_SmartParagraphBreakReplacement() const
```


## 示例



展示如何从包含嵌套表的表格单元格中删除段落。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 在第一个单元格中创建包含段落和内部表格的表格。
builder->StartTable();
builder->InsertCell();
builder->Write(u"TEXT1");
builder->StartTable();
builder->InsertCell();
builder->EndTable();
builder->EndTable();
builder->Writeln();

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
// 当以下选项设置为 'true' 时，Aspose.Words 将删除段落的文本
// 以及其段落标记全部删除。否则，Aspose.Words 将模仿 Word 并删除
// 仅删除段落的文本并保留段落标记完整（当表格紧随文本时）。
options->set_SmartParagraphBreakReplacement(isSmartParagraphBreakReplacement);
doc->get_Range()->Replace(System::MakeObject<System::Text::RegularExpressions::Regex>(u"TEXT1&p"), u"", options);

doc->Save(get_ArtifactsDir() + u"Table.RemoveParagraphTextAndMark.docx");
```

## 另见

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
