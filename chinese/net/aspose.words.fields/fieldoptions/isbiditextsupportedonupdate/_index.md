---
title: FieldOptions.IsBidiTextSupportedOnUpdate
linktitle: IsBidiTextSupportedOnUpdate
articleTitle: IsBidiTextSupportedOnUpdate
second_title: 用于 .NET 的 Aspose.Words
description: FieldOptions IsBidiTextSupportedOnUpdate 财产. 获取或设置字段更新时是否完全支持双向文本的值 在 C#.
type: docs
weight: 150
url: /zh/net/aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/
---
## FieldOptions.IsBidiTextSupportedOnUpdate property

获取或设置字段更新时是否完全支持双向文本的值。

```csharp
public bool IsBidiTextSupportedOnUpdate { get; set; }
```

## 评论

当此属性设置为**真的**，执行附加步骤以在更新期间生成从右到左的 language （即阿拉伯语或希伯来语）兼容的字段结果。

当此属性设置为**错误的**并且使用了从右到左的语言，不保证更新后字段 result 的正确性。

默认值为**错误的**.

## 例子

演示如何使用 FieldOptions 确保字段更新完全支持双向文本。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 确保任何涉及从右到左文本的字段操作都按预期执行。 
doc.FieldOptions.IsBidiTextSupportedOnUpdate = true;

// 使用文档构建器插入包含从右到左文本的字段。
FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "עֶשְׂרִים", "שְׁלוֹשִׁים", "אַרְבָּעִים", "חֲמִשִּׁים", "שִׁשִּׁים" }, 0);
comboBox.CalculateOnExit = true;

doc.UpdateFields();
doc.Save(ArtifactsDir + "FieldOptions.Bidi.docx");
```

### 也可以看看

* class [FieldOptions](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
