---
title: FieldOptions.TemplateName
linktitle: TemplateName
articleTitle: TemplateName
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FieldOptions TemplateName لإدارة اسم ملف قالب المستند الخاص بك بسهولة لتحسين التنظيم والكفاءة.
type: docs
weight: 190
url: /ar/net/aspose.words.fields/fieldoptions/templatename/
---
## FieldOptions.TemplateName property

يحصل على اسم ملف القالب الذي يستخدمه المستند أو يعينه.

```csharp
public string TemplateName { get; set; }
```

## ملاحظات

يتم استخدام هذه الخاصية بواسطة[`FieldTemplate`](../../fieldtemplate/) الحقل إذا كان[`AttachedTemplate`](../../../aspose.words/document/attachedtemplate/) العقار فارغ.

إذا كانت هذه الخاصية فارغة، فسيتم استخدام اسم ملف القالب الافتراضي`عادي.dotm` يتم استخدامه.

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

* class [FieldOptions](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
