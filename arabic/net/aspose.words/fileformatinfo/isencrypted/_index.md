---
title: FileFormatInfo.IsEncrypted
second_title: Aspose.Words لمراجع .NET API
description: FileFormatInfo ملكية. إرجاعحقيقي إذا كان المستند مشفرًا ويتطلب كلمة مرور لفتحه.
type: docs
weight: 30
url: /ar/net/aspose.words/fileformatinfo/isencrypted/
---
## FileFormatInfo.IsEncrypted property

إرجاع`حقيقي` إذا كان المستند مشفرًا ويتطلب كلمة مرور لفتحه.

```csharp
public bool IsEncrypted { get; }
```

### ملاحظات

توجد هذه الخاصية لمساعدتك في فرز المستندات المشفرة عن تلك غير المشفرة. إذا حاولت تحميل مستند مشفر باستخدام Aspose.Words دون توفير كلمة مرور، فسيتم طرح استثناء . يمكنك استخدام هذه الخاصية لاكتشاف ما إذا كان المستند يتطلب كلمة مرور واتخاذ بعض الإجراءات قبل تحميل مستند، على سبيل المثال، مطالبة المستخدم بإدخال كلمة مرور.

### أمثلة

يوضح كيفية استخدام فئة FileFormatUtil للكشف عن تنسيق المستند وتشفيره.

```csharp
Document doc = new Document();

// قم بتكوين كائن SaveOptions لتشفير المستند
// بكلمة مرور عندما نحفظها، ثم نحفظ المستند.
OdtSaveOptions saveOptions = new OdtSaveOptions(SaveFormat.Odt);
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "File.DetectDocumentEncryption.odt", saveOptions);

// تحقق من نوع ملف وثيقتنا وحالة التشفير الخاصة به.
FileFormatInfo info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDocumentEncryption.odt");

Assert.AreEqual(".odt", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.True(info.IsEncrypted);
```

### أنظر أيضا

* class [FileFormatInfo](../)
* مساحة الاسم [Aspose.Words](../../fileformatinfo/)
* المجسم [Aspose.Words](../../../)


