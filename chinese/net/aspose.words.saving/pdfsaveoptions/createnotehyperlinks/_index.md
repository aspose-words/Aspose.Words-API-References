---
title: PdfSaveOptions.CreateNoteHyperlinks
second_title: Aspose.Words for .NET API 参考
description: PdfSaveOptions 财产. 指定是否将正文故事中的脚注/尾注引用转换为活动超链接 单击超链接时将指向相应的脚注/尾注 默认为错误的.
type: docs
weight: 40
url: /zh/net/aspose.words.saving/pdfsaveoptions/createnotehyperlinks/
---
## PdfSaveOptions.CreateNoteHyperlinks property

指定是否将正文故事中的脚注/尾注引用转换为活动超链接。 单击超链接时，将指向相应的脚注/尾注。 默认为`错误的`.

```csharp
public bool CreateNoteHyperlinks { get; set; }
```

### 例子

演示如何使脚注和尾注充当超链接。

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

// 创建一个“PdfSaveOptions”对象，我们可以将它传递给文档的“Save”方法
// 修改该方法如何将文档转换为 .PDF。
PdfSaveOptions options = new PdfSaveOptions();

// 将“CreateNoteHyperlinks”属性设置为“true”以打开所有脚注/尾注符号
// 在文本中充当链接，单击后将我们带到各自的脚注/尾注。
// 将“CreateNoteHyperlinks”属性设置为“false”，以不让脚注/尾注符号链接到任何内容。
options.CreateNoteHyperlinks = createNoteHyperlinks;

doc.Save(ArtifactsDir + "PdfSaveOptions.NoteHyperlinks.pdf", options);
```

### 也可以看看

* class [PdfSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../pdfsaveoptions/)
* 部件 [Aspose.Words](../../../)


