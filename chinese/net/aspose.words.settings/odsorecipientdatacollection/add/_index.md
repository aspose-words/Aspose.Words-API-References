---
title: OdsoRecipientDataCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words for .NET
description: 使用 OdsoRecipientDataCollection Add 方法轻松增强您的数据管理——快速添加对象以简化您的收集流程。
type: docs
weight: 40
url: /zh/net/aspose.words.settings/odsorecipientdatacollection/add/
---
## OdsoRecipientDataCollection.Add method

将对象添加到此集合的末尾。

```csharp
public int Add(OdsoRecipientData value)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | OdsoRecipientData | 要添加的对象。不能`无效的`。 |

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

* class [OdsoRecipientData](../../odsorecipientdata/)
* class [OdsoRecipientDataCollection](../)
* 命名空间 [Aspose.Words.Settings](../../../aspose.words.settings/)
* 部件 [Aspose.Words](../../../)
