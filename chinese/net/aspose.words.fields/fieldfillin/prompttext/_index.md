---
title: FieldFillIn.PromptText
linktitle: PromptText
articleTitle: PromptText
second_title: 用于 .NET 的 Aspose.Words
description: FieldFillIn PromptText 财产. 获取或设置提示文本提示窗口的标题 在 C#.
type: docs
weight: 40
url: /zh/net/aspose.words.fields/fieldfillin/prompttext/
---
## FieldFillIn.PromptText property

获取或设置提示文本（提示窗口的标题）。

```csharp
public string PromptText { get; set; }
```

## 例子

演示如何使用 FILLIN 字段提示用户做出响应。

```csharp
public void FieldFillIn()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // 插入 FILLIN 字段。当我们在 Microsoft Word 中手动更新此字段时，
    // 它会提示我们输入响应。然后该字段将以文本形式显示响应。
    FieldFillIn field = (FieldFillIn)builder.InsertField(FieldType.FieldFillIn, true);
    field.PromptText = "Please enter a response:";
    field.DefaultResponse = "A default response.";

    // 我们还可以使用这些字段向用户询问每个页面的唯一响应
    // 在使用 Microsoft Word 完成邮件合并期间创建。
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
/// 在邮件合并期间，在每个 FILLIN 字段的默认响应前面添加一行。
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

* class [FieldFillIn](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
