---
title: IFieldUserPromptRespondent Interface
linktitle: IFieldUserPromptRespondent
articleTitle: IFieldUserPromptRespondent
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Fields.IFieldUserPromptRespondent 接口，旨在增强用户交互并无缝简化字段更新。
type: docs
weight: 3150
url: /zh/net/aspose.words.fields/ifielduserpromptrespondent/
---
## IFieldUserPromptRespondent interface

表示字段更新期间对用户提示的响应者。

```csharp
public interface IFieldUserPromptRespondent
```

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Respond](../../aspose.words.fields/ifielduserpromptrespondent/respond/)(*string, string*) | 实施后，返回用户在提示时的响应。 您的实施应该返回`无效的`表示用户尚未响应提示 （即用户按下了提示窗口中的“取消”按钮）。 |

## 评论

ASK 和 FILLIN 字段是提示用户输入内容的示例。请实现此接口 并将其分配给[`UserPromptRespondent`](../fieldoptions/userpromptrespondent/)属性来建立字段 update 和用户之间的交互。

## 例子

展示如何创建 ASK 字段并设置其属性。

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

    // 邮件合并期间，ASK 字段将默认响应应用于其各自的 REF 字段。
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

* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields/)
* 部件 [Aspose.Words](../../)
