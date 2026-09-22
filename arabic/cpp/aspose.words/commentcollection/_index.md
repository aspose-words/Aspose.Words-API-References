---
title: "Aspose::Words::CommentCollection class"
linktitle: "CommentCollection"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::CommentCollection class. يوفر وصولًا مكتوبًا إلى مجموعة من عقد التعليق. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 12000
url: /ar/cpp/aspose.words/commentcollection/
---
## CommentCollection class


يوفر وصولًا مكتوبًا إلى مجموعة من عقد [Comment](../comment/). لمعرفة المزيد، زر مقالة الوثائق [Working with Comments](https://docs.aspose.com/words/cpp/working-with-comments/).

```cpp
class CommentCollection : public Aspose::Words::NodeCollection
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
| [idx_get](./idx_get/)(int32_t) | يسترجع [Comment](../comment/) عند الفهرس المحدد. |
| [IndexOf](../nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يعيد الفهرس الصفري للعقدة المحددة. |
| [Insert](../nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | يدرج عقدة في المجموعة عند الفهرس المحدد. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يزيل العقدة من المجموعة ومن المستند. |
| [RemoveAt](../nodecollection/removeat/)(int32_t) | يزيل العقدة في الفهرس المحدد من المجموعة ومن المستند. |
| [ToArray](../nodecollection/toarray/)() | ينسخ جميع العقد من المجموعة إلى مصفوفة جديدة من العقد. |
| static [Type](./type/)() |  |

## أمثلة



يوضح كيفية وضع علامة "done" على التعليق.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Helo world!");

// أدرج تعليقًا لتوضيح خطأ.
auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"Fix the spelling error!");
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

// التعليقات تحتوي على علم "Done"، والذي يُضبط على "false" افتراضيًا.
// إذا اقترح تعليق أننا نجري تغييرًا داخل المستند،
// يمكننا تطبيق التغيير، ثم ضبط علم "Done" لاحقًا للإشارة إلى التصحيح.
ASSERT_FALSE(comment->get_Done());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->set_Text(u"Hello world!");
comment->set_Done(true);

// التعليقات التي تم وضع علامة "done" عليها ستميز نفسها.
// من العناصر التي ليست "مكتملة" بل بلون نص باهت.
comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"Add text to this paragraph.");
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

doc->Save(get_ArtifactsDir() + u"Comment.Done.docx");
```

## انظر أيضًا

* Class [NodeCollection](../nodecollection/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
