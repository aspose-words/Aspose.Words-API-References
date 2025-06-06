---
title: FieldBuilder
linktitle: FieldBuilder
articleTitle: FieldBuilder
second_title: Aspose.Words for .NET
description: 探索 FieldBuilder，这款强大的工具可轻松创建和管理项目中的字段。立即简化您的工作流程！
type: docs
weight: 10
url: /zh/net/aspose.words.fields/fieldbuilder/fieldbuilder/
---
## FieldBuilder constructor

初始化[`FieldBuilder`](../)类.

```csharp
public FieldBuilder(FieldType fieldType)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fieldType | FieldType | 要构建的字段的类型。 |

## 例子

展示如何使用字段构建器创建和插入字段。

```csharp
Document doc = new Document();

// 向文档添加文本内容的便捷方法是使用文档构建器。
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write(" Hello world! This text is one Run, which is an inline node.");

// 字段有其构建器，我们可以使用它来逐个构建字段代码。
// 在这种情况下，我们将构建一个代表美国邮政编码的 BARCODE 字段，
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
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
