---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Thumbnail طريقة"
linktitle: "get_Thumbnail"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Properties::BuiltInDocumentProperties::get_Thumbnail. يحصل على أو يحدد الصورة المصغرة للمستند في C++."
type: docs
weight: 28000
url: /ar/cpp/aspose.words.properties/builtindocumentproperties/get_thumbnail/
---
## BuiltInDocumentProperties::get_Thumbnail method


يحصل أو يضبط مصغّر المستند.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Properties::BuiltInDocumentProperties::get_Thumbnail()
```

## ملاحظات


في الوقت الحالي تُستخدم هذه الخاصية فقط عندما يتم تصدير مستند إلى ePub، ولا يتم قراءتها أو كتابتها إلى صيغ مستندات أخرى.

يمكن تعيين صورة بأي تنسيق إلى هذه الخاصية، لكن يتم التحقق من التنسيق أثناء التصدير.

يمكن فقط استخدام صور gif و jpeg و png للنشر بصيغة ePub.

## أمثلة



يوضح كيفية إضافة صورة مصغرة إلى مستند نحفظه كملف Epub.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// إذا حفظنا مستندًا، حيث تحتوي خاصية "Thumbnail" على بيانات الصورة التي أضفناها، كملف Epub،
// قد يعرض القارئ الذي يفتح ذلك المستند الصورة قبل الصفحة الأولى.
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> properties = doc->get_BuiltInDocumentProperties();

System::ArrayPtr<uint8_t> thumbnailBytes = System::IO::File::ReadAllBytes(get_ImageDir() + u"Logo.jpg");
properties->set_Thumbnail(thumbnailBytes);

doc->Save(get_ArtifactsDir() + u"DocumentProperties.Thumbnail.epub");

// يمكننا استخراج صورة المصغرة للمستند وحفظها في نظام الملفات المحلي.
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> thumbnail = doc->get_BuiltInDocumentProperties()->idx_get(u"Thumbnail");
System::IO::File::WriteAllBytes(get_ArtifactsDir() + u"DocumentProperties.Thumbnail.gif", thumbnail->ToByteArray());
```

## انظر أيضًا

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
