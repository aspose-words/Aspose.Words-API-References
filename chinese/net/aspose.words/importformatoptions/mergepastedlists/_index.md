---
title: ImportFormatOptions.MergePastedLists
linktitle: MergePastedLists
articleTitle: MergePastedLists
second_title: 用于 .NET 的 Aspose.Words
description: ImportFormatOptions MergePastedLists 财产. 获取或设置一个布尔值指定是否将粘贴的列表与周围的列表合并 默认值为错误的 在 C#.
type: docs
weight: 70
url: /zh/net/aspose.words/importformatoptions/mergepastedlists/
---
## ImportFormatOptions.MergePastedLists property

获取或设置一个布尔值，指定是否将粘贴的列表与周围的列表合并。 默认值为`错误的`.

```csharp
public bool MergePastedLists { get; set; }
```

## 例子

显示如何合并文档中的列表。

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
