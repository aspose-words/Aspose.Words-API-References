---
title: "Aspose::Words::Saving::DocSaveOptions::get_SavePictureBullet method"
linktitle: "get_SavePictureBullet"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::DocSaveOptions::get_SavePictureBullet method. عندما تكون false، لا يتم حفظ بيانات PictureBullet إلى المستند الناتج. القيمة الافتراضية هي true في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words.saving/docsaveoptions/get_savepicturebullet/
---
## DocSaveOptions::get_SavePictureBullet method


عند **false**، لا يتم حفظ بيانات PictureBullet إلى مستند الإخراج. القيمة الافتراضية هي **true**.

```cpp
bool Aspose::Words::Saving::DocSaveOptions::get_SavePictureBullet() const
```

## ملاحظات


هذا الخيار متوفر لـ Word 97، الذي لا يمكنه العمل بشكل صحيح مع بيانات PictureBullet. لإزالة بيانات PictureBullet، اضبط الخيار على "false".

## أمثلة



يوضح كيفية حذف بيانات PictureBullet من المستند عند الحفظ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Image bullet points.docx");

// بعض معالجات النصوص، مثل Microsoft Word 97، غير متوافقة مع بيانات PictureBullet.
// عن طريق ضبط علامة في كائن SaveOptions،
// يمكننا تحويل جميع نقاط التعداد النقطية المصورة إلى نقاط تعداد عادية أثناء الحفظ.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>(Aspose::Words::SaveFormat::Doc);
saveOptions->set_SavePictureBullet(false);

doc->Save(get_ArtifactsDir() + u"DocSaveOptions.PictureBullets.doc", saveOptions);
```

## انظر أيضًا

* Class [DocSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
