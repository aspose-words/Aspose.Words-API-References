---
title: MailMerge.GetFieldNamesForRegion
linktitle: GetFieldNamesForRegion
articleTitle: GetFieldNamesForRegion
second_title: Aspose.Words for .NET
description: 探索 MailMerge GetFieldNamesForRegion 方法，轻松访问指定区域内的邮件合并字段名称集合。简化您的工作流程！
type: docs
weight: 230
url: /zh/net/aspose.words.mailmerging/mailmerge/getfieldnamesforregion/
---
## GetFieldNamesForRegion(*string*) {#getfieldnamesforregion}

返回该区域可用的邮件合并字段名称集合。

```csharp
public string[] GetFieldNamesForRegion(string regionName)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| regionName | String | 区域名称（不区分大小写）。 |

## 评论

返回包含可选前缀的完整合并字段名称。不会消除重复的字段名称。

如果文档包含多个同名的区域，则处理第一个区域。

每次调用时都会创建一个新的字符串数组。

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

* class [MailMerge](../)
* 命名空间 [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* 部件 [Aspose.Words](../../../)

---

## GetFieldNamesForRegion(*string, int*) {#getfieldnamesforregion_1}

返回该区域可用的邮件合并字段名称集合。

```csharp
public string[] GetFieldNamesForRegion(string regionName, int regionIndex)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| regionName | String | 区域名称（不区分大小写）。 |
| regionIndex | Int32 | 区域索引（从零开始）。 |

## 评论

返回包含可选前缀的完整合并字段名称。不会消除重复的字段名称。

如果文档包含多个同名区域，则处理第 N 个区域（从零开始）。

每次调用时都会创建一个新的字符串数组。

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

* class [MailMerge](../)
* 命名空间 [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* 部件 [Aspose.Words](../../../)
