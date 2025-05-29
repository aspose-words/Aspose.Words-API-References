---
title: FieldInfo.InfoType
linktitle: InfoType
articleTitle: InfoType
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية إدارة خصائص FieldInfo InfoType بسهولة. حدّد أنواع المستندات أو استرجاعها بسهولة لضمان تكامل سلس في مشاريعك.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldinfo/infotype/
---
## FieldInfo.InfoType property

يحصل على نوع خاصية المستند المراد إدراجها أو يعينه.

```csharp
public string InfoType { get; set; }
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
