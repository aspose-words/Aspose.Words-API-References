---
title: "طريقة Aspose::Words::FileFormatInfo::get_IsEncrypted"
linktitle: "get_IsEncrypted"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::FileFormatInfo::get_IsEncrypted. تُعيد true إذا كان المستند مشفراً ويتطلب كلمة مرور للفتح في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words/fileformatinfo/get_isencrypted/
---
## FileFormatInfo::get_IsEncrypted method


يرجع **true** إذا كان المستند مشفرًا ويتطلب كلمة مرور للفتح.

```cpp
bool Aspose::Words::FileFormatInfo::get_IsEncrypted() const
```

## ملاحظات


هذه الخاصية موجودة لمساعدتك في فرز المستندات المشفرة عن غير المشفرة. إذا حاولت تحميل مستند مشفر باستخدام Aspose.Words دون توفير كلمة مرور، سيتم إلقاء استثناء. يمكنك استخدام هذه الخاصية لاكتشاف ما إذا كان المستند يتطلب كلمة مرور واتخاذ إجراء قبل تحميل المستند، على سبيل المثال، مطالبة المستخدم بكلمة مرور.

## أمثلة



يظهر كيفية استخدام الفئة [FileFormatUtil](../../fileformatutil/) لاكتشاف تنسيق المستند والتشفير.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// قم بتهيئة كائن SaveOptions لتشفير المستند
// مع كلمة مرور عند حفظه، ثم احفظ المستند.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>(Aspose::Words::SaveFormat::Odt);
saveOptions->set_Password(u"MyPassword");

doc->Save(get_ArtifactsDir() + u"File.DetectDocumentEncryption.odt", saveOptions);

// تحقق من نوع ملف مستندنا وحالة تشفيره.
System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"File.DetectDocumentEncryption.odt");

ASSERT_EQ(u".odt", Aspose::Words::FileFormatUtil::LoadFormatToExtension(info->get_LoadFormat()));
ASSERT_TRUE(info->get_IsEncrypted());
```

## انظر أيضًا

* Class [FileFormatInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
