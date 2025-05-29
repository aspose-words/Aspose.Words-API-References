---
title: PdfSaveOptions.CreateNoteHyperlinks
linktitle: CreateNoteHyperlinks
articleTitle: CreateNoteHyperlinks
second_title: Aspose.Words for .NET
description: 使用 PdfSaveOptions 的 CreateNoteHyperlinks 功能增强您的 PDF 文档。将脚注和尾注转换为可点击的链接，方便导航。默认值为 false。
type: docs
weight: 60
url: /zh/net/aspose.words.saving/pdfsaveoptions/createnotehyperlinks/
---
## PdfSaveOptions.CreateNoteHyperlinks property

指定是否将正文故事中的脚注/尾注引用转换为活动超链接。 单击后，超链接将指向相应的脚注/尾注。 默认值为`错误的`.

```csharp
public bool CreateNoteHyperlinks { get; set; }
```

## 例子

展示如何使脚注和尾注发挥超链接的作用。

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
PdfSaveOptions options = new PdfSaveOptions();

// 将“CreateNoteHyperlinks”属性设置为“true”，将所有脚注/尾注符号
// 在文本中充当链接，单击后将带我们到各自的脚注/尾注。
// 将“CreateNoteHyperlinks”属性设置为“false”，以使脚注/尾注符号不链接到任何内容。
options.CreateNoteHyperlinks = createNoteHyperlinks;

doc.Save(ArtifactsDir + "PdfSaveOptions.NoteHyperlinks.pdf", options);
```

### 也可以看看

* class [PdfSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
