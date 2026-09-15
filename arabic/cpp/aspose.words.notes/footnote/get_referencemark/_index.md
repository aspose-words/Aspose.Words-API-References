---
title: "Aspose::Words::Notes::Footnote::get_ReferenceMark method"
linktitle: "get_ReferenceMark"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Notes::Footnote::get_ReferenceMark. تحصل/تضبط علامة الإشارة المخصصة المستخدمة لهذه الحاشية السفلية. القيمة الافتراضية هي **empty string**، مما يعني أن الحواشي المرقمة تلقائيًا تُستخدم في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words.notes/footnote/get_referencemark/
---
## Footnote::get_ReferenceMark method


يحصل/يضبط علامة الإشارة المخصصة التي ستُستخدم لهذا الهامش السفلي. القيمة الافتراضية هي **empty string**، مما يعني استخدام الهوامش السفلية المرقمة تلقائيًا.

```cpp
System::String Aspose::Words::Notes::Footnote::get_ReferenceMark() const
```

## ملاحظات


إذا تم تعيين هذه الخاصية إلى **empty string** أو **null**، فسيتم ضبط الخاصية [IsAuto](../get_isauto/) تلقائيًا إلى **true**، وإذا تم تعيينها إلى أي قيمة أخرى فستُضبط الخاصية [IsAuto](../get_isauto/) إلى **false**.

يمكن لتنسيق RTF أن يخزن رمزًا واحدًا فقط كعلامة إشارة مخصصة، لذا عند التصدير سيُكتب الرمز الأول فقط وسيتم تجاهل البقية.

## أمثلة



يوضح كيفية إدراج وتخصيص الحواشي السفلية.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أضف نصًا، وأشر إليه بحاشية سفلية. ستضع هذه الحاشية السفلية إشارة صغيرة مرتفعة
// بعد النص الذي تشير إليه وتُنشئ إدخالًا أسفل النص الرئيسي في أسفل الصفحة.
// سيحتوي هذا الإدخال على علامة الإشارة الخاصة بالحاشية السفلية والنص المرجعي،
// والتي سنمررها إلى طريقة "InsertFootnote" الخاصة بـ document builder.
builder->Write(u"Main body text.");
System::SharedPtr<Aspose::Words::Notes::Footnote> footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text.");

// إذا تم ضبط هذه الخاصية إلى "true"، فإن علامة الإشارة الخاصة بحاشيتنا السفلية
// ستكون مؤشرها بين جميع حواشي القسم.
// هذه هي الحاشية السفلية الأولى، لذا ستكون علامة الإشارة "1".
ASSERT_TRUE(footnote->get_IsAuto());

// يمكننا نقل document builder داخل الحاشية السفلية لتعديل نص الإشارة الخاص بها.
builder->MoveTo(footnote->get_FirstParagraph());
builder->Write(u" More text added by a DocumentBuilder.");
builder->MoveToDocumentEnd();

ASSERT_EQ(u"\u0002 Footnote text. More text added by a DocumentBuilder.", footnote->GetText().Trim());

builder->Write(u" More main body text.");
footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text.");

// يمكننا ضبط علامة إشارة مخصصة ستستخدمها الحاشية السفلية بدلًا من رقم مؤشرها.
footnote->set_ReferenceMark(u"RefMark");

ASSERT_FALSE(footnote->get_IsAuto());

// إشارة مرجعية مع العلم "IsAuto" مضبوط على true ستظهر مؤشرها الحقيقي
// حتى وإن كانت الإشارات المرجعية السابقة تعرض علامات إشارة مخصصة، فإن علامة الإشارة لهذه الإشارة المرجعية ستكون "3".
builder->Write(u" More main body text.");
footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text.");

ASSERT_TRUE(footnote->get_IsAuto());

doc->Save(get_ArtifactsDir() + u"InlineStory.AddFootnote.docx");
```

## انظر أيضًا

* Class [Footnote](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
