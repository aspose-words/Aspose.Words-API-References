---
title: FieldOptions.UserPromptRespondent
linktitle: UserPromptRespondent
articleTitle: UserPromptRespondent
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية FieldOptions UserPromptRespondent على تحسين تجربة المستخدم من خلال إدارة تفاعلات المستجيب أثناء تحديثات الحقل.
type: docs
weight: 220
url: /ar/net/aspose.words.fields/fieldoptions/userpromptrespondent/
---
## FieldOptions.UserPromptRespondent property

يحصل على المستجيب أو يعينه على مطالبات المستخدم أثناء تحديث الحقل.

```csharp
public IFieldUserPromptRespondent UserPromptRespondent { get; set; }
```

## ملاحظات

إذا تم تعيين قيمة هذه الخاصية على`باطل` ، الحقول التي تتطلب استجابة المستخدم على prompting (مثل[`FieldAsk`](../../fieldask/) أو[`FieldFillIn`](../../fieldfillin/)) لا يتم تحديثها.

القيمة الافتراضية هي`باطل`.

## أمثلة

يوضح كيفية إنشاء حقل ASK وتعيين خصائصه.

```csharp
public void FieldAsk()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // ضع حقلًا حيث سيتم وضع الاستجابة لحقل ASK الخاص بنا.
    FieldRef fieldRef = (FieldRef)builder.InsertField(FieldType.FieldRef, true);
    fieldRef.BookmarkName = "MyAskField";
    builder.Writeln();

    Assert.AreEqual(" REF  MyAskField", fieldRef.GetFieldCode());

    // أدخل حقل ASK وقم بتحرير خصائصه للإشارة إلى حقل REF الخاص بنا عن طريق اسم الإشارة المرجعية.
    FieldAsk fieldAsk = (FieldAsk)builder.InsertField(FieldType.FieldAsk, true);
    fieldAsk.BookmarkName = "MyAskField";
    fieldAsk.PromptText = "Please provide a response for this ASK field";
    fieldAsk.DefaultResponse = "Response from within the field.";
    fieldAsk.PromptOnceOnMailMerge = true;
    builder.Writeln();

    Assert.AreEqual(
        " ASK  MyAskField \"Please provide a response for this ASK field\" \\d \"Response from within the field.\" \\o",
        fieldAsk.GetFieldCode());

    // تطبق حقول ASK الاستجابة الافتراضية على حقول REF الخاصة بها أثناء دمج البريد.
    DataTable table = new DataTable("My Table");
    table.Columns.Add("Column 1");
    table.Rows.Add("Row 1");
    table.Rows.Add("Row 2");

    FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
    fieldMergeField.FieldName = "Column 1";

    // يمكننا تعديل أو تجاوز الاستجابة الافتراضية في حقول ASK باستخدام مستجيب مطالبة مخصص،
    // والذي سيحدث أثناء دمج البريد.
    doc.FieldOptions.UserPromptRespondent = new MyPromptRespondent();
    doc.MailMerge.Execute(table);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.ASK.docx");
}

/// <summary>
/// إضافة نص إلى الاستجابة الافتراضية لحقل ASK أثناء دمج البريد.
/// </summary>
private class MyPromptRespondent : IFieldUserPromptRespondent
{
    public string Respond(string promptText, string defaultResponse)
    {
        return "Response from MyPromptRespondent. " + defaultResponse;
    }
}
```

### أنظر أيضا

* interface [IFieldUserPromptRespondent](../../ifielduserpromptrespondent/)
* class [FieldOptions](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
