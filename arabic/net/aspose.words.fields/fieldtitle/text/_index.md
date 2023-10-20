---
title: FieldTitle.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words لـ .NET
description: FieldTitle Text ملكية. الحصول على نص العنوان أو تعيينه في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldtitle/text/
---
## FieldTitle.Text property

الحصول على نص العنوان أو تعيينه.

```csharp
public string Text { get; set; }
```

## أمثلة

يوضح كيفية استخدام حقل العنوان.

```csharp
Document doc = new Document();

 // قم بتعيين قيمة لخاصية المستند المضمنة "العنوان".
doc.BuiltInDocumentProperties.Title = "My Title";

// يمكننا استخدام حقل العنوان لعرض قيمة هذه الخاصية في المستند.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldTitle field = (FieldTitle)builder.InsertField(FieldType.FieldTitle, false);
field.Update();

Assert.AreEqual(" TITLE ", field.GetFieldCode());
Assert.AreEqual("My Title", field.Result);

// تعيين قيمة لخاصية النص في الحقل،
// ثم تحديث الحقل سيؤدي أيضًا إلى استبدال الخاصية المضمنة المقابلة بالقيمة الجديدة.
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
