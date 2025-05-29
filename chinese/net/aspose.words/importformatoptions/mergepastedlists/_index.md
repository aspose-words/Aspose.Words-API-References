---
title: ImportFormatOptions.MergePastedLists
linktitle: MergePastedLists
articleTitle: MergePastedLists
second_title: Aspose.Words for .NET
description: 使用 ImportFormatOptions 的 MergePastedLists 属性控制列表合并。轻松管理粘贴的列表，增强文档格式。默认值为 false。
type: docs
weight: 70
url: /zh/net/aspose.words/importformatoptions/mergepastedlists/
---
## ImportFormatOptions.MergePastedLists property

获取或设置一个布尔值，指定粘贴的列表是否与周围列表合并。 默认值为`错误的`.

```csharp
public bool MergePastedLists { get; set; }
```

## 例子

展示如何合并文档中的列表。

```csharp
Document srcDoc = new Document(MyDir + "List item.docx");
Document dstDoc = new Document(MyDir + "List destination.docx");

ImportFormatOptions options = new ImportFormatOptions { MergePastedLists = true };

// 将“MergePastedLists”属性设置为“true”，粘贴的列表将与周围的列表合并。
dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles, options);

dstDoc.Save(ArtifactsDir + "Document.MergePastedLists.docx");
```

### 也可以看看

* class [ImportFormatOptions](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
