---
title: "الواجهة Aspose::Words::Fields::IBarcodeGenerator"
linktitle: "IBarcodeGenerator"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "الواجهة Aspose::Words::Fields::IBarcodeGenerator. واجهة عامة لمولد الباركود المخصص. يجب أن يقدم المستخدم التنفيذ في C++."
type: docs
weight: 118000
url: /ar/cpp/aspose.words.fields/ibarcodegenerator/
---
## IBarcodeGenerator interface


واجهة عامة لمولد الباركود المخصص. يجب أن يقدم المستخدم التنفيذ.

```cpp
class IBarcodeGenerator : public virtual System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| virtual [GetBarcodeImage](./getbarcodeimage/)(System::SharedPtr\<Aspose::Words::Fields::BarcodeParameters\>) | إنشاء صورة باركود باستخدام مجموعة المعلمات (لحقل DisplayBarcode). |
| virtual [GetOldBarcodeImage](./getoldbarcodeimage/)(System::SharedPtr\<Aspose::Words::Fields::BarcodeParameters\>) | إنشاء صورة باركود باستخدام مجموعة المعلمات (لحقل Barcode التقليدي). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## انظر أيضًا

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
