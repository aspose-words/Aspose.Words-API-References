---
title: Class MailMergeRegionInfo
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.MailMerging.MailMergeRegionInfo 班级. 包含有关邮件合并区域的信息
type: docs
weight: 3860
url: /zh/net/aspose.words.mailmerging/mailmergeregioninfo/
---
## MailMergeRegionInfo class

包含有关邮件合并区域的信息。

要了解更多信息，请访问[邮件合并和报告](https://docs.aspose.com/words/net/mail-merge-and-reporting/)文档文章。

```csharp
public class MailMergeRegionInfo
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [EndField](../../aspose.words.mailmerging/mailmergeregioninfo/endfield/) { get; } | 返回区域的结束字段。 |
| [EndMustacheTag](../../aspose.words.mailmerging/mailmergeregioninfo/endmustachetag/) { get; } | 返回该区域的结束“mustache”标签。 |
| [Fields](../../aspose.words.mailmerging/mailmergeregioninfo/fields/) { get; } | 返回子字段列表。 |
| [Level](../../aspose.words.mailmerging/mailmergeregioninfo/level/) { get; } | 返回区域的嵌套级别。 |
| [MustacheTags](../../aspose.words.mailmerging/mailmergeregioninfo/mustachetags/) { get; } | 返回子“mustache”标签的列表。 |
| [Name](../../aspose.words.mailmerging/mailmergeregioninfo/name/) { get; } | 返回区域名称。 |
| [ParentRegion](../../aspose.words.mailmerging/mailmergeregioninfo/parentregion/) { get; } | 返回父区域信息（顶级区域为空）。 |
| [Regions](../../aspose.words.mailmerging/mailmergeregioninfo/regions/) { get; } | 返回子区域列表。 |
| [StartField](../../aspose.words.mailmerging/mailmergeregioninfo/startfield/) { get; } | 返回区域的起始字段。 |
| [StartMustacheTag](../../aspose.words.mailmerging/mailmergeregioninfo/startmustachetag/) { get; } | 返回该区域的开始“mustache”标签。 |

### 例子

演示如何验证邮件合并区域。

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

// 获取第一个顶部区域内的字段列表。
IList<Field> fieldList = topRegions[0].Fields;

Assert.AreEqual(4, fieldList.Count);

FieldMergeField startFieldMergeField = nestedRegions[0].StartField;

Assert.AreEqual("TableStart:NestedRegion1", startFieldMergeField.FieldName);

FieldMergeField endFieldMergeField = nestedRegions[0].EndField;

Assert.AreEqual("TableEnd:NestedRegion1", endFieldMergeField.FieldName);
```

### 也可以看看

* 命名空间 [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* 部件 [Aspose.Words](../../)


