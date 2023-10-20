---
title: List.IsRestartAtEachSection
linktitle: IsRestartAtEachSection
articleTitle: IsRestartAtEachSection
second_title: 用于 .NET 的 Aspose.Words
description: List IsRestartAtEachSection 财产. 指定是否应在每个部分重新启动列表 默认值为错误的 在 C#.
type: docs
weight: 50
url: /zh/net/aspose.words.lists/list/isrestartateachsection/
---
## List.IsRestartAtEachSection property

指定是否应在每个部分重新启动列表。 默认值为`错误的`.

```csharp
public bool IsRestartAtEachSection { get; set; }
```

## 评论

仅 RTF、DOC 和 DOCX 文档格式支持此选项。

仅当以下情况时，此选项才会写入 DOCX：[`OoxmlCompliance`](../../../aspose.words.saving/ooxmlcompliance/)则更高Ecma376_2006。

## 例子

展示如何配置列表以在每个部分重新开始编号。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

doc.Lists.Add(ListTemplate.NumberDefault);

Aspose.Words.Lists.List list = doc.Lists[0];
list.IsRestartAtEachSection = restartListAtEachSection;

// “IsRestartAtEachSection”属性仅适用于
// 文档的 OOXML 合规级别符合比“OoxmlComplianceCore.Ecma376”更新的标准。
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
