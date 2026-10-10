---
title: "Aspose::Words::Notes::Footnote::get_FootnoteType method"
linktitle: "get_FootnoteType"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Notes::Footnote::get_FootnoteType method. تُرجع قيمة تحدد ما إذا كان هذا حاشية سفلية أو حاشية نهائية في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.notes/footnote/get_footnotetype/
---
## Footnote::get_FootnoteType method


يرجع قيمة تحدد ما إذا كان هذا هو هامش سفلي أم هامش نهائي.

```cpp
Aspose::Words::Notes::FootnoteType Aspose::Words::Notes::Footnote::get_FootnoteType() const
```


## أمثلة



يعرض الفرق بين الحواشي السفلية والحواشي النهائية.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// فيما يلي طريقتان لإرفاق مراجع مرقمة بالنص. كلا هذين المرجعين سيضيفان
// علامة مرجع مرتفعة صغيرة في الموقع الذي نُدرجها فيه.
// علامة المرجع، بشكل افتراضي، هي رقم الفهرس للمرجع بين جميع المراجع في المستند.
// كل مرجع سيُنشئ أيضًا إدخالًا، سيكون له نفس علامة المرجع كما في نص الجسم
// ونص المرجع، الذي سنمرره إلى طريقة "InsertFootnote" الخاصة بمنشئ المستند.
// 1 -  حاشية سفلية، سيظهر إدخالها في نفس الصفحة التي يظهر فيها النص الذي تشير إليه:
builder->Write(u"Footnote referenced main body text.");
System::SharedPtr<Aspose::Words::Notes::Footnote> footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text, will appear at the bottom of the page that contains the referenced text.");

// 2 -  حاشية نهائية، سيظهر مدخلها في نهاية المستند:
builder->Write(u"Endnote referenced main body text.");
System::SharedPtr<Aspose::Words::Notes::Footnote> endnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote text, will appear at the very end of the document.");

builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

ASSERT_EQ(Aspose::Words::Notes::FootnoteType::Footnote, footnote->get_FootnoteType());
ASSERT_EQ(Aspose::Words::Notes::FootnoteType::Endnote, endnote->get_FootnoteType());

doc->Save(get_ArtifactsDir() + u"InlineStory.FootnoteEndnote.docx");
```

## انظر أيضًا

* Enum [FootnoteType](../../footnotetype/)
* Class [Footnote](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
