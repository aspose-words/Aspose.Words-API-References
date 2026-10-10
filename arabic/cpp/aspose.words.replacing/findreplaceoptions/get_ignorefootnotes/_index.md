---
title: "طريقة Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFootnotes"
linktitle: "get_IgnoreFootnotes"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFootnotes method. يحصل أو يضبط قيمة منطقية تشير إلى ما إذا كان يجب تجاهل الحواشي السفلية. القيمة الافتراضية هي false في C++."
type: docs
weight: 10000
url: /ar/cpp/aspose.words.replacing/findreplaceoptions/get_ignorefootnotes/
---
## FindReplaceOptions::get_IgnoreFootnotes method


يحصل أو يعيّن قيمة منطقية تشير إلى ما إذا كان يجب تجاهل الحواشي السفلية. القيمة الافتراضية هي **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFootnotes() const
```


## أمثلة



يوضح كيفية تجاهل الحواشي السفلية أثناء عملية البحث والاستبدال.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

builder->InsertParagraph();

builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

// قم بتعيين العلامة "IgnoreFootnotes" إلى "true" للحصول على عملية البحث والاستبدال
// العملية لتجاهل النص داخل الحواشي السفلية.
// قم بتعيين العلامة "IgnoreFootnotes" إلى "false" للحصول على عملية البحث والاستبدال
// العملية للبحث أيضًا عن النص داخل الحواشي السفلية.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_IgnoreFootnotes(isIgnoreFootnotes);
doc->get_Range()->Replace(u"Lorem ipsum", u"Replaced Lorem ipsum", options);
```

## انظر أيضًا

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
