---
title: Odso.FieldMapDatas
second_title: Aspose.Words for .NET API 参考
description: Odso 财产. 获取或设置对象集合这些对象指定如何将外部数据源 中的列映射到文档中的预定义合并字段名称 该对象从不无效的.
type: docs
weight: 50
url: /zh/net/aspose.words.settings/odso/fieldmapdatas/
---
## Odso.FieldMapDatas property

获取或设置对象集合，这些对象指定如何将外部数据源 中的列映射到文档中的预定义合并字段名称。 该对象从不`无效的`.

```csharp
public OdsoFieldMapDataCollection FieldMapDatas { get; set; }
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

* class [OdsoFieldMapDataCollection](../../odsofieldmapdatacollection/)
* class [Odso](../)
* 命名空间 [Aspose.Words.Settings](../../odso/)
* 部件 [Aspose.Words](../../../)


