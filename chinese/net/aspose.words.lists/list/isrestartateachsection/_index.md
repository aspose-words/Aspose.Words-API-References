---
title: List.IsRestartAtEachSection
second_title: Aspose.Words for .NET API 参考
description: List 财产. 指定是否应在每个部分重新启动列表 默认值为 错误的.
type: docs
weight: 50
url: /zh/net/aspose.words.lists/list/isrestartateachsection/
---
## List.IsRestartAtEachSection property

指定是否应在每个部分重新启动列表。 默认值为 **错误的**.

```csharp
public bool IsRestartAtEachSection { get; set; }
```

### 评论

此选项仅在 RTF、DOC 和 DOCX 文档格式中受支持。

只有在以下情况下，此选项才会写入 DOCX[`OoxmlCompliance`](../../../aspose.words.saving/ooxmlcompliance/)高于Ecma376_2006.

### 例子

显示如何配置列表以在每个部分重新开始编号。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

doc.Lists.Add(ListTemplate.NumberDefault);

Aspose.Words.Lists.List list = doc.Lists[0];
list.IsRestartAtEachSection = restartListAtEachSection;

// “IsRestartAtEachSection”属性仅在以下情况下适用
// 文档的 OOXML 合规级别是比“OoxmlComplianceCore.Ecma376”更新的标准。
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
* 命名空间 [Aspose.Words.Lists](../../list/)
* 部件 [Aspose.Words](../../../)


