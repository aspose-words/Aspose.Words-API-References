---
title: FieldStart.FieldData
linktitle: FieldData
articleTitle: FieldData
second_title: Aspose.Words for .NET
description: 使用 FieldStart 的 FieldData 属性解锁自定义字段数据，增强数据管理并轻松提高生产力。
type: docs
weight: 10
url: /zh/net/aspose.words.fields/fieldstart/fielddata/
---
## FieldStart.FieldData property

获取与该字段关联的自定义字段数据。

```csharp
public byte[] FieldData { get; }
```

## 例子

显示如何获取与字段相关的数据。

```csharp
Document doc = new Document(MyDir + "Field sample - Field with data.docx");

Field field = doc.Range.Fields[2];
Console.WriteLine(Encoding.UTF8.GetString(field.Start.FieldData));
```

### 也可以看看

* class [FieldStart](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
