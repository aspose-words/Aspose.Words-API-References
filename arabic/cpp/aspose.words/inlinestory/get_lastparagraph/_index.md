---
title: "طريقة Aspose::Words::InlineStory::get_LastParagraph"
linktitle: "get_LastParagraph"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::InlineStory::get_LastParagraph. يحصل على الفقرة الأخيرة في القصة في C++."
type: docs
weight: 9000
url: /ar/cpp/aspose.words/inlinestory/get_lastparagraph/
---
## InlineStory::get_LastParagraph method


يحصل على الفقرة الأخيرة في القصة.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::InlineStory::get_LastParagraph() override
```


## أمثلة



يوضح كيفية إدراج عقد [InlineStory](../).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Notes::Footnote> footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, nullptr);

// عقد الجدول لديها طريقة "EnsureMinimum()" التي تضمن أن الجدول يحتوي على خلية واحدة على الأقل.
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
table->EnsureMinimum();

// يمكننا وضع جدول داخل حاشية، مما سيجعلها تظهر في تذييل الصفحة المرجعية.
ASSERT_EQ(0, footnote->get_Tables()->get_Count());
footnote->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);
ASSERT_EQ(1, footnote->get_Tables()->get_Count());
ASSERT_EQ(Aspose::Words::NodeType::Table, footnote->get_LastChild()->get_NodeType());

// لـ InlineStory طريقة "EnsureMinimum()" أيضًا، ولكن في هذه الحالة،
// تضمن أن العنصر الفرعي الأخير للعقدة هو فقرة،
// لكي نتمكن من النقر وكتابة النص بسهولة في Microsoft Word.
footnote->EnsureMinimum();
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, footnote->get_LastChild()->get_NodeType());

// حرّر مظهر المرساة، التي هي الرقم الصغير المرتفع.
// في النص الرئيسي الذي يشير إلى الحاشية.
footnote->get_Font()->set_Name(u"Arial");
footnote->get_Font()->set_Color(System::Drawing::Color::get_Green());

// جميع عقد القصة المتضمنة لديها أنواع القصة الخاصة بها.
ASSERT_EQ(Aspose::Words::StoryType::Footnotes, footnote->get_StoryType());

// التعليق هو نوع آخر من القصة المتضمنة.
auto comment = System::ExplicitCast<Aspose::Words::Comment>(builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J. D.", System::DateTime::get_Now())));

// الفقرة الأصلية لعقدة القصة المتضمنة ستكون الفقرة الموجودة في جسم المستند الرئيسي.
ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body()->get_FirstParagraph(), comment->get_ParentParagraph());

// مع ذلك، الفقرة الأخيرة هي الفقرة المستخرجة من محتوى نص التعليق،
// والتي ستكون خارج جسم المستند الرئيسي داخل فقاعة الكلام.
// التعليق لن يحتوي على أي عقد فرعية بشكل افتراضي،
// لذلك يمكننا تطبيق طريقة EnsureMinimum() لوضع فقرة هنا أيضًا.
ASSERT_TRUE(System::TestTools::IsNull(comment->get_LastParagraph()));
comment->EnsureMinimum();
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, comment->get_LastChild()->get_NodeType());

// بمجرد حصولنا على فقرة، يمكننا نقل الباني للقيام بذلك وكتابة تعليقنا.
builder->MoveTo(comment->get_LastParagraph());
builder->Write(u"My comment.");

ASSERT_EQ(Aspose::Words::StoryType::Comments, comment->get_StoryType());

doc->Save(get_ArtifactsDir() + u"InlineStory.InsertInlineStoryNodes.docx");
```

## انظر أيضًا

* Class [Paragraph](../../paragraph/)
* Class [InlineStory](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
