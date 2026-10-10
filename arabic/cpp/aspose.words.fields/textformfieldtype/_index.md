---
title: "Aspose::Words::Fields::TextFormFieldType تعداد"
linktitle: "TextFormFieldType"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::TextFormFieldType تعداد. يحدد نوع حقل نموذج نصي في C++."
type: docs
weight: 134000
url: /ar/cpp/aspose.words.fields/textformfieldtype/
---
## TextFormFieldType enum


يحدد نوع حقل النموذج النصي.

```cpp
enum class TextFormFieldType
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| Regular | 0 | يمكن لحقل النموذج النصي أن يحتوي على أي نص. |
| Number | 1 | يمكن لحقل النموذج النصي أن يحتوي على أرقام فقط. |
| التاريخ | 2 | يمكن لحقل النموذج النصي أن يحتوي على قيمة تاريخ صالحة فقط. |
| CurrentDate | 3 | قيمة حقل النموذج النصي هي التاريخ الحالي عند تحديث الحقل. |
| CurrentTime | 4 | قيمة حقل النموذج النصي هي الوقت الحالي عند تحديث الحقل. |
| Calculated | 5 | قيمة حقل النموذج النصي تُحسب من التعبير المحدد في الخاصية [TextInputDefault](../formfield/get_textinputdefault/). |


## أمثلة



يظهر كيفية إنشاء حقول النماذج.
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

// حقول النماذج هي كائنات في المستند يمكن للمستخدم التفاعل معها عن طريق طلب إدخال القيم.
// يمكننا إنشاؤها باستخدام مُنشئ المستند، وفيما يلي طريقتان للقيام بذلك.
// 1 -  إدخال نص أساسي:
builder->InsertTextInput(u"My text input", Aspose::Words::Fields::TextFormFieldType::Regular, u"", u"Enter your name here", 30);

// 2 -  مربع اختيار مع نص توجيه، ونطاق من القيم الممكنة:
System::ArrayPtr<System::String> items = System::MakeArray<System::String>({u"-- Select your favorite footwear --", u"Sneakers", u"Oxfords", u"Flip-flops", u"Other"});

builder->InsertParagraph();
builder->InsertComboBox(u"My combo box", items, 0);

builder->get_Document()->Save(get_ArtifactsDir() + u"DocumentBuilder.CreateForm.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
