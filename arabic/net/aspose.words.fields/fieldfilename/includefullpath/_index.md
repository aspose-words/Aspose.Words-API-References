---
title: FieldFileName.IncludeFullPath
linktitle: IncludeFullPath
articleTitle: IncludeFullPath
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FieldFileName IncludeFullPath، وقم بإدارة مسارات الملفات بسهولة باستخدام الإعدادات القابلة للتخصيص لتحسين التعامل مع الملفات وتنظيمها.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldfilename/includefullpath/
---
## FieldFileName.IncludeFullPath property

يحصل على أو يحدد ما إذا كان سيتم تضمين اسم مسار الملف الكامل.

```csharp
public bool IncludeFullPath { get; set; }
```

## أمثلة

يوضح كيفية استخدام FieldOptions لتجاوز القيمة الافتراضية لحقل FILENAME.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveToDocumentEnd();
builder.Writeln();

// سيعرض حقل FILENAME اسم ملف النظام المحلي للمستند الذي قمنا بتحميله.
FieldFileName field = (FieldFileName)builder.InsertField(FieldType.FieldFileName, true);
field.Update();

Assert.AreEqual(" FILENAME ", field.GetFieldCode());
Assert.AreEqual("Document.docx", field.Result);

builder.Writeln();

// بشكل افتراضي، يعرض حقل FILENAME اسم الملف، ولكن ليس مسار نظام الملفات المحلي الكامل.
//يمكننا تعيين علم لإظهار مسار الملف الكامل.
field = (FieldFileName)builder.InsertField(FieldType.FieldFileName, true);
field.IncludeFullPath = true;
field.Update();

Assert.AreEqual(MyDir + "Document.docx", field.Result);

// يمكننا أيضًا تعيين قيمة لهذه الخاصية إلى
// تجاوز القيمة التي يعرضها حقل اسم الملف.
doc.FieldOptions.FileName = "FieldOptions.FILENAME.docx";
field.Update();

Assert.AreEqual(" FILENAME  \\p", field.GetFieldCode());
Assert.AreEqual("FieldOptions.FILENAME.docx", field.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + doc.FieldOptions.FileName);
```

### أنظر أيضا

* class [FieldFileName](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
