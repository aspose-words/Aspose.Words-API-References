---
title: OdsoFieldMapDataCollection Class
linktitle: OdsoFieldMapDataCollection
articleTitle: OdsoFieldMapDataCollection
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words OdsoFieldMapDataCollection 类，这是一个功能强大的类型集合，用于有效管理 OdsoFieldMapData 对象。
type: docs
weight: 6740
url: /zh/net/aspose.words.settings/odsofieldmapdatacollection/
---
## OdsoFieldMapDataCollection class

类型的集合[`OdsoFieldMapData`](../odsofieldmapdata/)对象.

要了解更多信息，请访问[邮件合并和报告](https://docs.aspose.com/words/net/mail-merge-and-reporting/)文档文章。

```csharp
public class OdsoFieldMapDataCollection : IEnumerable<OdsoFieldMapData>
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [OdsoFieldMapDataCollection](odsofieldmapdatacollection/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Count](../../aspose.words.settings/odsofieldmapdatacollection/count/) { get; } | 获取集合中包含的元素数量。 |
| [Item](../../aspose.words.settings/odsofieldmapdatacollection/item/) { get; set; } | 获取或设置此集合中的项目。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Add](../../aspose.words.settings/odsofieldmapdatacollection/add/)(*[OdsoFieldMapData](../odsofieldmapdata/)*) | 将对象添加到此集合的末尾。 |
| [Clear](../../aspose.words.settings/odsofieldmapdatacollection/clear/)() | 从此集合中删除所有元素。 |
| [GetEnumerator](../../aspose.words.settings/odsofieldmapdatacollection/getenumerator/)() | 返回一个枚举器对象，可用于迭代集合中的所有项目。 |
| [RemoveAt](../../aspose.words.settings/odsofieldmapdatacollection/removeat/)(*int*) | 删除指定索引处的元素。 |

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

* class [OdsoFieldMapData](../odsofieldmapdata/)
* property [FieldMapDatas](../odso/fieldmapdatas/)
* 命名空间 [Aspose.Words.Settings](../../aspose.words.settings/)
* 部件 [Aspose.Words](../../)
