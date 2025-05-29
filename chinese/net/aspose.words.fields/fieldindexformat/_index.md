---
title: FieldIndexFormat Enum
linktitle: FieldIndexFormat
articleTitle: FieldIndexFormat
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.FieldIndexFormat 枚举，自定义文档中的 FieldIndex 格式。轻松增强文档结构！
type: docs
weight: 2480
url: /zh/net/aspose.words.fields/fieldindexformat/
---
## FieldIndexFormat enumeration

指定[`FieldIndex`](../fieldindex/)文档中的字段。

```csharp
public enum FieldIndexFormat
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Template | `0` | 来自模板。 |
| Classic | `1` | 经典的。 |
| Fancy | `2` | 想要。 |
| Modern | `3` | 现代的。 |
| Bulleted | `4` | 项目符号。 |
| Formal | `5` | 正式的。 |
| Simple | `6` | 简单的。 |

## 例子

展示如何格式化 FieldIndex 字段。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("A");
builder.InsertBreak(BreakType.LineBreak);
builder.InsertField("XE \"A\"");
builder.Write("B");

builder.InsertField(" INDEX \\e \" · \" \\h \"A\" \\c \"2\" \\z \"1033\"", null);

doc.FieldOptions.FieldIndexFormat = FieldIndexFormat.Fancy;
doc.UpdateFields();

doc.Save(ArtifactsDir + "Field.SetFieldIndexFormat.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields/)
* 部件 [Aspose.Words](../../)
