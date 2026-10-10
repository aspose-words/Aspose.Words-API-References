---
title: "Aspose::Words::ParagraphFormat::get_OutlineLevel 方法"
linktitle: "get_OutlineLevel"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ParagraphFormat::get_OutlineLevel 方法。指定文档中段落的提纲级别，适用于 C++。"
type: docs
weight: 26000
url: /zh/cpp/aspose.words/paragraphformat/get_outlinelevel/
---
## ParagraphFormat::get_OutlineLevel method


指定段落在文档中的大纲级别。

```cpp
Aspose::Words::OutlineLevel Aspose::Words::ParagraphFormat::get_OutlineLevel()
```


## 示例



展示如何配置段落大纲级别以创建可折叠的文本。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 每个段落都有一个 OutlineLevel，可以是 1 到 9 的任意数字，或使用默认的 "BodyText" 值。
// 将属性设置为其中一个编号值将会在左侧显示一个箭头
// 位于段落开头。
builder->get_ParagraphFormat()->set_OutlineLevel(Aspose::Words::OutlineLevel::Level1);
builder->Writeln(u"Paragraph outline level 1.");

// 级别 1 是最高级别。如果在较高级别的段落下面有一个较低级别的段落，
// 折叠较高级别的段落将会折叠较低级别的段落。
builder->get_ParagraphFormat()->set_OutlineLevel(Aspose::Words::OutlineLevel::Level2);
builder->Writeln(u"Paragraph outline level 2.");

// 相同级别的两个段落不会相互折叠，
// 并且箭头不会折叠它们指向的段落。
builder->get_ParagraphFormat()->set_OutlineLevel(Aspose::Words::OutlineLevel::Level3);
builder->Writeln(u"Paragraph outline level 3.");
builder->Writeln(u"Paragraph outline level 3.");

// 默认的 "BodyText" 值是最低的，任何级别的段落都可以折叠它。
builder->get_ParagraphFormat()->set_OutlineLevel(Aspose::Words::OutlineLevel::BodyText);
builder->Writeln(u"Paragraph at main text level.");

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.ParagraphOutlineLevel.docx");
```

## 另见

* Enum [OutlineLevel](../../outlinelevel/)
* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
