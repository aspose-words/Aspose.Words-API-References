---
title: "Aspose::Words::ParagraphFormat::get_NoSpaceBetweenParagraphsOfSameStyle 方法"
linktitle: "get_NoSpaceBetweenParagraphsOfSameStyle"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ParagraphFormat::get_NoSpaceBetweenParagraphsOfSameStyle 方法。当 **true** 时，C++ 中相同样式的段落之间的 SpaceBefore 和 SpaceAfter 将被忽略。"
type: docs
weight: 25000
url: /zh/cpp/aspose.words/paragraphformat/get_nospacebetweenparagraphsofsamestyle/
---
## ParagraphFormat::get_NoSpaceBetweenParagraphsOfSameStyle method


当 **true** 时，[SpaceBefore](../get_spacebefore/) 和 [SpaceAfter](../get_spaceafter/) 在相同样式的段落之间将被忽略。

```cpp
bool Aspose::Words::ParagraphFormat::get_NoSpaceBetweenParagraphsOfSameStyle()
```

## 备注


此设置仅在应用于段落样式时才生效。如果直接应用于段落，则没有任何效果。

## 示例



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
