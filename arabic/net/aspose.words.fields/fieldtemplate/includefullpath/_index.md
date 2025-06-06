---
title: FieldTemplate.IncludeFullPath
linktitle: IncludeFullPath
articleTitle: IncludeFullPath
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FieldTemplate IncludeFullPath لإدارة تضمين مسار الملف الكامل بسهولة، مما يعزز كفاءة مشروعك وتنظيمه.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldtemplate/includefullpath/
---
## FieldTemplate.IncludeFullPath property

يحصل على أو يحدد ما إذا كان سيتم تضمين اسم مسار الملف الكامل.

```csharp
public bool IncludeFullPath { get; set; }
```

## أمثلة

يوضح كيفية استخدام حقل القالب لعرض موقع نظام الملفات المحلي لقالب المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// يمكننا تعيين اسم القالب باستخدام الحقول. تُستخدم هذه الخاصية عندما يكون "doc.AttachedTemplate" فارغًا.
// إذا كانت هذه الخاصية فارغة، فسيتم استخدام اسم ملف القالب الافتراضي "Normal.dotm".
doc.FieldOptions.TemplateName = string.Empty;

FieldTemplate field = (FieldTemplate)builder.InsertField(FieldType.FieldTemplate, false);
Assert.AreEqual(" TEMPLATE ", field.GetFieldCode());

builder.Writeln();
field = (FieldTemplate)builder.InsertField(FieldType.FieldTemplate, false);
field.IncludeFullPath = true;

Assert.AreEqual(" TEMPLATE  \\p", field.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.TEMPLATE.docx");
```

### أنظر أيضا

* class [FieldTemplate](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
