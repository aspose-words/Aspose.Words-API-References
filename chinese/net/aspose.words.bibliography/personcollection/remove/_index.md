---
title: PersonCollection.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words for .NET
description: 使用 PersonCollection Remove 方法轻松从您的集合中移除人物。立即简化您的数据管理！
type: docs
weight: 70
url: /zh/net/aspose.words.bibliography/personcollection/remove/
---
## PersonCollection.Remove method

从集合中移除该人。

```csharp
public bool Remove(Person person)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| person | Person | 要从集合中移除的人员。 |

## 例子

展示如何使用人员集合。

```csharp
// 创建一个新的人员集合。
PersonCollection persons = new PersonCollection();
Person person = new Person("Roxanne", "Brielle", "Tejeda_updated");
// 将新人添加到集合中。
persons.Add(person);
Assert.AreEqual(1, persons.Count);
// 如果存在，则从集合中删除该人。
if (persons.Contains(person))
    persons.Remove(person);
Assert.AreEqual(0, persons.Count);

// 创建包含两个人的人员集合。
persons = new PersonCollection(new Person[] { new Person("Roxanne_1", "Brielle_1", "Tejeda_1"), new Person("Roxanne_2", "Brielle_2", "Tejeda_2") });
Assert.AreEqual(2, persons.Count);
// 根据索引从集合中删除人。
persons.RemoveAt(0);
Assert.AreEqual(1, persons.Count);
// 从集合中删除所有人。
persons.Clear();
Assert.AreEqual(0, persons.Count);
```

### 也可以看看

* class [Person](../../person/)
* class [PersonCollection](../)
* 命名空间 [Aspose.Words.Bibliography](../../../aspose.words.bibliography/)
* 部件 [Aspose.Words](../../../)
