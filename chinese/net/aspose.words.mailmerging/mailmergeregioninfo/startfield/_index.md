---
title: MailMergeRegionInfo.StartField
linktitle: StartField
articleTitle: StartField
second_title: Aspose.Words for .NET
description: 发现 MailMergeRegionInfo StartField 属性 - 有效检索合并区域的起始字段并简化文档自动化。
type: docs
weight: 90
url: /zh/net/aspose.words.mailmerging/mailmergeregioninfo/startfield/
---
## MailMergeRegionInfo.StartField property

返回该区域的起始字段。

```csharp
public FieldMergeField StartField { get; }
```

## 例子

显示如何验证邮件合并区域。

```csharp
Document doc = new Document(MyDir + "Mail merge regions.docx");

// 返回包含文档中可用的 MERGEFIELD 的合并区域的完整层次结构。
MailMergeRegionInfo regionInfo = doc.MailMerge.GetRegionsHierarchy();

// 获取文档中的顶部区域。
IList<MailMergeRegionInfo> topRegions = regionInfo.Regions;

Assert.AreEqual(2, topRegions.Count);
Assert.AreEqual("Region1", topRegions[0].Name);
Assert.AreEqual("Region2", topRegions[1].Name);
Assert.AreEqual(1, topRegions[0].Level);
Assert.AreEqual(1, topRegions[1].Level);

// 获取第一个顶部区域中的嵌套区域。
IList<MailMergeRegionInfo> nestedRegions = topRegions[0].Regions;

Assert.AreEqual(2, nestedRegions.Count);
Assert.AreEqual("NestedRegion1", nestedRegions[0].Name);
Assert.AreEqual("NestedRegion2", nestedRegions[1].Name);
Assert.AreEqual(2, nestedRegions[0].Level);
Assert.AreEqual(2, nestedRegions[1].Level);
Assert.AreEqual(0, nestedRegions[1].MustacheTags.Count);

// 获取第一个顶部区域内的字段列表。
IList<Field> fieldList = topRegions[0].Fields;

Assert.AreEqual(4, fieldList.Count);

FieldMergeField startFieldMergeField = nestedRegions[0].StartField;

Assert.AreEqual("TableStart:NestedRegion1", startFieldMergeField.FieldName);

FieldMergeField endFieldMergeField = nestedRegions[0].EndField;

Assert.AreEqual("TableEnd:NestedRegion1", endFieldMergeField.FieldName);
```

### 也可以看看

* class [FieldMergeField](../../../aspose.words.fields/fieldmergefield/)
* class [MailMergeRegionInfo](../)
* 命名空间 [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* 部件 [Aspose.Words](../../../)
