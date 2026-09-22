---
title: "طريقة Aspose::Words::DocumentBuilder::InsertField"
linktitle: "InsertField"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::DocumentBuilder::InsertField. تُدرج حقل Word في مستند وتحدّث نتيجة الحقل اختياريًا في C++."
type: docs
weight: 34000
url: /ar/cpp/aspose.words/documentbuilder/insertfield/
---
## DocumentBuilder::InsertField(Aspose::Words::Fields::FieldType, bool) method


يدرج حقل Word في مستند ويحدّث نتيجة الحقل اختياريًا.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::DocumentBuilder::InsertField(Aspose::Words::Fields::FieldType fieldType, bool updateField)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| fieldType | Aspose::Words::Fields::FieldType | نوع الحقل المراد إلحاقه. |
| updateField | bool | يحدد ما إذا كان يجب تحديث الحقل فورًا. |

### ReturnValue

كائن [Field](../../../aspose.words.fields/field/) الذي يمثل الحقل المُدرج.
## ملاحظات


تُدرج هذه الطريقة حقلًا في مستند. يمكن لـ Aspose.Words تحديث الحقول من معظم الأنواع، لكن ليس جميعها. لمزيد من التفاصيل راجع التحميل الزائد لـ [InsertField()](../).

## أمثلة



يظهر كيفية إدراج حقل في مستند باستخدام FieldType.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدرج حقلين مع تمرير علم يحدد ما إذا كان يجب تحديثهما أثناء إدراجهما بواسطة المُنشئ.
// في بعض الحالات، قد يكون تحديث الحقول مكلفًا حسابيًا، وقد يكون من الجيد تأجيل التحديث.
doc->get_BuiltInDocumentProperties()->set_Author(u"John Doe");
builder->Write(u"This document was written by ");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, updateInsertedFieldsImmediately);

builder->InsertParagraph();
builder->Write(u"\nThis is page ");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldPage, updateInsertedFieldsImmediately);

ASSERT_EQ(u" AUTHOR ", doc->get_Range()->get_Fields()->idx_get(0)->GetFieldCode());
ASSERT_EQ(u" PAGE ", doc->get_Range()->get_Fields()->idx_get(1)->GetFieldCode());

if (updateInsertedFieldsImmediately)
{
    ASSERT_EQ(u"John Doe", doc->get_Range()->get_Fields()->idx_get(0)->get_Result());
    ASSERT_EQ(u"1", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());
}
else
{
    ASSERT_EQ(System::String::Empty, doc->get_Range()->get_Fields()->idx_get(0)->get_Result());
    ASSERT_EQ(System::String::Empty, doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

    // سنحتاج إلى تحديث هذه الحقول يدويًا باستخدام طرق التحديث.
    doc->get_Range()->get_Fields()->idx_get(0)->Update();

    ASSERT_EQ(u"John Doe", doc->get_Range()->get_Fields()->idx_get(0)->get_Result());

    doc->UpdateFields();

    ASSERT_EQ(u"1", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());
}
```

## انظر أيضًا

* Class [Field](../../../aspose.words.fields/field/)
* Enum [FieldType](../../../aspose.words.fields/fieldtype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertField(const System::String\&) method


يدرج حقل Word في مستند ويحدّث نتيجة الحقل.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::DocumentBuilder::InsertField(const System::String &fieldCode)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| fieldCode | const System::String\& | رمز الحقل المراد إدراجه (بدون الأقواس المعقوفة). |

### ReturnValue

كائن [Field](../../../aspose.words.fields/field/) الذي يمثل الحقل المُدرج.
## ملاحظات


هذه الطريقة تُدرج حقلًا في مستند وتُحدّث نتيجة الحقل فورًا. يمكن لـ Aspose.Words تحديث الحقول لمعظم الأنواع، لكن ليس جميعها. لمزيد من التفاصيل، راجع التحميل الزائد لـ [InsertField()](../).

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


يظهر كيفية إدراج حقل في مستند باستخدام رمز الحقل.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"DATE \\@ \"dddd, MMMM dd, yyyy\"");

ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Type());
ASSERT_EQ(u"DATE \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());

// هذا التحميل الزائد لطريقة InsertField يقوم تلقائيًا بتحديث الحقول المدخلة.
ASSERT_TRUE((System::DateTime::get_Today() - System::DateTime::Parse(field->get_Result())).get_Days() <= 1);
```

## انظر أيضًا

* Class [Field](../../../aspose.words.fields/field/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertField(const System::String\&, const System::String\&) method


يدرج حقل Word في مستند دون تحديث نتيجة الحقل.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::DocumentBuilder::InsertField(const System::String &fieldCode, const System::String &fieldValue)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| fieldCode | const System::String\& | رمز الحقل المراد إدراجه (بدون الأقواس المعقوفة). |
| fieldValue | const System::String\& | قيمة الحقل المراد إدراجها. مرّر **null** للحقول التي لا تملك قيمة. |

### ReturnValue

كائن [Field](../../../aspose.words.fields/field/) الذي يمثل الحقل المُدرج.
## ملاحظات


[Fields](../../../aspose.words.fields/) in Microsoft Word documents consist of a field code and a field result. The field code is like a formula and the field result is like the value that the formula produces. The field code may also contain field switches that are like additional instructions to perform a specific action.

يمكنك التبديل بين عرض رموز الحقول والنتائج في مستندك في Microsoft Word باستخدام اختصار لوحة المفاتيح Alt+F9. تظهر رموز الحقول بين الأقواس المعقوفة ( { } ).

لإنشاء حقل، تحتاج إلى تحديد نوع الحقل، ورمز الحقل، وقيمة حقل "نائبة". إذا لم تكن متأكدًا من صياغة رمز حقل معين، أنشئ الحقل أولاً في Microsoft Word ثم قم بالتبديل لرؤية رمزه.

يمكن لـ Aspose.Words حساب نتائج الحقول لمعظم أنواع الحقول، لكن هذه الطريقة لا تُحدّث نتيجة الحقل تلقائيًا. نظرًا لعدم حساب نتيجة الحقل تلقائيًا، يُتوقع منك تمرير قيمة نصية (أو حتى سلسلة فارغة) سيتم إدراجها في نتيجة الحقل. ستظل هذه القيمة في نتيجة الحقل كنائب حتى يتم تحديث الحقل. لتحديث نتيجة الحقل يمكنك استدعاء [Update](../../../aspose.words.fields/field/update/) على كائن الحقل المُرجع إليك أو [UpdateFields](../../document/updatefields/) لتحديث الحقول في المستند بأكمله.

## أمثلة



يظهر كيفية إعداد ترقيم الصفحات في قسم.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Section 1, page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 1, page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 1, page 3.");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Writeln(u"Section 2, page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 2, page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 2, page 3.");

// انقل مُنشئ المستند إلى الرأس الأساسي للقسم الأول،
// الذي سيُظهره كل صفحة في ذلك القسم.
builder->MoveToSection(0);
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);

// أدرج حقل PAGE، الذي سيعرض رقم الصفحة الحالية.
builder->Write(u"Page ");
builder->InsertField(u"PAGE", u"");

// قم بتكوين القسم بحيث يبدأ عدد الصفحات الذي تعرضه حقول PAGE من 5.
// أيضًا، قم بتكوين جميع حقول PAGE لعرض أرقام صفحاتها باستخدام الأرقام الرومانية الكبيرة.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_RestartPageNumbering(true);
pageSetup->set_PageStartingNumber(5);
pageSetup->set_PageNumberStyle(Aspose::Words::NumberStyle::UppercaseRoman);

// أنشئ رأسًا أساسيًا آخر للقسم الثاني، مع حقل PAGE آخر.
builder->MoveToSection(1);
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
builder->Write(u" - ");
builder->InsertField(u"PAGE", u"");
builder->Write(u" - ");

// قم بتكوين القسم بحيث يبدأ عدد الصفحات الذي تعرضه حقول PAGE من 10.
// أيضًا، قم بتكوين جميع حقول PAGE لعرض أرقام صفحاتها باستخدام الأرقام العربية.
pageSetup = doc->get_Sections()->idx_get(1)->get_PageSetup();
pageSetup->set_PageStartingNumber(10);
pageSetup->set_RestartPageNumbering(true);
pageSetup->set_PageNumberStyle(Aspose::Words::NumberStyle::Arabic);

doc->Save(get_ArtifactsDir() + u"PageSetup.PageNumbering.docx");
```

## انظر أيضًا

* Class [Field](../../../aspose.words.fields/field/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
