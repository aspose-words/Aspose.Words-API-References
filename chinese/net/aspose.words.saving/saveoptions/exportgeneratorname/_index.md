---
title: SaveOptions.ExportGeneratorName
linktitle: ExportGeneratorName
articleTitle: ExportGeneratorName
second_title: 用于 .NET 的 Aspose.Words
description: SaveOptions ExportGeneratorName 财产. 当真的 导致 Aspose.Words 的名称和版本嵌入到生成的文件中 默认值为真的 在 C#.
type: docs
weight: 80
url: /zh/net/aspose.words.saving/saveoptions/exportgeneratorname/
---
## SaveOptions.ExportGeneratorName property

当`真的` ，导致 Aspose.Words 的名称和版本嵌入到生成的文件中。 默认值为`真的`.

```csharp
public bool ExportGeneratorName { get; set; }
```

## 例子

演示如何禁止将 Aspose.Words 的名称和版本添加到生成的文件中。

```csharp
Document doc = new Document();

// 使用 https://docs.aspose.com/words/net/generator-or- Producer-name-included-in-output-documents/ 了解如何检查结果。
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { ExportGeneratorName = false };

doc.Save(ArtifactsDir + "OoxmlSaveOptions.ExportGeneratorName.docx", saveOptions);
```

### 也可以看看

* class [SaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
