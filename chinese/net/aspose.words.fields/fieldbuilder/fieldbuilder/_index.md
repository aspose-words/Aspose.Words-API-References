---
title: FieldBuilder.FieldBuilder
second_title: Aspose.Words for .NET API 参考
description: FieldBuilder 构造函数. 初始化一个实例FieldBuilder类.
type: docs
weight: 10
url: /zh/net/aspose.words.fields/fieldbuilder/fieldbuilder/
---
## FieldBuilder constructor

初始化一个实例[`FieldBuilder`](../)类.

```csharp
public FieldBuilder(FieldType fieldType)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fieldType | FieldType | 要构建的字段的类型。 |

### 例子

演示如何使用字段生成器创建和插入字段。

```csharp
Document doc = new Document();

// 将文本内容添加到文档的一种便捷方法是使用文档生成器。
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write(" Hello world! This text is one Run, which is an inline node.");

// 字段有其构建器，我们可以使用它来逐段构建字段代码。
// 在本例中，我们将构造一个表示美国邮政编码的 BARCODE 字段，
// 然后将其插入到 Run 前面。
FieldBuilder fieldBuilder = new FieldBuilder(FieldType.FieldBarcode);
fieldBuilder.AddArgument("90210");
fieldBuilder.AddSwitch("\\f", "A");
fieldBuilder.AddSwitch("\\u");

fieldBuilder.BuildAndInsert(doc.FirstSection.Body.FirstParagraph.Runs[0]);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CreateWithFieldBuilder.docx");
```

### 也可以看看

* enum [FieldType](../../fieldtype/)
* class [FieldBuilder](../)
* 命名空间 [Aspose.Words.Fields](../../fieldbuilder/)
* 部件 [Aspose.Words](../../../)


