---
title: TxtSaveOptions.SaveFormat
second_title: Aspose.Words for .NET API 参考
description: TxtSaveOptions 财产. 指定使用此保存选项对象时文档将保存的格式 只能是Text.
type: docs
weight: 60
url: /zh/net/aspose.words.saving/txtsaveoptions/saveformat/
---
## TxtSaveOptions.SaveFormat property

指定使用此保存选项对象时文档将保存的格式。 只能是Text.

```csharp
public override SaveFormat SaveFormat { get; set; }
```

### 例子

显示如何使用自定义分节符保存 .txt 文档。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");
builder.Write("Paragraph 3.");

// 创建一个“TxtSaveOptions”对象，我们可以将它传递给文档的“Save”方法
// 修改我们如何将文档保存为纯文本。
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

Assert.AreEqual(SaveFormat.Text, txtSaveOptions.SaveFormat);

// 将“ParagraphBreak”设置为我们希望放在每个段落末尾的自定义值。
txtSaveOptions.ParagraphBreak = " End of paragraph.\n\n\t";

doc.Save(ArtifactsDir + "TxtSaveOptions.ParagraphBreak.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.ParagraphBreak.txt");

Assert.AreEqual("Paragraph 1. End of paragraph.\n\n\t" +
                "Paragraph 2. End of paragraph.\n\n\t" +
                "Paragraph 3. End of paragraph.\n\n\t", docText);
```

### 也可以看看

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [TxtSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../txtsaveoptions/)
* 部件 [Aspose.Words](../../../)


