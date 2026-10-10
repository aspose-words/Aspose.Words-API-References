---
title: "طريقة Aspose::Words::Fields::FieldOptions::get_IsBidiTextSupportedOnUpdate"
linktitle: "get_IsBidiTextSupportedOnUpdate"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fields::FieldOptions::get_IsBidiTextSupportedOnUpdate. يحصل على أو يعيّن القيمة التي تشير إلى ما إذا كان النص ثنائي الاتجاه مدعومًا بالكامل أثناء تحديث الحقل أم لا في C++."
type: docs
weight: 15000
url: /ar/cpp/aspose.words.fields/fieldoptions/get_isbiditextsupportedonupdate/
---
## FieldOptions::get_IsBidiTextSupportedOnUpdate method


الحصول على أو تعيين القيمة التي تشير إلى ما إذا كان النص ثنائي الاتجاه مدعومًا بالكامل أثناء تحديث الحقل أم لا.

```cpp
bool Aspose::Words::Fields::FieldOptions::get_IsBidiTextSupportedOnUpdate() const
```

## ملاحظات


عند تعيين هذه الخاصية إلى **true**، تُجرى خطوات إضافية لإنتاج نتيجة حقل متوافقة مع اللغة من اليمين إلى اليسار (مثل العربية أو العبرية) أثناء تحديثها.

عند تعيين هذه الخاصية إلى **false** واستخدام لغة من اليمين إلى اليسار، لا يُضمن صحة نتيجة الحقل بعد تحديثه.

القيمة الافتراضية هي **false**.

## أمثلة



يظهر كيفية استخدام [FieldOptions](../) لضمان أن تحديث الحقل يدعم النص ثنائي الاتجاه بالكامل.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// تأكد من أن أي عملية حقل تتضمن نصًا من اليمين إلى اليسار تُنفّذ كما هو متوقع.
doc->get_FieldOptions()->set_IsBidiTextSupportedOnUpdate(true);

// استخدم مُنشئ المستندات لإدراج حقل يحتوي على النص من اليمين إلى اليسار.
System::SharedPtr<Aspose::Words::Fields::FormField> comboBox = builder->InsertComboBox(u"MyComboBox", System::MakeArray<System::String>({u"עֶשְׂרִים", u"שְׁלוֹשִׁים", u"אַרְבָּעִים", u"חֲמִשִּׁים", u"שִׁשִּׁים"}), 0);
comboBox->set_CalculateOnExit(true);

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"FieldOptions.Bidi.docx");
```

## انظر أيضًا

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
