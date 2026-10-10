---
title: "فئة Aspose::Words::ParagraphCollection"
linktitle: "ParagraphCollection"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::ParagraphCollection. توفر وصولًا مكتوبًا إلى مجموعة من عقد Paragraph. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 48000
url: /ar/cpp/aspose.words/paragraphcollection/
---
## ParagraphCollection class


توفر وصولًا مكتوبًا إلى مجموعة من عقد [Paragraph](../paragraph/). لمعرفة المزيد، زر مقالة الوثائق [Working with Paragraphs](https://docs.aspose.com/words/cpp/working-with-paragraphs/).

```cpp
class ParagraphCollection : public Aspose::Words::NodeCollection
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Add](../nodecollection/add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يضيف عقدة إلى نهاية المجموعة. |
| [Clear](../nodecollection/clear/)() | يزيل جميع العقد من هذه المجموعة ومن المستند. |
| [Contains](../nodecollection/contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يحدد ما إذا كانت العقدة موجودة في المجموعة. |
| [get_Count](../nodecollection/get_count/)() | يحصل على عدد العقد في المجموعة. |
| [GetEnumerator](../nodecollection/getenumerator/)() override | يوفر تكرارًا بسيطًا بنمط "foreach" على مجموعة العقد. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | تسترجع [Paragraph](../paragraph/) عند الفهرس المحدد. |
| [IndexOf](../nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يعيد الفهرس الصفري للعقدة المحددة. |
| [Insert](../nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | يدرج عقدة في المجموعة عند الفهرس المحدد. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يزيل العقدة من المجموعة ومن المستند. |
| [RemoveAt](../nodecollection/removeat/)(int32_t) | يزيل العقدة في الفهرس المحدد من المجموعة ومن المستند. |
| [ToArray](./toarray/)() | ينسخ جميع الفقرات من المجموعة إلى مصفوفة جديدة من الفقرات. |
| static [Type](./type/)() |  |

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

* Class [NodeCollection](../nodecollection/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
