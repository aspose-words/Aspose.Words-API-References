---
title: OdsoRecipientDataCollection.Clear
second_title: Aspose.Words for .NET API 参考
description: OdsoRecipientDataCollection 方法. 从此集合中删除所有元素
type: docs
weight: 50
url: /zh/net/aspose.words.settings/odsorecipientdatacollection/clear/
---
## OdsoRecipientDataCollection.Clear method

从此集合中删除所有元素。

```csharp
public void Clear()
```

### 例子

显示如何访问指定邮件合并将排除哪些合并数据源记录的数据集合。

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

// 我们还可以单独删除元素，或者一次性清除整个集合。
dataCollection.RemoveAt(0);

Assert.AreEqual(69, dataCollection.Count);

dataCollection.Clear();

Assert.AreEqual(0, dataCollection.Count);
```

### 也可以看看

* class [OdsoRecipientDataCollection](../)
* 命名空间 [Aspose.Words.Settings](../../odsorecipientdatacollection/)
* 部件 [Aspose.Words](../../../)


