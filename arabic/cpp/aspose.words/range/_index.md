---
title: "فئة Aspose::Words::Range"
linktitle: "النطاق"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Range. تمثل مساحة متصلة في المستند. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 51000
url: /ar/cpp/aspose.words/range/
---
## Range class


يمثل مساحة متصلة في المستند. لمعرفة المزيد، زر مقالة الوثائق [Working with Ranges](https://docs.aspose.com/words/cpp/working-with-ranges/).

```cpp
class Range : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Node>>
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Delete](./delete/)() | يحذف جميع الأحرف في النطاق. |
| [get_Bookmarks](./get_bookmarks/)() | يرجع مجموعة [Bookmarks](./get_bookmarks/) تمثل جميع العلامات المرجعية في النطاق. |
| [get_Fields](./get_fields/)() | يرجع مجموعة [Fields](./get_fields/) تمثل جميع الحقول في النطاق. |
| [get_FormFields](./get_formfields/)() | يرجع مجموعة [FormFields](./get_formfields/) تمثل جميع حقول النماذج في النطاق. |
| [get_Revisions](./get_revisions/)() | يحصل على مجموعة من المراجعات (التغييرات المتتبعة) الموجودة في هذا النطاق. |
| [get_StructuredDocumentTags](./get_structureddocumenttags/)() | يرجع مجموعة [StructuredDocumentTags](./get_structureddocumenttags/) تمثل جميع العلامات المهيكلة للمستند في النطاق. |
| [get_Text](./get_text/)() | يحصل على نص النطاق. |
| [GetEnumerator](./getenumerator/)() override |  |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [NormalizeFieldTypes](./normalizefieldtypes/)() | يغيّر قيم نوع الحقل [FieldType](../../aspose.words.fields/fieldchar/get_fieldtype/) لـ [FieldStart](../../aspose.words.fields/fieldstart/)، [FieldSeparator](../../aspose.words.fields/fieldseparator/)، [FieldEnd](../../aspose.words.fields/fieldend/) في هذا النطاق بحيث تتطابق مع أنواع الحقول الموجودة في رموز الحقول. |
| [Replace](./replace/)(const System::String\&, const System::String\&) | يستبدل جميع تكرارات نمط سلسلة الأحرف المحدد بسلسلة استبدال. |
| [Replace](./replace/)(const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) | يستبدل جميع تكرارات نمط الحرف المحدد بتعبير عادي بسلسلة أخرى. |
| [Replace](./replace/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | يستبدل جميع تكرارات نمط سلسلة الأحرف المحدد بسلسلة استبدال. |
| [Replace](./replace/)(const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | يستبدل جميع تكرارات نمط الحرف المحدد بتعبير عادي بسلسلة أخرى. |
| [ToDocument](./todocument/)() | ينشئ مستندًا جديدًا مكتملًا يحتوي على النطاق. |
| static [Type](./type/)() |  |
| [UnlinkFields](./unlinkfields/)() | يفك ربط الحقول في هذا النطاق. |
| [UpdateFields](./updatefields/)() | يحدّث قيم حقول المستند في هذا النطاق. |
## ملاحظات


المستند ممثل بشجرة من العقد وتوفر العقد عمليات للعمل مع الشجرة، لكن بعض العمليات تكون أسهل إذا عُومل المستند كسلسلة متصلة من النص.

[Range](./) is a "facade" interface that provide methods that treat the document or portions of the document as "flat" text regardless of the fact that the document nodes are stored in a tree-like object model.

[Range](./) does not contain any text or nodes, it is merely a view or "window" over a fragment of a document.

## أمثلة



يوضح كيفية الحصول على محتوى النص لجميع العقد التي يغطيها النطاق.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");

ASSERT_EQ(u"Hello world!", doc->get_Range()->get_Text().Trim());
```

## انظر أيضًا

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
