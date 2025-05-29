---
title: Field.GetFieldCode
linktitle: GetFieldCode
articleTitle: GetFieldCode
second_title: Aspose.Words for .NET
description: 探索 GetFieldCode 方法，轻松检索字段起始和分隔符之间的文本，包括子字段代码和结果。提升您的编码效率！
type: docs
weight: 110
url: /zh/net/aspose.words.fields/field/getfieldcode/
---
## GetFieldCode() {#getfieldcode}

返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 包括子字段的字段代码和字段结果。

```csharp
public string GetFieldCode()
```

## 例子

展示如何使用字段代码将字段插入文档。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// InsertField 方法的此重载会自动更新插入的字段。
Assert.True((DateTime.Today - DateTime.Parse(field.Result)).Days <= 1);
```

显示如何获取字段的字段代码。

```csharp
// 打开包含 IF 字段内的 MERGEFIELD 的文档。
Document doc = new Document(MyDir + "Nested fields.docx");
FieldIf fieldIf = (FieldIf)doc.Range.Fields[0];

// 获取字段的字段代码有两种方法：
// 1 - 省略其内部字段：
Assert.AreEqual(" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf.GetFieldCode(false));

// 2 - 包括其内部字段：
Assert.AreEqual($" IF \u0013 MERGEFIELD NetIncome \u0014\u0015 > 0 \" (surplus of \u0013 MERGEFIELD  NetIncome \\f $ \u0014\u0015) \" \"\" ",
    fieldIf.GetFieldCode(true));

// 默认情况下，GetFieldCode 方法显示内部字段。
Assert.AreEqual(fieldIf.GetFieldCode(), fieldIf.GetFieldCode(true));
```

### 也可以看看

* class [Field](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)

---

## GetFieldCode(*bool*) {#getfieldcode_1}

返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。

```csharp
public string GetFieldCode(bool includeChildFieldCodes)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| includeChildFieldCodes | Boolean | `真的`是否应包括子字段代码。 |

## 例子

显示如何获取字段的字段代码。

```csharp
// 打开包含 IF 字段内的 MERGEFIELD 的文档。
Document doc = new Document(MyDir + "Nested fields.docx");
FieldIf fieldIf = (FieldIf)doc.Range.Fields[0];

// 获取字段的字段代码有两种方法：
// 1 - 省略其内部字段：
Assert.AreEqual(" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf.GetFieldCode(false));

// 2 - 包括其内部字段：
Assert.AreEqual($" IF \u0013 MERGEFIELD NetIncome \u0014\u0015 > 0 \" (surplus of \u0013 MERGEFIELD  NetIncome \\f $ \u0014\u0015) \" \"\" ",
    fieldIf.GetFieldCode(true));

// 默认情况下，GetFieldCode 方法显示内部字段。
Assert.AreEqual(fieldIf.GetFieldCode(), fieldIf.GetFieldCode(true));
```

### 也可以看看

* class [Field](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
