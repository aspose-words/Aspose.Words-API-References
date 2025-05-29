---
title: FieldFillIn Class
linktitle: FieldFillIn
articleTitle: FieldFillIn
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Fields.FieldFillIn 类，轻松实现 FILLIN 字段，增强文档自动化和用户交互性。
type: docs
weight: 2300
url: /zh/net/aspose.words.fields/fieldfillin/
---
## FieldFillIn class

实现 FILLIN 字段。

要了解更多信息，请访问[使用字段](https://docs.aspose.com/words/net/working-with-fields/)文档文章。

```csharp
public class FieldFillIn : Field
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [FieldFillIn](fieldfillin/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [DefaultResponse](../../aspose.words.fields/fieldfillin/defaultresponse/) { get; set; } | 获取或设置默认用户响应（提示窗口中包含的初始值）。 |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | 获取表示显示字段结果的文本。 |
| [End](../../aspose.words.fields/field/end/) { get; } | 获取代表字段结束的节点。 |
| [Format](../../aspose.words.fields/field/format/) { get; } | 获得[`FieldFormat`](../fieldformat/)提供对字段格式进行类型化访问的对象。 |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | 获取或设置字段的当前结果是否由于对文档所做的其他修改而不再正确（陈旧）。 |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | 获取或设置字段的 LCID。 |
| [PromptOnceOnMailMerge](../../aspose.words.fields/fieldfillin/promptonceonmailmerge/) { get; set; } | 获取或设置是否应在每次邮件合并操作中接收一次用户响应。 |
| [PromptText](../../aspose.words.fields/fieldfillin/prompttext/) { get; set; } | 获取或设置提示文本（提示窗口的标题）。 |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | 获取或设置字段分隔符和字段结尾之间的文本。 |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | 获取表示字段分隔符的节点。可以是`无效的`. |
| [Start](../../aspose.words.fields/field/start/) { get; } | 获取表示字段开始的节点。 |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | 获取 Microsoft Word 字段类型。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 包括子字段的字段代码和字段结果。 |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 |
| [Remove](../../aspose.words.fields/field/remove/)() | 从文档中移除该字段。返回紧接该字段之后的节点。如果该字段的末尾是其父节点的最后一个 child ，则返回其父段落。如果该字段已被移除，则返回`无效的`. |
| [Unlink](../../aspose.words.fields/field/unlink/)() | 执行字段取消链接。 |
| [Update](../../aspose.words.fields/field/update/)() | 执行字段更新。如果字段已在更新，则抛出异常。 |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | 执行字段更新。如果字段已在更新，则抛出异常。 |

## 评论

提示用户输入文本。

## 例子

展示如何使用 FILLIN 字段提示用户做出回应。

```csharp
public void FieldFillIn()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // 插入一个 FILLIN 字段。当我们在 Microsoft Word 中手动更新此字段时，
    // 它会提示我们输入答案。然后，该字段将以文本形式显示答案。
    FieldFillIn field = (FieldFillIn)builder.InsertField(FieldType.FieldFillIn, true);
    field.PromptText = "Please enter a response:";
    field.DefaultResponse = "A default response.";

    // 我们还可以使用这些字段来要求用户对每个页面做出唯一的响应
    // 在使用 Microsoft Word 进行邮件合并时创建。
    field.PromptOnceOnMailMerge = true;

    Assert.AreEqual(" FILLIN  \"Please enter a response:\" \\d \"A default response.\" \\o", field.GetFieldCode());

    FieldMergeField mergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
    mergeField.FieldName = "MergeField";

    // 如果我们以编程方式执行邮件合并，我们可以使用自定义提示响应者
    // 自动编辑邮件合并遇到的 FILLIN 字段的响应。
    doc.FieldOptions.UserPromptRespondent = new PromptRespondent();
    doc.MailMerge.Execute(new [] { "MergeField" }, new object[] { "" });

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.FILLIN.docx");
}

/// <summary>
/// 在邮件合并期间，在每个 FILLIN 字段的默认响应前添加一行。
/// </summary>
private class PromptRespondent : IFieldUserPromptRespondent
{
    public string Respond(string promptText, string defaultResponse)
    {
        return "Response modified by PromptRespondent. " + defaultResponse;
    }
}
```

### 也可以看看

* class [Field](../field/)
* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields/)
* 部件 [Aspose.Words](../../)
