---
title: List.HasSameTemplate
second_title: Aspose.Words for .NET API 参考
description: List 方法. 如果当前列表和给定列表是从同一模板创建的则返回 true
type: docs
weight: 120
url: /zh/net/aspose.words.lists/list/hassametemplate/
---
## List.HasSameTemplate method

如果当前列表和给定列表是从同一模板创建的，则返回 true。

```csharp
public bool HasSameTemplate(List other)
```

### 例子

演示如何使用相同的 ListDefId 定义列表。

```csharp
Document doc = new Document(MyDir + "Different lists.docx");

Assert.True(doc.Lists[0].HasSameTemplate(doc.Lists[1]));
Assert.False(doc.Lists[1].HasSameTemplate(doc.Lists[2]));
```

### 也可以看看

* class [List](../)
* 命名空间 [Aspose.Words.Lists](../../list/)
* 部件 [Aspose.Words](../../../)


