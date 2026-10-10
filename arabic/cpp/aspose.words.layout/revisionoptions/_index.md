---
title: "Aspose::Words::Layout::RevisionOptions فئة"
linktitle: "RevisionOptions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Layout::RevisionOptions فئة. يسمح بالتحكم في كيفية معالجة مراجعات المستند أثناء عملية التخطيط. لمعرفة المزيد، قم بزيارة مقالة الوثائق في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.layout/revisionoptions/
---
## RevisionOptions class


يسمح بالتحكم في كيفية معالجة مراجعات المستند أثناء عملية التخطيط. لمعرفة المزيد، قم بزيارة مقالة الوثائق [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/).

```cpp
class RevisionOptions : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_CommentColor](./get_commentcolor/)() const | يسمح بتحديد اللون المستخدم للتعليقات. القيمة الافتراضية هي [Red](../revisioncolor/). |
| [get_DeleteCellColor](./get_deletecellcolor/)() | يسمح بتحديد اللون المستخدم للخلايا المحذوفة [Deletion](../../aspose.words/revisiontype/). القيمة الافتراضية هي [Pink](../revisioncolor/). |
| [get_DeletedTextColor](./get_deletedtextcolor/)() | يسمح بتحديد اللون المستخدم للمحتوى المحذوف [Deletion](../../aspose.words/revisiontype/). القيمة الافتراضية هي [ByAuthor](../revisioncolor/). |
| [get_DeletedTextEffect](./get_deletedtexteffect/)() | يسمح بتحديد التأثير الذي سيُطبق على المحتوى المحذوف [Deletion](../../aspose.words/revisiontype/). القيمة الافتراضية هي [StrikeThrough](../revisiontexteffect/) |
| [get_InsertCellColor](./get_insertcellcolor/)() | يسمح بتحديد اللون المستخدم للخلايا المُدرجة [Insertion](../../aspose.words/revisiontype/). القيمة الافتراضية هي [Blue](../revisioncolor/). |
| [get_InsertedTextColor](./get_insertedtextcolor/)() | يسمح بتحديد اللون المستخدم للمحتوى المُدرج [Insertion](../../aspose.words/revisiontype/). القيمة الافتراضية هي [ByAuthor](../revisioncolor/). |
| [get_InsertedTextEffect](./get_insertedtexteffect/)() | يسمح بتحديد التأثير الذي سيُطبق على المحتوى المُدرج [Insertion](../../aspose.words/revisiontype/). القيمة الافتراضية هي [Underline](../revisiontexteffect/). |
| [get_MeasurementUnit](./get_measurementunit/)() const | يسمح بتحديد وحدات القياس لتعليقات المراجعة. القيمة الافتراضية هي [Centimeters](../../aspose.words/measurementunits/) |
| [get_MovedFromTextColor](./get_movedfromtextcolor/)() | يسمح بتحديد اللون المستخدم للمناطق التي تم نقل المحتوى منها [Moving](../../aspose.words/revisiontype/). القيمة الافتراضية هي [ByAuthor](../revisioncolor/). |
| [get_MovedFromTextEffect](./get_movedfromtexteffect/)() | يسمح بتحديد التأثير الذي سيُطبق على المناطق التي تم نقل المحتوى منها [Moving](../../aspose.words/revisiontype/). القيمة الافتراضية هي [DoubleStrikeThrough](../revisiontexteffect/) |
| [get_MovedToTextColor](./get_movedtotextcolor/)() | يسمح بتحديد اللون المستخدم للمناطق التي تم نقل المحتوى إليها [Moving](../../aspose.words/revisiontype/). القيمة الافتراضية هي [ByAuthor](../revisioncolor/). |
| [get_MovedToTextEffect](./get_movedtotexteffect/)() | يسمح بتحديد التأثير الذي سيُطبق على المناطق التي تم نقل المحتوى إليها [Moving](../../aspose.words/revisiontype/). القيمة الافتراضية هي [DoubleUnderline](../revisiontexteffect/) |
| [get_RevisedPropertiesColor](./get_revisedpropertiescolor/)() | يسمح بتحديد اللون المستخدم للمحتوى الذي يحتوي على تغييرات في خصائص التنسيق [FormatChange](../../aspose.words/revisiontype/) القيمة الافتراضية هي [NoHighlight](../revisioncolor/). |
| [get_RevisedPropertiesEffect](./get_revisedpropertieseffect/)() | يسمح بتحديد التأثير لمناطق المحتوى التي تحتوي على تغييرات في خصائص التنسيق [FormatChange](../../aspose.words/revisiontype/) القيمة الافتراضية هي [None](../revisiontexteffect/) |
| [get_RevisionBarsColor](./get_revisionbarscolor/)() const | يسمح بتحديد اللون المستخدم للأشرطة الجانبية التي تحدد سطور المستند التي تحتوي على معلومات مُراجعة. القيمة الافتراضية هي [Red](../revisioncolor/). |
| [get_RevisionBarsPosition](./get_revisionbarsposition/)() const | يحصل أو يضبط موضع عرض أشرطة المراجعة. القيمة الافتراضية هي [Outside](../../aspose.words.drawing/horizontalalignment/). |
| [get_RevisionBarsWidth](./get_revisionbarswidth/)() const | يحصل أو يضبط عرض أشرطة المراجعة، بالنقاط. |
| [get_ShowInBalloons](./get_showinballoons/)() const | يسمح بتحديد ما إذا كانت المراجعات تُعرض في الفقاعات. القيمة الافتراضية هي [None](../showinballoons/). |
| [get_ShowOriginalRevision](./get_showoriginalrevision/)() const | يسمح بتحديد ما إذا كان يجب إظهار النص الأصلي بدلاً من النص المُراجع. القيمة الافتراضية هي **false**. |
| [get_ShowRevisionBars](./get_showrevisionbars/)() const | يسمح بتحديد ما إذا كان يجب عرض أشرطة المراجعة بالقرب من السطور التي تحتوي على محتوى مُراجع. القيمة الافتراضية هي **true**. |
| [get_ShowRevisionMarks](./get_showrevisionmarks/)() const | السماح بتحديد ما إذا كان يجب وضع علامة على نص المراجعة بتنسيق خاص. القيمة الافتراضية هي **true**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CommentColor](./set_commentcolor/)(Aspose::Words::Layout::RevisionColor) | دالة ضبط لـ [Aspose::Words::Layout::RevisionOptions::get_CommentColor](./get_commentcolor/). |
| [set_DeleteCellColor](./set_deletecellcolor/)(Aspose::Words::Layout::RevisionColor) | محدد لـ [Aspose::Words::Layout::RevisionOptions::get_DeleteCellColor](./get_deletecellcolor/). |
| [set_DeletedTextColor](./set_deletedtextcolor/)(Aspose::Words::Layout::RevisionColor) | محدد لـ [Aspose::Words::Layout::RevisionOptions::get_DeletedTextColor](./get_deletedtextcolor/). |
| [set_DeletedTextEffect](./set_deletedtexteffect/)(Aspose::Words::Layout::RevisionTextEffect) | محدد لـ [Aspose::Words::Layout::RevisionOptions::get_DeletedTextEffect](./get_deletedtexteffect/). |
| [set_InsertCellColor](./set_insertcellcolor/)(Aspose::Words::Layout::RevisionColor) | محدد لـ [Aspose::Words::Layout::RevisionOptions::get_InsertCellColor](./get_insertcellcolor/). |
| [set_InsertedTextColor](./set_insertedtextcolor/)(Aspose::Words::Layout::RevisionColor) | محدد لـ [Aspose::Words::Layout::RevisionOptions::get_InsertedTextColor](./get_insertedtextcolor/). |
| [set_InsertedTextEffect](./set_insertedtexteffect/)(Aspose::Words::Layout::RevisionTextEffect) | محدد لـ [Aspose::Words::Layout::RevisionOptions::get_InsertedTextEffect](./get_insertedtexteffect/). |
| [set_MeasurementUnit](./set_measurementunit/)(Aspose::Words::MeasurementUnits) | يسمح بتحديد وحدات القياس لتعليقات المراجعة. القيمة الافتراضية هي [Centimeters](../../aspose.words/measurementunits/) |
| [set_MovedFromTextColor](./set_movedfromtextcolor/)(Aspose::Words::Layout::RevisionColor) | محدد لـ [Aspose::Words::Layout::RevisionOptions::get_MovedFromTextColor](./get_movedfromtextcolor/). |
| [set_MovedFromTextEffect](./set_movedfromtexteffect/)(Aspose::Words::Layout::RevisionTextEffect) | محدد لـ [Aspose::Words::Layout::RevisionOptions::get_MovedFromTextEffect](./get_movedfromtexteffect/). |
| [set_MovedToTextColor](./set_movedtotextcolor/)(Aspose::Words::Layout::RevisionColor) | محدد لـ [Aspose::Words::Layout::RevisionOptions::get_MovedToTextColor](./get_movedtotextcolor/). |
| [set_MovedToTextEffect](./set_movedtotexteffect/)(Aspose::Words::Layout::RevisionTextEffect) | محدد لـ [Aspose::Words::Layout::RevisionOptions::get_MovedToTextEffect](./get_movedtotexteffect/). |
| [set_RevisedPropertiesColor](./set_revisedpropertiescolor/)(Aspose::Words::Layout::RevisionColor) | محدد لـ [Aspose::Words::Layout::RevisionOptions::get_RevisedPropertiesColor](./get_revisedpropertiescolor/). |
| [set_RevisedPropertiesEffect](./set_revisedpropertieseffect/)(Aspose::Words::Layout::RevisionTextEffect) | محدد لـ [Aspose::Words::Layout::RevisionOptions::get_RevisedPropertiesEffect](./get_revisedpropertieseffect/). |
| [set_RevisionBarsColor](./set_revisionbarscolor/)(Aspose::Words::Layout::RevisionColor) | محدد لـ [Aspose::Words::Layout::RevisionOptions::get_RevisionBarsColor](./get_revisionbarscolor/). |
| [set_RevisionBarsPosition](./set_revisionbarsposition/)(Aspose::Words::Drawing::HorizontalAlignment) | محدد لـ [Aspose::Words::Layout::RevisionOptions::get_RevisionBarsPosition](./get_revisionbarsposition/). |
| [set_RevisionBarsWidth](./set_revisionbarswidth/)(float) | محدد لـ [Aspose::Words::Layout::RevisionOptions::get_RevisionBarsWidth](./get_revisionbarswidth/). |
| [set_ShowInBalloons](./set_showinballoons/)(Aspose::Words::Layout::ShowInBalloons) | محدد لـ [Aspose::Words::Layout::RevisionOptions::get_ShowInBalloons](./get_showinballoons/). |
| [set_ShowOriginalRevision](./set_showoriginalrevision/)(bool) | محدد لـ [Aspose::Words::Layout::RevisionOptions::get_ShowOriginalRevision](./get_showoriginalrevision/). |
| [set_ShowRevisionBars](./set_showrevisionbars/)(bool) | محدد لـ [Aspose::Words::Layout::RevisionOptions::get_ShowRevisionBars](./get_showrevisionbars/). |
| [set_ShowRevisionMarks](./set_showrevisionmarks/)(bool) | محدد لـ [Aspose::Words::Layout::RevisionOptions::get_ShowRevisionMarks](./get_showrevisionmarks/). |
| static [Type](./type/)() |  |

## أمثلة



يظهر كيفية تعديل مظهر المراجعات في مستند الإخراج المرسوم.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدرج مراجعة، ثم غيّر لون جميع المراجعات إلى الأخضر.
builder->Writeln(u"This is not a revision.");
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());
builder->Writeln(u"This is a revision.");
doc->StopTrackRevisions();
builder->Writeln(u"This is not a revision.");

// أزل الشريط الذي يظهر إلى يسار كل سطر مُراجَع.
doc->get_LayoutOptions()->get_RevisionOptions()->set_InsertedTextColor(Aspose::Words::Layout::RevisionColor::BrightGreen);
doc->get_LayoutOptions()->get_RevisionOptions()->set_ShowRevisionBars(false);
doc->get_LayoutOptions()->get_RevisionOptions()->set_RevisionBarsPosition(Aspose::Words::Drawing::HorizontalAlignment::Right);

doc->Save(get_ArtifactsDir() + u"Revision.LayoutOptionsRevisions.pdf");
```

## انظر أيضًا

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
