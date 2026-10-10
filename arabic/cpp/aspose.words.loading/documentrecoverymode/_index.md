---
title: "Aspose::Words::Loading::DocumentRecoveryMode enum"
linktitle: "DocumentRecoveryMode"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Loading::DocumentRecoveryMode enum. يحدد خيارات الاستعادة المتاحة عندما يواجه المستند أخطاءً أثناء التحميل في C++."
type: docs
weight: 13500
url: /ar/cpp/aspose.words.loading/documentrecoverymode/
---
## DocumentRecoveryMode enum


يحدد خيارات الاستعادة المتاحة عندما يواجه المستند أخطاءً أثناء التحميل.

```cpp
enum class DocumentRecoveryMode
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| None | 0 | لا يتم محاولة الاستعادة. إذا كان المستند غير صالح، سيفشل التحميل مع حدوث خطأ. |
| TryRecover | 1 | يحاول استعادة المستند مع الحفاظ على أكبر قدر ممكن من البيانات. |


## أمثلة



يوضح كيفية محاولة استعادة المستند إذا حدثت أخطاء أثناء التحميل.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_RecoveryMode(Aspose::Words::Loading::DocumentRecoveryMode::TryRecover);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Corrupted footnotes.docx", loadOptions);
```

## انظر أيضًا

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
