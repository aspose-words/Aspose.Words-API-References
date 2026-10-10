---
title: "Aspose::Words::ControlChar class"
linktitle: "ControlChar"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ControlChar 类。文档中常见的控制字符。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 18000
url: /zh/cpp/aspose.words/controlchar/
---
## ControlChar class


文档中常见的控制字符。要了解更多信息，请访问 [Working With Control Characters](https://docs.aspose.com/words/cpp/working-with-control-characters/) 文档文章。

```cpp
class ControlChar
```

## 方法

| 方法 | 描述 |
| --- | --- |
| static [Cell](./cell/)() | 表格单元格结束或表格行结束字符："\x0007" 或 "\a"。 |
| static [ColumnBreak](./columnbreak/)() | 列结束字符："\x000e"。 |
| [ControlChar](./controlchar/)() |  |
| static [Cr](./cr/)() | 回车字符："\x000d" 或 "\r"。同 [ParagraphBreak](./paragraphbreak/)。 |
| static [CrLf](./crlf/)() | 回车后跟换行字符："\x000d\x000a" 或 "\r\n"。在 Microsoft Word 文档中并非如此使用，但在文本文件中常用于段落换行。 |
| static [Lf](./lf/)() | 换行字符："\x000a" 或 "\n"。同 [LineFeed](./linefeed/)。 |
| static [LineBreak](./linebreak/)() | 换行符字符："\x000b" 或 "\v"。 |
| static [LineFeed](./linefeed/)() | 换行字符："\x000a" 或 "\n"。同 [Lf](./lf/)。 |
| static [NonBreakingSpace](./nonbreakingspace/)() | 不换行空格字符："\x00a0"。 |
| static [PageBreak](./pagebreak/)() | 分页符字符: "\x000c" 或 "\f"。注意它的值与 [SectionBreak](./sectionbreak/) 相同。 |
| static [ParagraphBreak](./paragraphbreak/)() | 段落结束字符: "\x000d" 或 "\r"。与 [Cr](./cr/) 相同。 |
| static [SectionBreak](./sectionbreak/)() | 节结束字符: "\x000c" 或 "\f"。注意它的值与 [PageBreak](./pagebreak/) 相同。 |
| static [Tab](./tab/)() | 制表符字符: "\x0009" 或 "\t"。 |
## 字段

| 字段 | 描述 |
| --- | --- |
| static constexpr [CellChar](./cellchar/) | 表格单元格结束或表格行结束字符: (char)7 或 "\a"。 |
| static constexpr [ColumnBreakChar](./columnbreakchar/) | 列结束字符: (char)14。 |
| static constexpr [DefaultTextInputChar](./defaulttextinputchar/) | 这是在文本输入表单字段中用作默认值的 "o" 字符。 |
| static constexpr [FieldEndChar](./fieldendchar/) | MS Word 字段结束字符: (char)21。 |
| static constexpr [FieldSeparatorChar](./fieldseparatorchar/) | 字段分隔符字符用于分隔字段代码和字段值。某些字段中可选。值: (char)20。 |
| static constexpr [FieldStartChar](./fieldstartchar/) | MS Word 字段开始字符: (char)19。 |
| static constexpr [LineBreakChar](./linebreakchar/) | 换行符字符: (char)11 或 "\v"。 |
| static constexpr [LineFeedChar](./linefeedchar/) | 换行字符: (char)10 或 "\n"。 |
| static constexpr [NonBreakingHyphenChar](./nonbreakinghyphenchar/) | Microsoft Word 中的不换行连字符是 (char)30。 |
| static constexpr [NonBreakingSpaceChar](./nonbreakingspacechar/) | 不换行空格字符: (char)160。 |
| static constexpr [OptionalHyphenChar](./optionalhyphenchar/) | Microsoft Word 中的可选连字符是 (char)31。 |
| static constexpr [PageBreakChar](./pagebreakchar/) | 分页符字符: (char)12 或 "\f"。 |
| static constexpr [ParagraphBreakChar](./paragraphbreakchar/) | 段落结束字符: (char)13 或 "\r"。 |
| static constexpr [SectionBreakChar](./sectionbreakchar/) | 节结束字符: (char)12 或 "\f"。 |
| static constexpr [SpaceChar](./spacechar/) | 空格字符: (char)32。 |
| static constexpr [TabChar](./tabchar/) | 制表符字符: (char)9 或 "\t"。 |

## 示例



展示如何使用控制字符。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 使用 DocumentBuilder 插入带文本的段落。
builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

// 将文档转换为文本形式会显示控制字符
// 表示文档的一些结构元素，例如分页符。
ASSERT_EQ(System::String::Format(u"Hello world!{0}", Aspose::Words::ControlChar::Cr()) + System::String::Format(u"Hello again!{0}", Aspose::Words::ControlChar::Cr()) + Aspose::Words::ControlChar::PageBreak(), doc->GetText());

// 在将文档转换为字符串形式时，
// 我们可以使用 Trim 方法省略一些控制字符。
ASSERT_EQ(System::String::Format(u"Hello world!{0}", Aspose::Words::ControlChar::Cr()) + u"Hello again!", doc->GetText().Trim());
```

## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
