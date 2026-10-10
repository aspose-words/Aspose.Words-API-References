---
title: "طريقة Aspose::Words::Paragraph::AppendField"
linktitle: "AppendField"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Paragraph::AppendField. يضيف حقلًا إلى هذه الفقرة في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words/paragraph/appendfield/
---
## Paragraph::AppendField(Aspose::Words::Fields::FieldType, bool) method


يضيف حقلًا إلى هذه الفقرة.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::AppendField(Aspose::Words::Fields::FieldType fieldType, bool updateField)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| fieldType | Aspose::Words::Fields::FieldType | نوع الحقل المراد إلحاقه. |
| updateField | bool | يحدد ما إذا كان يجب تحديث الحقل فورًا. |

### ReturnValue

كائن [Field](../../../aspose.words.fields/field/) يمثل الحقل المضاف.

## أمثلة



يوضح طرقًا متعددة لإضافة الحقول إلى فقرة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// فيما يلي ثلاث طرق لإضافة حقل إلى نهاية الفقرة.
// 1 -  أضف حقل DATE باستخدام نوع الحقل، ثم قم بتحديثه:
paragraph->AppendField(Aspose::Words::Fields::FieldType::FieldDate, true);

// 2 -  أضف حقل TIME باستخدام رمز الحقل:
paragraph->AppendField(u" TIME  \\@ \"HH:mm:ss\" ");

// 3 -  أضف حقل QUOTE باستخدام رمز الحقل، واجعل عرضه قيمة نائبة:
paragraph->AppendField(u" QUOTE \"Real value\"", u"Placeholder value");

ASSERT_EQ(u"Placeholder value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

// سيعرض هذا الحقل قيمته النائبة حتى نقوم بتحديثه.
doc->UpdateFields();

ASSERT_EQ(u"Real value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.AppendField.docx");
```

## انظر أيضًا

* Class [Field](../../../aspose.words.fields/field/)
* Enum [FieldType](../../../aspose.words.fields/fieldtype/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Paragraph::AppendField(const System::String\&) method


يضيف حقلًا إلى هذه الفقرة.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::AppendField(const System::String &fieldCode)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| fieldCode | const System::String\& | رمز الحقل الذي سيتم إضافته (بدون الأقواس المعقوفة). |

### ReturnValue

كائن [Field](../../../aspose.words.fields/field/) يمثل الحقل المضاف.

## أمثلة



يوضح طرقًا متعددة لإضافة الحقول إلى فقرة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// فيما يلي ثلاث طرق لإضافة حقل إلى نهاية الفقرة.
// 1 -  أضف حقل DATE باستخدام نوع الحقل، ثم قم بتحديثه:
paragraph->AppendField(Aspose::Words::Fields::FieldType::FieldDate, true);

// 2 -  أضف حقل TIME باستخدام رمز الحقل:
paragraph->AppendField(u" TIME  \\@ \"HH:mm:ss\" ");

// 3 -  أضف حقل QUOTE باستخدام رمز الحقل، واجعل عرضه قيمة نائبة:
paragraph->AppendField(u" QUOTE \"Real value\"", u"Placeholder value");

ASSERT_EQ(u"Placeholder value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

// سيعرض هذا الحقل قيمته النائبة حتى نقوم بتحديثه.
doc->UpdateFields();

ASSERT_EQ(u"Real value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.AppendField.docx");
```

## انظر أيضًا

* Class [Field](../../../aspose.words.fields/field/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Paragraph::AppendField(const System::String\&, const System::String\&) method


يضيف حقلًا إلى هذه الفقرة.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::AppendField(const System::String &fieldCode, const System::String &fieldValue)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| fieldCode | const System::String\& | رمز الحقل الذي سيتم إضافته (بدون الأقواس المعقوفة). |
| fieldValue | const System::String\& | قيمة الحقل التي سيتم إضافتها. مرّر **null** للحقول التي لا تحتوي على قيمة. |

### ReturnValue

كائن [Field](../../../aspose.words.fields/field/) يمثل الحقل المضاف.

## أمثلة



يوضح طرقًا متعددة لإضافة الحقول إلى فقرة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// فيما يلي ثلاث طرق لإضافة حقل إلى نهاية الفقرة.
// 1 -  أضف حقل DATE باستخدام نوع الحقل، ثم قم بتحديثه:
paragraph->AppendField(Aspose::Words::Fields::FieldType::FieldDate, true);

// 2 -  أضف حقل TIME باستخدام رمز الحقل:
paragraph->AppendField(u" TIME  \\@ \"HH:mm:ss\" ");

// 3 -  أضف حقل QUOTE باستخدام رمز الحقل، واجعل عرضه قيمة نائبة:
paragraph->AppendField(u" QUOTE \"Real value\"", u"Placeholder value");

ASSERT_EQ(u"Placeholder value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

// سيعرض هذا الحقل قيمته النائبة حتى نقوم بتحديثه.
doc->UpdateFields();

ASSERT_EQ(u"Real value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.AppendField.docx");
```

## انظر أيضًا

* Class [Field](../../../aspose.words.fields/field/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
