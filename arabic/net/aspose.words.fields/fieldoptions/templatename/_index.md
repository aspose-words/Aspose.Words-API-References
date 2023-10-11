---
title: FieldOptions.TemplateName
second_title: Aspose.Words لمراجع .NET API
description: FieldOptions ملكية. الحصول على أو تعيين اسم ملف القالب الذي يستخدمه المستند.
type: docs
weight: 190
url: /ar/net/aspose.words.fields/fieldoptions/templatename/
---
## FieldOptions.TemplateName property

الحصول على أو تعيين اسم ملف القالب الذي يستخدمه المستند.

```csharp
public string TemplateName { get; set; }
```

### ملاحظات

يتم استخدام هذه الخاصية من قبل[`FieldTemplate`](../../fieldtemplate/) الحقل إذا[`AttachedTemplate`](../../../aspose.words/document/attachedtemplate/) الملكية فارغة.

إذا كانت هذه الخاصية فارغة، اسم ملف القالب الافتراضي`عادي.dotm` يستخدم.

### أمثلة

يوضح كيفية استخدام حقل القالب لعرض موقع نظام الملفات المحلي لقالب المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// يمكننا تعيين اسم القالب باستخدام الحقول. يتم استخدام هذه الخاصية عندما يكون "doc.AttachedTemplate" فارغًا.
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

* class [FieldOptions](../)
* مساحة الاسم [Aspose.Words.Fields](../../fieldoptions/)
* المجسم [Aspose.Words](../../../)


