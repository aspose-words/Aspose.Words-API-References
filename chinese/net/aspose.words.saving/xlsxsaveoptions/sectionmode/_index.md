---
title: XlsxSaveOptions.SectionMode
linktitle: SectionMode
articleTitle: SectionMode
second_title: Aspose.Words for .NET
description: 了解 XlsxSaveOptions SectionMode 属性如何优化 XLSX 导出的部分处理，确保无缝文档管理和多个工作表。
type: docs
weight: 50
url: /zh/net/aspose.words.saving/xlsxsaveoptions/sectionmode/
---
## XlsxSaveOptions.SectionMode property

获取或设置保存到输出 XLSX 文档时处理各部分的方式。 默认值为MultipleWorksheets.

```csharp
public XlsxSectionMode SectionMode { get; set; }
```

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

* enum [XlsxSectionMode](../../xlsxsectionmode/)
* class [XlsxSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
