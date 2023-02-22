---
title: PdfSaveOptions.AdditionalTextPositioning
second_title: Aspose.Words for .NET API 参考
description: PdfSaveOptions 财产. 一个标志指定是否编写额外的文本定位操作符
type: docs
weight: 20
url: /zh/net/aspose.words.saving/pdfsaveoptions/additionaltextpositioning/
---
## PdfSaveOptions.AdditionalTextPositioning property

一个标志，指定是否编写额外的文本定位操作符。

```csharp
public bool AdditionalTextPositioning { get; set; }
```

### 评论

如果`真的`，额外的文本定位运算符被写入输出 PDF。这可能有助于克服某些打印机的文本定位不准确的 问题。缺点是 PDF 文档大小增加。

默认值为`错误的`.

### 例子

展示如何编写额外的文本定位操作符。

```csharp
Document doc = new Document(MyDir + "Text positioning operators.docx");

// 创建一个“PdfSaveOptions”对象，我们可以将它传递给文档的“Save”方法
// 修改该方法如何将文档转换为 .PDF。
PdfSaveOptions saveOptions = new PdfSaveOptions
{
    TextCompression = PdfTextCompression.None,

    // 将“AdditionalTextPositioning”属性设置为“true”以尝试修复不正确的
    // 输出 PDF 中的元素定位，如果有的话，以增加文件大小为代价。
    // 将“AdditionalTextPositioning”属性设置为“false”以照常呈现文档。
    AdditionalTextPositioning = applyAdditionalTextPositioning
};

doc.Save(ArtifactsDir + "PdfSaveOptions.AdditionalTextPositioning.pdf", saveOptions);
```

### 也可以看看

* class [PdfSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../pdfsaveoptions/)
* 部件 [Aspose.Words](../../../)


