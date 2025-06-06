---
title: OdsoRecipientDataCollection Class
linktitle: OdsoRecipientDataCollection
articleTitle: OdsoRecipientDataCollection
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Settings.OdsoRecipientDataCollection，这是一个功能强大的类型集合，用于在您的应用程序中有效地管理 OdsoRecipientData。
type: docs
weight: 6770
url: /zh/net/aspose.words.settings/odsorecipientdatacollection/
---
## OdsoRecipientDataCollection class

类型的集合[`OdsoRecipientData`](../odsorecipientdata/)

要了解更多信息，请访问[邮件合并和报告](https://docs.aspose.com/words/net/mail-merge-and-reporting/)文档文章。

```csharp
public class OdsoRecipientDataCollection : IEnumerable<OdsoRecipientData>
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [OdsoRecipientDataCollection](odsorecipientdatacollection/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Count](../../aspose.words.settings/odsorecipientdatacollection/count/) { get; } | 获取集合中包含的元素数量。 |
| [Item](../../aspose.words.settings/odsorecipientdatacollection/item/) { get; set; } | 获取或设置此集合中的项目。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Add](../../aspose.words.settings/odsorecipientdatacollection/add/)(*[OdsoRecipientData](../odsorecipientdata/)*) | 将对象添加到此集合的末尾。 |
| [Clear](../../aspose.words.settings/odsorecipientdatacollection/clear/)() | 从此集合中删除所有元素。 |
| [GetEnumerator](../../aspose.words.settings/odsorecipientdatacollection/getenumerator/)() | 返回一个枚举器对象，可用于迭代集合中的所有项目。 |
| [RemoveAt](../../aspose.words.settings/odsorecipientdatacollection/removeat/)(*int*) | 删除指定索引处的元素。 |

## 例子

展示如何访问指定邮件合并将排除哪些合并数据源记录的数据集合。

```csharp
Document doc = new Document(MyDir + "Odso data.docx");

OdsoRecipientDataCollection dataCollection = doc.MailMergeSettings.Odso.RecipientDatas;

Assert.AreEqual(70, dataCollection.Count);

using (IEnumerator<OdsoRecipientData> enumerator = dataCollection.GetEnumerator())
{
    int index = 0;
    while (enumerator.MoveNext())
    {
        Console.WriteLine(
            $"Odso recipient data index {index++} will {(enumerator.Current.Active ? "" : "not ")}be imported upon mail merge.");
        Console.WriteLine($"\tColumn #{enumerator.Current.Column}");
        Console.WriteLine($"\tHash code: {enumerator.Current.Hash}");
        Console.WriteLine($"\tContents array length: {enumerator.Current.UniqueTag.Length}");
    }
}

// 我们可以克隆这个集合中的元素。
Assert.AreNotEqual(dataCollection[0], dataCollection[0].Clone());

// 我们还可以单独删除元素，或者一次清除整个集合。
dataCollection.RemoveAt(0);

Assert.AreEqual(69, dataCollection.Count);

dataCollection.Clear();

Assert.AreEqual(0, dataCollection.Count);
```

### 也可以看看

* class [OdsoRecipientData](../odsorecipientdata/)
* 命名空间 [Aspose.Words.Settings](../../aspose.words.settings/)
* 部件 [Aspose.Words](../../)
