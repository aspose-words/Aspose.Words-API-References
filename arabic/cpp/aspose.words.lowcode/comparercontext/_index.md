---
title: "فئة Aspose::Words::LowCode::ComparerContext"
linktitle: "ComparerContext"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::LowCode::ComparerContext. سياق مقارنة المستندات في C++."
type: docs
weight: 550
url: /ar/cpp/aspose.words.lowcode/comparercontext/
---
## ComparerContext class


[Document](../../aspose.words/document/) comparer context.

```cpp
class ComparerContext : public Aspose::Words::LowCode::ProcessorContext
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [ComparerContext](./comparercontext/)() |  |
| [get_AcceptRevisions](./get_acceptrevisions/)() const | يشير إلى ما إذا كان يجب قبول المراجعات في المستندات قبل مقارنتها. إذا كانت المستندات المقارنة تحتوي على مراجعات وتم تعيين هذه العلامة إلى false، فسيقوم المعالج برفض المراجعات. القيمة الافتراضية هي **true**. |
| [get_Author](./get_author/)() const | المؤلف الذي سيتم تعيينه للمراجعات التي تم إنشاؤها أثناء مقارنة المستندات. |
| [get_CompareOptions](./get_compareoptions/)() const | الخيارات المستخدمة عند مقارنة المستندات. |
| [get_DateTime](./get_datetime/)() const | التاريخ والوقت المعين للمراجعات التي تم إنشاؤها أثناء مقارنة المستندات. |
| [get_FontSettings](../processorcontext/get_fontsettings/)() const | إعدادات [الخط](../../aspose.words/font/) المستخدمة بواسطة المعالج. |
| [get_LayoutOptions](../processorcontext/get_layoutoptions/)() const | خيارات تخطيط [المستند](../../aspose.words/document/) المستخدمة بواسطة المعالج. |
| [get_WarningCallback](../processorcontext/get_warningcallback/)() const | استدعاء التحذير المستخدم بواسطة المعالج. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ProcessorContext](../processorcontext/processorcontext/)() |  |
| [set_AcceptRevisions](./set_acceptrevisions/)(bool) | يشير إلى ما إذا كان يجب قبول المراجعات في المستندات قبل مقارنتها. إذا كانت المستندات المقارنة تحتوي على مراجعات وتم تعيين هذه العلامة إلى false، فسيقوم المعالج برفض المراجعات. القيمة الافتراضية هي **true**. |
| [set_Author](./set_author/)(const System::String\&) | المؤلف الذي سيتم تعيينه للمراجعات التي تم إنشاؤها أثناء مقارنة المستندات. |
| [set_DateTime](./set_datetime/)(System::DateTime) | التاريخ والوقت المعين للمراجعات التي تم إنشاؤها أثناء مقارنة المستندات. |
| [set_FontSettings](../processorcontext/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | إعدادات [الخط](../../aspose.words/font/) المستخدمة بواسطة المعالج. |
| [set_WarningCallback](../processorcontext/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | استدعاء التحذير المستخدم بواسطة المعالج. |
| static [Type](./type/)() |  |
## انظر أيضًا

* Class [ProcessorContext](../processorcontext/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
