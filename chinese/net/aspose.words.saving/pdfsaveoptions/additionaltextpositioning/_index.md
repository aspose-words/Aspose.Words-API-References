---
title: PdfSaveOptions.AdditionalTextPositioning
linktitle: AdditionalTextPositioning
articleTitle: AdditionalTextPositioning
second_title: 用于 .NET 的 Aspose.Words
description: PdfSaveOptions AdditionalTextPositioning 财产. 指定是否写入附加文本定位运算符的标志 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words.saving/pdfsaveoptions/additionaltextpositioning/
---
## PdfSaveOptions.AdditionalTextPositioning property

指定是否写入附加文本定位运算符的标志。

```csharp
public bool AdditionalTextPositioning { get; set; }
```

## 评论

如果`真的` ，附加文本定位运算符将写入输出 PDF。这可能有助于克服某些打印机文本定位不准确的 问题。缺点是 PDF 文档大小增加。

默认值为`错误的`。

## 例子

展示如何编写附加文本定位运算符。

```csharp
Document doc = new Document(MyDir + "Text positioning operators.docx");

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
PdfSaveOptions saveOptions = new PdfSaveOptions
{
    TextCompression = PdfTextCompression.None,

    // 将“AdditionalTextPositioning”属性设置为“true”以尝试修复不正确的情况
    // 输出 PDF 中的元素定位（如果有的话），但代价是文件大小增加。
    // 将“AdditionalTextPositioning”属性设置为“false”以照常呈现文档。
    AdditionalTextPositioning = applyAdditionalTextPositioning
};

doc.Save(ArtifactsDir + "PdfSaveOptions.AdditionalTextPositioning.pdf", saveOptions);
```

### 也可以看看

* class [PdfSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
