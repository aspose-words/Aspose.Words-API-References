---
title: Document.NormalizeFieldTypes
linktitle: NormalizeFieldTypes
articleTitle: NormalizeFieldTypes
second_title: Aspose.Words for .NET
description: 使用 NormalizeFieldTypes 方法优化您的文档，确保所有字段类型值与字段代码一致，以增强一致性和准确性。
type: docs
weight: 670
url: /zh/net/aspose.words/document/normalizefieldtypes/
---
## Document.NormalizeFieldTypes method

更改字段类型值[`FieldType`](../../../aspose.words.fields/fieldchar/fieldtype/)的[`FieldStart`](../../../aspose.words.fields/fieldstart/)，[`FieldSeparator`](../../../aspose.words.fields/fieldseparator/)，[`FieldEnd`](../../../aspose.words.fields/fieldend/) 在整个文档中，以便它们与字段代码中包含的字段类型相对应。

```csharp
public void NormalizeFieldTypes()
```

## 评论

在影响字段类型的文档更改后使用此方法。

要更改文档特定部分的字段类型值，请使用[`NormalizeFieldTypes`](../../range/normalizefieldtypes/)。

## 例子

展示如何使字段类型与字段代码保持同步。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE", null);

// Aspose.Words 根据字段代码自动检测字段类型。
Assert.AreEqual(FieldType.FieldDate, field.Type);

// 手动更改字段的原始文本，这决定了字段代码。
Run fieldText = (Run)doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Run, true)[0];
fieldText.Text = "PAGE";

// 更改字段代码已将此字段更改为其他类型，
// 但字段的类型属性仍然显示旧类型。
Assert.AreEqual("PAGE", field.GetFieldCode());
Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual(FieldType.FieldDate, field.Start.FieldType);
Assert.AreEqual(FieldType.FieldDate, field.Separator.FieldType);
Assert.AreEqual(FieldType.FieldDate, field.End.FieldType);

// 使用此方法更新这些属性以显示当前值。
doc.NormalizeFieldTypes();

Assert.AreEqual(FieldType.FieldPage, field.Type);
Assert.AreEqual(FieldType.FieldPage, field.Start.FieldType);
Assert.AreEqual(FieldType.FieldPage, field.Separator.FieldType);
Assert.AreEqual(FieldType.FieldPage, field.End.FieldType);
```

### 也可以看看

* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
