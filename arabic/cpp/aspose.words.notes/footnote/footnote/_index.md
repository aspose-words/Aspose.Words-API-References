---
title: "Aspose::Words::Notes::Footnote::Footnote constructor"
linktitle: "حاشية سفلية"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "منشئ Aspose::Words::Notes::Footnote::Footnote. يهيئ نسخة من فئة Footnote في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.notes/footnote/footnote/
---
## Footnote::Footnote constructor


يُهيئ مثيلًا من الفئة [Footnote](../).

```cpp
Aspose::Words::Notes::Footnote::Footnote(const System::SharedPtr<Aspose::Words::DocumentBase> &doc, Aspose::Words::Notes::FootnoteType footnoteType)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | المستند المالك. |
| footnoteType | Aspose::Words::Notes::FootnoteType | قيمة [FootnoteType](../get_footnotetype/) تحدد ما إذا كان هذا حاشية سفلية أو حاشية نهائية. |
## ملاحظات


عند إنشاء [Footnote](../)، ينتمي إلى المستند المحدد، لكنه ليس جزءًا من المستند بعد و[ParentNode](../../../aspose.words/node/get_parentnode/) هو **null**.

لإرفاق [Footnote](../) بالمستند استخدم [InsertAfter1()</see> أو <see cref="Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\>, System::SharedPtr\<Aspose::Words::Node\>)">InsertBefore1()](../) في الفقرة التي تريد إدراج الحاشية فيها.

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

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Enum [FootnoteType](../../footnotetype/)
* Class [Footnote](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
