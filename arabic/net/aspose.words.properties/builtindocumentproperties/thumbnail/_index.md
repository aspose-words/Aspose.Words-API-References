---
title: BuiltInDocumentProperties.Thumbnail
linktitle: Thumbnail
articleTitle: Thumbnail
second_title: Aspose.Words لـ .NET
description: أدر مظهر مستندك البصري باستخدام BuiltInDocumentProperties. احصل على صور مصغّرة أو عيّنها بسهولة لتحسين العرض والتنظيم.
type: docs
weight: 310
url: /ar/net/aspose.words.properties/builtindocumentproperties/thumbnail/
---
## BuiltInDocumentProperties.Thumbnail property

يحصل على الصورة المصغرة للمستند أو يعينها.

```csharp
public byte[] Thumbnail { get; set; }
```

### استثناءات

| استثناء | حالة |
| --- | --- |
| InvalidOperationException | يتم إلقاؤه إذا كانت الصورة غير صالحة أو تنسيقها غير مدعوم لتنسيق معين من المستند. |

## ملاحظات

في الوقت الحالي يتم استخدام هذه الخاصية فقط عندما يتم تصدير مستند إلى ePub، ولا يتم قراءته أو كتابته إلى تنسيقات مستندات أخرى.

من الممكن تعيين صورة بتنسيق عشوائي لهذه الخاصية، ولكن يتم التحقق من التنسيق أثناء التصدير.

لا يمكن استخدام سوى الصور بتنسيق gif وjpeg وpng للنشر بتنسيق ePub.

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

* class [BuiltInDocumentProperties](../)
* مساحة الاسم [Aspose.Words.Properties](../../../aspose.words.properties/)
* المجسم [Aspose.Words](../../../)
