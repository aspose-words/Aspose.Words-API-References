---
title: BuiltInDocumentProperties.Thumbnail
second_title: Aspose.Words لمراجع .NET API
description: BuiltInDocumentProperties ملكية. الحصول على الصورة المصغرة للمستند أو تعيينها.
type: docs
weight: 280
url: /ar/net/aspose.words.properties/builtindocumentproperties/thumbnail/
---
## BuiltInDocumentProperties.Thumbnail property

الحصول على الصورة المصغرة للمستند أو تعيينها.

```csharp
public byte[] Thumbnail { get; set; }
```

### ملاحظات

في الوقت الحالي، يتم استخدام هذه الخاصية فقط عندما يتم تصدير مستند إلى ePub، ولا تتم قراءته منه أو كتابته إلى تنسيقات المستندات الأخرى.

يمكن تعيين صورة ذات تنسيق عشوائي على هذه الخاصية، ولكن يتم التحقق من التنسيق أثناء التصدير. InvalidOperationException يتم طرحها إذا كانت الصورة غير صالحة أو كان تنسيقها غير مدعوم لتنسيق معين للمستند.

يمكن استخدام صور gif وjpeg وpng فقط لنشر ePub.

### أمثلة

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

* class [BuiltInDocumentProperties](../)
* مساحة الاسم [Aspose.Words.Properties](../../builtindocumentproperties/)
* المجسم [Aspose.Words](../../../)


