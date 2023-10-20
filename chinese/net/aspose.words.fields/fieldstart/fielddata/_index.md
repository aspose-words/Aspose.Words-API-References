---
title: FieldStart.FieldData
linktitle: FieldData
articleTitle: FieldData
second_title: 用于 .NET 的 Aspose.Words
description: FieldStart FieldData 财产. 获取与字段关联的自定义字段数据 在 C#.
type: docs
weight: 10
url: /zh/net/aspose.words.fields/fieldstart/fielddata/
---
## FieldStart.FieldData property

获取与字段关联的自定义字段数据。

```csharp
public byte[] FieldData { get; }
```

## 例子

展示如何获取与字段关联的数据。

```csharp
Document doc = new Document(MyDir + "Field sample - Field with data.docx");

Field field = doc.Range.Fields[2];
Console.WriteLine(Encoding.Default.GetString(field.Start.FieldData));
```

### 也可以看看

* class [FieldStart](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
