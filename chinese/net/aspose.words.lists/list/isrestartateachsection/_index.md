---
title: List.IsRestartAtEachSection
linktitle: IsRestartAtEachSection
articleTitle: IsRestartAtEachSection
second_title: Aspose.Words for .NET
description: 探索 IsRestartAtEachSection 属性，控制各节的列表编号。使用这项简单易用的功能，增强文档的组织性！
type: docs
weight: 50
url: /zh/net/aspose.words.lists/list/isrestartateachsection/
---
## List.IsRestartAtEachSection property

指定列表是否应在每个部分重新启动。 默认值为`错误的`.

```csharp
public bool IsRestartAtEachSection { get; set; }
```

## 评论

此选项仅支持 RTF、DOC 和 DOCX 文档格式。

此选项仅在以下情况下写入 DOCX：[`OoxmlCompliance`](../../../aspose.words.saving/ooxmlcompliance/)高于Ecma376_2006。

## 例子

显示如何配置列表以在每个部分重新开始编号。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

doc.Lists.Add(ListTemplate.NumberDefault);

Aspose.Words.Lists.List list = doc.Lists[0];
list.IsRestartAtEachSection = restartListAtEachSection;

// “IsRestartAtEachSection”属性仅在以下情况下适用
// 该文档的 OOXML 合规级别符合比“OoxmlComplianceCore.Ecma376”更新的标准。
OoxmlSaveOptions options = new OoxmlSaveOptions
{
    Compliance = OoxmlCompliance.Iso29500_2008_Transitional
};

builder.ListFormat.List = list;

builder.Writeln("List item 1");
builder.Writeln("List item 2");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Writeln("List item 3");
builder.Writeln("List item 4");

doc.Save(ArtifactsDir + "OoxmlSaveOptions.RestartingDocumentList.docx", options);

doc = new Document(ArtifactsDir + "OoxmlSaveOptions.RestartingDocumentList.docx");

Assert.AreEqual(restartListAtEachSection, doc.Lists[0].IsRestartAtEachSection);
```

### 也可以看看

* class [List](../)
* 命名空间 [Aspose.Words.Lists](../../../aspose.words.lists/)
* 部件 [Aspose.Words](../../../)
