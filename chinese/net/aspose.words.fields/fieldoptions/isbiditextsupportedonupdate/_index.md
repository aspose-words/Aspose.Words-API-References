---
title: FieldOptions.IsBidiTextSupportedOnUpdate
linktitle: IsBidiTextSupportedOnUpdate
articleTitle: IsBidiTextSupportedOnUpdate
second_title: 用于 .NET 的 Aspose.Words
description: FieldOptions IsBidiTextSupportedOnUpdate 财产. 获取或设置指示字段更新期间是否完全支持双向文本的值 在 C#.
type: docs
weight: 150
url: /zh/net/aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/
---
## FieldOptions.IsBidiTextSupportedOnUpdate property

获取或设置指示字段更新期间是否完全支持双向文本的值。

```csharp
public bool IsBidiTextSupportedOnUpdate { get; set; }
```

## 评论

当该属性设置为`真的`，在更新期间执行附加步骤以生成从右到左的 language （即阿拉伯语或希伯来语）兼容的字段结果。

当该属性设置为`错误的`并且使用从右到左的语言，不保证字段result 更新后的正确性。

默认值为`错误的`。

## 例子

演示如何使用 FieldOptions 确保字段更新完全支持双向文本。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

 // 确保涉及从右到左文本的任何字段操作均按预期执行。
doc.FieldOptions.IsBidiTextSupportedOnUpdate = true;

// 使用文档生成器插入包含从右到左文本的字段。
FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "עֶשְׂרִים", "שְׁלוֹשִׁים", "אַרְבָּעִים", "חֲמִשִּׁים", "שִׁשִּׁים" }, 0);
comboBox.CalculateOnExit = true;

doc.UpdateFields();
doc.Save(ArtifactsDir + "FieldOptions.Bidi.docx");
```

### 也可以看看

* class [FieldOptions](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
