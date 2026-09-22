---
title: "تعداد Aspose::Words::Drawing::HorizontalAlignment"
linktitle: "HorizontalAlignment"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "تعداد Aspose::Words::Drawing::HorizontalAlignment. يحدد محاذاة أفقية لشكل عائم أو إطار نص أو جدول عائم في C++."
type: docs
weight: 26000
url: /ar/cpp/aspose.words.drawing/horizontalalignment/
---
## HorizontalAlignment enum


يحدد المحاذاة الأفقية لشكل عائم أو إطار نص أو جدول عائم.

```cpp
enum class HorizontalAlignment
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| None | 0 | يتم وضع الكائن صراحةً، عادةً باستخدام خاصية **Left**. |
| Default | n/a | نفس [None](./). |
| يسار | 1 | يحدد أن الكائن يجب أن يكون محاذيًا إلى اليسار بالنسبة لقاعدة المحاذاة الأفقية. |
| وسط | 2 | يحدد أن الكائن يجب أن يكون مركزيًا بالنسبة لقاعدة المحاذاة الأفقية. |
| يمين | 3 | يحدد أن الكائن يجب أن يكون محاذيًا إلى اليمين لقاعدة المحاذاة الأفقية. |
| داخل | 4 | يحدد أن الكائن يجب أن يكون داخل قاعدة المحاذاة الأفقية. |
| خارج | 5 | يحدد أن الكائن يجب أن يكون خارج قاعدة المحاذاة الأفقية. |


## أمثلة



يوضح كيفية إدراج صورة عائمة في مركز الصفحة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدرج صورة عائمة ستظهر خلف النص المتداخل ووازنها إلى مركز الصفحة.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
shape->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Center);

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPageCenter.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
