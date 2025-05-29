---
title: DocumentProperty.ToByteArray
linktitle: ToByteArray
articleTitle: ToByteArray
second_title: Aspose.Words لـ .NET
description: حوّل DocumentProperty إلى مصفوفة بايتات بسهولة باستخدام دالة ToByteArray. حسّن معالجة البيانات وحسّن كفاءة الترميز لديك!
type: docs
weight: 70
url: /ar/net/aspose.words.properties/documentproperty/tobytearray/
---
## DocumentProperty.ToByteArray method

يعيد قيمة الخاصية كمصفوفة بايت.

```csharp
public byte[] ToByteArray()
```

## ملاحظات

يُلقي استثناءً إذا لم يكن نوع الخاصيةByteArray.

## أمثلة

يوضح كيفية إضافة صورة مصغرة إلى مستند نحفظه بتنسيق Epub.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// إذا قمنا بحفظ مستند، تحتوي خاصية "الصورة المصغرة" فيه على بيانات الصورة التي أضفناها، كملف Epub،
// قد يقوم القارئ الذي يفتح هذا المستند بعرض الصورة قبل الصفحة الأولى.
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

byte[] thumbnailBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");
properties.Thumbnail = thumbnailBytes;

doc.Save(ArtifactsDir + "DocumentProperties.Thumbnail.epub");

// يمكننا استخراج صورة مصغرة من مستند وحفظها في نظام الملفات المحلي.
DocumentProperty thumbnail = doc.BuiltInDocumentProperties["Thumbnail"];
File.WriteAllBytes(ArtifactsDir + "DocumentProperties.Thumbnail.gif", thumbnail.ToByteArray());
```

### أنظر أيضا

* class [DocumentProperty](../)
* مساحة الاسم [Aspose.Words.Properties](../../../aspose.words.properties/)
* المجسم [Aspose.Words](../../../)
