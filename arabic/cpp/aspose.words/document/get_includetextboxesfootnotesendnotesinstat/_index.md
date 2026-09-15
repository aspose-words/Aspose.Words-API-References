---
title: "طريقة Aspose::Words::Document::get_IncludeTextboxesFootnotesEndnotesInStat"
linktitle: "get_IncludeTextboxesFootnotesEndnotesInStat"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Document::get_IncludeTextboxesFootnotesEndnotesInStat. تحدد ما إذا كان يجب تضمين مربعات النص، الحواشي السفلية والنهائية في إحصاءات عدد الكلمات في C++."
type: docs
weight: 33000
url: /ar/cpp/aspose.words/document/get_includetextboxesfootnotesendnotesinstat/
---
## Document::get_IncludeTextboxesFootnotesEndnotesInStat method


يحدد ما إذا كان يجب تضمين مربعات النص والحواشي السفلية والختامية في إحصاءات عدد الكلمات.

```cpp
bool Aspose::Words::Document::get_IncludeTextboxesFootnotesEndnotesInStat()
```


## أمثلة



يظهر كيفية تضمين أو استبعاد مربعات النص، الحواشي السفلية والنهائية من إحصاءات عدد الكلمات.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Lorem ipsum");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"sit amet");

// بشكل افتراضي يتم تعيين الخيار إلى 'false'.
doc->UpdateWordCount();
// عدد الكلمات بدون مربعات النص، الحواشي السفلية والنهائية.
ASSERT_EQ(2, doc->get_BuiltInDocumentProperties()->get_Words());

doc->set_IncludeTextboxesFootnotesEndnotesInStat(true);
doc->UpdateWordCount();
// عدد الكلمات مع مربعات النص، الحواشي السفلية والنهائية.
ASSERT_EQ(4, doc->get_BuiltInDocumentProperties()->get_Words());
```

## انظر أيضًا

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
