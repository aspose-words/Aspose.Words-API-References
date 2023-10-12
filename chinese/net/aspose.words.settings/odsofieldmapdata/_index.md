---
title: Class OdsoFieldMapData
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Settings.OdsoFieldMapData 班级. 指定如何将外部数据源中的列映射到文档中的预定义合并字段
type: docs
weight: 5900
url: /zh/net/aspose.words.settings/odsofieldmapdata/
---
## OdsoFieldMapData class

指定如何将外部数据源中的列映射到文档中的预定义合并字段。

要了解更多信息，请访问[邮件合并和报告](https://docs.aspose.com/words/net/mail-merge-and-reporting/)文档文章。

```csharp
public class OdsoFieldMapData
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [OdsoFieldMapData](odsofieldmapdata/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Column](../../aspose.words.settings/odsofieldmapdata/column/) { get; set; } | 指定外部数据源中列的从零开始的索引，该索引应 映射到特定 MERGEFIELD 字段的本地名称。 默认值为 0。 |
| [MappedName](../../aspose.words.settings/odsofieldmapdata/mappedname/) { get; set; } | 指定预定义的合并字段名称，该名称应映射到由 指定的列号[`Column`](./column/)此字段映射内的属性。 默认值为空字符串。 |
| [Name](../../aspose.words.settings/odsofieldmapdata/name/) { get; set; } | 指定外部数据源中 索引由[`Column`](./column/)属性。 默认值为空字符串。 |
| [Type](../../aspose.words.settings/odsofieldmapdata/type/) { get; set; } | 指定给定邮件合并字段是否已映射到给定外部数据源中的列。 默认值为Default. |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Clone](../../aspose.words.settings/odsofieldmapdata/clone/)() | 返回此对象的深度克隆。 |

### 评论

Microsoft Word 提供了一些预定义的合并字段名称，允许将它们作为 MERGEFIELD 或 在 ADDRESSBLOCK 或 GREETINGLINE 字段中使用插入到文档中。中指定的信息`OdsoFieldMapData` 允许将外部数据源中的一列映射到单个预定义的合并字段。

### 例子

演示如何访问将数据源列映射到合并字段的数据集合。

```csharp
Document doc = new Document(MyDir + "Odso data.docx");

// 该集合定义邮件合并如何映射数据源中的列
// 预定义的 MERGEFIELD、ADDRESSBLOCK 和 GREETINGLINE 字段。
OdsoFieldMapDataCollection dataCollection = doc.MailMergeSettings.Odso.FieldMapDatas;
Assert.AreEqual(30, dataCollection.Count);

using (IEnumerator<OdsoFieldMapData> enumerator = dataCollection.GetEnumerator())
{
    int index = 0;
    while (enumerator.MoveNext())
    {
        Console.WriteLine($"Field map data index {index++}, type \"{enumerator.Current.Type}\":");

        Console.WriteLine(
            enumerator.Current.Type != OdsoFieldMappingType.Null
                ? $"\tColumn \"{enumerator.Current.Name}\", number {enumerator.Current.Column} mapped to merge field \"{enumerator.Current.MappedName}\"."
                : "\tNo valid column to field mapping data present.");
    }
}

// 克隆此集合中的元素。
Assert.AreNotEqual(dataCollection[0], dataCollection[0].Clone());

// 按索引单独使用“RemoveAt”方法元素。
dataCollection.RemoveAt(0);

Assert.AreEqual(29, dataCollection.Count);

// 使用“Clear”方法一次性清除整个集合。
dataCollection.Clear();

Assert.AreEqual(0, dataCollection.Count);
```

### 也可以看看

* 命名空间 [Aspose.Words.Settings](../../aspose.words.settings/)
* 部件 [Aspose.Words](../../)


