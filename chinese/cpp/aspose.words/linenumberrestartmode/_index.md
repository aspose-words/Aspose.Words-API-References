---
title: "Aspose::Words::LineNumberRestartMode enum"
linktitle: "LineNumberRestartMode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::LineNumberRestartMode 枚举。确定 C++ 中自动行号何时重新开始。"
type: docs
weight: 94000
url: /zh/cpp/aspose.words/linenumberrestartmode/
---
## LineNumberRestartMode enum


确定自动行号何时重新开始。

```cpp
enum class LineNumberRestartMode
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| RestartPage | 0 | 行号在每页的开头重新开始。 |
| RestartSection | 1 | 行号在章节开始时重新开始。 |
| Continuous | 2 | 行号从前一章节继续。 |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
