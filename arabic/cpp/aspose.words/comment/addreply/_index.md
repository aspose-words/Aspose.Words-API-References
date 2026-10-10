---
title: "طريقة Aspose::Words::Comment::AddReply"
linktitle: "AddReply"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Comment::AddReply. يضيف ردًا على هذا التعليق في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words/comment/addreply/
---
## Comment::AddReply method


يضيف ردًا على هذا التعليق.

```cpp
System::SharedPtr<Aspose::Words::Comment> Aspose::Words::Comment::AddReply(const System::String &author, const System::String &initial, System::DateTime dateTime, const System::String &text)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| المؤلف | const System::String\& | اسم المؤلف للرد. |
| الاسم الأول | const System::String\& | حروف اسم المؤلف للرد. |
| dateTime | System::DateTime | التاريخ والوقت للرد. |
| نص | const System::String\& | نص الرد. |

### ReturnValue

العقدة [Comment](../) التي تم إنشاؤها للرد.
## ملاحظات


نظرًا لقيود MS Office الحالية، يُسمح بمستوى واحد فقط من الردود في المستند.

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
* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
