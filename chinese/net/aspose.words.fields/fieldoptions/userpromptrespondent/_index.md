---
title: FieldOptions.UserPromptRespondent
linktitle: UserPromptRespondent
articleTitle: UserPromptRespondent
second_title: 用于 .NET 的 Aspose.Words
description: FieldOptions UserPromptRespondent 财产. 获取或设置字段更新期间对用户提示的响应者 在 C#.
type: docs
weight: 220
url: /zh/net/aspose.words.fields/fieldoptions/userpromptrespondent/
---
## FieldOptions.UserPromptRespondent property

获取或设置字段更新期间对用户提示的响应者。

```csharp
public IFieldUserPromptRespondent UserPromptRespondent { get; set; }
```

## 评论

如果此属性的值设置为**无效的** 需要用户在 prompting 上响应的字段（例如[`FieldAsk`](../../fieldask/)或者[`FieldFillIn`](../../fieldfillin/)不更新。

默认值为**无效的**.

## 例子

展示如何创建 ASK 字段并设置其属性。

```csharp
[Test]
public void FieldAsk()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // 放置一个字段，将放置对我们的 ASK 字段的响应。
    FieldRef fieldRef = (FieldRef)builder.InsertField(FieldType.FieldRef, true);
    fieldRef.BookmarkName = "MyAskField";
    builder.Writeln();

    Assert.AreEqual(" REF  MyAskField", fieldRef.GetFieldCode());

    // 插入 ASK 字段并编辑其属性以通过书签名称引用我们的 REF 字段。
    FieldAsk fieldAsk = (FieldAsk)builder.InsertField(FieldType.FieldAsk, true);
    fieldAsk.BookmarkName = "MyAskField";
    fieldAsk.PromptText = "Please provide a response for this ASK field";
    fieldAsk.DefaultResponse = "Response from within the field.";
    fieldAsk.PromptOnceOnMailMerge = true;
    builder.Writeln();

    Assert.AreEqual(
        " ASK  MyAskField \"Please provide a response for this ASK field\" \\d \"Response from within the field.\" \\o",
        fieldAsk.GetFieldCode());

    // ASK 字段在邮件合并期间将默认响应应用于其各自的 REF 字段。
    DataTable table = new DataTable("My Table");
    table.Columns.Add("Column 1");
    table.Rows.Add("Row 1");
    table.Rows.Add("Row 2");

    FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
    fieldMergeField.FieldName = "Column 1";

    // 我们可以使用自定义提示响应器修改或覆盖 ASK 字段中的默认响应，
    // 这将在邮件合并期间发生。
    doc.FieldOptions.UserPromptRespondent = new MyPromptRespondent();
    doc.MailMerge.Execute(table);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.ASK.docx");

/// <summary>
/// 在邮件合并期间将文本添加到 ASK 字段的默认响应中。
/// </summary>
private class MyPromptRespondent : IFieldUserPromptRespondent
{
    public string Respond(string promptText, string defaultResponse)
    {
        return "Response from MyPromptRespondent. " + defaultResponse;
    }
}
```

### 也可以看看

* interface [IFieldUserPromptRespondent](../../ifielduserpromptrespondent/)
* class [FieldOptions](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
