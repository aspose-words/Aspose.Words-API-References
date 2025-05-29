---
title: ImportFormatOptions Class
linktitle: ImportFormatOptions
articleTitle: ImportFormatOptions
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.ImportFormatOptions，实现可自定义的文档格式。使用定制的导入设置增强您的输出效果，以获得最佳效果。
type: docs
weight: 3690
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
| [ForceCopyStyles](../../aspose.words/importformatoptions/forcecopystyles/) { get; set; } | 获取或设置一个布尔值，指示是否复制冲突的样式 KeepSourceFormatting mode. 默认值为`错误的`. |
| [IgnoreHeaderFooter](../../aspose.words/importformatoptions/ignoreheaderfooter/) { get; set; } | 获取或设置一个布尔值，该值指定页眉/页脚内容的源格式是否被忽略 KeepSourceFormatting模式。 默认值为`真的`. |
| [IgnoreTextBoxes](../../aspose.words/importformatoptions/ignoretextboxes/) { get; set; } | 获取或设置一个布尔值，该值指定文本框内容的源格式是否被忽略 KeepSourceFormatting模式。 默认值为`真的`. |
| [KeepSourceNumbering](../../aspose.words/importformatoptions/keepsourcenumbering/) { get; set; } | 获取或设置一个布尔值，该值指定当源文档和目标文档中的编号发生冲突时如何导入编号。 默认值为`错误的`. |
| [MergePastedLists](../../aspose.words/importformatoptions/mergepastedlists/) { get; set; } | 获取或设置一个布尔值，指定粘贴的列表是否与周围列表合并。 默认值为`错误的`. |
| [SmartStyleBehavior](../../aspose.words/importformatoptions/smartstylebehavior/) { get; set; } | 获取或设置一个布尔值，该值指定当样式在源文档和目标文档中具有相同的名称时，如何导入样式。 默认值为`错误的`. |

## 例子

展示如何在插入文档时解决重复样式。

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
// 如果我们将克隆插入到原始文档中，则两个同名的样式将引起冲突。
Document srcDoc = dstDoc.Clone();
srcDoc.Styles["MyStyle"].Font.Color = Color.Red;

// 当我们启用 SmartStyleBehavior 并使用 KeepSourceFormatting 导入格式模式时，
// Aspose.Words 将通过转换源文档样式来解决样式冲突。
// 将与目标样式同名的样式放入直接段落属性中。
ImportFormatOptions options = new ImportFormatOptions();
options.SmartStyleBehavior = true;

builder.InsertDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.SmartStyleBehavior.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
