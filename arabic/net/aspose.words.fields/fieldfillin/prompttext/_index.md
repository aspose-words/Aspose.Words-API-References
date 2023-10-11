---
title: FieldFillIn.PromptText
second_title: Aspose.Words لمراجع .NET API
description: FieldFillIn ملكية. الحصول على نص المطالبة أو تعيينه عنوان نافذة المطالبة.
type: docs
weight: 40
url: /ar/net/aspose.words.fields/fieldfillin/prompttext/
---
## FieldFillIn.PromptText property

الحصول على نص المطالبة أو تعيينه (عنوان نافذة المطالبة).

```csharp
public string PromptText { get; set; }
```

### أمثلة

يوضح كيفية استخدام حقل FILLIN لمطالبة المستخدم بالرد.

```csharp
public void FieldFillIn()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // أدخل حقل FILLIN. عندما نقوم بتحديث هذا الحقل يدويًا في Microsoft Word،
    // سيطالبنا بإدخال الرد. سيعرض الحقل بعد ذلك الرد كنص.
    FieldFillIn field = (FieldFillIn)builder.InsertField(FieldType.FieldFillIn, true);
    field.PromptText = "Please enter a response:";
    field.DefaultResponse = "A default response.";

    // يمكننا أيضًا استخدام هذه الحقول لمطالبة المستخدم باستجابة فريدة لكل صفحة
    // تم إنشاؤه أثناء عملية دمج البريد باستخدام Microsoft Word.
    field.PromptOnceOnMailMerge = true;

    Assert.AreEqual(" FILLIN  \"Please enter a response:\" \\d \"A default response.\" \\o", field.GetFieldCode());

    FieldMergeField mergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
    mergeField.FieldName = "MergeField";

    // إذا قمنا بدمج البريد برمجيًا، فيمكننا استخدام مستجيب موجه مخصص
    // لتحرير الاستجابات تلقائيًا لحقول FILLIN التي يواجهها دمج البريد.
    doc.FieldOptions.UserPromptRespondent = new PromptRespondent();
    doc.MailMerge.Execute(new [] { "MergeField" }, new object[] { "" });

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.FILLIN.docx");
}

/// <summary>
/// يسبق سطرًا للاستجابة الافتراضية لكل حقل FILLIN أثناء دمج البريد.
/// </summary>
private class PromptRespondent : IFieldUserPromptRespondent
{
    public string Respond(string promptText, string defaultResponse)
    {
        return "Response modified by PromptRespondent. " + defaultResponse;
    }
}
```

### أنظر أيضا

* class [FieldFillIn](../)
* مساحة الاسم [Aspose.Words.Fields](../../fieldfillin/)
* المجسم [Aspose.Words](../../../)


