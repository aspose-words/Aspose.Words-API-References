---
title: DocumentProperty.ToByteArray
linktitle: ToByteArray
articleTitle: ToByteArray
second_title: Aspose.Words لـ .NET
description: DocumentProperty ToByteArray طريقة. إرجاع قيمة الخاصية كمصفوفة بايت في C#.
type: docs
weight: 70
url: /ar/net/aspose.words.properties/documentproperty/tobytearray/
---
## DocumentProperty.ToByteArray method

إرجاع قيمة الخاصية كمصفوفة بايت.

```csharp
public byte[] ToByteArray()
```

## ملاحظات

يطرح استثناءً إذا لم يكن نوع الخاصية كذلكByteArray.

## أمثلة

يوضح كيفية إضافة صورة مصغرة إلى مستند نحفظه كملف Epub.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// إذا قمنا بحفظ مستند، تحتوي خاصية "الصورة المصغرة" الخاصة به على بيانات الصورة التي أضفناها، كملف Epub،
// القارئ الذي يفتح هذا المستند قد يعرض الصورة قبل الصفحة الأولى.
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

byte[] thumbnailBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");
properties.Thumbnail = thumbnailBytes;

doc.Save(ArtifactsDir + "DocumentProperties.Thumbnail.epub");

// يمكننا استخراج الصورة المصغرة للمستند وحفظها في نظام الملفات المحلي.
DocumentProperty thumbnail = doc.BuiltInDocumentProperties["Thumbnail"];
File.WriteAllBytes(ArtifactsDir + "DocumentProperties.Thumbnail.gif", thumbnail.ToByteArray());
```

### أنظر أيضا

* class [DocumentProperty](../)
* مساحة الاسم [Aspose.Words.Properties](../../../aspose.words.properties/)
* المجسم [Aspose.Words](../../../)
