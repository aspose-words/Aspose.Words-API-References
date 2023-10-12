---
title: OdsoFieldMapDataCollection.GetEnumerator
second_title: Aspose.Words for .NET API 参考
description: OdsoFieldMapDataCollection 方法. 返回一个枚举器对象可用于迭代集合中的所有项目
type: docs
weight: 60
url: /zh/net/aspose.words.settings/odsofieldmapdatacollection/getenumerator/
---
## OdsoFieldMapDataCollection.GetEnumerator method

返回一个枚举器对象，可用于迭代集合中的所有项目。

```csharp
public IEnumerator<OdsoFieldMapData> GetEnumerator()
```

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

* class [OdsoFieldMapData](../../odsofieldmapdata/)
* class [OdsoFieldMapDataCollection](../)
* 命名空间 [Aspose.Words.Settings](../../odsofieldmapdatacollection/)
* 部件 [Aspose.Words](../../../)


