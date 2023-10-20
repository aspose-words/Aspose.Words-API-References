---
title: IFieldUserPromptRespondent Interface
linktitle: IFieldUserPromptRespondent
articleTitle: IFieldUserPromptRespondent
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Fields.IFieldUserPromptRespondent واجهه المستخدم. يمثل المستجيب لمطالبات المستخدم أثناء التحديث الميداني في C#.
type: docs
weight: 2740
url: /ar/net/aspose.words.fields/ifielduserpromptrespondent/
---
## IFieldUserPromptRespondent interface

يمثل المستجيب لمطالبات المستخدم أثناء التحديث الميداني.

```csharp
public interface IFieldUserPromptRespondent
```

## طُرق

| اسم | وصف |
| --- | --- |
| [Respond](../../aspose.words.fields/ifielduserpromptrespondent/respond/)(*string, string*) | عند التنفيذ، يُرجع استجابة من المستخدم عند المطالبة. يجب أن يعود التنفيذ الخاص بك`باطل` للإشارة إلى أن المستخدم لم يستجب للمطالبة (أي أن المستخدم قام بالضغط على زر إلغاء في نافذة المطالبة). |

## ملاحظات

حقول ASK وFILLIN هي أمثلة للحقول التي تطالب المستخدم ببعض الاستجابة. قم بتنفيذ هذه الواجهة وقم بتعيينها إلى[`UserPromptRespondent`](../fieldoptions/userpromptrespondent/) خاصية إنشاء تفاعل بين الحقل update والمستخدم.

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

* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)
