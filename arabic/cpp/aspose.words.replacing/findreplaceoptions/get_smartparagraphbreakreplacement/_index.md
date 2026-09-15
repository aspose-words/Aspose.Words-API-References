---
title: "طريقة Aspose::Words::Replacing::FindReplaceOptions::get_SmartParagraphBreakReplacement"
linktitle: "get_SmartParagraphBreakReplacement"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Replacing::FindReplaceOptions::get_SmartParagraphBreakReplacement. يحصل على أو يضبط قيمة منطقية تشير إلى ما إذا كان مسموحًا باستبدال فاصل الفقرة عندما لا يوجد فقرة شقيقة تالٍ. القيمة الافتراضية هي false في C++."
type: docs
weight: 16000
url: /ar/cpp/aspose.words.replacing/findreplaceoptions/get_smartparagraphbreakreplacement/
---
## FindReplaceOptions::get_SmartParagraphBreakReplacement method


يحصل أو يعيّن قيمة منطقية تشير إلى ما إذا كان مسموحًا باستبدال فاصل الفقرة عندما لا يوجد فقرة شقيقة تالٍ. القيمة الافتراضية هي **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_SmartParagraphBreakReplacement() const
```


## أمثلة



يوضح كيفية إزالة الفقرة من خلية جدول تحتوي على جدول متداخل.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// إنشاء جدول يحتوي على فقرة وجدول داخلي في الخلية الأولى.
builder->StartTable();
builder->InsertCell();
builder->Write(u"TEXT1");
builder->StartTable();
builder->InsertCell();
builder->EndTable();
builder->EndTable();
builder->Writeln();

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
// عند ضبط الخيار التالي على 'true'، سيقوم Aspose.Words بإزالة نص الفقرة
// كليًا مع علامة الفقرة الخاصة بها. وإلا، سيحاكي Aspose.Words برنامج Word ويزيل
// نص الفقرة فقط ويترك علامة الفقرة دون تغيير (عند وجود جدول بعد النص).
options->set_SmartParagraphBreakReplacement(isSmartParagraphBreakReplacement);
doc->get_Range()->Replace(System::MakeObject<System::Text::RegularExpressions::Regex>(u"TEXT1&p"), u"", options);

doc->Save(get_ArtifactsDir() + u"Table.RemoveParagraphTextAndMark.docx");
```

## انظر أيضًا

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
