---
title: KnownTypeSet.Add
linktitle: Add
articleTitle: Add
second_title: 用于 .NET 的 Aspose.Words
description: KnownTypeSet Add 方法. 添加指定的Type对象到集合投掷ArgumentException在 以下情况 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words.reporting/knowntypeset/add/
---
## KnownTypeSet.Add method

添加指定的Type对象到集合。投掷ArgumentException在 以下情况：

-*type*是`无效的`。

-*type*代表一个void类型。

-*type*表示不可见类型，即非公共类型或具有非公共外部类型的公共嵌套 type 。

-*type*代表一个泛型类型。

-*type*代表数组类型。

-*type*已经添加到集合中。

```csharp
public void Add(Type type)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| type | Type | AType要添加的对象。 |

### 也可以看看

* class [KnownTypeSet](../)
* 命名空间 [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* 部件 [Aspose.Words](../../../)
