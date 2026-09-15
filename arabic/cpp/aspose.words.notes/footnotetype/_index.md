---
title: "Aspose::Words::Notes::FootnoteType enum"
linktitle: "نوع الحاشية السفلية"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Notes::FootnoteType enum. يحدد ما إذا كانت هذه حاشية سفلية أم حاشية ختامية في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words.notes/footnotetype/
---
## FootnoteType enum


يحدد ما إذا كان هذا حاشية سفلية أم حاشية ختامية.

```cpp
enum class FootnoteType
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| حاشية سفلية | 0 | الكائن هو حاشية سفلية. |
| حاشية نهائية | 1 | الكائن هو حاشية نهائية. |

## ملاحظات


كلا من الحواشي السفلية والحواشي النهائية يتم تمثيلهما ككائنات بواسطة الفئة [Footnote](./). استخدم [FootnoteType](../footnote/get_footnotetype/) للتمييز بين الحواشي السفلية والحواشي النهائية.

## أمثلة



يوضح كيفية الإشارة إلى النص باستخدام حاشية سفلية وحاشية نهائية.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدرج بعض النصوص وضع علامة عليها بحاشية سفلية مع ضبط الخاصية IsAuto إلى "true" بشكل افتراضي،
// بحيث سيتم ترقيم العلامة التي تُرى في نص الجسم تلقائيًا إلى "1",
// وستظهر الحاشية السفلية في أسفل الصفحة.
builder->Write(u"This text will be referenced by a footnote.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote comment regarding referenced text.");

// أدرج نصًا إضافيًا وضع علامة عليه بحاشية نهائية مع علامة إشارة مخصصة،
// والتي ستُستَخدم بدلًا من الرقم "2" وتضبط "IsAuto" إلى false.
builder->Write(u"This text will be referenced by an endnote.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote comment regarding referenced text.", u"CustomMark");

// الحواشي السفلية تظهر دائمًا في أسفل النص المُشار إليه،
// وبالتالي فإن فاصل الصفحة هذا لن يؤثر على الحاشية السفلية.
// من ناحية أخرى، الحواشي النهائية تكون دائمًا في نهاية المستند
// وبذلك سيؤدي فاصل الصفحة هذا إلى دفع الحاشية النهائية إلى الصفحة التالية.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertFootnote.docx");
```


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

* Namespace [Aspose::Words::Notes](../)
* Library [Aspose.Words for C++](../../)
