---
title: FieldFillIn.DefaultResponse
second_title: Aspose.Words for .NET API 参考
description: FieldFillIn 财产. 获取或设置默认用户响应初始值包含在提示窗口中
type: docs
weight: 20
url: /zh/net/aspose.words.fields/fieldfillin/defaultresponse/
---
## FieldFillIn.DefaultResponse property

获取或设置默认用户响应（初始值包含在提示窗口中）。

```csharp
public string DefaultResponse { get; set; }
```

### 例子

显示如何使用 FILLIN 字段提示用户做出响应。

```csharp
public void FieldFillIn()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // 插入一个 FILLIN 字段。当我们在 Microsoft Word 中手动更新此字段时，
    // 它将提示我们输入响应。然后该字段会将响应显示为文本。
    FieldFillIn field = (FieldFillIn)builder.InsertField(FieldType.FieldFillIn, true);
    field.PromptText = "Please enter a response:";
    field.DefaultResponse = "A default response.";

    // 我们也可以使用这些字段来询问用户对每个页面的唯一响应
    // 在使用 Microsoft Word 完成的邮件合并期间创建。
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

/// <summary>
/// 在邮件合并期间为每个 FILLIN 字段的默认响应添加一行。
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
* 命名空间 [Aspose.Words.Fields](../../fieldfillin/)
* 部件 [Aspose.Words](../../../)


