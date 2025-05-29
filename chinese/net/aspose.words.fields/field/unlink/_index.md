---
title: Field.Unlink
linktitle: Unlink
articleTitle: Unlink
second_title: Aspose.Words for .NET
description: 探索“字段取消链接”方法，轻松取消字段链接，增强数据管理并简化工作流程以获得最佳结果。
type: docs
weight: 130
url: /zh/net/aspose.words.fields/field/unlink/
---
## Field.Unlink method

执行字段取消链接。

```csharp
public bool Unlink()
```

### 返回值

`真的`如果该字段已取消链接，否则`错误的`.

## 评论

用最新的结果替换该字段。

某些字段（例如 XE（索引条目）字段和 SEQ（序列）字段）无法取消链接。

## 例子

显示如何取消链接字段。

```csharp
Document doc = new Document(MyDir + "Linked fields.docx");
doc.Range.Fields[1].Unlink();
```

### 也可以看看

* class [Field](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
