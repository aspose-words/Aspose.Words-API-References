---
title: "Aspose::Words::Paragraph::InsertField طريقة"
linktitle: "InsertField"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Paragraph::InsertField طريقة. يدرج حقلًا في هذه الفقرة في C++."
type: docs
weight: 29000
url: /ar/cpp/aspose.words/paragraph/insertfield/
---
## Paragraph::InsertField(Aspose::Words::Fields::FieldType, bool, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) method


يدرج حقلًا في هذه الفقرة.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::InsertField(Aspose::Words::Fields::FieldType fieldType, bool updateField, const System::SharedPtr<Aspose::Words::Node> &refNode, bool isAfter)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| fieldType | Aspose::Words::Fields::FieldType | نوع الحقل الذي سيتم إدراجه. |
| updateField | bool | يحدد ما إذا كان يجب تحديث الحقل فورًا. |
| refNode | const System::SharedPtr\<Aspose::Words::Node\>\& | العقدة المرجعية داخل هذه الفقرة (إذا كان *refNode* **null**, فسيتم الإلحاق بنهاية الفقرة). |
| isAfter | bool | ما إذا كان سيتم إدراج الحقل بعد أو قبل العقدة المرجعية. |

### ReturnValue

كائن [Field](../../../aspose.words.fields/field/) الذي يمثل الحقل المُدرج.

## أمثلة



يعرض طرقًا مختلفة لإضافة حقول إلى فقرة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// فيما يلي ثلاث طرق لإدراج حقل في فقرة.
// 1 -  أدخل حقل AUTHOR في فقرة بعد أحد العقد الفرعية للفقرة:
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"This run was written by ");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->get_BuiltInDocumentProperties()->idx_get(u"Author")->set_Value(System::ExplicitCast<System::Object>(u"John Doe"));
para->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true, run, true);

// 2 -  أدخل حقل QUOTE بعد أحد العقد الفرعية للفقرة:
run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u".");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

System::SharedPtr<Aspose::Words::Fields::Field> field = para->InsertField(u" QUOTE \" Real value\" ", run, true);

// 3 -  أدخل حقل QUOTE قبل أحد العقد الفرعية للفقرة،
// واحصل على عرضه لقيمة العنصر النائب:
para->InsertField(u" QUOTE \" Real value.\"", u" Placeholder value.", field->get_Start(), false);

ASSERT_EQ(u" Placeholder value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

// سيعرض هذا الحقل قيمته النائبة حتى نقوم بتحديثه.
doc->UpdateFields();

ASSERT_EQ(u" Real value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.InsertField.docx");
```

## انظر أيضًا

* Class [Field](../../../aspose.words.fields/field/)
* Enum [FieldType](../../../aspose.words.fields/fieldtype/)
* Class [Node](../../node/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Paragraph::InsertField(const System::String\&, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) method


يدرج حقلًا في هذه الفقرة.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::InsertField(const System::String &fieldCode, const System::SharedPtr<Aspose::Words::Node> &refNode, bool isAfter)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| fieldCode | const System::String\& | رمز الحقل المراد إدراجه (بدون الأقواس المعقوفة). |
| refNode | const System::SharedPtr\<Aspose::Words::Node\>\& | العقدة المرجعية داخل هذه الفقرة (إذا كان *refNode* **null**, فسيتم الإلحاق بنهاية الفقرة). |
| isAfter | bool | ما إذا كان سيتم إدراج الحقل بعد أو قبل العقدة المرجعية. |

### ReturnValue

كائن [Field](../../../aspose.words.fields/field/) الذي يمثل الحقل المُدرج.

## أمثلة



يعرض طرقًا مختلفة لإضافة حقول إلى فقرة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// فيما يلي ثلاث طرق لإدراج حقل في فقرة.
// 1 -  أدخل حقل AUTHOR في فقرة بعد أحد العقد الفرعية للفقرة:
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"This run was written by ");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->get_BuiltInDocumentProperties()->idx_get(u"Author")->set_Value(System::ExplicitCast<System::Object>(u"John Doe"));
para->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true, run, true);

// 2 -  أدخل حقل QUOTE بعد أحد العقد الفرعية للفقرة:
run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u".");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

System::SharedPtr<Aspose::Words::Fields::Field> field = para->InsertField(u" QUOTE \" Real value\" ", run, true);

// 3 -  أدخل حقل QUOTE قبل أحد العقد الفرعية للفقرة،
// واحصل على عرضه لقيمة العنصر النائب:
para->InsertField(u" QUOTE \" Real value.\"", u" Placeholder value.", field->get_Start(), false);

ASSERT_EQ(u" Placeholder value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

// سيعرض هذا الحقل قيمته النائبة حتى نقوم بتحديثه.
doc->UpdateFields();

ASSERT_EQ(u" Real value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.InsertField.docx");
```

## انظر أيضًا

* Class [Field](../../../aspose.words.fields/field/)
* Class [Node](../../node/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Paragraph::InsertField(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) method


يدرج حقلًا في هذه الفقرة.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::InsertField(const System::String &fieldCode, const System::String &fieldValue, const System::SharedPtr<Aspose::Words::Node> &refNode, bool isAfter)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| fieldCode | const System::String\& | رمز الحقل المراد إدراجه (بدون الأقواس المعقوفة). |
| fieldValue | const System::String\& | قيمة الحقل المراد إدراجها. مرّر **null** للحقول التي لا تملك قيمة. |
| refNode | const System::SharedPtr\<Aspose::Words::Node\>\& | العقدة المرجعية داخل هذه الفقرة (إذا كان *refNode* **null**, فسيتم الإلحاق بنهاية الفقرة). |
| isAfter | bool | ما إذا كان سيتم إدراج الحقل بعد أو قبل العقدة المرجعية. |

### ReturnValue

كائن [Field](../../../aspose.words.fields/field/) الذي يمثل الحقل المُدرج.

## أمثلة



يعرض طرقًا مختلفة لإضافة حقول إلى فقرة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// فيما يلي ثلاث طرق لإدراج حقل في فقرة.
// 1 -  أدخل حقل AUTHOR في فقرة بعد أحد العقد الفرعية للفقرة:
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"This run was written by ");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->get_BuiltInDocumentProperties()->idx_get(u"Author")->set_Value(System::ExplicitCast<System::Object>(u"John Doe"));
para->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true, run, true);

// 2 -  أدخل حقل QUOTE بعد أحد العقد الفرعية للفقرة:
run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u".");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

System::SharedPtr<Aspose::Words::Fields::Field> field = para->InsertField(u" QUOTE \" Real value\" ", run, true);

// 3 -  أدخل حقل QUOTE قبل أحد العقد الفرعية للفقرة،
// واحصل على عرضه لقيمة العنصر النائب:
para->InsertField(u" QUOTE \" Real value.\"", u" Placeholder value.", field->get_Start(), false);

ASSERT_EQ(u" Placeholder value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

// سيعرض هذا الحقل قيمته النائبة حتى نقوم بتحديثه.
doc->UpdateFields();

ASSERT_EQ(u" Real value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.InsertField.docx");
```

## انظر أيضًا

* Class [Field](../../../aspose.words.fields/field/)
* Class [Node](../../node/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
