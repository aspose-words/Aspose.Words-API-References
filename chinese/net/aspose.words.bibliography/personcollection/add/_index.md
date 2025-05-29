---
title: PersonCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words for .NET
description: 使用 PersonCollection 的 Add 方法，轻松将 Person 添加到您的集合中。简化数据管理，提升项目效率！
type: docs
weight: 40
url: /zh/net/aspose.words.bibliography/personcollection/add/
---
## PersonCollection.Add method

添加[`Person`](../../person/)到收藏夹。

```csharp
public void Add(Person person)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| person | Person | 要添加到收藏夹的人员。 |

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
