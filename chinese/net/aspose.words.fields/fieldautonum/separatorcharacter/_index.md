---
title: FieldAutoNum.SeparatorCharacter
linktitle: SeparatorCharacter
articleTitle: SeparatorCharacter
second_title: Aspose.Words for .NET
description: 发现 FieldAutoNum SeparatorCharacter 属性，轻松自定义分隔符以增强数据格式并提高可用性。
type: docs
weight: 20
url: /zh/net/aspose.words.fields/fieldautonum/separatorcharacter/
---
## FieldAutoNum.SeparatorCharacter property

获取或设置要使用的分隔符。

```csharp
public string SeparatorCharacter { get; set; }
```

## 例子

展示如何使用自动编号字段对段落进行编号。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 每个 AUTONUM 字段显示 AUTONUM 字段运行计数的当前值，
// 允许我们像编号列表一样自动对项目进行编号。
// 该字段将显示数字“1”。
FieldAutoNum field = (FieldAutoNum)builder.InsertField(FieldType.FieldAutoNum, true);
builder.Writeln("\tParagraph 1.");

Assert.AreEqual(" AUTONUM ", field.GetFieldCode());

field = (FieldAutoNum)builder.InsertField(FieldType.FieldAutoNum, true);
builder.Writeln("\tParagraph 2.");

// 字段结果中紧跟在数字后面的分隔符默认为句号。
// 如果我们将此属性保留为空，则我们的第二个 AUTONUM 字段将在文档中显示“2”。
Assert.IsNull(field.SeparatorCharacter);

// 我们可以设置此属性以将其字符串的第一个字符作为新的分隔符。
// 在这种情况下，我们的 AUTONUM 字段现在将显示“2：”。
field.SeparatorCharacter = ":";

Assert.AreEqual(" AUTONUM  \\s :", field.GetFieldCode());

doc.Save(ArtifactsDir + "Field.AUTONUM.docx");
```

### 也可以看看

* class [FieldAutoNum](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
