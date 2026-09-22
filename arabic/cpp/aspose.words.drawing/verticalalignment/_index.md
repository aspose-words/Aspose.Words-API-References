---
title: "Aspose::Words::Drawing::VerticalAlignment enum"
linktitle: "VerticalAlignment"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::VerticalAlignment enum. يحدد المحاذاة العمودية لشكل عائم أو إطار نص أو جدول عائم في C++."
type: docs
weight: 43000
url: /ar/cpp/aspose.words.drawing/verticalalignment/
---
## VerticalAlignment enum


يحدد المحاذاة العمودية لشكل عائم أو إطار نص أو جدول عائم.

```cpp
enum class VerticalAlignment
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| None | 0 | الكائن موضعه صراحةً، عادةً باستخدام خاصية **Top** الخاصة به. |
| أعلى | 1 | يحدد أن الكائن يجب أن يكون في أعلى قاعدة المحاذاة العمودية. |
| وسط | 2 | يحدد أن الكائن يجب أن يكون مركّزًا بالنسبة لقاعدة المحاذاة العمودية. |
| أسفل | 3 | يحدد أن الكائن يجب أن يكون في أسفل قاعدة المحاذاة العمودية. |
| داخل | 4 | يحدد أن الكائن يجب أن يكون داخل قاعدة المحاذاة الأفقية. |
| خارج | 5 | يحدد أن الكائن يجب أن يكون خارج قاعدة المحاذاة العمودية. |
| متضمن | -1 | غير موثّق. يبدو أنه قيمة محتملة للفقرات والجداول العائمة. |
| Default | n/a | نفس [None](./). |


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
