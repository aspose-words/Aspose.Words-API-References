---
title: "طريقة Aspose::Words::Loading::LoadOptions::get_RecoveryMode"
linktitle: "get_RecoveryMode"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Loading::LoadOptions::get_RecoveryMode. تحدد كيفية التعامل مع المستند إذا حدثت أخطاء أثناء التحميل. استخدم هذه الخاصية لتحديد ما إذا كان النظام يجب أن يحاول استعادة المستند أو يتبع سلوكًا معرفًا آخر. القيمة الافتراضية هي TryRecover في C++."
type: docs
weight: 14500
url: /ar/cpp/aspose.words.loading/loadoptions/get_recoverymode/
---
## LoadOptions::get_RecoveryMode method


تحدد كيفية التعامل مع المستند إذا حدثت أخطاء أثناء التحميل. استخدم هذه الخاصية لتحديد ما إذا كان النظام يجب أن يحاول استعادة المستند أو يتبع سلوكًا معرفًا آخر. القيمة الافتراضية هي [TryRecover](../../documentrecoverymode/).

```cpp
Aspose::Words::Loading::DocumentRecoveryMode Aspose::Words::Loading::LoadOptions::get_RecoveryMode() const
```


## أمثلة



يوضح كيفية محاولة استعادة المستند إذا حدثت أخطاء أثناء التحميل.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_RecoveryMode(Aspose::Words::Loading::DocumentRecoveryMode::TryRecover);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Corrupted footnotes.docx", loadOptions);
```

## انظر أيضًا

* Enum [DocumentRecoveryMode](../../documentrecoverymode/)
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
