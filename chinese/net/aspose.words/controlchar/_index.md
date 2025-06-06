---
title: ControlChar Class
linktitle: ControlChar
articleTitle: ControlChar
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.ControlChar 类，以有效管理文档中的控制字符，从而增强格式和可读性。
type: docs
weight: 550
url: /zh/net/aspose.words/controlchar/
---
## ControlChar class

文档中经常遇到的控制字符。

要了解更多信息，请访问[使用控制字符](https://docs.aspose.com/words/net/working-with-control-characters/)文档文章。

```csharp
public static class ControlChar
```

## 字段

| 姓名 | 描述 |
| --- | --- |
| static readonly [Cell](../../aspose.words/controlchar/cell/) | 表格单元格结尾或表格行结尾字符：“\x0007”或“\a”。 |
| const [CellChar](../../aspose.words/controlchar/cellchar/) | 表格单元格结尾或表格行结尾字符：(char)7 或“\a”. |
| static readonly [ColumnBreak](../../aspose.words/controlchar/columnbreak/) | 列结束字符：“\x000e”. |
| const [ColumnBreakChar](../../aspose.words/controlchar/columnbreakchar/) | 列结束字符： (char)14. |
| static readonly [Cr](../../aspose.words/controlchar/cr/) | 回车符：“\x000d”或“\r”。与[`ParagraphBreak`](./paragraphbreak/). |
| static readonly [CrLf](../../aspose.words/controlchar/crlf/) | 回车符后跟换行符：“\x000d\x000a”或“\r\n”。 在 Microsoft Word 文档中不使用，但通常用于文本文件中的段落分隔符。 |
| const [DefaultTextInputChar](../../aspose.words/controlchar/defaulttextinputchar/) | 这是在文本输入表单字段中用作默认值的“o”字符。 |
| const [FieldEndChar](../../aspose.words/controlchar/fieldendchar/) | MS Word 字段结束字符： (char)21. |
| const [FieldSeparatorChar](../../aspose.words/controlchar/fieldseparatorchar/) | 字段分隔符，用于分隔字段代码和字段值。某些字段可选。值：(char)20. |
| const [FieldStartChar](../../aspose.words/controlchar/fieldstartchar/) | MS Word 字段字符的开始： (char)19. |
| static readonly [Lf](../../aspose.words/controlchar/lf/) | 换行符：“\x000a”或“\n”。与[`LineFeed`](./linefeed/). |
| static readonly [LineBreak](../../aspose.words/controlchar/linebreak/) | 换行符：“\x000b”或“\v”. |
| const [LineBreakChar](../../aspose.words/controlchar/linebreakchar/) | 换行符：(char)11 或 "\v". |
| static readonly [LineFeed](../../aspose.words/controlchar/linefeed/) | 换行符：“\x000a”或“\n”。与[`Lf`](./lf/). |
| const [LineFeedChar](../../aspose.words/controlchar/linefeedchar/) | 换行符：(char)10 或“\n”. |
| const [NonBreakingHyphenChar](../../aspose.words/controlchar/nonbreakinghyphenchar/) | Microsoft Word 中的不间断连字符是 (char)30. |
| static readonly [NonBreakingSpace](../../aspose.words/controlchar/nonbreakingspace/) | 不间断空格字符：“\x00a0”. |
| const [NonBreakingSpaceChar](../../aspose.words/controlchar/nonbreakingspacechar/) | 不间断空格字符： (char)160. |
| const [OptionalHyphenChar](../../aspose.words/controlchar/optionalhyphenchar/) | Microsoft Word 中的可选连字符是 (char)31. |
| static readonly [PageBreak](../../aspose.words/controlchar/pagebreak/) | 分页符：“\x000c”或“\f”。注意，其值与[`SectionBreak`](./sectionbreak/). |
| const [PageBreakChar](../../aspose.words/controlchar/pagebreakchar/) | 分页符：(char)12 或“\f”. |
| static readonly [ParagraphBreak](../../aspose.words/controlchar/paragraphbreak/) | 段落结束字符：“\x000d”或“\r”。与[`Cr`](./cr/) |
| const [ParagraphBreakChar](../../aspose.words/controlchar/paragraphbreakchar/) | 段落结束字符：(char)13 或“\r”. |
| static readonly [SectionBreak](../../aspose.words/controlchar/sectionbreak/) | 节尾字符：“\x000c”或“\f”。注意，它与[`PageBreak`](./pagebreak/). |
| const [SectionBreakChar](../../aspose.words/controlchar/sectionbreakchar/) | 节尾字符：(char)12 或“\f”. |
| const [SpaceChar](../../aspose.words/controlchar/spacechar/) | 空格字符： (char)32. |
| static readonly [Tab](../../aspose.words/controlchar/tab/) | 制表符：“\x0009”或“\t”。 |
| const [TabChar](../../aspose.words/controlchar/tabchar/) | 制表符：(char)9 或 "\t". |

## 评论

提供相同常量的字符和字符串版本。例如： 字符串[`LineBreak`](./linebreak/)和字符[`LineBreakChar`](./linebreakchar/)具有相同的值。

## 例子

展示如何使用控制字符。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 使用 DocumentBuilder 插入带有文本的段落。
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// 将文档转换为文本形式显示控制字符
// 表示文档的一些结构元素，例如分页符。
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                $"Hello again!{ControlChar.Cr}" +
                ControlChar.PageBreak, doc.GetText());

// 将文档转换为字符串形式时，
// 我们可以使用 Trim 方法省略一些控制字符。
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                "Hello again!", doc.GetText().Trim());
```

### 也可以看看

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
