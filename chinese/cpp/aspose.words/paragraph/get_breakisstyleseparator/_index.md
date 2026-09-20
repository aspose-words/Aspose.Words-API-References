---
title: "Aspose::Words::Paragraph::get_BreakIsStyleSeparator method"
linktitle: "get_BreakIsStyleSeparator"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Paragraph::get_BreakIsStyleSeparator 方法。如果此段落换行是样式分隔符，则返回 true。样式分隔符允许一个段落由具有不同段落样式的部分组成（C++）。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words/paragraph/get_breakisstyleseparator/
---
## Paragraph::get_BreakIsStyleSeparator method


如果此段落换行是 [Style](../../style/) 分隔符。样式分隔符允许一个段落由具有不同段落样式的部分组成。

```cpp
bool Aspose::Words::Paragraph::get_BreakIsStyleSeparator()
```


## 示例



展示如何在与目录标题同一行写入文本且不在目录中显示。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertTableOfContents(u"\\o \\h \\z \\u");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 插入一个段落，使用目录会将其识别为条目的样式。
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);

// 这两个字符串位于同一段落，因此会在同一目录条目中显示。
builder->Write(u"Heading 1. ");
builder->Write(u"Will appear in the TOC. ");

// 如果我们插入样式分隔符，就可以在同一段落中写入更多文本
// 并使用不同的样式而不在目录中显示。
// 如果在分隔符后使用标题样式，我们可以从文档中的一行文本生成多个目录条目。
builder->InsertStyleSeparator();
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Quote);
builder->Write(u"Won't appear in the TOC. ");

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_BreakIsStyleSeparator());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Paragraph.BreakIsStyleSeparator.docx");
```

## 另见

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
