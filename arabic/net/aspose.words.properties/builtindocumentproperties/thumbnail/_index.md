---
title: BuiltInDocumentProperties.Thumbnail
second_title: Aspose.Words لمراجع .NET API
description: BuiltInDocumentProperties ملكية. الحصول على أو تحديد مصغر المستند.
type: docs
weight: 280
url: /ar/net/aspose.words.properties/builtindocumentproperties/thumbnail/
---
## BuiltInDocumentProperties.Thumbnail property

الحصول على أو تحديد مصغر المستند.

```csharp
public byte[] Thumbnail { get; set; }
```

### ملاحظات

في الوقت الحالي ، يتم استخدام هذه الخاصية فقط عندما يتم تصدير مستند إلى ePub ، لا تتم قراءته وكتابته إلى تنسيقات مستندات أخرى.

يمكن تعيين صورة بتنسيق عشوائي على هذه الخاصية ، ولكن يتم فحص التنسيق أثناء التصدير.InvalidOperationException يتم طرحها إذا كانت الصورة غير صالحة أو كان تنسيقها غير مدعوم لتنسيق معين من المستند.

يمكن استخدام صور gif و jpeg و png فقط لنشر ePub.

### أمثلة

يوضح كيفية إضافة صورة مصغرة إلى مستند نقوم بحفظه على هيئة Epub.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// إذا قمنا بحفظ مستند ، تحتوي خاصية "Thumbnail" الخاصة به على بيانات الصورة التي أضفناها ، مثل Epub ،
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

* class [BuiltInDocumentProperties](../)
* مساحة الاسم [Aspose.Words.Properties](../../builtindocumentproperties/)
* المجسم [Aspose.Words](../../../)


