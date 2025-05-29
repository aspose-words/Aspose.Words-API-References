---
title: OdsoFieldMapData.MappedName
linktitle: MappedName
articleTitle: MappedName
second_title: Aspose.Words for .NET
description: 发现 OdsoFieldMapData MappedName 属性，该属性将合并字段名称链接到指定的列，从而提高数据映射的效率和准确性。
type: docs
weight: 30
url: /zh/net/aspose.words.settings/odsofieldmapdata/mappedname/
---
## OdsoFieldMapData.MappedName property

指定预定义的合并字段名称，该名称应映射到由[`Column`](../column/)此字段映射内的属性。 默认值为空字符串。

```csharp
public string MappedName { get; set; }
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

* class [OdsoFieldMapData](../)
* 命名空间 [Aspose.Words.Settings](../../../aspose.words.settings/)
* 部件 [Aspose.Words](../../../)
