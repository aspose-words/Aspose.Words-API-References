---
title: "منشئ Aspose::Words::Comment::Comment"
linktitle: "Comment"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "منشئ Aspose::Words::Comment::Comment. يهيئ مثيلاً جديداً لفئة Comment في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words/comment/comment/
---
## Comment::Comment(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) constructor


يهيئ مثيلاً جديداً لفئة [Comment](../).

```cpp
Aspose::Words::Comment::Comment(const System::SharedPtr<Aspose::Words::DocumentBase> &doc)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | المستند المالك. |
## ملاحظات


عند إنشاء [Comment](../)، ينتمي إلى المستند المحدد، لكنه ليس جزءًا من المستند بعد و[ParentNode](../../node/get_parentnode/) هو **null**.

لإضافة [Comment](../) إلى المستند استخدم [InsertAfter1()</see> أو <see cref=\"Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\\>, System::SharedPtr\\<Aspose::Words::Node\\>)\">InsertBefore1()](../) في الفقرة التي تريد إدراج التعليق فيها.

بعد إنشاء تعليق، لا تنس ضبط خصائصه [Author](../get_author/)، [Initial](../get_initial/) و[DateTime](../get_datetime/).

## انظر أيضًا

* Class [DocumentBase](../../documentbase/)
* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Comment::Comment(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::String\&, const System::String\&, System::DateTime) constructor


يهيئ مثيلاً جديداً لفئة [Comment](../).

```cpp
Aspose::Words::Comment::Comment(const System::SharedPtr<Aspose::Words::DocumentBase> &doc, const System::String &author, const System::String &initial, System::DateTime dateTime)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | المستند المالك. |
| المؤلف | const System::String\& | اسم المؤلف للتعليق. لا يمكن أن يكون **null**. |
| الاسم الأول | const System::String\& | الأحرف الأولى لاسم المؤلف للتعليق. لا يمكن أن تكون **null**. |
| dateTime | System::DateTime | التاريخ والوقت للتعليق. |

## أمثلة



يعرض كيفية إضافة تعليق إلى فقرة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Hello world!");

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"JD", System::DateTime::get_Today());
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);
builder->MoveTo(comment->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc)));
builder->Write(u"Comment text.");

ASSERT_EQ(System::DateTime::get_Today(), comment->get_DateTime());

// في Microsoft Word، يمكننا النقر بزر الماوس الأيمن على هذا التعليق في جسم المستند لتعديله، أو الرد عليه.
doc->Save(get_ArtifactsDir() + u"InlineStory.AddComment.docx");
```

## انظر أيضًا

* Class [DocumentBase](../../documentbase/)
* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
