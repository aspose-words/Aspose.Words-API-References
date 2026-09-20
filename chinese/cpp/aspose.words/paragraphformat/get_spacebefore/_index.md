---
title: "Aspose::Words::ParagraphFormat::get_SpaceBefore 方法"
linktitle: "get_SpaceBefore"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ParagraphFormat::get_SpaceBefore 方法。获取或设置段落前的间距量（以点为单位）（在 C++ 中）。"
type: docs
weight: 33000
url: /zh/cpp/aspose.words/paragraphformat/get_spacebefore/
---
## ParagraphFormat::get_SpaceBefore method


获取或设置段落之前的间距量（以点为单位）。

```cpp
double Aspose::Words::ParagraphFormat::get_SpaceBefore()
```

## 备注


当 [SpaceBeforeAuto](../get_spacebeforeauto/) 为 **true** 时无效。

有效值范围为 0 到 1584（含）。

## 示例



展示如何设置自动段落间距。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 在此生成器将创建的段落前后应用大量间距。
builder->get_ParagraphFormat()->set_SpaceBefore(24);
builder->get_ParagraphFormat()->set_SpaceAfter(24);

// 将这些标志设置为 "true" 以应用自动间距，
// 实际上会忽略我们上面设置的属性中的间距。
// 将它们保留为 "false" 将应用我们的自定义段落间距。
builder->get_ParagraphFormat()->set_SpaceAfterAuto(autoSpacing);
builder->get_ParagraphFormat()->set_SpaceBeforeAuto(autoSpacing);

// 插入两个段落，使其上下都有间距，并保存文档。
builder->Writeln(u"Paragraph 1.");
builder->Writeln(u"Paragraph 2.");

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.ParagraphSpacingAuto.docx");
```


展示如何在相同样式的段落之间应用无间距。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 在此生成器将创建的段落前后应用大量间距。
builder->get_ParagraphFormat()->set_SpaceBefore(24);
builder->get_ParagraphFormat()->set_SpaceAfter(24);

// 将 "NoSpaceBetweenParagraphsOfSameStyle" 标志设置为 "true" 以应用
// 相同样式的段落之间不留间距，这将把相似的段落归为一组。
// 将 "NoSpaceBetweenParagraphsOfSameStyle" 标志保持为 "false"
// 以均匀地对每个段落应用间距。
builder->get_ParagraphFormat()->set_NoSpaceBetweenParagraphsOfSameStyle(noSpaceBetweenParagraphsOfSameStyle);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Quote"));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.ParagraphSpacingSameStyle.docx");
```

## 另见

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
