---
title: FieldDocVariable.VariableName
linktitle: VariableName
articleTitle: VariableName
second_title: Aspose.Words for .NET
description: 探索 FieldDocVariable VariableName 属性，轻松管理文档变量。立即简化检索并增强您的文档管理！
type: docs
weight: 20
url: /zh/net/aspose.words.fields/fielddocvariable/variablename/
---
## FieldDocVariable.VariableName property

获取或设置要检索的文档变量的名称。

```csharp
public string VariableName { get; set; }
```

## 例子

展示如何使用 DOCPROPERTY 字段显示文档属性和变量。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 以下是使用 DOCPROPERTY 字段的两种方法。
// 1 - 显示内置属性：
// 为“Category”内置属性设置自定义值，然后插入引用它的 DOCPROPERTY 字段。
doc.BuiltInDocumentProperties.Category = "My category";

FieldDocProperty fieldDocProperty = (FieldDocProperty)builder.InsertField(" DOCPROPERTY Category ");
fieldDocProperty.Update();

Assert.AreEqual(" DOCPROPERTY Category ", fieldDocProperty.GetFieldCode());
Assert.AreEqual("My category", fieldDocProperty.Result);

builder.InsertParagraph();

// 2 - 显示自定义文档变量：
// 定义一个自定义变量，然后使用 DOCPROPERTY 字段引用该变量。
Assert.AreEqual(0, doc.Variables.Count);
doc.Variables.Add("My variable", "My variable's value");

FieldDocVariable fieldDocVariable = (FieldDocVariable)builder.InsertField(FieldType.FieldDocVariable, true);
fieldDocVariable.VariableName = "My Variable";
fieldDocVariable.Update();

Assert.AreEqual(" DOCVARIABLE  \"My Variable\"", fieldDocVariable.GetFieldCode());
Assert.AreEqual("My variable's value", fieldDocVariable.Result);

doc.Save(ArtifactsDir + "Field.DOCPROPERTY.DOCVARIABLE.docx");
```

### 也可以看看

* class [FieldDocVariable](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
