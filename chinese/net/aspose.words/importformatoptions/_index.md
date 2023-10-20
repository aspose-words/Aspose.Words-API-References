---
title: ImportFormatOptions Class
linktitle: ImportFormatOptions
articleTitle: ImportFormatOptions
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.ImportFormatOptions 班级. 允许指定各种导入选项来格式化输出 在 C#.
type: docs
weight: 3240
url: /zh/net/aspose.words/importformatoptions/
---
## ImportFormatOptions class

允许指定各种导入选项来格式化输出。

要了解更多信息，请访问[指定加载选项](https://docs.aspose.com/words/net/specify-load-options/)文档文章。

```csharp
public class ImportFormatOptions
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [ImportFormatOptions](importformatoptions/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [AdjustSentenceAndWordSpacing](../../aspose.words/importformatoptions/adjustsentenceandwordspacing/) { get; set; } | 获取或设置一个布尔值，指定是否自动调整句子和单词间距。 默认值为`错误的`. |
| [ForceCopyStyles](../../aspose.words/importformatoptions/forcecopystyles/) { get; set; } | 获取或设置一个布尔值，指示是否将冲突的样式 复制到KeepSourceFormattingmode. 默认值为`错误的`. |
| [IgnoreHeaderFooter](../../aspose.words/importformatoptions/ignoreheaderfooter/) { get; set; } | 获取或设置一个布尔值，该值指定忽略页眉/页脚内容的源格式 ifKeepSourceFormatting使用模式。 默认值为`真的`. |
| [IgnoreTextBoxes](../../aspose.words/importformatoptions/ignoretextboxes/) { get; set; } | 获取或设置一个布尔值，该值指定忽略文本框内容的源格式 ifKeepSourceFormatting使用模式。 默认值为`真的`. |
| [KeepSourceNumbering](../../aspose.words/importformatoptions/keepsourcenumbering/) { get; set; } | 获取或设置一个布尔值，该值指定当编号与源文档和 目标文档发生冲突时如何导入编号。 默认值为`错误的`. |
| [MergePastedLists](../../aspose.words/importformatoptions/mergepastedlists/) { get; set; } | 获取或设置一个布尔值，指定粘贴的列表是否与周围的列表合并。 默认值为`错误的`. |
| [SmartStyleBehavior](../../aspose.words/importformatoptions/smartstylebehavior/) { get; set; } | 获取或设置一个布尔值，该值指定当样式在源文档和目标文档中具有相同名称时如何导入样式。 默认值为`错误的`. |

## 例子

演示如何在插入文档时解决重复样式。

```csharp
Document dstDoc = new Document();
DocumentBuilder builder = new DocumentBuilder(dstDoc);

Style myStyle = builder.Document.Styles.Add(StyleType.Paragraph, "MyStyle");
myStyle.Font.Size = 14;
myStyle.Font.Name = "Courier New";
myStyle.Font.Color = Color.Blue;

builder.ParagraphFormat.StyleName = myStyle.Name;
builder.Writeln("Hello world!");

// 克隆文档并编辑克隆的“MyStyle”样式，使其颜色与原始颜色不同。
// 如果我们将克隆插入到原始文档中，两个同名的样式会产生冲突。
Document srcDoc = dstDoc.Clone();
srcDoc.Styles["MyStyle"].Font.Color = Color.Red;

// 当我们启用SmartStyleBehavior并使用KeepSourceFormatting导入格式模式时，
// Aspose.Words 将通过转换源文档样式来解决样式冲突。
// 与目标样式同名的直接段落属性。
ImportFormatOptions options = new ImportFormatOptions();
options.SmartStyleBehavior = true;

builder.InsertDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.SmartStyleBehavior.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
