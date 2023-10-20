---
title: FieldSubject.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words لـ .NET
description: FieldSubject Text ملكية. الحصول على نص الموضوع أو تعيينه في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldsubject/text/
---
## FieldSubject.Text property

الحصول على نص الموضوع أو تعيينه.

```csharp
public string Text { get; set; }
```

## أمثلة

يوضح كيفية استخدام حقل SUBJECT.

```csharp
Document doc = new Document();

// قم بتعيين قيمة للخاصية المضمنة "الموضوع" في المستند.
doc.BuiltInDocumentProperties.Subject = "My subject";

// قم بإنشاء حقل SUBJECT لعرض قيمة تلك الخاصية المضمنة.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldSubject field = (FieldSubject)builder.InsertField(FieldType.FieldSubject, true);
field.Update();

Assert.AreEqual(" SUBJECT ", field.GetFieldCode());
Assert.AreEqual("My subject", field.Result);

// إذا أعطينا قيمة خاصية النص لحقل الموضوع وقمنا بتحديثها، فسيقوم الحقل بذلك
// استبدل القيمة الحالية للخاصية المضمنة "الموضوع" بقيمة خاصية النص الخاصة بها،
// ثم قم بعرض القيمة الجديدة.
field.Text = "My new subject";
field.Update();

Assert.AreEqual(" SUBJECT  \"My new subject\"", field.GetFieldCode());
Assert.AreEqual("My new subject", field.Result);

Assert.AreEqual("My new subject", doc.BuiltInDocumentProperties.Subject);

doc.Save(ArtifactsDir + "Field.SUBJECT.docx");
```

### أنظر أيضا

* class [FieldSubject](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
