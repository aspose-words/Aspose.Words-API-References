---
title: FieldOptions.FileName
linktitle: FileName
articleTitle: FileName
second_title: Aspose.Words لـ .NET
description: FieldOptions FileName ملكية. الحصول على اسم ملف المستند أو تعيينه في C#.
type: docs
weight: 140
url: /ar/net/aspose.words.fields/fieldoptions/filename/
---
## FieldOptions.FileName property

الحصول على اسم ملف المستند أو تعيينه.

```csharp
public string FileName { get; set; }
```

## ملاحظات

يتم استخدام هذه الخاصية من قبل[`FieldFileName`](../../fieldfilename/) الحقل ذو أولوية أعلى من[`OriginalFileName`](../../../aspose.words/document/originalfilename/) ملكية.

## أمثلة

يوضح كيفية استخدام FieldOptions لتجاوز القيمة الافتراضية لحقل FILENAME.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveToDocumentEnd();
builder.Writeln();

// سيعرض حقل اسم الملف هذا اسم ملف النظام المحلي للمستند الذي قمنا بتحميله.
FieldFileName field = (FieldFileName)builder.InsertField(FieldType.FieldFileName, true);
field.Update();

Assert.AreEqual(" FILENAME ", field.GetFieldCode());
Assert.AreEqual("Document.docx", field.Result);

builder.Writeln();

// افتراضيًا، يُظهر الحقل FILENAME اسم الملف، ولكن ليس مسار نظام الملفات المحلي الكامل الخاص به.
// يمكننا تعيين علامة لجعلها تظهر مسار الملف بالكامل.
field = (FieldFileName)builder.InsertField(FieldType.FieldFileName, true);
field.IncludeFullPath = true;
field.Update();

Assert.AreEqual(MyDir + "Document.docx", field.Result);

// يمكننا أيضًا تعيين قيمة لهذه الخاصية
// تجاوز القيمة التي يعرضها حقل اسم الملف.
doc.FieldOptions.FileName = "FieldOptions.FILENAME.docx";
field.Update();

Assert.AreEqual(" FILENAME  \\p", field.GetFieldCode());
Assert.AreEqual("FieldOptions.FILENAME.docx", field.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + doc.FieldOptions.FileName);
```

### أنظر أيضا

* class [FieldOptions](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
