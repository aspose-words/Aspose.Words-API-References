---
title: FieldTitle.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words لـ .NET
description: أدر خاصية نص عنوان الحقل بسهولة. احصل على نص العنوان أو عيّنه بسهولة لتحسين الوضوح وتجربة المستخدم في تطبيقك.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldtitle/text/
---
## FieldTitle.Text property

يحصل على نص العنوان أو يعينه.

```csharp
public string Text { get; set; }
```

## أمثلة

يوضح كيفية استخدام حقل العنوان.

```csharp
Document doc = new Document();

 // تعيين قيمة لخاصية المستند المضمنة "العنوان".
doc.BuiltInDocumentProperties.Title = "My Title";

//يمكننا استخدام حقل TITLE لعرض قيمة هذه الخاصية في المستند.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldTitle field = (FieldTitle)builder.InsertField(FieldType.FieldTitle, false);
field.Update();

Assert.AreEqual(" TITLE ", field.GetFieldCode());
Assert.AreEqual("My Title", field.Result);

// تعيين قيمة لخاصية النص الخاصة بالحقل،
// ثم سيؤدي تحديث الحقل أيضًا إلى استبدال الخاصية المضمنة المقابلة بالقيمة الجديدة.
builder.Writeln();
field = (FieldTitle)builder.InsertField(FieldType.FieldTitle, false);
field.Text = "My New Title";
field.Update();

Assert.AreEqual(" TITLE  \"My New Title\"", field.GetFieldCode());
Assert.AreEqual("My New Title", field.Result);
Assert.AreEqual("My New Title", doc.BuiltInDocumentProperties.Title);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.TITLE.docx");
```

### أنظر أيضا

* class [FieldTitle](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
