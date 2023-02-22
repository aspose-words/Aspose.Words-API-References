---
title: FieldComments.Text
second_title: Aspose.Words لمراجع .NET API
description: FieldComments ملكية. الحصول على نص التعليقات أو تعيينه.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldcomments/text/
---
## FieldComments.Text property

الحصول على نص التعليقات أو تعيينه.

```csharp
public string Text { get; set; }
```

### أمثلة

يوضح كيفية استخدام حقل "التعليقات".

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// تعيين قيمة لخاصية "التعليقات" المضمنة في المستند.
doc.BuiltInDocumentProperties.Comments = "My comment.";

// قم بإنشاء حقل "تعليقات" لعرض قيمة هذه الخاصية المضمنة.
FieldComments field = (FieldComments)builder.InsertField(FieldType.FieldComments, true);
field.Update();

Assert.AreEqual(" COMMENTS ", field.GetFieldCode());
Assert.AreEqual("My comment.", field.Result);

// إذا قدمنا قيمة الخاصية Text في حقل "التعليقات" وقمنا بتحديثها ، فسيعمل الحقل على ذلك
// الكتابة فوق القيمة الحالية لخاصية "التعليقات" المضمنة بقيمة خاصية النص الخاصة بها ،
// ثم اعرض القيمة الجديدة.
field.Text = "My overriding comment.";
field.Update();

Assert.AreEqual(" COMMENTS  \"My overriding comment.\"", field.GetFieldCode());
Assert.AreEqual("My overriding comment.", field.Result);

doc.Save(ArtifactsDir + "Field.COMMENTS.docx");
```

### أنظر أيضا

* class [FieldComments](../)
* مساحة الاسم [Aspose.Words.Fields](../../fieldcomments/)
* المجسم [Aspose.Words](../../../)


