---
title: "Aspose::Words::ParagraphFormat::get_SuppressLineNumbers 方法"
linktitle: "get_SuppressLineNumbers"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ParagraphFormat::get_SuppressLineNumbers 方法。指定当前段落的行是否应免于在父节中应用的行号（C++）。"
type: docs
weight: 39000
url: /zh/cpp/aspose.words/paragraphformat/get_suppresslinenumbers/
---
## ParagraphFormat::get_SuppressLineNumbers method


指定当前段落的行是否应免除在父节中应用的行号编号。

```cpp
bool Aspose::Words::ParagraphFormat::get_SuppressLineNumbers()
```


## 示例



展示如何为章节启用行号。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 我们可以使用章节的 PageSetup 对象在章节文本行左侧显示编号。
// 这与 List 对象的行为相同，
// 但它覆盖整个章节，且不会以任何方式修改文本。
// 我们的章节将在每个新页面从 1 重新开始编号并显示该数字，
// 如果它是 3 的倍数，则在行左侧 50pt 处显示。
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();
pageSetup->set_LineStartingNumber(1);
pageSetup->set_LineNumberCountBy(3);
pageSetup->set_LineNumberRestartMode(Aspose::Words::LineNumberRestartMode::RestartPage);
pageSetup->set_LineNumberDistanceFromText(50.0);

for (int32_t i = 1; i <= 25; i++)
{
    builder->Writeln(System::String::Format(u"Line {0}.", i));
}

// 行计数器将跳过任何将 "SuppressLineNumbers" 标志设置为 "true" 的段落。
// This paragraph is on the 15th line, which is a multiple of 3, and thus would normally display a line number.
// The section's line counter will also ignore this line, treat the next line as the 15th,
// and continue the count from that point onward.
doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(14)->get_ParagraphFormat()->set_SuppressLineNumbers(true);

doc->Save(get_ArtifactsDir() + u"PageSetup.LineNumbers.docx");
```

## 另见

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
