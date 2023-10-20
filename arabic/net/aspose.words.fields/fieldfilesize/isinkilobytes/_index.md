---
title: FieldFileSize.IsInKilobytes
linktitle: IsInKilobytes
articleTitle: IsInKilobytes
second_title: Aspose.Words لـ .NET
description: FieldFileSize IsInKilobytes ملكية. الحصول على أو تعيين ما إذا كان سيتم عرض حجم الملف بالكيلوبايت في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldfilesize/isinkilobytes/
---
## FieldFileSize.IsInKilobytes property

الحصول على أو تعيين ما إذا كان سيتم عرض حجم الملف بالكيلوبايت.

```csharp
public bool IsInKilobytes { get; set; }
```

## أمثلة

يوضح كيفية عرض حجم ملف المستند باستخدام حقل FILESIZE.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Assert.AreEqual(18105, doc.BuiltInDocumentProperties.Bytes);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.InsertParagraph();

// فيما يلي ثلاث وحدات قياس مختلفة
// التي يمكن لحقول FILESIZE من خلالها عرض حجم ملف المستند.
// 1 - البايتات:
FieldFileSize field = (FieldFileSize)builder.InsertField(FieldType.FieldFileSize, true);
field.Update();

Assert.AreEqual(" FILESIZE ", field.GetFieldCode());
Assert.AreEqual("18105", field.Result);

// 2 - كيلو بايت:
builder.InsertParagraph();
field = (FieldFileSize)builder.InsertField(FieldType.FieldFileSize, true);
field.IsInKilobytes = true;
field.Update();

Assert.AreEqual(" FILESIZE  \\k", field.GetFieldCode());
Assert.AreEqual("18", field.Result);

// 3 - ميغابايت:
builder.InsertParagraph();
field = (FieldFileSize)builder.InsertField(FieldType.FieldFileSize, true);
field.IsInMegabytes = true;
field.Update();

Assert.AreEqual(" FILESIZE  \\m", field.GetFieldCode());
Assert.AreEqual("0", field.Result);

// لتحديث قيم هذه الحقول أثناء التحرير في Microsoft Word،
// يجب علينا أولاً حفظ التغييرات، ثم تحديث هذه الحقول يدويًا.
doc.Save(ArtifactsDir + "Field.FILESIZE.docx");
```

### أنظر أيضا

* class [FieldFileSize](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
