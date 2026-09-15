---
title: "فئة Aspose::Words::Layout::LayoutOptions"
linktitle: "LayoutOptions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Layout::LayoutOptions. تحتوي على الخيارات التي تسمح بالتحكم في عملية تخطيط المستند. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.layout/layoutoptions/
---
## LayoutOptions class


يحتوي على الخيارات التي تسمح بالتحكم في عملية تخطيط المستند. لمعرفة المزيد، قم بزيارة مقالة الوثائق [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/).

```cpp
class LayoutOptions : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_Callback](./get_callback/)() const | يحصل على تنفيذ [IPageLayoutCallback](../ipagelayoutcallback/) المستخدم من قبل نموذج تخطيط الصفحة. |
| [get_CommentDisplayMode](./get_commentdisplaymode/)() const | يحصل أو يعيّن طريقة عرض التعليقات. القيمة الافتراضية هي [ShowInBalloons](../commentdisplaymode/). |
| [get_ContinuousSectionPageNumberingRestart](./get_continuoussectionpagenumberingrestart/)() const | يحصل أو يعيّن وضع السلوك لحساب أرقام الصفحات عندما يعيد قسم متواصل ترقيم الصفحات. |
| [get_IgnorePrinterMetrics](./get_ignoreprintermetrics/)() const | يحصل أو يعيّن إشارة ما إذا كان خيار التوافق "استخدام مقاييس الطابعة لتنسيق المستند" يتم تجاهله. القيمة الافتراضية هي **true**. |
| [get_KeepOriginalFontMetrics](./get_keeporiginalfontmetrics/)() const | يحصل أو يعيّن إشارة ما إذا كان يجب استخدام مقاييس الخط الأصلية بعد استبدال الخط. القيمة الافتراضية هي **true**. |
| [get_RevisionOptions](./get_revisionoptions/)() const | يحصل على خيارات المراجعة. |
| [get_ShowHiddenText](./get_showhiddentext/)() const | يحصل أو يعيّن إشارة ما إذا كان النص المخفي في المستند يتم عرضه. القيمة الافتراضية هي **false**. |
| [get_ShowParagraphMarks](./get_showparagraphmarks/)() const | يحصل أو يعيّن إشارة ما إذا كانت علامات الفقرات تُعرض. القيمة الافتراضية هي **false**. |
| [get_TextShaperFactory](./get_textshaperfactory/)() const | يحصل على تنفيذ [ITextShaperFactory](../) المستخدم لميزات عرض الطباعة المتقدمة. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LayoutOptions](./layoutoptions/)() |  |
| [set_Callback](./set_callback/)(const System::SharedPtr\<Aspose::Words::Layout::IPageLayoutCallback\>\&) | يعيّن تنفيذ [IPageLayoutCallback](../ipagelayoutcallback/) المستخدم من قبل نموذج تخطيط الصفحة. |
| [set_CommentDisplayMode](./set_commentdisplaymode/)(Aspose::Words::Layout::CommentDisplayMode) | محدد لـ [Aspose::Words::Layout::LayoutOptions::get_CommentDisplayMode](./get_commentdisplaymode/). |
| [set_ContinuousSectionPageNumberingRestart](./set_continuoussectionpagenumberingrestart/)(Aspose::Words::Layout::ContinuousSectionRestart) | محدد لـ [Aspose::Words::Layout::LayoutOptions::get_ContinuousSectionPageNumberingRestart](./get_continuoussectionpagenumberingrestart/). |
| [set_IgnorePrinterMetrics](./set_ignoreprintermetrics/)(bool) | محدد لـ [Aspose::Words::Layout::LayoutOptions::get_IgnorePrinterMetrics](./get_ignoreprintermetrics/). |
| [set_KeepOriginalFontMetrics](./set_keeporiginalfontmetrics/)(bool) | محدد لـ [Aspose::Words::Layout::LayoutOptions::get_KeepOriginalFontMetrics](./get_keeporiginalfontmetrics/). |
| [set_ShowHiddenText](./set_showhiddentext/)(bool) | محدد لـ [Aspose::Words::Layout::LayoutOptions::get_ShowHiddenText](./get_showhiddentext/). |
| [set_ShowParagraphMarks](./set_showparagraphmarks/)(bool) | محدد لـ [Aspose::Words::Layout::LayoutOptions::get_ShowParagraphMarks](./get_showparagraphmarks/). |
| [set_TextShaperFactory](./set_textshaperfactory/)(const System::SharedPtr\<Aspose::Words::Shaping::ITextShaperFactory\>\&) | يعيّن تنفيذ [ITextShaperFactory](../) المستخدم لميزات عرض الطباعة المتقدمة. |
| static [Type](./type/)() |  |
## ملاحظات


لا تقوم بإنشاء مثيلات من هذه الفئة مباشرة. استخدم الخاصية [LayoutOptions](../../aspose.words/document/get_layoutoptions/) للوصول إلى خيارات التخطيط لهذا المستند.

لاحظ أنه بعد تغيير أي من الخيارات الموجودة في هذه الفئة، يجب استدعاء الطريقة [UpdatePageLayout](../../aspose.words/document/updatepagelayout/) لتطبيق الخيارات المتغيّرة على التخطيط.

## أمثلة



يظهر كيفية إخفاء النص في مستند الإخراج المرسوم.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدرج نصًا مخفيًا، ثم حدد ما إذا كنا نرغب في حذفه من المستند المرسوم.
builder->Writeln(u"This text is not hidden.");
builder->get_Font()->set_Hidden(true);
builder->Writeln(u"This text is hidden.");

doc->get_LayoutOptions()->set_ShowHiddenText(showHiddenText);

doc->Save(get_ArtifactsDir() + u"Document.LayoutOptionsHiddenText.pdf");
```


يظهر كيفية إظهار علامات الفقرات في مستند الإخراج المرسوم.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أضف بعض الفقرات، ثم فعّل علامات الفقرات لإظهار نهايات الفقرات
// مع رمز الفقرة (¶) عند رسم المستند.
builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

doc->get_LayoutOptions()->set_ShowParagraphMarks(showParagraphMarks);

doc->Save(get_ArtifactsDir() + u"Document.LayoutOptionsParagraphMarks.pdf");
```


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
