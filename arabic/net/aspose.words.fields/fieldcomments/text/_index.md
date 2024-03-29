---
title: FieldComments.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words لـ .NET
description: FieldComments Text ملكية. الحصول على نص التعليقات أو تعيينه في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldcomments/text/
---
## FieldComments.Text property

الحصول على نص التعليقات أو تعيينه.

```csharp
public string Text { get; set; }
```

## أمثلة

يوضح كيفية استخدام حقل التعليقات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بتعيين قيمة لخاصية "التعليقات" المضمنة في المستند.
doc.BuiltInDocumentProperties.Comments = "My comment.";

// قم بإنشاء حقل التعليقات لعرض قيمة تلك الخاصية المضمنة.
FieldComments field = (FieldComments)builder.InsertField(FieldType.FieldComments, true);
field.Update();

Assert.AreEqual(" COMMENTS ", field.GetFieldCode());
Assert.AreEqual("My comment.", field.Result);

// إذا أعطينا قيمة خاصية النص لحقل التعليقات وقمنا بتحديثها، فسيقوم الحقل بذلك
// استبدل القيمة الحالية لخاصية "التعليقات" المضمنة بقيمة خاصية النص الخاصة بها،
// ثم قم بعرض القيمة الجديدة.
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
