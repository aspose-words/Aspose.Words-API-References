---
title: "Aspose::Words::Notes::FootnoteOptions فئة"
linktitle: "FootnoteOptions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Notes::FootnoteOptions. تمثل خيارات ترقيم الحواشي السفلية لمستند أو قسم. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.notes/footnoteoptions/
---
## FootnoteOptions class


يمثل خيارات ترقيم الهوامش السفلية لمستند أو قسم. لمعرفة المزيد، زر مقالة الوثائق [Working with Footnote and Endnote](https://docs.aspose.com/words/cpp/working-with-footnote-and-endnote/).

```cpp
class FootnoteOptions : public Aspose::Words::Notes::IFootnoteOptions
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_Columns](./get_columns/)() | يحدد عدد الأعمدة التي يتم تنسيق منطقة الحواشي السفلية بها. |
| [get_NumberStyle](./get_numberstyle/)() override | يحدد تنسيق الرقم للحواشي السفلية المرقمة تلقائيًا. |
| [get_Position](./get_position/)() | يحدد موضع الحواشي السفلية. |
| [get_RestartRule](./get_restartrule/)() override | يحدد متى يتم إعادة تشغيل الترقيم التلقائي. |
| [get_StartNumber](./get_startnumber/)() override | يحدد الرقم أو الحرف الابتدائي لأول حواشي سفلية مرقمة تلقائيًا. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Columns](./set_columns/)(int32_t) | دالة تعيين لـ [Aspose::Words::Notes::FootnoteOptions::get_Columns](./get_columns/). |
| [set_NumberStyle](./set_numberstyle/)(Aspose::Words::NumberStyle) override | دالة تعيين لـ [Aspose::Words::Notes::FootnoteOptions::get_NumberStyle](./get_numberstyle/). |
| [set_Position](./set_position/)(Aspose::Words::Notes::FootnotePosition) | دالة تعيين لـ [Aspose::Words::Notes::FootnoteOptions::get_Position](./get_position/). |
| [set_RestartRule](./set_restartrule/)(Aspose::Words::Notes::FootnoteNumberingRule) override | دالة تعيين لـ [Aspose::Words::Notes::FootnoteOptions::get_RestartRule](./get_restartrule/). |
| [set_StartNumber](./set_startnumber/)(int32_t) override | دالة تعيين لـ [Aspose::Words::Notes::FootnoteOptions::get_StartNumber](./get_startnumber/). |
| static [Type](./type/)() |  |

## أمثلة



يظهر كيفية تقسيم قسم الحواشي السفلية إلى عدد محدد من الأعمدة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

doc->get_FootnoteOptions()->set_Columns(2);
doc->Save(get_ArtifactsDir() + u"Document.FootnoteColumns.docx");
```


يعرض كيفية اختيار مكان مختلف حيث يجمع المستند ويعرض الحواشي الخاصة به.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// الحاشية هي طريقة لإرفاق مرجع أو تعليق جانبي بالنص
// الذي لا يتداخل مع تدفق نص الجسم الرئيسي.
// إدراج حاشية يضيف رمز مرجع صغير مرتفع
// في نص الجسم الرئيسي حيث نقوم بإدراج الحاشية.
// كل حاشية تنشئ أيضًا مدخلاً في أسفل الصفحة، يتكون من رمز
// يتطابق مع رمز الإشارة في نص الجسم الرئيسي.
// نص المرجع الذي نمرره إلى طريقة "InsertFootnote" في مُنشئ المستند.
builder->Write(u"Hello world!");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote contents.");

// يمكننا استخدام الخاصية "Position" لتحديد المكان الذي سيضع فيه المستند جميع حواشيه.
// إذا قمنا بتعيين قيمة الخاصية "Position" إلى "FootnotePosition.BottomOfPage",
// ستظهر كل حاشية في أسفل الصفحة التي تحتوي على علامة مرجعها. هذه هي القيمة الافتراضية.
// إذا قمنا بتعيين قيمة الخاصية "Position" إلى "FootnotePosition.BeneathText",
// ستظهر كل حاشية في نهاية نص الصفحة الذي يحتوي على علامة مرجعها.
doc->get_FootnoteOptions()->set_Position(footnotePosition);

doc->Save(get_ArtifactsDir() + u"InlineStory.PositionFootnote.docx");
```


يعرض كيفية تغيير نمط رقم علامات مرجع الحاشية/الحاشية الختامية.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// الحواشي والحواشي الختامية هي طريقة لإرفاق مرجع أو تعليق جانبي بالنص
// الذي لا يتداخل مع تدفق نص الجسم الرئيسي.
// إدراج حاشية/حاشية ختامية يضيف رمز مرجع صغير مرتفع
// في نص الجسم الرئيسي حيث نقوم بإدراج الحاشية/الحاشية الختامية.
// كل حاشية/حاشية ختامية تنشئ أيضًا مدخلاً يتكون من رمز يطابق المرجع
// الرمز في نص الجسم الرئيسي. نص المرجع الذي نمرره إلى طريقة "InsertEndnote" في مُنشئ المستند.
// مدخلات الحواشي، بشكل افتراضي، تظهر في أسفل كل صفحة تحتوي على
// رموز مرجعها، وتظهر الحواشي الختامية في نهاية المستند.
builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 2.");
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 3.", u"Custom footnote reference mark");

builder->InsertParagraph();

builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 2.");
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 3.", u"Custom endnote reference mark");

// بشكل افتراضي، رمز المرجع لكل حاشية وحاشية ختامية هو فهرسها
// بين جميع حواشي/حواشي المستند. كل مستند يحتفظ بعدّات منفصلة
// للحواشي وللحواشي الختامية. بشكل افتراضي، تعرض الحواشي أرقامها باستخدام الأرقام العربية،
// وتعرض الحواشي الختامية أرقامها بالأحرف الرومانية الصغيرة.
ASSERT_EQ(Aspose::Words::NumberStyle::Arabic, doc->get_FootnoteOptions()->get_NumberStyle());
ASSERT_EQ(Aspose::Words::NumberStyle::LowercaseRoman, doc->get_EndnoteOptions()->get_NumberStyle());

// يمكننا استخدام الخاصية "NumberStyle" لتطبيق أنماط ترقيم مخصصة على الحواشي والحواشي الختامية.
// هذا لن يؤثر على الحواشي/الحواشي الختامية ذات علامات مرجع مخصصة.
doc->get_FootnoteOptions()->set_NumberStyle(Aspose::Words::NumberStyle::UppercaseRoman);
doc->get_EndnoteOptions()->set_NumberStyle(Aspose::Words::NumberStyle::UppercaseLetter);

doc->Save(get_ArtifactsDir() + u"InlineStory.RefMarkNumberStyle.docx");
```


يظهر كيفية إعادة تشغيل ترقيم footnote/endnote في أماكن معينة داخل المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// الحواشي والحواشي الختامية هي طريقة لإرفاق مرجع أو تعليق جانبي بالنص
// الذي لا يتداخل مع تدفق نص الجسم الرئيسي.
// إدراج حاشية/حاشية ختامية يضيف رمز مرجع صغير مرتفع
// في نص الجسم الرئيسي حيث نقوم بإدراج الحاشية/الحاشية الختامية.
// كل حاشية/حاشية ختامية تنشئ أيضًا مدخلاً يتكون من رمز يطابق المرجع
// الرمز في نص الجسم الرئيسي. نص المرجع الذي نمرره إلى طريقة "InsertEndnote" في مُنشئ المستند.
// مدخلات الحواشي، بشكل افتراضي، تظهر في أسفل كل صفحة تحتوي على
// رموز مرجعها، وتظهر الحواشي الختامية في نهاية المستند.
builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 3.");
builder->Write(u"Text 4. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 4.");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 2.");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 3.");
builder->Write(u"Text 4. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 4.");

// بشكل افتراضي، رمز المرجع لكل حاشية وحاشية ختامية هو فهرسها
// بين جميع حواشي/حواشي المستند. كل مستند يحتفظ بعدّات منفصلة
// لـ footnotes و endnotes ولا يعيد تشغيل هذه العدادات في أي نقطة.
ASSERT_EQ(doc->get_FootnoteOptions()->get_RestartRule(), Aspose::Words::Notes::FootnoteNumberingRule::Default);
ASSERT_EQ(Aspose::Words::Notes::FootnoteNumberingRule::Default, Aspose::Words::Notes::FootnoteNumberingRule::Continuous);

// يمكننا استخدام الخاصية "RestartRule" لجعل المستند يعيد التشغيل
// عدد footnote/endnote عند صفحة جديدة أو قسم.
doc->get_FootnoteOptions()->set_RestartRule(Aspose::Words::Notes::FootnoteNumberingRule::RestartPage);
doc->get_EndnoteOptions()->set_RestartRule(Aspose::Words::Notes::FootnoteNumberingRule::RestartSection);

doc->Save(get_ArtifactsDir() + u"InlineStory.NumberingRule.docx");
```


يظهر كيفية تعيين رقم يبدأ عنده المستند عدّ footnote/endnote.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// الحواشي والحواشي الختامية هي طريقة لإرفاق مرجع أو تعليق جانبي بالنص
// الذي لا يتداخل مع تدفق نص الجسم الرئيسي.
// إدراج حاشية/حاشية ختامية يضيف رمز مرجع صغير مرتفع
// في نص الجسم الرئيسي حيث نقوم بإدراج الحاشية/الحاشية الختامية.
// كل footnote/endnote ينشئ أيضًا مدخلاً يتكون من رمز
// يتطابق مع رمز الإشارة في نص الجسم الرئيسي.
// نص الإشارة الذي نمرره إلى طريقة "InsertEndnote" الخاصة بمنشئ المستند.
// مدخلات الحواشي، بشكل افتراضي، تظهر في أسفل كل صفحة تحتوي على
// رموز مرجعها، وتظهر الحواشي الختامية في نهاية المستند.
builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 2.");
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 3.");

builder->InsertParagraph();

builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 2.");
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 3.");

// بشكل افتراضي، رمز المرجع لكل حاشية وحاشية ختامية هو فهرسها
// بين جميع حواشي/حواشي المستند. كل مستند يحتفظ بعدّات منفصلة
// لـ footnotes و لـ endnotes، حيث يبدأ كل منهما من 1.
ASSERT_EQ(1, doc->get_FootnoteOptions()->get_StartNumber());
ASSERT_EQ(1, doc->get_EndnoteOptions()->get_StartNumber());

// يمكننا استخدام الخاصية "StartNumber" لجعل المستند يـ
// يبدأ عدّ footnote أو endnote برقم مختلف.
doc->get_EndnoteOptions()->set_NumberStyle(Aspose::Words::NumberStyle::Arabic);
doc->get_EndnoteOptions()->set_StartNumber(50);

doc->Save(get_ArtifactsDir() + u"InlineStory.StartNumber.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words::Notes](../)
* Library [Aspose.Words for C++](../../)
