---
title: FileFormatInfo.IsEncrypted
linktitle: IsEncrypted
articleTitle: IsEncrypted
second_title: Aspose.Words لـ .NET
description: اكتشف ما إذا كانت مستندك آمنة باستخدام خاصية FileFormatInfo IsEncrypted—ترجع القيمة true للملفات المشفرة التي تحتاج إلى كلمة مرور للوصول إليها.
type: docs
weight: 40
url: /ar/net/aspose.words/fileformatinfo/isencrypted/
---
## FileFormatInfo.IsEncrypted property

إرجاع`حقيقي` إذا تم تشفير المستند ويتطلب كلمة مرور لفتحه.

```csharp
public bool IsEncrypted { get; }
```

## ملاحظات

هذه الخاصية موجودة لمساعدتك على فرز المستندات المشفرة عن غير المشفرة. إذا حاولت تحميل مستند مشفر باستخدام Aspose.Words دون إدخال كلمة مرور، فسيتم طرح استثناء . يمكنك استخدام هذه الخاصية لمعرفة ما إذا كان المستند يتطلب كلمة مرور واتخاذ إجراء قبل تحميله، على سبيل المثال، مطالبة المستخدم بإدخال كلمة مرور.

## أمثلة

يوضح كيفية استخدام فئة FileFormatUtil لاكتشاف تنسيق المستند والتشفير.

```csharp
Document doc = new Document();

// تكوين كائن SaveOptions لتشفير المستند
// بكلمة مرور عندما نحفظه، ثم نحفظ المستند.
OdtSaveOptions saveOptions = new OdtSaveOptions(SaveFormat.Odt);
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "File.DetectDocumentEncryption.odt", saveOptions);

// التحقق من نوع الملف الخاص بمستندنا وحالة تشفيره.
FileFormatInfo info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDocumentEncryption.odt");

Assert.AreEqual(".odt", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.True(info.IsEncrypted);
```

### أنظر أيضا

* class [FileFormatInfo](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
