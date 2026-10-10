---
title: "فئة Aspose::Words::Comparing::CompareOptions"
linktitle: "CompareOptions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Comparing::CompareOptions. تسمح باختيار خيارات إضافية لعملية مقارنة المستندات. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 1000
url: /ar/cpp/aspose.words.comparing/compareoptions/
---
## CompareOptions class


يسمح باختيار خيارات إضافية لعملية مقارنة المستندات. لمعرفة المزيد، زر مقالة الوثائق [Compare Documents](https://docs.aspose.com/words/cpp/compare-documents/).

```cpp
class CompareOptions : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [CompareOptions](./compareoptions/)() |  |
| [get_AdvancedOptions](./get_advancedoptions/)() const | يحدد خيارات مقارنة متقدمة قد تساعد في إنتاج مخرجات مقارنة أكثر دقة. |
| [get_CompareMoves](./get_comparemoves/)() const | يحدد ما إذا كان يجب مقارنة الاختلافات بين المستندين. |
| [get_Granularity](./get_granularity/)() const | يحدد ما إذا كانت التغييرات تُتبع حسب الحرف أو حسب الكلمة. |
| [get_IgnoreCaseChanges](./get_ignorecasechanges/)() const | True تشير إلى أن مقارنة المستندات غير حساسة لحالة الأحرف. |
| [get_IgnoreComments](./get_ignorecomments/)() const | يحدد ما إذا كان يجب مقارنة الاختلافات في التعليقات. |
| [get_IgnoreDmlUniqueId](./get_ignoredmluniqueid/)() | يحدد ما إذا كان يجب تجاهل الاختلاف في المعرف الفريد لـ DrawingML. |
| [get_IgnoreFields](./get_ignorefields/)() const | يحدد ما إذا كان يجب مقارنة الاختلافات في الحقول. |
| [get_IgnoreFootnotes](./get_ignorefootnotes/)() const | يحدد ما إذا كان يجب مقارنة الاختلافات في الحواشي السفلية والختامية. |
| [get_IgnoreFormatting](./get_ignoreformatting/)() const | True تشير إلى أن التنسيق يتم تجاهله. |
| [get_IgnoreHeadersAndFooters](./get_ignoreheadersandfooters/)() const | True تشير إلى أن محتوى رؤوس وتذييلات الصفحات يتم تجاهله. |
| [get_IgnoreTables](./get_ignoretables/)() const | يحدد ما إذا كان يجب مقارنة الاختلافات في البيانات الموجودة في الجداول. |
| [get_IgnoreTextboxes](./get_ignoretextboxes/)() const | يحدد ما إذا كان يجب مقارنة الاختلافات في البيانات الموجودة داخل مربعات النص. |
| [get_Target](./get_target/)() const | يحدد أي مستند سيُستخدم كهدف أثناء المقارنة. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CompareMoves](./set_comparemoves/)(bool) | مُعيّن لـ [Aspose::Words::Comparing::CompareOptions::get_CompareMoves](./get_comparemoves/). |
| [set_Granularity](./set_granularity/)(Aspose::Words::Comparing::Granularity) | مُعيّن لـ [Aspose::Words::Comparing::CompareOptions::get_Granularity](./get_granularity/). |
| [set_IgnoreCaseChanges](./set_ignorecasechanges/)(bool) | مُعيّن لـ [Aspose::Words::Comparing::CompareOptions::get_IgnoreCaseChanges](./get_ignorecasechanges/). |
| [set_IgnoreComments](./set_ignorecomments/)(bool) | مُعيّن لـ [Aspose::Words::Comparing::CompareOptions::get_IgnoreComments](./get_ignorecomments/). |
| [set_IgnoreDmlUniqueId](./set_ignoredmluniqueid/)(bool) | مُعيّن لـ [Aspose::Words::Comparing::CompareOptions::get_IgnoreDmlUniqueId](./get_ignoredmluniqueid/). |
| [set_IgnoreFields](./set_ignorefields/)(bool) | مُعيّن لـ [Aspose::Words::Comparing::CompareOptions::get_IgnoreFields](./get_ignorefields/). |
| [set_IgnoreFootnotes](./set_ignorefootnotes/)(bool) | مُعيّن لـ [Aspose::Words::Comparing::CompareOptions::get_IgnoreFootnotes](./get_ignorefootnotes/). |
| [set_IgnoreFormatting](./set_ignoreformatting/)(bool) | مُعيّن لـ [Aspose::Words::Comparing::CompareOptions::get_IgnoreFormatting](./get_ignoreformatting/). |
| [set_IgnoreHeadersAndFooters](./set_ignoreheadersandfooters/)(bool) | المُعيّن لـ [Aspose::Words::Comparing::CompareOptions::get_IgnoreHeadersAndFooters](./get_ignoreheadersandfooters/). |
| [set_IgnoreTables](./set_ignoretables/)(bool) | المُعيّن لـ [Aspose::Words::Comparing::CompareOptions::get_IgnoreTables](./get_ignoretables/). |
| [set_IgnoreTextboxes](./set_ignoretextboxes/)(bool) | المُعيّن لـ [Aspose::Words::Comparing::CompareOptions::get_IgnoreTextboxes](./get_ignoretextboxes/). |
| [set_Target](./set_target/)(Aspose::Words::Comparing::ComparisonTargetType) | المُعيّن لـ [Aspose::Words::Comparing::CompareOptions::get_Target](./get_target/). |
| static [Type](./type/)() |  |

## أمثلة



يعرض كيفية تصفية أنواع محددة من عناصر المستند عند إجراء مقارنة.
```cpp
// أنشئ المستند الأصلي واملأه بأنواع مختلفة من العناصر.
auto docOriginal = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(docOriginal);

// نص الفقرة المشار إليه بحاشية سفلية:
builder->Writeln(u"Hello world! This is the first paragraph.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Original endnote text.");

// جدول:
builder->StartTable();
builder->InsertCell();
builder->Write(u"Original cell 1 text");
builder->InsertCell();
builder->Write(u"Original cell 2 text");
builder->EndTable();

// مربع نص:
System::SharedPtr<Aspose::Words::Drawing::Shape> textBox = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 150, 20);
builder->MoveTo(textBox->get_FirstParagraph());
builder->Write(u"Original textbox contents");

// حقل DATE:
builder->MoveTo(docOriginal->get_FirstSection()->get_Body()->AppendParagraph(u""));
builder->InsertField(u" DATE ");

// تعليق:
auto newComment = System::MakeObject<Aspose::Words::Comment>(docOriginal, u"John Doe", u"J.D.", System::DateTime::get_Now());
newComment->SetText(u"Original comment.");
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(newComment);

// ترويسة:
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Writeln(u"Original header contents.");

// أنشئ نسخة مكررة من مستندنا وقم بتحرير سريع لكل عنصر من عناصر المستند المكرر.
auto docEdited = System::ExplicitCast<Aspose::Words::Document>(System::ExplicitCast<Aspose::Words::Node>(docOriginal)->Clone(true));
System::SharedPtr<Aspose::Words::Paragraph> firstParagraph = docEdited->get_FirstSection()->get_Body()->get_FirstParagraph();

firstParagraph->get_Runs()->idx_get(0)->set_Text(u"hello world! this is the first paragraph, after editing.");
firstParagraph->get_ParagraphFormat()->set_Style(docEdited->get_Styles()->idx_get(Aspose::Words::StyleIdentifier::Heading1));
(System::ExplicitCast<Aspose::Words::Notes::Footnote>(docEdited->GetChild(Aspose::Words::NodeType::Footnote, 0, true)))->get_FirstParagraph()->get_Runs()->idx_get(1)->set_Text(u"Edited endnote text.");
(System::ExplicitCast<Aspose::Words::Tables::Table>(docEdited->GetChild(Aspose::Words::NodeType::Table, 0, true)))->get_FirstRow()->get_Cells()->idx_get(1)->get_FirstParagraph()->get_Runs()->idx_get(0)->set_Text(u"Edited Cell 2 contents");
(System::ExplicitCast<Aspose::Words::Drawing::Shape>(docEdited->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_FirstParagraph()->get_Runs()->idx_get(0)->set_Text(u"Edited textbox contents");
(System::ExplicitCast<Aspose::Words::Fields::FieldDate>(docEdited->get_Range()->get_Fields()->idx_get(0)))->set_UseLunarCalendar(true);
(System::ExplicitCast<Aspose::Words::Comment>(docEdited->GetChild(Aspose::Words::NodeType::Comment, 0, true)))->get_FirstParagraph()->get_Runs()->idx_get(0)->set_Text(u"Edited comment.");
docEdited->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->get_FirstParagraph()->get_Runs()->idx_get(0)->set_Text(u"Edited header contents.");

// إن مقارنة المستندات تُنشئ مراجعة لكل تعديل في المستند المُحرر.
// كائن CompareOptions يحتوي على سلسلة من العلامات التي يمكنها قمع المراجعات
// على كل نوع من العناصر على حدة، مما يتجاهل تغييره فعليًا.
auto compareOptions = System::MakeObject<Aspose::Words::Comparing::CompareOptions>();
compareOptions->set_CompareMoves(false);
compareOptions->set_IgnoreFormatting(false);
compareOptions->set_IgnoreCaseChanges(false);
compareOptions->set_IgnoreComments(false);
compareOptions->set_IgnoreTables(false);
compareOptions->set_IgnoreFields(false);
compareOptions->set_IgnoreFootnotes(false);
compareOptions->set_IgnoreTextboxes(false);
compareOptions->set_IgnoreHeadersAndFooters(false);
compareOptions->set_Target(Aspose::Words::Comparing::ComparisonTargetType::New);

docOriginal->Compare(docEdited, u"John Doe", System::DateTime::get_Now(), compareOptions);
docOriginal->Save(get_ArtifactsDir() + u"Revision.CompareOptions.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words::Comparing](../)
* Library [Aspose.Words for C++](../../)
