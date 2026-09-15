---
title: "طريقة Aspose::Words::DocumentBuilder::MoveToMergeField"
linktitle: "MoveToMergeField"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::DocumentBuilder::MoveToMergeField. ينقل المؤشر إلى موقع يبعد قليلاً عن حقل الدمج المحدد ويزيل حقل الدمج في C++."
type: docs
weight: 58000
url: /ar/cpp/aspose.words/documentbuilder/movetomergefield/
---
## DocumentBuilder::MoveToMergeField(const System::String\&) method


ينقل المؤشر إلى موضع يقع مباشرة بعد حقل الدمج المحدد ويزيل حقل الدمج.

```cpp
bool Aspose::Words::DocumentBuilder::MoveToMergeField(const System::String &fieldName)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| fieldName | const System::String\& | الاسم غير حساس لحالة حقل دمج البريد. |

### ReturnValue

**true** if the merge field was found and the cursor was moved; **false** otherwise.
## ملاحظات


لاحظ أن هذه الطريقة تحذف حقل الدمج من المستند بعد نقل المؤشر.

## أمثلة



يظهر كيفية ملء حقول MERGEFIELD بالبيانات باستخدام مُنشئ المستند بدلاً من الدمج البريدي.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدرج بعض حقول MERGEFIELD، التي تقبل البيانات من أعمدة ذات الاسم نفسه في مصدر البيانات أثناء الدمج البريدي،
// ثم قم بملئها يدويًا.
builder->InsertField(u" MERGEFIELD Chairman ");
builder->InsertField(u" MERGEFIELD ChiefFinancialOfficer ");
builder->InsertField(u" MERGEFIELD ChiefTechnologyOfficer ");

builder->MoveToMergeField(u"Chairman");
builder->set_Bold(true);
builder->Writeln(u"John Doe");

builder->MoveToMergeField(u"ChiefFinancialOfficer");
builder->set_Italic(true);
builder->Writeln(u"Jane Doe");

builder->MoveToMergeField(u"ChiefTechnologyOfficer");
builder->set_Italic(true);
builder->Writeln(u"John Bloggs");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.FillMergeFields.docx");
```

## انظر أيضًا

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::MoveToMergeField(const System::String\&, bool, bool) method


ينقل حقل الدمج إلى حقل الدمج المحدد.

```cpp
bool Aspose::Words::DocumentBuilder::MoveToMergeField(const System::String &fieldName, bool isAfter, bool isDeleteField)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| fieldName | const System::String\& | الاسم غير حساس لحالة حقل دمج البريد. |
| isAfter | bool | عند **true**، ينقل المؤشر ليكون بعد نهاية الحقل. عند **false**، ينقل المؤشر ليكون قبل بداية الحقل. |
| isDeleteField | bool | عند **true**، يحذف حقل الدمج. |

### ReturnValue

**true** if the merge field was found and the cursor was moved; **false** otherwise.

## أمثلة



يوضح كيفية إدراج الحقول، وتحريك مؤشر منشئ المستند إليها.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertField(u"MERGEFIELD MyMergeField1 \\* MERGEFORMAT");
builder->InsertField(u"MERGEFIELD MyMergeField2 \\* MERGEFORMAT");

// حرك المؤشر إلى أول MERGEFIELD.
builder->MoveToMergeField(u"MyMergeField1", true, false);

// لاحظ أن المؤشر يُوضع مباشرةً بعد أول MERGEFIELD، وقبل الثاني.
ASPOSE_ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(1)->get_Start(), builder->get_CurrentNode());
ASPOSE_ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(0)->get_End(), builder->get_CurrentNode()->get_PreviousSibling());

// إذا رغبنا في تعديل رمز الحقل أو محتوياته باستخدام المنشئ،
// يجب أن يكون مؤشره داخل حقل.
// لوضعه داخل حقل، سيتعين علينا استدعاء طريقة MoveTo الخاصة بمنشئ المستند
// وتمرير عقدة بداية الحقل أو الفاصل كمعامل.
builder->Write(u" Text between our merge fields. ");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.MergeFields.docx");
```

## انظر أيضًا

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
