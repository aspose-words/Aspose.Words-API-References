---
title: OdsoRecipientData.Hash
linktitle: Hash
articleTitle: Hash
second_title: 用于 .NET 的 Aspose.Words
description: OdsoRecipientData Hash 财产. 表示该记录的哈希码 有时 Microsoft Word 使用Hash整个记录而不是UniqueTag值. 默认值为 0 在 C#.
type: docs
weight: 40
url: /zh/net/aspose.words.settings/odsorecipientdata/hash/
---
## OdsoRecipientData.Hash property

表示该记录的哈希码。 有时 Microsoft Word 使用`Hash`整个记录而不是[`UniqueTag`](../uniquetag/)值. 默认值为 0.

```csharp
public int Hash { get; set; }
```

## 例子

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

* class [OdsoRecipientData](../)
* 命名空间 [Aspose.Words.Settings](../../../aspose.words.settings/)
* 部件 [Aspose.Words](../../../)
