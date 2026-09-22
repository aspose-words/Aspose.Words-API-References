---
title: "Aspose::Words::Layout::RevisionColor enum"
linktitle: "RevisionColor"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Layout::RevisionColor enum. يسمح بتحديد لون مراجعات المستند في C++."
type: docs
weight: 11000
url: /ar/cpp/aspose.words.layout/revisioncolor/
---
## RevisionColor enum


يسمح بتحديد لون مراجعات المستند.

```cpp
enum class RevisionColor
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| تلقائي | 0 | افتراضي. |
| أسود | 1 | يمثل اللون 000000. |
| أزرق | 2 | يمثل اللون 2e97d3. |
| أخضر ساطع | 3 | يمثل اللون 84a35b. |
| أزرق كلاسيكي | 4 | يمثل اللون 0000ff. |
| أحمر كلاسيكي | 5 | يمثل اللون ff0000. |
| أزرق داكن | 6 | يمثل اللون 376e96. |
| أحمر داكن | 7 | يمثل اللون 881824. |
| أصفر داكن | 8 | يمثل اللون e09a2b. |
| رمادي25 | 9 | يمثل اللون a0a3a9. |
| رمادي50 | 10 | يمثل اللون 50565e. |
| أخضر | 11 | يمثل اللون 2c6234. |
| وردي | 12 | يمثل اللون ce338f. |
| أحمر | 13 | يمثل اللون b5082e. |
| تركوازي | 14 | يمثل اللون 1b9cab. |
| فيروزي | 15 | يمثل اللون 3eafc2. |
| بنفسجي | 16 | يمثل اللون 633277. |
| أبيض | 17 | يمثل اللون ffffff. |
| أصفر | 18 | يمثل اللون fad272. |
| وردي فاتح | 19 | يمثل اللون fce6f4. |
| أزرق فاتح | 20 | يمثل اللون e1f2fa. |
| أصفر فاتح | 21 | يمثل اللون fef4de. |
| أرجواني فاتح | 22 | يمثل اللون eadfef. |
| برتقالي فاتح | 23 | يمثل اللون fce3d0. |
| أخضر فاتح | 24 | يمثل اللون e9f8ce. |
| رمادي | 25 | يمثل اللون efeded. |
| بدون تمييز | 26 | لا يُستخدم أي لون لتسليط الضوء على تغييرات المراجعة. |
| حسب المؤلف | 27 | تحصل مراجعات كل مؤلف على لون خاص بها للتسليط من مجموعة مسبقة من الألوان ذات التباين العالي. |


## أمثلة



يظهر كيفية تعديل مظهر المراجعات في مستند الإخراج المرسوم.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدرج مراجعة، ثم غيّر لون جميع المراجعات إلى الأخضر.
builder->Writeln(u"This is not a revision.");
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());
builder->Writeln(u"This is a revision.");
doc->StopTrackRevisions();
builder->Writeln(u"This is not a revision.");

// أزل الشريط الذي يظهر إلى يسار كل سطر مُراجَع.
doc->get_LayoutOptions()->get_RevisionOptions()->set_InsertedTextColor(Aspose::Words::Layout::RevisionColor::BrightGreen);
doc->get_LayoutOptions()->get_RevisionOptions()->set_ShowRevisionBars(false);
doc->get_LayoutOptions()->get_RevisionOptions()->set_RevisionBarsPosition(Aspose::Words::Drawing::HorizontalAlignment::Right);

doc->Save(get_ArtifactsDir() + u"Revision.LayoutOptionsRevisions.pdf");
```

## انظر أيضًا

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
