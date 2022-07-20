---
title: FieldData
second_title: Aspose.Words for .NET API 参考
description: 获取与字段关联的自定义字段数据
type: docs
weight: 10
url: /zh/net/aspose.words.fields/fieldstart/fielddata/
---
## FieldStart.FieldData property

获取与字段关联的自定义字段数据。

```csharp
public byte[] FieldData { get; }
```

### 例子

显示如何获取与字段关联的数据。

```csharp
Document doc = new Document(MyDir + "Field sample - Field with data.docx");

Field field = doc.Range.Fields[2];
Console.WriteLine(Encoding.Default.GetString(field.Start.FieldData));
```

### 也可以看看

* class [FieldStart](../../fieldstart)
* 命名空间 [Aspose.Words.Fields](../../fieldstart)
* 部件 [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->