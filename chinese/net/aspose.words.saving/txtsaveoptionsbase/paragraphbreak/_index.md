---
title: TxtSaveOptionsBase.ParagraphBreak
linktitle: ParagraphBreak
articleTitle: ParagraphBreak
second_title: 用于 .NET 的 Aspose.Words
description: TxtSaveOptionsBase ParagraphBreak 财产. 指定以文本格式导出时用作段落分隔符的字符串 在 C#.
type: docs
weight: 40
url: /zh/net/aspose.words.saving/txtsaveoptionsbase/paragraphbreak/
---
## TxtSaveOptionsBase.ParagraphBreak property

指定以文本格式导出时用作段落分隔符的字符串。

```csharp
public string ParagraphBreak { get; set; }
```

## 评论

默认值为[`CrLf`](../../../aspose.words/controlchar/crlf/)。

## 例子

演示如何使用自定义分段符保存 .txt 文档。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");
builder.Write("Paragraph 3.");

// 创建一个“TxtSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改我们将文档保存为纯文本的方式。
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

* class [TxtSaveOptionsBase](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
