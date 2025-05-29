---
title: FieldComments.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words لـ .NET
description: قم بإدارة تعليقاتك بسهولة باستخدام خاصية نص FieldComments—احصل على نص التعليق أو قم بتعيينه بسهولة لتحسين تفاعل المستخدم.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldcomments/text/
---
## FieldComments.Text property

يحصل على نص التعليقات أو يعينه.

```csharp
public string Text { get; set; }
```

## أمثلة

يوضح كيفية استخدام حقل التعليقات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// تعيين قيمة لخاصية "التعليقات" المضمنة في المستند.
doc.BuiltInDocumentProperties.Comments = "My comment.";

// قم بإنشاء حقل التعليقات لعرض قيمة تلك الخاصية المضمنة.
FieldComments field = (FieldComments)builder.InsertField(FieldType.FieldComments, true);
field.Update();

Assert.AreEqual(" COMMENTS ", field.GetFieldCode());
Assert.AreEqual("My comment.", field.Result);

// إذا قمنا بإعطاء قيمة خاصية النص لحقل التعليقات وقمنا بتحديثها، فسيصبح الحقل
//استبدل القيمة الحالية للخاصية المضمنة "التعليقات" بقيمة خاصية النص الخاصة بها،
//ثم عرض القيمة الجديدة.
field.Text = "My overriding comment.";
field.Update();

Assert.AreEqual(" COMMENTS  \"My overriding comment.\"", field.GetFieldCode());
Assert.AreEqual("My overriding comment.", field.Result);

doc.Save(ArtifactsDir + "Field.COMMENTS.docx");
```

### أنظر أيضا

* class [FieldComments](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
