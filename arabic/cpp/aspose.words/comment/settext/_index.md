---
title: "طريقة Aspose::Words::Comment::SetText"
linktitle: "SetText"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Comment::SetText. هذه طريقة مريحة تسمح بتعيين نص التعليق بسهولة في C++."
type: docs
weight: 22000
url: /ar/cpp/aspose.words/comment/settext/
---
## Comment::SetText method


هذه طريقة مريحة تسمح بتعيين نص التعليق بسهولة.

```cpp
void Aspose::Words::Comment::SetText(const System::String &text)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| نص | const System::String\& | النص الجديد للتعليق. |
## ملاحظات


تسمح هذه الطريقة بتعيين نص التعليق بسرعة من سلسلة نصية. يمكن أن تحتوي السلسلة على فواصل فقرات، مما سيُنشئ فقرات نصية في التعليق وفقًا لذلك. إذا كنت تريد إدراج عناصر أكثر تعقيدًا في التعليق، مثل الإشارات المرجعية أو الجداول أو تطبيق تنسيق غني، فستحتاج إلى استخدام فئات العقد المناسبة لبناء نص التعليق.

## أمثلة



يوضح كيفية إضافة تعليق إلى مستند، ثم الرد عليه.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"My comment.");

// ضع التعليق عند عقدة في جسم المستند.
// سيظهر هذا التعليق في موقع الفقرة الخاصة به،
// خارج الهامش الأيمن للصفحة، ومع خط منقط يربطه بفقرتها.
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

// أضف ردًا، سيظهر تحت التعليق الأب.
comment->AddReply(u"Joe Bloggs", u"J.B.", System::DateTime::get_Now(), u"New reply");

// التعليقات والردود كلاهما عقد من نوع Comment.
ASSERT_EQ(2, doc->GetChildNodes(Aspose::Words::NodeType::Comment, true)->get_Count());

// التعليقات التي لا ترد على تعليقات أخرى هي "مستوى أعلى". ليس لها تعليقات سلفية.
ASSERT_TRUE(System::TestTools::IsNull(comment->get_Ancestor()));

// الردود لها تعليق سلفي من المستوى الأعلى.
ASPOSE_ASSERT_EQ(comment, comment->get_Replies()->idx_get(0)->get_Ancestor());

doc->Save(get_ArtifactsDir() + u"Comment.AddCommentWithReply.docx");
```

## انظر أيضًا

* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
