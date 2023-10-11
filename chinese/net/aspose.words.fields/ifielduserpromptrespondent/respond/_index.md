---
title: IFieldUserPromptRespondent.Respond
second_title: Aspose.Words for .NET API 参考
description: IFieldUserPromptRespondent 方法. 实现后根据提示返回用户的响应 您的实现应该返回无效的表示用户尚未响应提示 即用户已按下提示窗口中的取消按钮
type: docs
weight: 10
url: /zh/net/aspose.words.fields/ifielduserpromptrespondent/respond/
---
## IFieldUserPromptRespondent.Respond method

实现后，根据提示返回用户的响应。 您的实现应该返回`无效的`表示用户尚未响应提示 （即用户已按下提示窗口中的“取消”按钮）。

```csharp
public string Respond(string promptText, string defaultResponse)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| promptText | String | 提示文本（即提示窗口的标题）。 |
| defaultResponse | String | 默认用户响应（即提示窗口中包含的初始值）。 |

### 返回值

用户响应（即提示窗口中包含的确认值）。

### 例子

演示如何创建 ASK 字段并设置其属性。

```csharp
public void FieldAsk()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // 放置一个字段，用于放置对 ASK 字段的响应。
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

    // 在邮件合并期间，ASK 字段将默认响应应用于各自的 REF 字段。
    DataTable table = new DataTable("My Table");
    table.Columns.Add("Column 1");
    table.Rows.Add("Row 1");
    table.Rows.Add("Row 2");

    FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
    fieldMergeField.FieldName = "Column 1";

    // 我们可以使用自定义提示响应程序修改或覆盖 ASK 字段中的默认响应，
    // 这将在邮件合并期间发生。
    doc.FieldOptions.UserPromptRespondent = new MyPromptRespondent();
    doc.MailMerge.Execute(table);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.ASK.docx");
}

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

* interface [IFieldUserPromptRespondent](../)
* 命名空间 [Aspose.Words.Fields](../../ifielduserpromptrespondent/)
* 部件 [Aspose.Words](../../../)


