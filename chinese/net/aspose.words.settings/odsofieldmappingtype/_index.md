---
title: OdsoFieldMappingType Enum
linktitle: OdsoFieldMappingType
articleTitle: OdsoFieldMappingType
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.OdsoFieldMappingType 枚举，高效地将邮件合并字段映射到外部数据源。立即增强您的文档自动化！
type: docs
weight: 6750
url: /zh/net/aspose.words.settings/odsofieldmappingtype/
---
## OdsoFieldMappingType enumeration

指定用于指示给定邮件合并字段是否已映射到给定外部数据源中的列的可能类型。

```csharp
public enum OdsoFieldMappingType
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Column | `0` | 指定邮件合并字段已映射到给定外部数据源中的列。 |
| Null | `1` | 指定邮件合并字段尚未映射到给定外部数据源中的列。 |
| Default | `1` | 等于Null. |

## 例子

展示如何访问将数据源列映射到合并字段的数据集合。

```csharp
Document doc = new Document(MyDir + "Odso data.docx");

// 此集合定义邮件合并如何映射数据源中的列
// 到预定义的 MERGEFIELD、ADDRESSBLOCK 和 GREETINGLINE 字段。
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

// 使用“RemoveAt”方法按索引单独删除元素。
dataCollection.RemoveAt(0);

Assert.AreEqual(29, dataCollection.Count);

// 使用“Clear”方法一次清除整个集合。
dataCollection.Clear();

Assert.AreEqual(0, dataCollection.Count);
```

### 也可以看看

* property [Type](../odsofieldmapdata/type/)
* 命名空间 [Aspose.Words.Settings](../../aspose.words.settings/)
* 部件 [Aspose.Words](../../)
