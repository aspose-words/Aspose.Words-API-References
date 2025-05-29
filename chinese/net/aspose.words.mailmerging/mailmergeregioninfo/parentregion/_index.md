---
title: MailMergeRegionInfo.ParentRegion
linktitle: ParentRegion
articleTitle: ParentRegion
second_title: Aspose.Words for .NET
description: 探索 MailMergeRegionInfo ParentRegion 属性，该属性提供必要的父区域详细信息，对于顶级区域则返回 null。增强您的文档自动化！
type: docs
weight: 70
url: /zh/net/aspose.words.mailmerging/mailmergeregioninfo/parentregion/
---
## MailMergeRegionInfo.ParentRegion property

返回父区域信息（顶级区域为空）。

```csharp
public MailMergeRegionInfo ParentRegion { get; }
```

## 例子

展示如何创建、列出和阅读邮件合并区域。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// “TableStart” 和 “TableEnd” 标签，位于 MERGEFIELDs 内部，
// 表示邮件合并区域开始和结束的字符串。
Assert.AreEqual("TableStart", doc.MailMerge.RegionStartTag);
Assert.AreEqual("TableEnd", doc.MailMerge.RegionEndTag);

// 使用这些标签来开始和结束名为“MailMergeRegion1”的邮件合并区域，
// 其中将包含两列的 MERGEFIELDs。
builder.InsertField(" MERGEFIELD TableStart:MailMergeRegion1");
builder.InsertField(" MERGEFIELD Column1");
builder.Write(", ");
builder.InsertField(" MERGEFIELD Column2");
builder.InsertField(" MERGEFIELD TableEnd:MailMergeRegion1");

// 我们可以通过查看这些集合来跟踪合并区域及其列。
IList<MailMergeRegionInfo> regions = doc.MailMerge.GetRegionsByName("MailMergeRegion1");

Assert.AreEqual(1, regions.Count);
Assert.AreEqual("MailMergeRegion1", regions[0].Name);

string[] mergeFieldNames = doc.MailMerge.GetFieldNamesForRegion("MailMergeRegion1");

Assert.AreEqual("Column1", mergeFieldNames[0]);
Assert.AreEqual("Column2", mergeFieldNames[1]);

// 在现有区域内插入一个同名区域，这将使其成为父区域。
// 现在“Column2”字段将位于新区域内。
builder.MoveToField(regions[0].Fields[1], false); 
builder.InsertField(" MERGEFIELD TableStart:MailMergeRegion1");
builder.MoveToField(regions[0].Fields[1], true);
builder.InsertField(" MERGEFIELD TableEnd:MailMergeRegion1");

// 如果我们使用“GetRegionsByName”方法查找重复区域的名称，
// 它将返回集合中的所有此类区域。
regions = doc.MailMerge.GetRegionsByName("MailMergeRegion1");

Assert.AreEqual(2, regions.Count);
// 检查第二个区域现在是否有父区域。
Assert.AreEqual("MailMergeRegion1", regions[1].ParentRegion.Name);

mergeFieldNames = doc.MailMerge.GetFieldNamesForRegion("MailMergeRegion1", 1);

Assert.AreEqual("Column2", mergeFieldNames[0]);
```

### 也可以看看

* class [MailMergeRegionInfo](../)
* 命名空间 [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* 部件 [Aspose.Words](../../../)
