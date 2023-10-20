---
title: ImportFormatOptions.SmartStyleBehavior
linktitle: SmartStyleBehavior
articleTitle: SmartStyleBehavior
second_title: 用于 .NET 的 Aspose.Words
description: ImportFormatOptions SmartStyleBehavior 财产. 获取或设置一个布尔值该值指定当样式在源文档和目标文档中具有相同名称时如何导入样式 默认值为错误的 在 C#.
type: docs
weight: 80
url: /zh/net/aspose.words/importformatoptions/smartstylebehavior/
---
## ImportFormatOptions.SmartStyleBehavior property

获取或设置一个布尔值，该值指定当样式在源文档和目标文档中具有相同名称时如何导入样式。 默认值为`错误的`.

```csharp
public bool SmartStyleBehavior { get; set; }
```

## 评论

当该选项为**已启用**，源样式将扩展为a 目标文档内的直接属性，如果KeepSourceFormatting使用导入模式。

当该选项为**残疾人**，只有编号的源样式才会展开。现有 目标属性不会被覆盖，包括列表。

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

* class [ImportFormatOptions](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
