---
title: IFieldUserPromptRespondent.Respond
linktitle: Respond
articleTitle: Respond
second_title: Aspose.Words لـ .NET
description: IFieldUserPromptRespondent Respond طريقة. عند التنفيذ يُرجع استجابة من المستخدم عند المطالبة. يجب أن يعود التنفيذ الخاص بكباطل للإشارة إلى أن المستخدم لم يستجب للمطالبة أي أن المستخدم قام بالضغط على زر إلغاء في نافذة المطالبة في C#.
type: docs
weight: 10
url: /ar/net/aspose.words.fields/ifielduserpromptrespondent/respond/
---
## IFieldUserPromptRespondent.Respond method

عند التنفيذ، يُرجع استجابة من المستخدم عند المطالبة. يجب أن يعود التنفيذ الخاص بك`باطل` للإشارة إلى أن المستخدم لم يستجب للمطالبة (أي أن المستخدم قام بالضغط على زر إلغاء في نافذة المطالبة).

```csharp
public string Respond(string promptText, string defaultResponse)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| promptText | String | نص موجه (أي عنوان نافذة المطالبة). |
| defaultResponse | String | استجابة المستخدم الافتراضية (أي القيمة الأولية الموجودة في نافذة المطالبة). |

### قيمة الإرجاع

استجابة المستخدم (أي القيمة المؤكدة الموجودة في نافذة المطالبة).

## أمثلة

يوضح كيفية إنشاء حقل ASK وتعيين خصائصه.

```csharp
public void FieldAsk()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // ضع حقلاً حيث سيتم وضع الرد على حقل ASK الخاص بنا.
    FieldRef fieldRef = (FieldRef)builder.InsertField(FieldType.FieldRef, true);
    fieldRef.BookmarkName = "MyAskField";
    builder.Writeln();

    Assert.AreEqual(" REF  MyAskField", fieldRef.GetFieldCode());

    // أدخل حقل ASK وقم بتحرير خصائصه للإشارة إلى حقل REF الخاص بنا حسب اسم الإشارة المرجعية.
    FieldAsk fieldAsk = (FieldAsk)builder.InsertField(FieldType.FieldAsk, true);
    fieldAsk.BookmarkName = "MyAskField";
    fieldAsk.PromptText = "Please provide a response for this ASK field";
    fieldAsk.DefaultResponse = "Response from within the field.";
    fieldAsk.PromptOnceOnMailMerge = true;
    builder.Writeln();

    Assert.AreEqual(
        " ASK  MyAskField \"Please provide a response for this ASK field\" \\d \"Response from within the field.\" \\o",
        fieldAsk.GetFieldCode());

    // تقوم حقول ASK بتطبيق الاستجابة الافتراضية على حقول REF الخاصة بها أثناء دمج البريد.
    DataTable table = new DataTable("My Table");
    table.Columns.Add("Column 1");
    table.Rows.Add("Row 1");
    table.Rows.Add("Row 2");

    FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
    fieldMergeField.FieldName = "Column 1";

    // يمكننا تعديل أو تجاوز الاستجابة الافتراضية في حقول ASK الخاصة بنا باستخدام مستجيب سريع مخصص،
    // والذي سيحدث أثناء دمج البريد.
    doc.FieldOptions.UserPromptRespondent = new MyPromptRespondent();
    doc.MailMerge.Execute(table);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.ASK.docx");
}

/// <summary>
/// يُلحق النص بالاستجابة الافتراضية لحقل ASK أثناء دمج البريد.
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

* interface [IFieldUserPromptRespondent](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
