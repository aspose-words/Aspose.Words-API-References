---
title: FieldInfo.NewValue
linktitle: NewValue
articleTitle: NewValue
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FieldInfo NewValue، وقم بإدارة القيم الاختيارية بسهولة لتحسين تحديثات البيانات وتبسيط تجربة الترميز الخاصة بك.
type: docs
weight: 30
url: /ar/net/aspose.words.fields/fieldinfo/newvalue/
---
## FieldInfo.NewValue property

يحصل على قيمة اختيارية لتحديث الخاصية أو يعينها.

```csharp
public string NewValue { get; set; }
```

## أمثلة

يوضح كيفية العمل مع حقول المعلومات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بتعيين قيمة لخاصية "التعليقات" المضمنة ثم أدخل حقل INFO لعرض قيمة تلك الخاصية.
doc.BuiltInDocumentProperties.Comments = "My comment";
FieldInfo field = (FieldInfo)builder.InsertField(FieldType.FieldInfo, true);
field.InfoType = "Comments";
field.Update();

Assert.AreEqual(" INFO  Comments", field.GetFieldCode());
Assert.AreEqual("My comment", field.Result);

builder.Writeln();

// تعيين قيمة لخاصية NewValue للحقل وتحديثها
// سوف يقوم الحقل أيضًا باستبدال الخاصية المضمنة المقابلة بالقيمة الجديدة.
field = (FieldInfo)builder.InsertField(FieldType.FieldInfo, true);
field.InfoType = "Comments";
field.NewValue = "New comment";
field.Update();

Assert.AreEqual(" INFO  Comments \"New comment\"", field.GetFieldCode());
Assert.AreEqual("New comment", field.Result);
Assert.AreEqual("New comment", doc.BuiltInDocumentProperties.Comments);

doc.Save(ArtifactsDir + "Field.INFO.docx");
```

### أنظر أيضا

* class [FieldInfo](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
