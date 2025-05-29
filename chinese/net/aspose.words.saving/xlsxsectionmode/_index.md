---
title: XlsxSectionMode Enum
linktitle: XlsxSectionMode
articleTitle: XlsxSectionMode
second_title: Aspose.Words for .NET
description: 了解 Aspose.Words XlsxSectionMode 枚举如何优化 XLSX 格式的文档保存，增强您的工作流程和文档管理。
type: docs
weight: 6530
url: /zh/net/aspose.words.saving/xlsxsectionmode/
---
## XlsxSectionMode enumeration

指定以 XLSX 格式保存文档时如何处理各个部分。

```csharp
public enum XlsxSectionMode
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| MultipleWorksheets | `0` | 指定为文档的每个部分创建单独的工作表。 |
| SingleWorksheet | `1` | 指定将文档的所有部分保存在一个工作表上。 |

## 例子

展示如何将文档保存为单独的工作表。

```csharp
Document doc = new Document(MyDir + "Big document.docx");

// 文档的每个部分都将创建为单独的工作表。
// 使用“SingleWorksheet”在一个工作表上显示所有文档。
XlsxSaveOptions xlsxSaveOptions = new XlsxSaveOptions();
xlsxSaveOptions.SectionMode = XlsxSectionMode.MultipleWorksheets;

doc.Save(ArtifactsDir + "XlsxSaveOptions.SelectionMode.xlsx", xlsxSaveOptions);
```

### 也可以看看

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
