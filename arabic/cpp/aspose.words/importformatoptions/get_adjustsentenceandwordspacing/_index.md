---
title: "Aspose::Words::ImportFormatOptions::get_AdjustSentenceAndWordSpacing طريقة"
linktitle: "get_AdjustSentenceAndWordSpacing"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::ImportFormatOptions::get_AdjustSentenceAndWordSpacing طريقة. يحصل أو يضبط قيمة منطقية تحدد ما إذا كان سيتم تعديل تباعد الجمل والكلمات تلقائيًا. القيمة الافتراضية هي false في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words/importformatoptions/get_adjustsentenceandwordspacing/
---
## ImportFormatOptions::get_AdjustSentenceAndWordSpacing method


يحصل أو يضبط قيمة منطقية تحدد ما إذا كان يجب تعديل تباعد الجمل والكلمات تلقائيًا. القيمة الافتراضية هي **false**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_AdjustSentenceAndWordSpacing() const
```


## أمثلة



يوضح كيفية تعديل تباعد الجمل والكلمات تلقائيًا.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
auto dstDoc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(srcDoc);
builder->Write(u"Dolor sit amet.");

builder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);
builder->Write(u"Lorem ipsum.");

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_AdjustSentenceAndWordSpacing(true);
builder->InsertDocument(srcDoc, Aspose::Words::ImportFormatMode::UseDestinationStyles, options);

ASSERT_EQ(u"Lorem ipsum. Dolor sit amet.", dstDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());
```

## انظر أيضًا

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
