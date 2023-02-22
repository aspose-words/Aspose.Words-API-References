---
title: Class OdsoRecipientData
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Settings.OdsoRecipientData 班级. 表示有关要从邮件合并中排除的外部数据源中的单个记录的信息
type: docs
weight: 5630
url: /zh/net/aspose.words.settings/odsorecipientdata/
---
## OdsoRecipientData class

表示有关要从邮件合并中排除的外部数据源中的单个记录的信息。

```csharp
public class OdsoRecipientData
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [OdsoRecipientData](odsorecipientdata/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Active](../../aspose.words.settings/odsorecipientdata/active/) { get; set; } | 指定在进行邮件合并时是否将来自数据源的记录导入到文档中。 默认值为`真的`. |
| [Column](../../aspose.words.settings/odsorecipientdata/column/) { get; set; } | 指定数据源中包含当前记录的唯一数据的列。 默认值为 0。 |
| [Hash](../../aspose.words.settings/odsorecipientdata/hash/) { get; set; } | 表示此记录的哈希码。 有时 Microsoft Word 使用[`Hash`](./hash/)整条记录而不是[`UniqueTag`](./uniquetag/)value. 默认值为 0. |
| [UniqueTag](../../aspose.words.settings/odsorecipientdata/uniquetag/) { get; set; } | 指定包含唯一数据的列中给定记录的内容。 默认值为`无效的`. |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Clone](../../aspose.words.settings/odsorecipientdata/clone/)() | 返回此对象的深层克隆。 |

### 评论

如果将记录合并到合并文档中，则不需要有关该记录的信息。 但是，如果给定记录不应合并到合并文档中，则该记录的唯一键 的值应存储在[`UniqueTag`](./uniquetag/)此对象的属性以指示此排除。

### 例子

显示如何访问指定邮件合并将排除的合并数据源记录的数据集合。

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

// 我们也可以单独删除元素，或者一次清除整个集合。
dataCollection.RemoveAt(0);

Assert.AreEqual(69, dataCollection.Count);

dataCollection.Clear();

Assert.AreEqual(0, dataCollection.Count);
```

### 也可以看看

* 命名空间 [Aspose.Words.Settings](../../aspose.words.settings/)
* 部件 [Aspose.Words](../../)


