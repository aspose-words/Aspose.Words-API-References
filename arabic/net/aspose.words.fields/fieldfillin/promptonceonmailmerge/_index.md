---
title: FieldFillIn.PromptOnceOnMailMerge
linktitle: PromptOnceOnMailMerge
articleTitle: PromptOnceOnMailMerge
second_title: Aspose.Words لـ .NET
description: حسّن دمج البريد باستخدام خاصية PromptOnceOnMailMerge. تحكّم في ردود المستخدمين لجمع البيانات بكفاءة في مستنداتك.
type: docs
weight: 30
url: /ar/net/aspose.words.fields/fieldfillin/promptonceonmailmerge/
---
## FieldFillIn.PromptOnceOnMailMerge property

يحصل على أو يحدد ما إذا كان يجب استلام استجابة المستخدم مرة واحدة لكل عملية دمج بريد.

```csharp
public bool PromptOnceOnMailMerge { get; set; }
```

## أمثلة

يوضح كيفية استخدام حقل FILLIN لمطالبة المستخدم بالاستجابة.

```csharp
public void FieldFillIn()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // أدخل حقل FILLIN. عند تحديث هذا الحقل يدويًا في Microsoft Word،
    // سيُطلب منا إدخال رد. سيعرض الحقل الرد كنص.
    FieldFillIn field = (FieldFillIn)builder.InsertField(FieldType.FieldFillIn, true);
    field.PromptText = "Please enter a response:";
    field.DefaultResponse = "A default response.";

    // يمكننا أيضًا استخدام هذه الحقول لطلب استجابة فريدة من المستخدم لكل صفحة
    // تم إنشاؤه أثناء دمج البريد باستخدام Microsoft Word.
    field.PromptOnceOnMailMerge = true;

    Assert.AreEqual(" FILLIN  \"Please enter a response:\" \\d \"A default response.\" \\o", field.GetFieldCode());

    FieldMergeField mergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
    mergeField.FieldName = "MergeField";

    // إذا قمنا بدمج البريد برمجيًا، فيمكننا استخدام مستجيب مطالبة مخصص
    // لتحرير الاستجابات تلقائيًا لحقول FILLIN التي يواجهها دمج البريد.
    doc.FieldOptions.UserPromptRespondent = new PromptRespondent();
    doc.MailMerge.Execute(new [] { "MergeField" }, new object[] { "" });

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.FILLIN.docx");
}

/// <summary>
/// إضافة سطر إلى الاستجابة الافتراضية لكل حقل FILLIN أثناء دمج البريد.
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
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
