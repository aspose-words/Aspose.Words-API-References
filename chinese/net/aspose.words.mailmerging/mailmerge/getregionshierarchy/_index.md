---
title: MailMerge.GetRegionsHierarchy
linktitle: GetRegionsHierarchy
articleTitle: GetRegionsHierarchy
second_title: Aspose.Words for .NET
description: 探索 MailMerge GetRegionsHierarchy 方法，轻松检索具有可访问文档字段的完整区域层次结构，从而简化工作流程。
type: docs
weight: 250
url: /zh/net/aspose.words.mailmerging/mailmerge/getregionshierarchy/
---
## MailMerge.GetRegionsHierarchy method

返回文档中可用的区域（带有字段）的完整层次结构。

```csharp
public MailMergeRegionInfo GetRegionsHierarchy()
```

### 返回值

区域的层次结构。

## 评论

层次结构以以下形式返回[`MailMergeRegionInfo`](../../mailmergeregioninfo/)班级。

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

* class [MailMergeRegionInfo](../../mailmergeregioninfo/)
* class [MailMerge](../)
* 命名空间 [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* 部件 [Aspose.Words](../../../)
