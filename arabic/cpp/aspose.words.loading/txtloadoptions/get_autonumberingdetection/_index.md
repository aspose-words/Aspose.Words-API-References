---
title: "طريقة Aspose::Words::Loading::TxtLoadOptions::get_AutoNumberingDetection"
linktitle: "get_AutoNumberingDetection"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Loading::TxtLoadOptions::get_AutoNumberingDetection. تحصل أو تعيّن قيمة منطقية تشير إلى ما إذا كان سيتم تنفيذ اكتشاف الترقيم التلقائي أثناء تحميل المستند. القيمة الافتراضية هي true في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.loading/txtloadoptions/get_autonumberingdetection/
---
## TxtLoadOptions::get_AutoNumberingDetection method


يحصل أو يعيّن قيمة منطقية تشير إلى ما إذا كان سيتم تنفيذ اكتشاف الترقيم التلقائي أثناء تحميل مستند. القيمة الافتراضية هي **true**.

```cpp
bool Aspose::Words::Loading::TxtLoadOptions::get_AutoNumberingDetection() const
```


## أمثلة



يوضح كيفية تعطيل اكتشاف الترقيم التلقائي.
```cpp
auto options = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();
options->set_AutoNumberingDetection(false);
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Number detection.txt", options);
```

## انظر أيضًا

* Class [TxtLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
