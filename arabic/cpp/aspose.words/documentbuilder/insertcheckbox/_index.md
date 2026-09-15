---
title: "Aspose::Words::DocumentBuilder::InsertCheckBox method"
linktitle: "InsertCheckBox"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::DocumentBuilder::InsertCheckBox method. يُدرج حقل نموذج خانة اختيار في الموضع الحالي في C++."
type: docs
weight: 31000
url: /ar/cpp/aspose.words/documentbuilder/insertcheckbox/
---
## DocumentBuilder::InsertCheckBox(const System::String\&, bool, int32_t) method


يدرج حقل نموذج خانة اختيار في الموضع الحالي.

```cpp
System::SharedPtr<Aspose::Words::Fields::FormField> Aspose::Words::DocumentBuilder::InsertCheckBox(const System::String &name, bool checkedValue, int32_t size)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| name | const System::String\& | اسم حقل النموذج. يمكن أن يكون سلسلة فارغة. سيتم قطع القيمة التي تتجاوز 20 حرفًا. |
| checkedValue | bool | حالة التحديد لحقل نموذج خانة الاختيار. |
| size | int32_t | يحدد حجم خانة الاختيار بالنقاط. حدد 0 لـ MS Word لحساب حجم خانة الاختيار تلقائيًا. |

### ReturnValue

عقدة حقل النموذج التي تم إدراجها للتو.
## ملاحظات


إذا قمت بتحديد اسم لحقل النموذج، فسيتم إنشاء إشارة مرجعية تلقائيًا بنفس الاسم.

## أمثلة



يظهر كيفية إدراج خانات الاختيار في المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// إدراج خانات اختيار بأحجام مختلفة وحالات تحديد افتراضية.
builder->Write(u"Unchecked check box of a default size: ");
builder->InsertCheckBox(System::String::Empty, false, false, 0);
builder->InsertParagraph();

builder->Write(u"Large checked check box: ");
builder->InsertCheckBox(u"CheckBox_Default", true, true, 50);
builder->InsertParagraph();

// حقول النموذج لها حد طول اسم يبلغ 20 حرفًا.
builder->Write(u"Very large checked check box: ");
builder->InsertCheckBox(u"CheckBox_OnlyCheckedValue", true, 100);

ASSERT_EQ(u"CheckBox_OnlyChecked", doc->get_Range()->get_FormFields()->idx_get(2)->get_Name());

// يمكننا التفاعل مع هذه الخانات في Microsoft Word بالنقر المزدوج عليها.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertCheckBox.docx");
```

## انظر أيضًا

* Class [FormField](../../../aspose.words.fields/formfield/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertCheckBox(const System::String\&, bool, bool, int32_t) method


يدرج حقل نموذج خانة اختيار في الموضع الحالي.

```cpp
System::SharedPtr<Aspose::Words::Fields::FormField> Aspose::Words::DocumentBuilder::InsertCheckBox(const System::String &name, bool defaultValue, bool checkedValue, int32_t size)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| name | const System::String\& | اسم حقل النموذج. يمكن أن يكون سلسلة فارغة. سيتم قطع القيمة التي تتجاوز 20 حرفًا. |
| defaultValue | bool | القيمة الافتراضية لحقل نموذج خانة الاختيار. |
| checkedValue | bool | الحالة الحالية للعلامة في حقل نموذج خانة الاختيار. |
| size | int32_t | يحدد حجم خانة الاختيار بالنقاط. حدد 0 لـ MS Word لحساب حجم خانة الاختيار تلقائيًا. |

### ReturnValue

عقدة حقل النموذج التي تم إدراجها للتو.
## ملاحظات


إذا قمت بتحديد اسم لحقل النموذج، فسيتم إنشاء إشارة مرجعية تلقائيًا بنفس الاسم.

## أمثلة



يظهر كيفية إدراج خانات الاختيار في المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// إدراج خانات اختيار بأحجام مختلفة وحالات تحديد افتراضية.
builder->Write(u"Unchecked check box of a default size: ");
builder->InsertCheckBox(System::String::Empty, false, false, 0);
builder->InsertParagraph();

builder->Write(u"Large checked check box: ");
builder->InsertCheckBox(u"CheckBox_Default", true, true, 50);
builder->InsertParagraph();

// حقول النموذج لها حد طول اسم يبلغ 20 حرفًا.
builder->Write(u"Very large checked check box: ");
builder->InsertCheckBox(u"CheckBox_OnlyCheckedValue", true, 100);

ASSERT_EQ(u"CheckBox_OnlyChecked", doc->get_Range()->get_FormFields()->idx_get(2)->get_Name());

// يمكننا التفاعل مع هذه الخانات في Microsoft Word بالنقر المزدوج عليها.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertCheckBox.docx");
```

## انظر أيضًا

* Class [FormField](../../../aspose.words.fields/formfield/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
