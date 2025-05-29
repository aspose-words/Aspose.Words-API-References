---
title: OdsoRecipientData.Hash
linktitle: Hash
articleTitle: Hash
second_title: Aspose.Words for .NET
description: 探索 OdsoRecipientData Hash 属性，该属性为记录提供唯一的哈希码，从而增强 Microsoft Word 中的数据完整性。默认值为 0。
type: docs
weight: 40
url: /zh/net/aspose.words.settings/odsorecipientdata/hash/
---
## OdsoRecipientData.Hash property

表示此记录的哈希码。 有时 Microsoft Word 使用`Hash`整个记录，而不是[`UniqueTag`](../uniquetag/)值. 默认值为 0.

```csharp
public int Hash { get; set; }
```

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

* class [OdsoRecipientData](../)
* 命名空间 [Aspose.Words.Settings](../../../aspose.words.settings/)
* 部件 [Aspose.Words](../../../)
