---
title: Odso.FieldMapDatas
linktitle: FieldMapDatas
articleTitle: FieldMapDatas
second_title: Aspose.Words for .NET
description: 发现 Odso FieldMapDatas，轻松将外部数据列映射到预定义的合并字段，确保无缝文档集成和增强数据准确性。
type: docs
weight: 50
url: /zh/net/aspose.words.settings/odso/fieldmapdatas/
---
## Odso.FieldMapDatas property

获取或设置对象集合，指定如何将外部数据源 中的列映射到文档中预定义的合并字段名称。 此对象永远不会`无效的`.

```csharp
public OdsoFieldMapDataCollection FieldMapDatas { get; set; }
```

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

* class [OdsoFieldMapDataCollection](../../odsofieldmapdatacollection/)
* class [Odso](../)
* 命名空间 [Aspose.Words.Settings](../../../aspose.words.settings/)
* 部件 [Aspose.Words](../../../)
