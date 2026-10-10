---
title: "طريقة Aspose::Words::Story::get_Paragraphs"
linktitle: "get_Paragraphs"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Story::get_Paragraphs. يسترجع مجموعة من الفقرات التي هي أبناء مباشرة للقصة في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words/story/get_paragraphs/
---
## Story::get_Paragraphs method


يحصل على مجموعة من الفقرات التي هي أطفال مباشرون للقصة.

```cpp
System::SharedPtr<Aspose::Words::ParagraphCollection> Aspose::Words::Story::get_Paragraphs() override
```


## أمثلة



يوضح كيفية التحقق مما إذا كانت الفقرة مراجعة نقل.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

// يحتوي هذا المستند على مراجعات "Move"، التي تظهر عندما نحدد النص بالمؤشر،
// ثم نسحبها لنقلها إلى موقع آخر
// أثناء تتبع المراجعات في Microsoft Word عبر "Review" -> "Track changes".
ASSERT_EQ(6, doc->get_Revisions()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Revision>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Revision> r)>>([](System::SharedPtr<Aspose::Words::Revision> r) -> bool
{
    return r->get_RevisionType() == Aspose::Words::RevisionType::Moving;
}))));

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

// مراجعات النقل تتكون من أزواج من مراجعات "Move from" و "Move to".
// هذه المراجعات هي تغييرات محتملة في المستند يمكننا إما قبولها أو رفضها.
// قبل أن نقبل/نرفض مراجعة النقل، المستند
// يجب أن يتتبع كلًا من وجهتي المغادرة والوصول للنص.
// الفقرة الثانية والرابعة تحددان مثل هذه المراجعة، وبالتالي كلاهما يحتويان على نفس المحتوى.
ASSERT_EQ(paragraphs->idx_get(1)->GetText(), paragraphs->idx_get(3)->GetText());

// مراجعة "Move from" هي الفقرة التي سحبنا النص منها.
// إذا قبلنا المراجعة، ستختفي هذه الفقرة،
// والأخرى ستبقى ولن تكون مراجعة بعد الآن.
ASSERT_TRUE(paragraphs->idx_get(1)->get_IsMoveFromRevision());

// مراجعة "Move to" هي الفقرة التي سحبنا النص إليها.
// إذا رفضنا المراجعة، ستختفي هذه الفقرة بدلاً من ذلك، وستبقى الأخرى.
ASSERT_TRUE(paragraphs->idx_get(3)->get_IsMoveToRevision());
```

## انظر أيضًا

* Class [ParagraphCollection](../../paragraphcollection/)
* Class [Story](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
